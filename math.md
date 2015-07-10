
How Did Archimedes Do It?
===================


How did Archimedes discover the value of $\pi$ without using trigonometry or
calculus or analytic geometry?  How did he do it using only the relatively blunt
mathematical tools available to him, namely the Pythagorean Theorem and
Euclidean Geometry.

Archimedes knew from studying other shapes that the circumference of a circle
grows in linear porportion to its diameter.  The constant of porportionality in
this case being the number $\pi$ and leading to the formula: $$ c = \pi d $$

So Archimedes set out to calculate the circumference of a circle with diameter
$1$, which would then yield the number $\pi$.  But how do you calculate the
circumference of a circle without the constant $\pi$?  Archimedes discovered a
method to estimate the circumference of a circle to an arbitary degree of
accurary by using regular polygons.

His method is conceptually very simple to visualize.  Consider a polygon of however
many sides you like, Archimedes used a 96-sided polygon.  Take that polygon and
_inscribe_ it inside a circle of diameter $1$ such that each vertex of the
polygon lies on the circle.  Now, calculate the permiter of that polygon and
you'll have a "lower-bound" on the value of $\pi$.  The number will be slightly
smaller than the actual value of $\pi$ because, while the
edges of the polygon take a "short cut" between the vertices in the form of a
straight line, the arc of the circle goes the longer way around.  Therefore the
circumference of the circle is larger than the perimeter of the polygon.

Now, take a slightly larger version of that same $n$-sided polygon and this time
_circumscribe_ it about the circle of diameter $1$.  By similar reasoning, its
perimeter will be slightly _larger_ than the value of $\pi$, establishing an
upper-bound on what $\pi$ is.  In theory, you can choose polygons of increasing
number of sides to get whatever degree of accuracy you like in computing the
value of $\pi$.

#### The Perimeter of a Regular Polygon

So... how exactly did Archimedes calculate the perimter of a 96-sided polygon
without using trigonometry?  He did it by a clever application of Euclidean
geometry, in which he established a "recurrence" relation that allowed him to
compute the perimeter of a $2n$-sided polygon knowing the perimeter of a polygon
of $n$ sides.

To understand how he did this, first consider this diagram.

![Archimedes Triange Proof Image](http://gustavotron.com/archimedes.png)

We begin with the isosceles triangle $\triangle{ABZ}$, and we swing the line
$ZM$ along an arc until it creates points $C$ and $D$ such that $ZM=ZD=ZC$, thus
the two triangles $\triangle{ABZ}\approx\triangle{CDZ}$ are similar.

Now extend a line from point $C$ perpendicular to $ZA$, and call $O$ the point
where it intersects $AB$.  Observe that $\triangle{ACO}\approx\triangle{AMZ}$
are similar since the two right triangles share the angle $\angle{A}$.  Also
$\triangle{CNZ}\approx\triangle{AMZ}$.

Perhaps more subtle is the similarity relationship
$\triangle{COM}\approx\triangle{CDM}$.  To see why this is so, first observe
that $\angle{CMZ}=\angle{MCZ}$ because $\triangle{CMZ}$ is isosceles.  The angle
$\angle{MCN}$ is the same as $\angle{MCO}$ because, for the former $\angle{MCN}
= 180 - 90 - \angle{CMZ}$ because the interior angles of a triangle must add up
to $180$ degrees, and for the latter $\angle{MCO} = 180 - 90 - \angle{MCZ}$
because a straight line $ZA$ divided into angles must sum to $180$ degrees.
Since $\angle{CMZ}=\angle{MCZ}$ then $\angle{MCN} = \angle{CMZ}$.  Finally,
$\angle{CMO}=\angle{MCO}$ because $\angle{MCO} = 180 - 90 - \angle{MCZ}$,
therefore $\angle{MCZ} + \angle{MCO} = 90$, and since $\angle{CMZ} + \angle{CMO}
= 90$ and $\angle{CMZ}=\angle{MCZ}$, we have $\angle{CMO}=\angle{MCO}$.  Putting
it all together, $\triangle{COM}$ and $\triangle{CDM}$ are similar and
isosceles.

