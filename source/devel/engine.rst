.. _Adding new engine:


=================
Adding new engine
=================

The litesoph code base is structered in a modular format :ref:`code overview` so that 
it is simple and staright-forward to add a new engine or task.

The step by step procedure to add a new engine to the 
litesoph code base is described below.


1. Add engine to the :class:`litesoph.engines.engine_classname` dictionary. The key
should be the name of the engine and the value should be the class name used to defines 
the engine manager. For Example, if the engine name is: ``newengine``.

::

    {'newengine': 'NewEngine'}

Where ``NewEngine`` will be the class name used to define the engine manager

2. Create a new directory in :mod:`litesoph.engines` name it as ``newengine`` and a new python file
in this directory and name it as ``newengine_manager.py``.

3. In the new file ``newengine_manager.py`` create a new subclass of :class:`~litesoph.common.engine_manager.EngineManager` 
and name it as ``NewEngineManager``

4. Implement all the abstract methods of :class:`litesoph.engines.engine_manager.EngineManager`


.. seealso::
    * The code for our NWChem interface: :git:`litesoph.engines.newchem.nwchem_manager.py`


Description of base-classes
===========================


The Engine base-classes
-----------------------

.. autoclass:: litesoph.common.engine_manager.EngineManager
   :members:
   :private-members:
   :member-order: bysource



