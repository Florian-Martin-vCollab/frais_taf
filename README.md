        <?php

        function diffDates($dateFournie) : int {
            $dateAuj = date('Ym');
            $d1 = new DateTime($dateAuj);
            $d2 = new DateTime($dateFournie);

            $intervalle = $d2->diff($d1);
            $diffMois = $intervalle->y * 12 + $intervalle->m;
            return $diffMois;
        }




        $date1 = '2010-08';
        $date2 = '2009-09';
        $d1 = new DateTime($date1);
        $d2 = new DateTime($date2);

        // Retourne un objet DateInterval
        // la fonction diff() calcule l'intervalle entre la date de référence, incluse,
        // et la date fournie à partir du mois suivant
        $intervalle = $d2->diff($d1);

        // Si la date fournie est antérieure à la date du jour
        if ($intervalle->invert == 0) {
            $diffMois = $intervalle->y * 12 + $intervalle->m;

            if ($diffMois < 12) {
                print 'hola';
            }

            //print_r($difference);
        }
        ?>
