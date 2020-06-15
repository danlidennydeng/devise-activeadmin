1. In activeadmin, we cannot know who has made what changes to the database if we have multiple admin_users. I don't think public_activity gem might work for activeadmin.

2. must disable downloading data locally.

3. admin_users can delete each others and edit each others. So we need to disable deleting admin_users. must delete admin_users from raw database with SQL

4. must disable deleting records of each model.

5. only allow edit necessary columns.

6. might be ONLY good for internal management of non-critical data, such as models of local, property_management, real_estate_developer.

------------------------------------------------------------------------------------------------
denny@desktop-ubuntu18:~/apps/devise-activeadmin$ rails db:migrate
rails aborted!
NameError: uninitialized constant Apartment::Elevators
 
When I tried to upgrade to Rails 5.0.7