How do you write programs that are maintainable, readable, and adaptable?

I write maintainable, readable, and adaptable programs by separating responsibilities, using clear naming conventions, and keeping code modular. In this course, the best example of that was building the CRUD Python module in Project One and then reusing it in Project Two to connect the dashboard widgets to the MongoDB database. Keeping all database logic inside the CRUD module meant the dashboard code stayed focused on UI behavior (filters, tables, map updates) instead of being cluttered with database connection details and query logic.

The advantage of working this way is that changes are easier and safer. If the database connection settings, query structure, or collection changes, I can update the CRUD module once and the dashboard continues to work without needing edits in multiple places. It also improves testing because I can validate database operations independently from the UI. In the future, I could reuse this CRUD module for other dashboards, add new methods for aggregation queries, connect it to a different collection, or build a separate API/service layer that uses the same CRUD functions for consistent database access.

How do you approach a problem as a computer scientist?

I approach problems by translating requirements into specific technical tasks, validating assumptions using small tests, and building the solution in layers. For the Grazioso Salvare requirements, I started by identifying what data the dashboard needed to display and filter (such as rescue-animal attributes and location data), then verified that my MongoDB queries returned correct results before wiring those queries into the dashboard callbacks. This helped prevent the common issue of debugging UI problems that are actually caused by incorrect data retrieval.

Compared to previous assignments in other courses, this project felt more like building for a real client instead of completing a single isolated program. I had to think about usability, data accuracy, and how different parts of the system (database, CRUD module, and dashboard UI) interact. In the future, to create databases that meet other client requests, I would continue using strategies like: modeling the data early, writing queries directly in the database shell to confirm results, defining reusable data-access methods (like CRUD), and iterating with incremental testing so each layer works before adding the next.

What do computer scientists do, and why does it matter?

Computer scientists design and build systems that turn data into useful information and automate processes that would otherwise be slow, error-prone, or difficult to scale. This work matters because companies depend on accurate data access, reliable software, and clear interfaces to make decisions and complete their mission efficiently.

A project like this helps a company like Grazioso Salvare by giving them a faster and more consistent way to explore their data. Instead of manually searching records, the dashboard allows users to filter, view, and visualize information quickly, which improves decision-making and response time. The combination of MongoDB, a reusable CRUD layer, and an interactive dashboard demonstrates how software can reduce manual workload, increase accuracy, and provide actionable insight from complex datasets.
