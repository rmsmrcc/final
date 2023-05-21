# prismacrud-cbs-final-project

1. type npm install -g express-generator@4 ejs prisma@latest -g nodemon caesar-encrypt
2. type express
3. type npx prisma init
4. modify mongodb database url to env file
5. modify prisma file located @ /prisma/schema-prisma
6. change datasource db provider to mongodb
7. insert this after datasource db 

        model Student_Info { 
  
            id String @id @default(auto()) @map("_id") @db.ObjectId 

            firstname String? 
        
            middlename String? 
    
            lastname String? 
    
            birthdate DateTime? 
    
            gender String? 
    
            civilstatus String? 
    
            country String? 
    
            region String? 
    
            province String? 
    
            city String? 
    
            barangay String? 
    
            zipcode String? 
    
            address String? 
    
            hobbies String? 
    
            keya String? 
    
            keyb String? 
    
            createdAt DateTime @default(now()) 
    
            updatedAt DateTime @default(now()) 
        } 
   
        model User { 
     
            id String @id @default(auto()) @map("_id") @db.ObjectId 
     
            email String @unique 
     
            password String? 
     
            createdAt DateTime @default(now()) 
     
            userlevel String? @default("User") 
     
            shift Int 
        }

8. type prisma db push
9. type prisma generate client
10. modify package.json scripts to

        "scripts": { 
    
            "start": "nodemon app.js" 
        },
    
11. type npm start
12. open browser and type localhost:3000 for data table
13. open browser and type localhost:3000/register for register account
14. open browser and type localhost:3000/login for login account
