url:  

    http://localhost:8000/graphql

# ``#Core Module``


## Get About Us 

    query{
      aboutUs{
        id
        title
        description
        image
        createdAt
        updatedAt
      }
    }


## Get Privacy Policy

    query{
      privacyPolicy{
        id
        title
        description
        createdAt
        updatedAt
        
      }
    }


## Get TermsAndConditions

    query{
      termsAndConditions{
        id
        title
        description
        createdAt
        updatedAt
      }
    }


## Get All Report Type

    query{
      reportTypes{
        id
        name
      }
      bugReports{
        id
        name
        reason
        reportType{
          id
          name
        }
        createdAt
      }
     }

## Create Report Type

    mutation{
      createReportType(input:{
        name: "Debug Error"

      }){
        reportType{
          id
          name
        }
      }
    }

## Update Report Type

      mutation{
          updateReportType(id:3,input:{name:"data not found"}){
            reportType{
              id
            }
          }
        }

## Delete Report Type

    mutation{
      deleteReportType(id:3){
        success
      }
    }

## Get Bug Report List

      query{
        bugReports{
          id
          name
          title
          reason
          reportType{
            id
            name
          }
          createdAt
        }
      }

## Create Bug Report

    mutation{
      createReport(input:{
        title: "Bug1"
        name: "No jani"
        reason:"erorr"
        reportType: 2
      }){
        report{
          id
          title
          name
          reason
          reportType{
            id
            name
          }
        }
      }
    }

## Update Bug Report

    mutation{
      updateReport(id:2,input:{
        title:"Report Update"
        name:"Foysal"
        reason:"Site Error"
        reportType:1

      }){
    report{
          id
          title
          name
          reason
          reportType{
            id
            name
          }
        }
      }
    }
    
## Delete Bug Report

    mutation{
      deleteReport(id:2){
       success
      }
    }

# ``#Setup Module ``
## Get Language & Currencies

    query{
      allLanguages{
        id
        name
        code
      }
      allCurrencies{
        id
        name
        code
      }
    }

## Get All All Nomination Types

    query{
      allNominationTypes{
        id
        name

      }
    }

## Create  All Nomination Types

    mutation{
      createNominationType(input:{
        name: "New Nomination Types"
      }){
        nominationType{
          id
          name
        }
      }
    }

## Update  All Nomination Types

    mutation{
      updateNominationType(id:16, input:{
        name: "update  All Nomination Types"
        })
        {
        success
      }
    }

## Delete  All Nomination Types

    mutation{
      deleteNominationType(id:16){
        success
      }
    }



## Get All Nominations
    query{
      allNominations{
        id
        nominee{
          id
          name
          email
        }
        doner{
          id
          name
          email
        }
        nominationType{
          id
          name 
        }
        reason
      }
    }

## Create Nomination

    mutation{
      createNomination(input:{
        nominee:1
        doner:2
        nominationType:2
        reason:"New Nomination"
      }){
        nomination{
          id
        }
      }
    }

## Update Nomination

      mutation{
        updateNomination(id:5, input:{
          nominee:2
          doner:1
          nominationType:3
          reason:"Update Nomination"
        }){
          nomination{
            id
    
          }
        }
      }
## Delete Nomination
      mutation{
        deleteNomination(id:5){
          success
        }
      }

    
## Get All Address Type


	query{
      allAddressTypes{
        id
        name
      }
    }

## Create Address Type 


	 mutation{
    createAddressType(input:{name:"Shipping"}) {
      addressType{
        id
        name
      }
    }
  }

# Create Address Type 
    mutation{
      updateAddressType(id:12,input:{name:"Billing"}){
        addressType{
          id
          name
        }
        success
      }
    }

## Delete Address Type
    mutation{
      deleteAddressType(id:12){
        success

      }
    }



## Get All Product Types 
    query{
      allProductTypes{
        id
        name
      }
    }

## Create Product Type
    mutation{
      createProductType(input:{
        name:"Bikes"
      }){
        productType{
          id
          name
        }
        success
      }
    }


## Update Product Type

    mutation{
      updateProductType(id:1,input:{
        name:"car"
      }){
        productType{
          id
          name
        }
        success
      }
    }

## Delete Product Type

    mutation{
      deleteProductType(id:4){
        success
      }
    }

## Get all Product Rate Type

    query{
      allProductRateTypes{
        id
        name
      }
    }

## Create Product Rate Type

    mutation{
      createProductRateType(input:{name:"Box"}){
        productRateType{
          id
          name
        }
      }
    }


## Update Product Rate Type
    mutation{
      updateProductRateType(id:3,input:{name:"Cartons"}){
        productRateType{
          id
          name
        }
        success
      }
    }


## Delete Product Rate Type

    mutation{
      deleteProductRateType(id:3)
      {
        success
      }
    }

## Get All Contact Types
    query{
      allContactTypes{
        id
        name
      }
    }


## Create Contact Type

    mutation{
      createContactType(input:{name:"Individual"}){
        contactType{
          id
          name
        }
        success
      }
    }


## Update Contact Type

    mutation{
      updateContactType(id:3,input:{name:"Employee"}){
        contactType{
          id
          name
        }
        success
      }
    }


## Update Contact Type
    mutation{
      deleteContactType(id:3){
        success
      }
    }


## Get All Contacts

    query{
      allContacts{
        id
        contactedBy{
          id
          name
          email
        }
        contactType{
          id
          name
        }
        contactMessage
        contactedWith{
          id
          name
          email
        }
      }
    }

## Create Contact

    mutation{
      createContact(input:{
        contactedBy:1
        contactType:2
        contactMessage:"New Contacts Hello Boss"
        contactedWith:2
      }){
        success
      } 
    }


## Update Contact

    mutation{
      updateContact(id:4,input:{
        contactedBy:2
        contactType:1
        contactMessage:"Update Contact Hello Sir"
        contactedWith:1
      }){
        success
      } 
    }


## Delete Contact

    mutation{
      deleteContact(id:4){
        success
      }
    }


# ``# Shop Module``

## Get All Shops 

    query{
      allShops{
        id
        name
        street
        city
        state
        zipCode
        areaCode
        country
        phone
        website
        email
        description
        shopImage
        owner{
          id
          name
          email
        }
        createdAt     
      }
    }

## Create New Shop 

    mutation{
      createShop(input:{
        name:"My Shop"
      })
      {
        shop{
          id
          name
        }
        success
      }
    }


## Update Shop 

    mutation{
      updateShop(id:11,input:{
        name:"Shop1"
      })
      {
        shop{
          id
          name
        }
        success
      }
    }

## Delete Shop 

    mutation{
      deleteShop(id:11){
        success
      }
    }

# ``# Product Module ``
## Get All Product 

    query{
      allProducts{
        id
        name
        productType{
          id
          name
        }
        shop{
          id
          name
          email
          website
        }
        description
        createdAt
      }
    }



## Create New Product

    mutation{
      createProduct(input:{
        name:"Royal enfield"
        productType:2
        shop:2
        description:"Explore latest motorcycles in India from Royal Enfield including Meteor 350."
      }){
        product{
          id
          name
          productType{
            id
            name  
          }
          shop{
            id 
            name
          }
          description
        }
        success
      }
    }



## Update product 

    mutation{
      updateProduct(id:2,input:{
        name:"Mobile"
      }) {
        product{
          id
          name
        }
        success
      }
    }


## Delete Product 
        mutation{
          deleteProduct(id:2){
            success
          }
        }



## Get All Product Image 

    query{
      allProductsImages{
        id
        image
        isDefault
        product{
          id
          name
        }
      }
    }



