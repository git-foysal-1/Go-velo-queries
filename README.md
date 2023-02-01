
# ``#Users Module``

#### `Authentication:`

## Registration


	http://localhost:8000/auth/registration/

## Login 

	http://localhost:8000/auth/login/


## Change Password : 

	http://localhost:8000/auth/password/change/

## Password Reset

	http://localhost:8000/auth/password/reset/
	
## Password reset confirm 

	http://localhost:8000/auth/password/reset/confirm/

## User Details

	http://localhost:8000/auth/user/


## Logout 

	http://localhost:8000/auth/logout/



## Verify Token  

	mutation{
	  verifyToken(token: "Your_Token")
	  {
	    payload

	  }
	}



# `graphql API`

url:  

    http://localhost:8000/graphql



# ``#Core Module``

## Get About Us 

    query{
      aboutUs{
        id
        title
        content
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
        content
        createdAt
        updatedAt
        
      }
    }


## Get TermsAndConditions

    query{
      termsAndConditions{
        id
        title
        content
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
     languages{
        id
        name
        code
      }
      currencies{
        id
        name
        code
      }
    }

## Get All Nomination Types

    query{
      nominationTypes{
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
        name: "update Nomination Types"
        })
        {
        success
      }
    }

## Delete Nomination Types

    mutation{
      deleteNominationType(id:1){
        success
      }
    }



## Get All Nominations
   
	query{
	  nominations{
	    id
	    name
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
	    name:"new nomination"
	    nominationType:1
	    reason:"shop related"
	  })
	  {
	    nomination{
	      id
	      name
	      reason
	      nominationType{
		id
		name
	      }
	    }
	    success
	  }
	}


## Update Nomination

	mutation{
	  updateNomination(id:1, input:{
	    name:"update nomination"
	    nominationType:1
	    reason:"buy bike"
	  })
	  {
	    nomination{
	      id
	      name    
	    }
	    success
	  }
	}

      
## Delete Nomination
      mutation{
        deleteNomination(id:1){
          success
        }
      }

    
## Get All Address Type

      query{
      addressTypes{
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
	  

## Update Address Type 

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
      productTypes{
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
      productRateTypes{
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
      contactTypes{
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


## Delete Contact Type
    mutation{
      deleteContactType(id:3){
        success
      }
    }


## Get All Contacts

	query{
	  contacts{
	    id
	    name
	    rentalBooking
	    email
	    contactType{
	      id
	      name
	    }
	  }
	}

## Create Contact

	mutation{
	  createContact(input:{
	    name:"new contact"
	    email: "email@gmail.com"
	    contactType:1
	    rentalBooking:"shop1"
	  })
	  {
	    success
	    contact{
	      id
	      name
	      email
	    }
	  }
	}


## Update Contact

	mutation{
	  updateContact(id:1,input:{
	    name:"Majedul Islam"
	    email:"ex@gmail.com"
	    rentalBooking:"shop101"
	    contactType:1
	  }){
	    success
	    contact{
	      id
	      name
	      email
	      rentalBooking
	      contactType{
		name
	      }
	    }
	  }
	}
	

## Delete Contact

    
	mutation{
	  deleteContact(id:1)
	  {
	    success
	  }
	}


# ``# Shop Module``

## Get All Shops 

    query{
	  shops{
	    edges {
	      node {
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
		shopCover
		owner {
		  id
		  name
		  email
		}
		createdAt
		productSet {
		  edges {
		    node {
		      id
		      model
		      brand
		      shop {
			id
			name
		      }
		      productType {
			id
			name
		      }
		      rating
		      totalReviews
		      stock
		      description
		      isAvailable
		      createdAt
		    }
		  }
		}
	      }
	    }
	  }
	}


## Create New Shop 

 
	
        mutation{
	  createShop(input:{
	    name:"New Shop"
      	    legalEntity:"Shop Legal Entity"
	    street: "Dhaka"
	    city: "Dhaka City"
	    state: "Dhaka Uttara"
	    zipCode :"1230"
	    areaCode: "1230"
	    country: "Canada"
	    phone: "+85452825"
	    website: "www.web.com"
	    email: "shopmail@gmail.com"
	    description: "shop description"
	    shopImage:uploadImage
	    openingTime: time
	    closingTime: time  

	  })
	  {
	    shop{
	     id
	     name
        owner{
          id
          username
        }
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
    
    
## Get shop by owner/user id

	query{
	  shops(ownerId:"3"){
	    edges {
	      node {
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
		owner {
		  id
		  name
		  email
		}
		createdAt
		productSet {
		  edges {
		    node {
		      id
		      model
		      brand
		      shop {
			id
			name
		      }
		      productType {
			id
			name
		      }
		      rating
		      totalReviews
		      stock
		      description
		      isAvailable
		      createdAt
		    }
		  }
		}
	      }
	    }
	  }
	}




# ``# Product Module ``
## Get All Product 

	query{
	  products{
	    edges{
	     node{
	      id
	      model
	      brand
	      shop{
		id
		name
	      }
	      productType{
		id
		name
	      }
	      rating
	      totalReviews
	      stock
	      description
	      isAvailable
	      createdAt
	      productrateSet{
		id
		rate
	      }
	      productimageSet{
		id 
		image
		isDefault
	      }
	      productstockSet{
		id
		stock
	      }
	      productsizeSet{
		id
		size
	      }
	      productoptionSet{
		id
		option
	      }
	      productconditionSet{
		id
		condition
	      }
	      productreviewSet{
		id
		review
		rating
		user{
		  id
		  username
		  userImage

		}

	      }

	      }

	    }
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
      productsImages{
        id
        image
        isDefault
        product{
          id
          name
        }
      }
    }
    
    

## Get all product review


	query{
	  productReviews{
	    id
	    product{
	      id
	      brand
	      model
	    }
	    review
	    rating
	    user{
	      id
	      username
	      userImage
	    }

	  }
	}


## Product review by product id 

	query{
	  getProductReviewsByProductId(id:1){
	    id
	    review
	    rating
	    user{
	      id
	      username
	      userImage
	    }
	    product{
	      id
	      brand
	      model
	      productimageSet{
		id
		image
		isDefault
	      }  
	    }
	  }
	}



## Get product review by shop id 

	query{
	  getProductReviewsByShopId(id: 1) {
	    review
	    rating
	    product {
	      id
	      brand
	      model
	      productimageSet {
		id
		image
		isDefault
	      }
	      }
	    }
	  }


## Create product review 


	mutation{
	  createProductReview(input:{
	    user:1
	    product:1
	    review:"good product"
	    rating:5
	  })
	  {
	    success
	    productReview{
	      id
	      product{
		id
		model
		brand
		createdAt
		rating
	      }

	    }
	    productReview{
	      id
	      rating
	      review

	    }
	  }
	}



## Update product review 

	mutation{
	  updateProductReview(id:37,input:{
	    user:1
	    product:1
	    review:"good"
	    rating:5
	  })
	  {
	    success
	    productReview{
	      id
	      product{
		  id
		  model
		  brand
		  createdAt
		  rating
	      }

	    }
	    productReview{
		  id
		  rating
		  review
		  user{
		    id
		    username
		  }
	    }
	  }
	}

## Delete product review 

	mutation{
	  deleteProductReview(id:1){
	    success
	  }
	}




# `#Product Demurrage`

## Get all Product demurrages:

	query{
	  productDemurrages{
	    id
	    product{
	      id
	      model
	    }
	    description
	    image
	    createdAt

	  }
	}


## Get Product demurrages by product id :


	query{
	  getProductDemurragesByProductId(id:1){
	    id
	    description
		image
	    product{
	      id
	      model
	      shop{
		id
		name
	      }
	    }

	  }
	}



## Create product damage:

	mutation{
	  createProductDamage(input:{
	    product:1
	    description:"damage product"
	    user:2

	  }){
	    productDamage{
	      id
	      description
	      product{
		id
		brand
	      }
	    }

	    success

	  }
	}


## Update product damage:


	mutation{
	  updateProductDamage(id:2,input:{
		product:1
	    description:"Update damage example"
	    user:2
	  }){
	    productDamage{
	      id
	      description
	      product{
		id
		brand
	      }
	    }
	    success
	  }
	}
	
	
## Delete product damage:

	mutation{
	  deleteProductDamage(id:1){
	    success
	  }
	}




# `#Cart Module`



## Add to cart 



	mutation {
	  addToCart(userId: 2, productId: 1, quantity: 10){
	    cart {
	      id
	      user {
		id
		username
	      }
	      cartitemSet {
		edges {
		  node {
		    id
		    price
		    quantity
		    product {
		      id
		      brand
		    }
		  }
		}
	      }
	    }
	  }
	}




## Remove cart Item 

	mutation {
	  removeFromCart(userId: 2, productId: 1, quantity: 1) {
	    cart {
	      id
	      user {
		id
		username
	      }
	      cartitemSet {
		edges {
		  node {
		    id
		    price
		    quantity
		    product {
		      id
		      brand
		    }
		  }
		}
	      }
	    }
	  }
	}



## Get all cart items


	query{
	  cartItems{
	    edges{
	      node
	      {
		id
		cart{
		  id
		  user{
		    id
		    username
		  }

		}
		price
		product{
		  id
		  brand
		}
		quantity
	      }
	    }
	  }
	}


## get cart items by cart id 

	query{
	  cartItems(cartId:2){
	    edges{
	      node
	      {
		id
		price
		product{
		  id
		  brand
		}
		quantity
	      }
	    }
	  }
	}






