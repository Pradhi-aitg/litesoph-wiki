.. _code overview:

=================
Code Architecture
=================


This document describes the overall code architecture.


Full Picture of Class hierarchy::

                       +---------+             
                       |LSManager|
                       +---------+
                     ______|_______
                    |              |
                    V              V
            ProjectInfo <---------ProjectManager
                |                   |
                V                   V
            WorkflowInfo <--------WorkflowManager
                |                   | 
                |                   V             
                |                  EngineManager
                |                     |  
                V                     V
            TaskInfo  <-------------Task
                                _______|______
                                |             |
                                V             V          
                            SubmitLocal   SubmitNetwork
                                                |
                                                V
                                        NetworkJobSubmission



.. autoclass:: litesoph.common.ls_manager.LSManager
   :members:
   :inherited-members:

.. autoclass:: litesoph.common.project_manager.ProjectManager
   :members:
   :inherited-members:

.. autoclass:: litesoph.common.workflow_manager.WorkflowManager
   :members:
   :inherited-members:


.. autoclass:: litesoph.common.engine_manager.EngineManager
   :members:
   :inherited-members:


.. autoclass:: litesoph.common.data_sturcture.data_classes.ProjectInfo
   :members:
   :inherited-members:

.. autoclass:: litesoph.common.data_sturcture.data_classes.WorkflowInfo
   :members:
   :inherited-members:

.. autoclass:: litesoph.common.data_sturcture.data_classes.TaskInfo
   :members:
   :inherited-members:


The LITESOPH Architecture has the following model.

.. image:: ../_static/images/litesoph_layers_30_11_22.png
   :width: 800
   :alt: LITESOPH_home

User's Navigation for LITESOPH:
#######################
The User's Navigation for LITESOPH is as the following:

.. image:: ../_static/images/User-navigation.png
   :width: 800
   :alt: Pre      

