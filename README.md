# Review and Plots of data available in moja global's Land Sector Datasets.
---
Contribution to moja global.
---
# **DATASETS GUIDE**

> Note that this compilation is focused in datasets that include Peru, South América.

1. **Adminitrative Boundaries**

  NOTE: The first 2 geodataframes are **NOT HOSTED IN THE MOJA GOBAL DATASET**. They below to Level 0 adminitration boundaries.

  * `world_df` - **World boundaries** - (Level 0, data source: [Natural Earth](https://www.naturalearthdata.com/downloads/110m-cultural-vectors/110m-admin-0-boundary-lines/))
  * `southamerica_df` - **South American boundaries** - Clipped from (*world_df*).
  * `boundary_df` - **Peruvian Administrative boundaries** (Level 2, data source: [OpenStreetMap](https://planet.openstreetmap.org/) NOTE: As these datasets seems to be clipped from a bigger dataframe, correction in the georeference is necessary with [Peru EPSG: 5389 / UTM zones 19S](https://epsg.io/5389).
    * `mdiosBoundary_df` - **boundary of Madre de Dios Province** (Level 4, data source : same as 1) NOTE: Same correction a (*boundary_df*).
    * `cuscoBoundary_df` - **boundary of Cusco Province** (Level 4, data source : same as 1). NOTE: Same correction a `boundary_df`.
    * `regionsBoundary_df` - **boundaries of both Peruvian Provinces**

2. **Soil resources**

  The dataset uses the World Referece Base ([WBR](https://www.fao.org/soils-portal/data-hub/soil-classification/world-reference-base/en/)) which is the international standard for soil classification system endorsed by the International Union of Soil Sciences, this system also includes a modern soil classification concepts and [USDA Soil Taxonomy](https://www.fao.org/soils-portal/data-hub/soil-classification/usda-soil-taxonomy/en/). 

  * `soil_df` - **World soil resources** (data source: World Soil Resources Coverage in Geographic Projection (ARC/Info Export format) "wsrll" Reports from [FAO](https://www.fao.org/soils-portal/data-hub/soil-maps-and-databases/other-global-soil-maps-and-databases/en/))
  * `south_americaSoil_df` - **South America soil resources** clipped from the *World soil resources* (above).
  * `peruSoil_df` - **Peruvian soil resources** (data source: same as *World soil resources*)
    * `mdiosSoil_df` - **Soil resources of Madre de Dios**
    * `cuscoSoil_df` - **Soil resources of Cusco**
    * `regionsSoil_df` - **Soil resources of both Peruvian Provinces**

3. **CI Biodiversity Hotspots** Contains information of the 36 recognzed bioidiversity hotspots in the earth. Contains a lot of biodiversity criteria , this dataaset focus on endemism on many plants species.
  * `bioHot_df` - **World Biodiversity Hotspots** (data source: [Zenodo](https://zenodo.org/record/3261807#.YX9zib_MK03))
  * `south_americaBioHot_df` - **South America Biodiversity Hotspots** clipped from the (*bioHot_df*)
  * `peruBioHot_df` - **Peruvian Biodiversity Hotspots** clipped from the (*bioHot_df*)
    * `mdiosBioHot_df` - **Biodiversity Hotspots of Madre de Dios** clipped from the (*bioHot_df*)
    * `cuscoBioHot_df` - **Biodiversity Hotspots of Cusco** clipped from the (*bioHot_df*)
    * `regionsBioHot_df` - **Biodiversity Hotspots of both Peruvian Provinces** clipped from the (*bioHot_df*)

4. **Bioclimatic and ecological zones**  This dataset has developed over the years from covering only the tropical areas (1990) to the globe (2000), due constant changes in climate and landcover, a new map where develoaped in 2010 (the one is loaded in this notebook).

  * `bioEco_df` - **Bioclimatic and ecological zones of the World** (data source: The Global ecological zones (GEZ), reports from [FAO](https://data.apps.fao.org/map/catalog/srv/eng/catalog.search?id=47105&fname=gez2010.zip&access=private#/metadata/2fb209d0-fd34-4e5e-a3d8-a13c241eb61b).
  * `south_americabioEco_df` - **Bioclimatic and ecological zones of South America** clipped from the (*bioEco_df*)
  * `perubioEco_df` - **Bioclimatic and ecological zones of Peru** (data source: The Global ecological zones (GEZ), reports from [FAO](https://data.apps.fao.org/map/catalog/srv/eng/catalog.search?id=47105&fname=gez2010.zip&access=private#/metadata/2fb209d0-fd34-4e5e-a3d8-a13c241eb61b). NOTE: worng georeference, review.
    * `mdiosBioEco_df` - **Bioclimatic and ecological zones of Madre de Dios** clipped from the (*peruBioHot_df*). NOTE: worng georeference, review.
    * `cuscoBioEco_df` - **Bioclimatic and ecological zones of Cusco** clipped from the (*peruBioHot_df*). NOTE: worng georeference, review.
    * `regionsEcoHot_df` - ***Bioclimatic and ecological zones of of both Peruvian Provinces** clipped from the (*peruBioHot_df*)

5. **Holdridge Life zones** 
  * `holdrigde_df` - **World Holdridge Life zones** (data source: FAO, not avalaible for consult (October, 2021) but stated in the [Global ecological Zones for FAO forest reporting: 2010 update](https://www.fao.org/3/ap861e/ap861e00.pdf))
  * `south_americaHoldridge_df` - **Holdridge Life Zones of South America** clipped from the (*holdridge_df*).
  * `peruHoldridge_df` - **Holdridge Life Zones of Peru**, clipped from the (*holdridge_df*).
    * `mdiosHoldridge_df` - **Holdridge Life Zones of Madre de Dios** clipped from the (*holdridge_df*).
    * `cuscoHoldridge_df` - **Holdridge Life Zones of Cusco**, clipped from the (*holdridge_df*).
    * `regionsHoldridge_df` - ***Holdridge Life Zones of of both Peruvian Provinces**, clipped from the (*holdridge_df*).

6. **Agro ecological zones.**  The GAEZ programs utilize the land resources inventory to assess all feasible agricultural land-use options and to quantify expected production of cropping activities relevant in a particular agro-ecological context, for specified management conditions and levels of inputs. The characterization of land resources includes all relevant components of climate, soils and landform, which are basic for the supply of water, energy, nutrients and physical support to plants.) Support for the used codes from the [documentation](https://webarchive.iiasa.ac.at/Research/LUC/GAEZv3.0/docs/GAEZ_User_Guide.pdf) (pag 49).
  * `agroEco_df` - **World Agro ecological zones** (data source: [The Global Agro‐Ecological Zones system (GAEZ) developed by the FAO](https://webarchive.iiasa.ac.at/Research/LUC/GAEZv3.0/))
  * `south_americaagroEco_df` - **Agro ecological zones of South America** clipped from the (*agroEco_df*).
  * `peruagroEco_df` - **Agro ecological zones of Peru**, clipped from the (*agroEco_df*).
    * `mdiosagroEco_df` - **Agro ecological zones of Madre de Dios** clipped from the (*agroEco_df*).
    * `cuscoagroEco_df` - **Agro ecological zones of Cusco**, clipped from the (*agroEco_df*).
    * `regionsagroEco_df` - **Agro ecological zones of of both Peruvian Provinces**, clipped from the (*agroEco_df*).

7. **Planted Forest.** Taken from the Spatial Database of Planted Trees (SDPT), compiled by Global Forest Watch using data obtained from national governments, non-governmental organizations and independent researchers). Also, some features where review from the [documentation](https://www.wri.org/research/spatial-database-planted-trees-sdpt-version-10).
  * `forest_df`- **Planted Forest in Peru** (data source: [Arcgis](https://www.arcgis.com/home/item.html?id=224e00192f6d408fa5147bbfc13b62dd))
    * `mdiosForest_df` - **Planted Forest in Madre de Dios**, clipped from (*forest_df*).
    * `cuscoForest_df` - **Planted Forest in Cusco**, clipped from (*forest_df*).
    * `regionsForest_df` - **Planted Forest in both Peruvian Province**, clipped from (*forest_df*).

8. **Climate zones.** Based on the classification of IPCC.The zones are defined by a set of rules based on : annual mean daily, temperature, total annual precipitation, total annual potential evapo-transpiration (PET) and elevation. Extra featuures where revied from the [documentation](https://maps3.arcgisonline.com/arcgis/rest/services/A-16/Koeppen-Geiger_Observed_and_Predicted_Climate_Shifts/MapServer).
  
  Class names labels where collected from the [Guidelines for the calculation of land carbon stocks for the purpose of Annex V to Directive 2009/28/EC](https://eur-lex.europa.eu/LexUriServ/LexUriServ.do?uri=OJ:L:2010:151:0019:0041:EN:PDF) (Page 3).

  * `climate_df` - **World Climate zones** (data source: The [Climatic Zone layer](https://esdac.jrc.ec.europa.eu/projects/RenewableEnergy/).
  * `south_americaClimate_df` - **Climate zones of South America** clipped from the (*climate_df*).
  * `peruClimate_df` - **Climatic zones of Peru**, clipped from the (*climate_df*).
    * `mdiosClimate_df` - **Climatic zones of Madre de Dios** clipped from the (*climate_df*).
    * `cuscoClimate_df` - **Climatic zones of Cusco**, clipped from the (*climate_df*).
    * `regionsClimate_df` - **Climatic zones of of both Peruvian Provinces**, clipped from the (*climate_df*).

8. **Koppen-Geiger Climate Changes (1901-2100)** `koppen` (**in a list of dataframes**, data source: Wladimir Köppen vegetation-based [empirical climate classification system](https://sos.noaa.gov/catalog/datasets/koppen-geiger-climate-changes-1901-2100/), this system is based on the idea that climate is best defined by native vegetation. The formulas used in the classification correspond to those of the vegetation zones (biomes) that were being mapped for the first time in the late 19th century. [Documentation](https://www.researchgate.net/publication/26640584_Updated_World_Map_of_the_Koppen-Geiger_Climate_Classification).

  The dataset contains different version:
  - **Shifts bases on observations** (1901 - 2000):
    * `observations_world` - **World - Shifts bases on observations** 
    * `observations_southamerica` - **South America - Shifts based on observations**
    * `observations_peru` - **Peru - Shifts based on observations**
    * `observations_region` - **Region (Madre de Dios and Cusco) - Shifts based on observations.**

  Another versions based on the [A1F1 IPCC climate scenario](http://www.ipcc-data.org/observ/ddc_co2.html) (2001 - 2100):
  
  - **A1FI Emision Scenarios**, based on: 
  > Rapid economic growth, low population growth and rapid introduction of new and more efficient technology.

    - `a1f1_world` - **World - Shifts based A1F1 Emision Scenarios**
    - `a1f1_southamerica` - **South America - Shifts based A1F1 Emision Scenarios**
    - `a1f1_peru` - **Peru - Shifts based A1F1 Emision Scenarios**
    - `a1f1_region` - **Region (Madre de Dios and Cusco) - Shifts based A1F1 Emision Scenarios**

  - **A2 Emision Scenario**, based on:
  > A very heterogeneous world, high population growth, and less concern for rapid economic development.

    * `a2_world` - **World - Shifts based A2 Emision Scenarios**
    * `a2_southamerica` - **South America - Shifts based A2 Emision Scenarios**
    * `a2_peru` - **Peru - Shifts based A2 Emision Scenarios**
    * `a2_region` - **Region (Madre de Dios and Cusco) - Shifts based A2 Emision Scenarios**

  - **B1 Emision Scenario**, based on:
  > A convergent world but with rapid changes in economic structures toward a service and information economy, with reductions in materials intensity, and the introduction of clean and resource-efficient technologies.
  
    * `b1_world` - **World - Shifts based B1 Emision Scenarios**
    * `b1_southamerica` - **South America - Shifts based B1 Emision Scenarios**
    * `b1_peru` - **Peru - Shifts based B1 Emision Scenarios**
    * `b1_region` - **Region (Madre de Dios and Cusco) - Shifts based B1 Emision Scenarios** 

  - **B2 Emissions Scenarios**, based on:
  > A heterogeneous world in which the emphasis is on local solutions to economic, social, and environmental sustainability. With less rapid, and more diverse technological, society looking for local solutions (rather than global).

    * `b2_world` - **World - Shifts based B2 Emision Scenarios**
    * `b2_southamerica` - **South America - Shifts based B2 Emision Scenarios**
    * `b2_peru` - **Peru - Shifts based B2 Emision Scenarios**
    * `b2_region` - **Region (Madre de Dios and Cusco) - Shifts based B2 Emision Scenarios** 
