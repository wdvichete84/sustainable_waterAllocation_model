# Sustainable water allocation based on hydro-economic externalities
This model is based on PhD Thesis called (portuguese): Modelo de hidrossustentabilidade econômica como suporte à decisão na alocação de água em sistemas de recursos hídricos complexos.

The proposed model rely on an optimization core using priorities and economic parameters to represent the costs in a objetive funcion to minimize the network flow cost in each time-step. The optimization core used the Pywr (1) python librarie to solve the priority-based and hydro-economic proposed model.

The grafical user interface of AcquanetGIS is under development and will be fully available here as soon as possible.
(Link to repository of AcquanetGIS GUI).

The topology of the network flow should represent the water infrastructure as nodes with parameters configuration according to the option of representation (storage, turbines, water abstraction, etc). Figure 1 represent the AcquanetGIS topology.

![image](https://user-images.githubusercontent.com/62769737/208078741-6249234a-057c-4b7c-a0d3-944eb6805880.png)

Figure 1. Acquanet topology.

The AcquanetGIS consists of building and configuring a network using the priority and economic benefits/losses. Results are further analyzed in the context of hydrological indicators, sustainability indicators, economic indicators, and indicators of hydrological changes. Among the scenarios considered, operational rules, institutional conditions, and sustainable water use planning in a collaborative and participatory decision-making process will have information of the externalities and trade-off between multiple water uses for better water allocation solution option. Figure 2 present the model proposed scheme.

![model_flux](https://user-images.githubusercontent.com/62769737/209545135-2299219f-7216-4e6e-ad89-ef43f1dc2a5b.png)

Figure 2. AcquanetGIS water allocation proposed model. 

AcquanetGIS allow others optimization core based on the extensions of Pywr. The standard configuration use the linear programming (LP). However, using the linear program-ming optimization method will require the use of the piece wise technique. In other words, this technique consists in partitioning the non-linear demand curve into small pieces. Pywr library allow the piece wise node to include the minimum and maximum flow constrain based on the cost for each segment of the demand water function. In other words, the piece wise link node has multiples link with different flow and cost values in parallel. Figure 3 shows the piece wise node used in AcquanetGIS.

![image](https://user-images.githubusercontent.com/62769737/208078807-318ef7c4-5f55-46b5-8c79-8e73599debd8.png)

Figure 3. Representation of hydro-economic node based on piece wise linearization.

The proposed model was applyied to Sao Francisco Transboundary System (SFTS), one of the larger transposition of the world. The SFTS has capacity to abstract water up to 127 m3.s-1. The network flow topology of the model application is presented in Figure 4.

![image](https://user-images.githubusercontent.com/62769737/208078839-0359b78c-f2dd-4c7b-8de9-c87b51384d41.png)

Figure 4. São Francisco basin downstream of Sobradinho hydropower and transboundary system topology to network flow optimization.

The scenarios of model apllication was:
A1: priority-based optimization using water demand estimated for 2020, with and without SFTS;
A2: priority-based optimization using water demand estimated for 2040, with and without SFTS;
B1: hydro-economic optimization using water demand estimated for 2020, with and without SFTS;
B2: hydro-economic optimization using water demand estimated for 2040, with and without SFTS;

The model formulation and results is presend in paper: (will be filled as soon as the paper can be publish).

References and Supllementary Information:

(1) Tomlinson, J.E., Arnott, J.H. and Harou, J.J., 2020. A water resource simulator in Python. Environmental Modelling & Software. https://doi.org/10.1016/j.envsoft.2020.104635
