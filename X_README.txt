Thoughts on formatting:
In the "BookingController" I noticed numerous controller methods. For better code organization and enhanced readability, it's recommended to have only CRUD (Create, Read, Update, Delete) functions within a controller.
For instance, the "BookingController" should ideally contain CRUD functions such as "index," "create," "store," "edit," "update," and "delete" or "destroy." If additional methods related to bookings are needed, consider creating new controllers rather than adding unlimited methods to a single controller.
Here's a suggestion for reorganizing the current BookingController methods:
"index," "show," "store," "update" methods should remain in the "BookingController."
Methods like "getHistory," "acceptJob," "acceptJobWithId," "cancelJob," and "endJob" should be moved to a separate controller named "BookingJobController" If feasible, align the method names with CRUD functions and provide documentation for each method

In the "BookingController," there's a "distanceFeed" method. the logic within this function should ideally reside inside its corresponding repository class not in controller. actually its okay if we write business logic in controller but but maintaining consistency across the entire application would be beneficial.
In "BookingRepository" class there are lot of places code commented and unused variables


Conclusion:
Overall code looks good to me. only few adjustment which i describe above can make this code more robust and accessible.
The code utilizes the Repository pattern which is suitable for handling complex and extensive applications. It separate the business logic from other MVC components, help in centralized code management, Allow code reuse and improve code readability.
I've observed that the method names in the Repository class are meaningful, effectively describing their functionality. Additionally, each method has properly documented parameter descriptions.
