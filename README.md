Calculation of the diameter of a roller shutter around its axis when the shutter is open
The solution found requires taking a 60mm diameter axle instead of the current 40mm one.
The length of the apron is 2.40m in the closed position. In this case, the blades are joined together and a
blade measures 36mm wide/high. Otherwise 40mm when the apron is "deployed" (or the slats
are “stretched”).
The thickness "l" of a blade is 7.5mm. When the blade wraps around the axis the thickness
increases by 1.5 mm due to the inflexibility of the blades.
The box measures 25 cm x 20 cm in interior dimensions.
Will this motor shaft modification allow the shutter to be fully mounted?
To answer this question, it is interesting to start with these:

1. How many "full" slats are needed for the apron in the closed position?

    (Deck length / slat width) = (2.4 m / 0.036 m) ≈ 67 slats required
    
2. Deduce the length to be rolled up.

    (Number of slats * Width of a stretched slat) = (67 * 40 m) = Rolling length of 2680 mm

3. Give the equation of the arithmetic sequence of the diameter "dn" for the turn "n".

    dn = Initial diameter of the axis + (2 * Thickness of a blade * Number of turns)
    (Given as result of the function calcul_diametre)
    
4. Deduce the circumference “cn” traveled for lap “n”.

    Pi * (Axle diameter at turn n - 1)
    (Given as the value of the circumference_traveled variable)
    
5. Calculate the rolled length “Ln” at turn “n”. The turns being complete, it will be necessary to
do a linear interpolation to correctly define the diameter according to the length
rolled up.

   Pi * (Axle diameter at turn n)

6. In reality, so that the fasteners of the apron are not extended or strained when it is
closed, the apron is considered to remain rolled up for 2 turns. To put it simply, these 2 towers
take into account the distance between the axis and the slides.
Calculate the new length “Ln” to wind.
    no answer
Conclude.

