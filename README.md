# week4-omeruysal
week4-omeruysal created by GitHub Classroom


Tech Stacks: Node.js Typescript Mysql Typeorm Jwt Express

With this project people can register the system, they can upload products, create orders and many operations. There are some roles for authorization with priorities.
Project runs on 8080 as default. Before start project, you can run those commands for sample datas;

### npm run roles:bootstrap  
### npm run products:bootstrap  
### npm run orders:bootstrap   

Endpoints :  
  
   POST('/api/register', Register);  
   POST('/api/login', Login);  
   GET('/api/user',  AuthenticatedUser);  
   POST('/api/logout',  Logout);  
   PUT('/api/user/info',  UpdateInfo);  
   PUT('/api/user/password',  UpdatePassword);  
  
   GET('/api/users',   Users);  
   POST('/api/users',   CreateUser);  
   GET('/api/users/:id',   GetUser);  
   PUT('/api/users/:id',   UpdatedUser);  
   DELETE('/api/users/:id',   DeleteUser);  
  
   GET('/api/permissions',  Permissions);  
  
   GET('/api/roles', Roles);  
   POST('/api/roles', CreateRole);  
   GET('/api/roles/:id', GetRole);  
   PUT('/api/roles/:id', UpdateRole);  
   DELETE('/api/roles/:id', DeleteRole);  
  
   GET('/api/products', Products);  
   POST('/api/products', CreateProduct);  
   GET('/api/products/:id', GetProduct);  
   PUT('/api/products/:id', UpdateProduct);  
   DELETE('/api/products/:id', DeleteProduct);  
  
   POST('/api/upload', Upload);  

   GET('/api/orders', Orders);  
   POST('/api/export', Export);  
   GET('/api/chart', Chart);  
  
  
1 - First we register system  
POST Register : http://localhost:8080/api/register  
{  
    "firstName":"user",  
    "lastName":"user",  
    "email":"user@user.com",  
    "password":"12345",  
    "passwordConfirm":"12345"  
}  
2 - We log in  
POST Login : http://localhost:8080/api/login   
{  
    "email":"user@user1.com",  
    "password":"12345",  
}  
3 - We update our role as admin
 PUT http://localhost:8080/api/user/info
{
  "role": {
      "id": 1,
      "name": "Admin"
       }
}  
4 - After uploading our account as admin, we can reach all endpoints.

