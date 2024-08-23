# journey_builder_api_event
This documentation explain how to create and test an api entry event inside Journey Builder.

1º Create a new package to use a API SERVER-TO-SERVER integration (it will be used to get the request a valid SFMC token and realize tests in Postman)
Learn more here: https://developer.salesforce.com/docs/marketing/marketing-cloud/guide/install-packages.html

2º Data Designer <br>
Seriously, you NEED to use Data Designer without creating complex SQL queries that use a lot of time running between data extensions, just use Data Designer to build relationships with your data extensions, this is a game changer when you know how to do it and separates the juniors from experts in data extensions.
Use case: you have a data extension abandon chart that has a pk inside of it and another data extension with profile details, you can simply create this relationship without any type of automation previously running on Automation Studio by simply adding a relationship in Data Designer, by doing this you can control on what data extension do you want to save the API entry data and also use customization in your content without running complex SSJS inside your document.
Learn more here: https://help.salesforce.com/s/articleView?id=sf.mc_cab_data_designer.htm&type=5

3º Create a multi-step journey and select API event as entry source

4 º The journey builder API entry event will create a **EVENT DEFINITION KEY** this will be used to refers the correct journey that you wanted to insert data.

5º You can use flow control to filter specific type of data to split your audience if you need, for example, a person that have input in a form some preferences and them put this persona in a different path in your journey.

learn more here: https://help.salesforce.com/s/articleView?id=sf.mc_jb_canvas_activities.htm&language=en_US&type=5 or https://deselect.com/blog/flow-activities-integrations-sfmc-journey-builder/

6º Define your goals, for example, a column specific of data that has increased, this can be a goal (like an increase RFM metric of an specific persona).

7º Test your journey using Postman, here is the collection of Postman https://www.postman.com/salesforce-developers/salesforce-developers/collection/yzxd2wj/salesforce-marketing-cloud-apis

8º Publish and keep analyzing the metrics

9º You can also use flags inside your journey builder activity to control the entire flow of users in your journey.

