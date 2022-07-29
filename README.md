# AspNetCoreWebAPIAngular

tutorial link https://www.youtube.com/playlist?list=PLjC4UKOOcfDQfrxjOgGKM_UmydQig8pq5
Implemented User Registration with Asp.Net Core Web API and Angular 7.


            app.Use(async(ctx,next) => {
                await next();
                if (ctx.Response.StatusCode == 204) {
                    ctx.Response.ContentLength = 0;
                }
            });

            services.Configure<IdentityOptions>(options =>
            {
                options.Password.RequireDigit = false;
                options.Password.RequireNonAlphanumeric = false;
                options.Password.RequireUppercase = false;
                options.Password.RequiredLength = 4;
            });

            services.AddCors();
       

 ![image](https://user-images.githubusercontent.com/12700182/181708350-889fe0a7-b187-4034-8810-3ab2a40713c8.png)
 
```
First we install the Microsoft.EntityFrameworkCore.SqlServer NuGet Package:

PM > Install-Package Microsoft.EntityFrameworkCore.SqlServer
Then, after importing the namespace with

using Microsoft.EntityFrameworkCore;
we add the database context:

services.AddDbContext<AspDbContext>(options =>
    options.UseSqlServer(config.GetConnectionString("optimumDB")));
```
