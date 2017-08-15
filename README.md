Vitalii sent his public key to me, he should now be able to log into our 2nd development system dev2.shapediver.com. This development system can be accessed here:

https://dev2.shapediver.com

http user: access
http passwd: 13a27s

Some information important for development:

The mysql database can be accessed using portforwarding:

ssh -i ~/.ssh/PRIVATE_KEY.pem -L3306:shapedivermysqlfreetier.c8o4qufxicjx.us-east-1.rds.amazonaws.com:3306 ec2-user@dev2.shapediver.com

Name of database: ShapeDiverDevelopment
user: shapediverdev
passwd: NSSbHWjhshWWdU7qP3tg

The webserver document root:

/var/www/dev2.shapediver.com

On this instance its possible to become superuser without password, simply use sudo.

In a few minutes I will send a separate email regarding the test assignment
[17:19:27] Vira Nikitenko: please find below our test assignments we would like Vitalii to work on. In case of questions we are typically available to answer on short notice.


1) Blog author role:
Currently the users in our database have three possible roles:
 - Normal users using the free platform (role number: 0)
 - PRO users who pay and have access to more features (role number: 1)
 - Administrators (just the ShapeDiver team, role number: 10).

At the moment, only the administrators can be authors of blog articles on our blog. We would like to add a new role (role number: 2) for other users to be able to post in the blog (guest posts). So far, we had to make them administrators, which is not good (example: https://www.shapediver.com//blog/parametricism-and-attractors)
The role is just a column in the "users" table in our database.
Can you please add the role number 2, where users have all the rights of role number 1 PLUS the ability to be the author of blog posts?


2) List private models: (this is actually kind of a bug that would be nice to fix)
All users, registered or not, can see all the public models of the platform (https://www.shapediver.com/m).
However, registered users can choose to make some models private, in which case they are not publicly visible. Only the authors can see their private models. The authors... and us of course ;)
The admins (role 10) can see all the private models. However we would like even more power: when you click on a user's name and go to their profile, you can see the list of all their public models. We would like the admins to be able to see all the public AND private models on this page. For example, this user has over 20 models (public and private), but when I visit his profile page I only see his 3 public models: https://www.shapediver.com/jewelrydesigns
Admins can already access the private models through a search, but they are not listed on the profile pages.
Can you give the admins the possibility to list all public and private models on profile pages?

