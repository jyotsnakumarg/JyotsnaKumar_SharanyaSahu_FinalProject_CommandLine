# Faith Based Affordable Housing 

This project is based on the research of Dr. Nadia Mian at the Voorhees Center for Civic Engagement on "YIGBY" developments. YIBGY refers to "Yes in God's Backyard" in which faith-based
insitutions such as churches, synagouges, mosques, etc that had redeveloped a part of their sites to be turned into affordable housing units. The following map intreprets data that 
has been collected through scraping data about the developments created from 2015-2025, as well as data from the US Census and current YIBGY legislature. 

This webmap will include two static maps and two dynamic maps to held visualize the current state of faith-based Affordable Housing in the United States. 

<style>
  .map-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 24px;
    align-items: start;
  }

  .map-item img {
    width: 100%;
    height: auto;
    max-height: 800px;
    object-fit: contain;
    border: 1px solid #ddd;
  }

  .map-item p {
    margin-top: 8px;
    font-size: 0.95rem;
    line-height: 1.4;
  }

  /* Stack on mobile */
  @media (max-width: 900px) {
    .map-grid {
      grid-template-columns: 1fr;
    }
  }
</style>

## Static Maps

<div class="map-grid">

  <div class="map-item">
    <img src="Rent Burdened Map.png" alt="Rent Burdened Population by State">
    <p>
This map represents the percentage of each state in which there is ‘rent burden’ this means renter spend 30% or more of the household income on their rent. The map represents the percentage of people who are rent burdened in each state. This was created using the ACS 2016-2020 Estimates from the US Census. Overlaid is the faith-based development points. The intention with this static map is to showcase the relationship between affordable housing development and rent burdened populations.
    </p>
  </div>

  <div class="map-item">
    <img src="YIGBYMap (1).png" alt="YIGBY Legislation and Development Counts">
    <p>
      The status of YIGBY legislation* compared with statewise development counts, as of 2025, can be compared here. Each state is colored based on whether they have passed laws, considered laws, declined to pass laws, or have not considered YIGBY legislation. Overlaid are circles representing the total number of developments passed in each state.

      <br><br>
      <em>*This map includes statewise legislation. YIGBY laws have also been passed at the local level, which is not included in the visualization.</em>
    </p>
  </div>

</div>


## Interactive Maps
<iframe src="InteractiveWebmapFB.html" height="855" width="95%"></iframe>
All 200 developments in the database (as of December 2025) are included in this map. The pattern of faith-based housing developments being constructed can be visualized using the timeline slider, which populates the developments by year*. 

Clicking on each development reveals a small popup which provides information on:
- The project name
- The congregation name and denomination/religion
- The year the project was completed
- The type of housing
- The project size
- The developer’s name
- If the property has a historic status
- The project description

Statewise trends can be toggled on/off, in the upper right-hand corner of the map. They provide information on the rent-burdened population, the status of YIGBY law implementation**, and the number of developments in each state. Hovering over each feature reveals information on each trend.

The basemap can also be switched between a simple Carto Positron basemap and Open Street Map, which can be helpful to examine other local features if you zoom into the basemap.

*4 developments’ opening dates have not been identified. They populate in the final year of the timeline slider, 2025.
**As per December, 2025.


<iframe src="NYCFaithBased.html" height="855" width="95%"></iframe>

This dynamic map showcases the developments that are specific to New York City. It is overlayed with a heat map representing the residential evictions that have happened within the past two year (2023-2025), in addition to this, one can see the parts of NYC that are zoned as “inclusionary Housing Areas.” This means that developers building in those areas get a tax credit for including affordable housing units in their buildings. The data was pulled from the NYC open data portal.
