.. Generated automatically by doc/tools/makerst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the doc/base/classes.xml source instead.

.. _class_AStar:

AStar
=====

**Inherits:** :ref:`Reference<class_reference>` **<** :ref:`Object<class_object>`

**Category:** Core

Brief Description
-----------------

AStar class representation that uses vectors as edges.

Member Functions
----------------

+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                             | :ref:`_compute_cost<class_AStar__compute_cost>`  **(** :ref:`int<class_int>` from_id, :ref:`int<class_int>` to_id  **)** virtual                                  |
+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                             | :ref:`_estimate_cost<class_AStar__estimate_cost>`  **(** :ref:`int<class_int>` from_id, :ref:`int<class_int>` to_id  **)** virtual                                |
+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                             | :ref:`add_point<class_AStar_add_point>`  **(** :ref:`int<class_int>` id, :ref:`Vector3<class_vector3>` pos, :ref:`float<class_float>` weight_scale=null  **)**    |
+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                          | :ref:`are_points_connected<class_AStar_are_points_connected>`  **(** :ref:`int<class_int>` id, :ref:`int<class_int>` to_id  **)** const                           |
+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                             | :ref:`clear<class_AStar_clear>`  **(** **)**                                                                                                                      |
+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                             | :ref:`connect_points<class_AStar_connect_points>`  **(** :ref:`int<class_int>` id, :ref:`int<class_int>` to_id, :ref:`bool<class_bool>` bidirectional=null  **)** |
+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                             | :ref:`disconnect_points<class_AStar_disconnect_points>`  **(** :ref:`int<class_int>` id, :ref:`int<class_int>` to_id  **)**                                       |
+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                            | :ref:`get_available_point_id<class_AStar_get_available_point_id>`  **(** **)** const                                                                              |
+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`int<class_int>`                            | :ref:`get_closest_point<class_AStar_get_closest_point>`  **(** :ref:`Vector3<class_vector3>` to_pos  **)** const                                                  |
+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Vector3<class_vector3>`                    | :ref:`get_closest_pos_in_segment<class_AStar_get_closest_pos_in_segment>`  **(** :ref:`Vector3<class_vector3>` to_pos  **)** const                                |
+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`PoolIntArray<class_poolintarray>`          | :ref:`get_id_path<class_AStar_get_id_path>`  **(** :ref:`int<class_int>` from_id, :ref:`int<class_int>` to_id  **)**                                              |
+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`PoolVector3Array<class_poolvector3array>`  | :ref:`get_point_path<class_AStar_get_point_path>`  **(** :ref:`int<class_int>` from_id, :ref:`int<class_int>` to_id  **)**                                        |
+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`Vector3<class_vector3>`                    | :ref:`get_point_pos<class_AStar_get_point_pos>`  **(** :ref:`int<class_int>` id  **)** const                                                                      |
+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`float<class_float>`                        | :ref:`get_point_weight_scale<class_AStar_get_point_weight_scale>`  **(** :ref:`int<class_int>` id  **)** const                                                    |
+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| :ref:`bool<class_bool>`                          | :ref:`has_point<class_AStar_has_point>`  **(** :ref:`int<class_int>` id  **)** const                                                                              |
+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+
| void                                             | :ref:`remove_point<class_AStar_remove_point>`  **(** :ref:`int<class_int>` id  **)**                                                                              |
+--------------------------------------------------+-------------------------------------------------------------------------------------------------------------------------------------------------------------------+

Description
-----------

A\* (A star) is a computer algorithm that is widely used in pathfinding and graph traversal, the process of plotting an efficiently directed path between multiple points. It enjoys widespread use due to its performance and accuracy. Godot's A\* implementation make use of vectors as points.

You must add points manually with :ref:`AStar.add_point<class_AStar_add_point>` and create segments manually with :ref:`AStar.connect_points<class_AStar_connect_points>`. So you can test if there is a path between two points with the :ref:`AStar.are_points_connected<class_AStar_are_points_connected>` function, get the list of existing ids in the found path with :ref:`AStar.get_id_path<class_AStar_get_id_path>`, or the points list with :ref:`AStar.get_point_path<class_AStar_get_point_path>`.

Member Function Description
---------------------------

.. _class_AStar__compute_cost:

- void  **_compute_cost**  **(** :ref:`int<class_int>` from_id, :ref:`int<class_int>` to_id  **)** virtual

.. _class_AStar__estimate_cost:

- void  **_estimate_cost**  **(** :ref:`int<class_int>` from_id, :ref:`int<class_int>` to_id  **)** virtual

.. _class_AStar_add_point:

- void  **add_point**  **(** :ref:`int<class_int>` id, :ref:`Vector3<class_vector3>` pos, :ref:`float<class_float>` weight_scale=null  **)**

Add a new point at the given position ``pos`` with the given identifier ``id``. The ``weight_scale`` has to be 1 or larger.

.. _class_AStar_are_points_connected:

- :ref:`bool<class_bool>`  **are_points_connected**  **(** :ref:`int<class_int>` id, :ref:`int<class_int>` to_id  **)** const

Returns if there is a connection/segment between points ``id`` and ``from_id``

.. _class_AStar_clear:

- void  **clear**  **(** **)**

Clear all the points and segments from AStar instance.

.. _class_AStar_connect_points:

- void  **connect_points**  **(** :ref:`int<class_int>` id, :ref:`int<class_int>` to_id, :ref:`bool<class_bool>` bidirectional=null  **)**

Create a segment between points ``id`` and ``to_id``.

.. _class_AStar_disconnect_points:

- void  **disconnect_points**  **(** :ref:`int<class_int>` id, :ref:`int<class_int>` to_id  **)**

Deletes a segment between points ``id`` and ``to_id``.

.. _class_AStar_get_available_point_id:

- :ref:`int<class_int>`  **get_available_point_id**  **(** **)** const

.. _class_AStar_get_closest_point:

- :ref:`int<class_int>`  **get_closest_point**  **(** :ref:`Vector3<class_vector3>` to_pos  **)** const

Returns the id of closest point of given point.  -1 is returned if there are no points on AStar.

.. _class_AStar_get_closest_pos_in_segment:

- :ref:`Vector3<class_vector3>`  **get_closest_pos_in_segment**  **(** :ref:`Vector3<class_vector3>` to_pos  **)** const

Returns the position of closest point that has segments.

.. _class_AStar_get_id_path:

- :ref:`PoolIntArray<class_poolintarray>`  **get_id_path**  **(** :ref:`int<class_int>` from_id, :ref:`int<class_int>` to_id  **)**

Returns an array with the point ids of path found by AStar between two given points.

.. _class_AStar_get_point_path:

- :ref:`PoolVector3Array<class_poolvector3array>`  **get_point_path**  **(** :ref:`int<class_int>` from_id, :ref:`int<class_int>` to_id  **)**

Returns an array with the points of path found by AStar between two given points.

.. _class_AStar_get_point_pos:

- :ref:`Vector3<class_vector3>`  **get_point_pos**  **(** :ref:`int<class_int>` id  **)** const

Returns the position of point with given id.

.. _class_AStar_get_point_weight_scale:

- :ref:`float<class_float>`  **get_point_weight_scale**  **(** :ref:`int<class_int>` id  **)** const

Returns the weight scale of point with given id.

.. _class_AStar_has_point:

- :ref:`bool<class_bool>`  **has_point**  **(** :ref:`int<class_int>` id  **)** const

Returns if the point with given id exists on AStar;

.. _class_AStar_remove_point:

- void  **remove_point**  **(** :ref:`int<class_int>` id  **)**

Removes the point with given id.


