:author: Kevin Winters
:email: Kevin.Winters@erdc.dren.mil
:institution: US Army Engineer Research and Development Center
:corresponding:

:author: Mark Anthony
:email: mark37@rome.it
:institution: Egyptian Embassy, S.P.Q.R.

:author: Jarrod Millman
:email: millman@rome.it
:institution: Egyptian Embassy, S.P.Q.R.
:institution: Yet another place, S.P.Q.R.
:equal-contributor:

:author: Brutus
:email: brutus@rome.it
:institution: Unaffiliated
:equal-contributor:

:video: http://www.youtube.com/watch?v=dhRUe-gz690

------------------------------------------------
A Numerical Perspective to Terraforming a Desert
------------------------------------------------

.. class:: abstract

   Motivation:

   Traditionally, the p rimary method of performing environmental simulation requires a
   combination of heavy proprietary desktop tools that do not interoperate well with each
   other. The process of building and running environmental simulations using these tools is
   a time‑consuming process and lacks the flexibility needed to provide basic predictions of
   environmental conditions quickly for any region of the globe.
   EarthSim, introduced at SciPy2018, is a new flexible approach to environmental simulation.
   Streamlining simulations using lightweight modules has been an audacious effort, and in
   the past year we have improved the following key capabilities: gathering data from local
   and web services, numerical model domain generation, model parameterization, model
   execution on dedicated High Performance Computing (HPC) clusters, and results analyses.
   Visualization is also a key aspect of all of these steps. The goal of these modular
   capabilities is to rapidly develop custom modeling workflows that can easily be presented
   in dashboards and deployed as web apps.

   Methods:

   To achieve the environmental simulation dashboarding capabilities described above, we
   have created a coordinating project called EarthSim where we have developed and
   prototyped new capabilities. As these capabilities have matured, we have moved them into
   existing open source software packages or, when necessary, created new ones. The
   following projects have seen extensive improvements as part of this effort:

   • EarthSim – for interactive compound geometric object drawing
   • Panel – for support for widget‑only workflow pipelines (sequential dashboard steps)
   • Param – for parameter dependency
   • HoloViews, GeoViews, Datashader – for efficient visualizations
   • Bokeh framework – for flexibility in deploying workflows in various modes, including embedded in web pages
   • XmsMesh – for triangula ted unstructured mesh generation and manipulation
   • pyUIT – for HPC job submission

   Results:

   We have demonstrated the effectiveness of these new capabilities by creating
   hydrodynamic modeling workflows using the Adaptive Hydraulics (AdH) simulator in Jupyter
   Notebooks and then deploying them as Bokeh web apps.

   Conclusion:

   Our environment al simulation dashboards have demonstrated that this modular approach
   can successfully replace monolithic desktop solutions.

.. class:: keywords

   environmental simulation, hydrodynamics, workflows, dashboard, visualization, parameterization, HPC

Introduction (1/2 page)
------------

Dashboard Tools Background [Abstract Motivation]

Quickly create hydrodynamic workflows

   A typical environmental simulation model requires components/steps...

      * Annotate scenario [locate in world]
      * Generate domain
      * Attribute model [apply BCs]
      * Execute
      * Visualize/Analyze

   To enable rapid generation, these are the python tools to support that...

Introduce Riverine Workflow Example


Methods (5 pages)
------------

Annotation
============

Domain Generation
============

Model Attribution
============

Model Execution
============

Visualization & Analysis
============



Results (2 page)
------------

Final Dashboard (User experience)

Conclusion (1/2 page)
------------











Twelve hundred years ago  |---| in a galaxy just across the hill...

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum sapien
tortor, bibendum et pretium molestie, dapibus ac ante. Nam odio orci, interdum
sit amet placerat non, molestie sed dui. Pellentesque eu quam ac mauris
tristique sodales. Fusce sodales laoreet nulla, id pellentesque risus convallis
eget. Nam id ante gravida justo eleifend semper vel ut nisi. Phasellus
adipiscing risus quis dui facilisis fermentum. Duis quis sodales neque. Aliquam
ut tellus dolor. Etiam ac elit nec risus lobortis tempus id nec erat. Morbi eu
purus enim. Integer et velit vitae arcu interdum aliquet at eget purus. Integer
quis nisi neque. Morbi ac odio et leo dignissim sodales. Pellentesque nec nibh
nulla. Donec faucibus purus leo. Nullam vel lorem eget enim blandit ultrices.
Ut urna lacus, scelerisque nec pellentesque quis, laoreet eu magna. Quisque ac
justo vitae odio tincidunt tempus at vitae tortor.

Of course, no paper would be complete without some source code.  Without
highlighting, it would look like this::

   def sum(a, b):
       """Sum two numbers."""

       return a + b

With code-highlighting:

.. code-block:: python

   def sum(a, b):
       """Sum two numbers."""

       return a + b

Maybe also in another language, and with line numbers:

.. code-block:: c
   :linenos:

   int main() {
       for (int i = 0; i < 10; i++) {
           /* do something */
       }
       return 0;
   }

Or a snippet from the above code, starting at the correct line number:

.. code-block:: c
   :linenos:
   :linenostart: 2

   for (int i = 0; i < 10; i++) {
       /* do something */
   }
   
Inline code looks like this: :code:`chunk of code`.

Important Part
--------------

It is well known [Atr03]_ that Spice grows on the planet Dune.  Test
some maths, for example :math:`e^{\pi i} + 3 \delta`.  Or maybe an
equation on a separate line:

.. math::

   g(x) = \int_0^\infty f(x) dx

or on multiple, aligned lines:

.. math::
   :type: eqnarray

   g(x) &=& \int_0^\infty f(x) dx \\
        &=& \ldots

The area of a circle and volume of a sphere are given as

.. math::
   :label: circarea

   A(r) = \pi r^2.

.. math::
   :label: spherevol

   V(r) = \frac{4}{3} \pi r^3

We can then refer back to Equation (:ref:`circarea`) or
(:ref:`spherevol`) later.

Mauris purus enim, volutpat non dapibus et, gravida sit amet sapien. In at
consectetur lacus. Praesent orci nulla, blandit eu egestas nec, facilisis vel
lacus. Fusce non ante vitae justo faucibus facilisis. Nam venenatis lacinia
turpis. Donec eu ultrices mauris. Ut pulvinar viverra rhoncus. Vivamus
adipiscing faucibus ligula, in porta orci vehicula in. Suspendisse quis augue
arcu, sit amet accumsan diam. Vestibulum lacinia luctus dui. Aliquam odio arcu,
faucibus non laoreet ac, condimentum eu quam. Quisque et nunc non diam
consequat iaculis ut quis leo. Integer suscipit accumsan ligula. Sed nec eros a
orci aliquam dictum sed ac felis. Suspendisse sit amet dui ut ligula iaculis
sollicitudin vel id velit. Pellentesque hendrerit sapien ac ante facilisis
lacinia. Nunc sit amet sem sem. In tellus metus, elementum vitae tincidunt ac,
volutpat sit amet mauris. Maecenas [#]_ diam turpis, placerat [#]_ at adipiscing ac,
pulvinar id metus.

.. [#] On the one hand, a footnote.
.. [#] On the other hand, another footnote.

.. figure:: figure1.png

   This is the caption.:code:`chunk of code` inside of it. :label:`egfig` 

.. figure:: figure1.png
   :align: center
   :figclass: w

   This is a wide figure, specified by adding "w" to the figclass.  It is also
   center aligned, by setting the align keyword (can be left, right or center).
   This caption also has :code:`chunk of code`.

.. figure:: figure1.png
   :scale: 20%
   :figclass: bht

   This is the caption on a smaller figure that will be placed by default at the
   bottom of the page, and failing that it will be placed inline or at the top.
   Note that for now, scale is relative to a completely arbitrary original
   reference size which might be the original size of your image - you probably
   have to play with it.  :label:`egfig2`

As you can see in Figures :ref:`egfig` and :ref:`egfig2`, this is how you reference auto-numbered
figures.

.. table:: This is the caption for the materials table. :label:`mtable`

   +------------+----------------+
   | Material   | Units          |
   +============+================+
   | Stone      | 3              |
   +------------+----------------+
   | Water      | 12             |
   +------------+----------------+
   | Cement     | :math:`\alpha` |
   +------------+----------------+


We show the different quantities of materials required in Table
:ref:`mtable`.


.. The statement below shows how to adjust the width of a table.

.. raw:: latex

   \setlength{\tablewidth}{0.8\linewidth}


.. table:: This is the caption for the wide table.
   :class: w

   +--------+----+------+------+------+------+--------+
   | This   | is |  a   | very | very | wide | table  |
   +--------+----+------+------+------+------+--------+

Unfortunately, restructuredtext can be picky about tables, so if it simply
won't work try raw LaTeX:


.. raw:: latex

   \begin{table*}

     \begin{longtable*}{|l|r|r|r|}
     \hline
     \multirow{2}{*}{Projection} & \multicolumn{3}{c|}{Area in square miles}\tabularnewline
     \cline{2-4}
      & Large Horizontal Area & Large Vertical Area & Smaller Square Area\tabularnewline
     \hline
     Albers Equal Area  & 7,498.7 & 10,847.3 & 35.8\tabularnewline
     \hline
     Web Mercator & 13,410.0 & 18,271.4 & 63.0\tabularnewline
     \hline
     Difference & 5,911.3 & 7,424.1 & 27.2\tabularnewline
     \hline
     Percent Difference & 44\% & 41\% & 43\%\tabularnewline
     \hline
     \end{longtable*}

     \caption{Area Comparisons \DUrole{label}{quanitities-table}}

   \end{table*}

Perhaps we want to end off with a quote by Lao Tse [#]_:

  *Muddy water, let stand, becomes clear.*

.. [#] :math:`\mathrm{e^{-i\pi}}`

.. Customised LaTeX packages
.. -------------------------

.. Please avoid using this feature, unless agreed upon with the
.. proceedings editors.

.. ::

..   .. latex::
..      :usepackage: somepackage

..      Some custom LaTeX source here.

References
----------
.. [Atr03] P. Atreides. *How to catch a sandworm*,
           Transactions on Terraforming, 21(3):261-300, August 2003.


