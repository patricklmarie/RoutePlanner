<h1>GPX Route Planner</h1>
<p>GPX Route Planner is an open-source route planning application released under the MIT License.</p>
<p>© 2026 Patrick Marie</p>
<h2>Overview</h2>
<p>GPX Route Planner is a small <strong>route planning application</strong>. It is designed to enable hikers, cyclists, and even motorists to plan their trips by plotting a route on a map.</p>
<p>It is also a <strong>GPX editor</strong>: the route can be exported as a GPX file and then used with GPS devices or mobile navigation apps such as OsmAnd or Locus.</p>
<p>The application is written in JavaScript, contained in a single HTML file (GPX_Route_Planner.html), and can be run simply by opening this file in a web browser.</p>
<p>This application is entirely based on open-source technologies part of the <strong>OpenStreetMap</strong> ecosystem: <strong>Leaflet</strong> to render the map and the route, <strong>Nominatim</strong> to locate places from their addresses, <strong>BRouter</strong> to calculate routes between locations. 
The browser’s <strong>Geolocation API</strong> is used to determine the user’s position.</p>
<h2>Route structure</h2>
<p>In this tool, <strong>a route</strong> consists of:</p>
<ul>
<li><strong>One or more stages</strong>. A stage represents a journey planned to be completed in one go or in a single day. It consists of:
<ul>
<li><strong>A starting point, an end point, and optional waypoints</strong>. These points are rendered on the map using Leaflet <strong>circle markers</strong>.</li>
<li><strong>One or more sections</strong>. A section is a path (curved or straight) connecting two points of a stage. Sections are rendered on the map using Leaflet <strong>polylines</strong>. Their position and shape are calculated using <strong>BRouter</strong> or by drawing a straight segment, depending on the selected option.</li>
</ul>
</ul>
<h2>Event-driven design</h2>
<p>The tool provides functions to create, modify, and delete stages, as well as their points and sections.</p>
<p>A key feature of this application is its extensive use of Leaflet <strong>event handlers</strong> attached to various objects: the map, circle markers, and polylines. Depending on the context (stage editing mode or supervision mode), the required event handlers differ, and most of them cannot be assigned once and for all. Instead, they must be <strong>registered</strong>, in order to be dynamically <strong>retrieved</strong>, <strong>removed</strong>, and <strong>replaced</strong> by others as the context changes.</p>
<h2>Live demo</h2>
<p>https://yourusername.github.io/your-repo/</p>
<img width="1919" height="919" alt="image" src="https://github.com/user-attachments/assets/47730927-e211-4993-bbf6-30d31706b25c" />
