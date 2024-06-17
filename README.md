Compatible (well, as of 6/17/2024 still was) with https://github.com/DontDoThat21/Angular16 Angular basic demo application for the management of Employees and their Departments with a simple SQL Server DB powering this Legacy .NET FW API's datas.

Want to use .NET Core API with Ang16 (.NET 8) instead?

See: https://github.com/DontDoThat21/WebAPI.NET-Core

Table creation SQL (SQL Server): 

  create table Departments(
  DepartmentId int identity(1,1),
  DepartmentName varchar(500)
  );

  create table Employees(
  EmployeeId int identity(1,1),
  EmployeeName varchar(500),
  Department varchar(500),
  DateJoined date,
  PhotoFileName varchar(500)
  );

SELECT TOP (1000) [DepartmentId]
      ,[DepartmentName]
  FROM [AngularNETCoreEmployeesDB].[dbo].[Departments]

SELECT TOP (1000) [EmployeeId]
      ,[EmployeeName]
      ,[Department]
      ,[DateJoined]
      ,[PhotoFileName]
  FROM [AngularNETCoreEmployeesDB].[dbo].[Employees]
