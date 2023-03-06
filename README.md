
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



## Home page logo and video :

	query{
	  homePageContent{
	    id
	    siteLogo
	    siteVideo
	  }

	  }


## How Go Velo Works > Content 

	query{
	  workFlow{
	    id
	    title
	    description
	    icon
	  }
	}



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
		openingTime
		closingTime
		createdAt
		owner {
		  id
		  name
		  email
		}

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
	    userId:4
	    street: "Dhaka"
	    city: "Dhaka City"
	    state: "Dhaka Uttara"
	    zipCode :"1230"
	    areaCode: "1230"
	    country: "Canada"
	    latitude:"45.454214"
	    longitude: "82.544565"
	    phone: "+85452825"
	    website: "www.web.com"
	    email: "shopmail@gmail.com"
	    description: "shop description"
	    shopImage:Upload
	    shopCover:Upload
	    openingTime:Time
	    closingTime:Time

	    pickupLocations:[
	    {country:"Bangladesh", city:"Dhaka", state:"Uttara", street:"Uttara",zipCode:"4521", areaCode:"6243",
	    latitude:"42.545545", longitude: "86.545223"},
	    {country:"Bangladesh", city:"CTG", state:"Pahartali", street:"Ferozshah",zipCode:"4521", areaCode:"6243",
	    latitude:"49.545545", longitude: "86.545223"}
	    ]

	  })

	  {
	    success
	  }

	}



## Update Shop 

    
        mutation{
	  updateShop(input:{
	    id:6
	    name:"New Shop"
	    legalEntity:"Shop Legal Entity"
	    street: "Dhaka"
	    city: "Dhaka City"
	    state: "Dhaka Uttara"
	    zipCode :"1230"
	    areaCode: "1230"
	    country: "Canada"
	    latitude:"45.454214"
	    longitude: "82.544565"
	    phone: "+85452825"
	    website: "www.web.com"
	    email: "shopmail@gmail.com"
	    description: "shop description"
	    shopImage:Upload
	    shopCover:Upload
	    openingTime:Time
	    closingTime:Time
	    pickupLocations:[
	    {id:24,country:"Bangladesh", city:"Dhaka", state:"Uttara", street:"Uttara",zipCode:"4521", areaCode:"6243",
	    latitude:"42.545545", longitude: "86.545223"},
	    {id:25,country:"Bangladesh", city:"CTG", state:"Pahartali", street:"Ferozshah",zipCode:"4521", areaCode:"6243",
	    latitude:"49.545545", longitude: "86.545223"}
	    ]

	  })

	  {
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
	  shops(ownerId: "1") {
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
		shopCover
		openingTime
		closingTime
		rating
		totalReviews
		createdAt
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
		      image
		      
			size{
			      id
			      productSize
			    }
		      productrateSet{
			id
			rate
			rateType{
			  id
			  name
			}
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


## create Shop Verification 

	mutation{
	  createShopVerification(input:{
	    shopId:2
	    ownerImage: Upload
	    idFrontImage: Upload
	    idBackImage: Upload

	  }){
	    success
	    shopVerification{
	      id
	      shop{
		id
		isVerified
	      }
	      status
	      ownerImage
	      idFrontImage
	      idBackImage
	    }
	  } 
	}


## Update Shop Verification

	mutation{
	  updateShopVerification(input:{
	    id:3
	    ownerImage: Upload
	    idFrontImage: Upload
	    idBackImage: Upload
	  })
	  {
	    success

	    shopVerification{
	    id
	    shop{
	      id
	      name
	    }
	    status
	    idFrontImage
	    status
	    idBackImage

	  }
	  }
	}






# ``# Product Module ``
## Get All Product 

	query{
	  products {
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
		stock
		size{
		  id
		  productSize
		}
		condition
		createdAt
		productrateSet {
		  id
		  rate
		}
		 image
		productoptionSet {
		  id
		  option
		}

		productreviewSet {
		  id
		  review
		  rating
		  user {
		    id
		    username
		    userImage
		  }
		}
	      }
	    }
	  }
	}



## Create Product Mutation

	mutation{
	  createProduct(input:{
	    brand:"product brand100"
	    model:"pdoruct model20"
	    productType:1
	    shop:2
	    description:"shop details"
	    stock:500
	    size:1
	    condition:"product conditation"
	    image: Upload
	    prices:[{rateType:1, rate:100,},{rateType:1, rate:100,}]

	  })
	  {
	    success
	    product{
	      id
	      brand
	      model
	      size{
		id
		productSize
	      }
	      productType{
		id
		name
	      }
	      shop{
		id
	      }
	      description
	      stock
	      productrateSet{
		id
		product{
		  id
		}
		rateType{
		  id
		}
		rate
	      }
	      condition
	    }
	  }
	}




## Update product 

	 mutation{
	  updateProduct(id:24,input:{
	    brand:"productupdated"
	    model:"pdoruct model20"
	    productType:1
	    description:"shop details"
	    stock:500
	    size:2
	    condition:"product conditation"
	    prices:[{rateType:2, rate:40,},{rateType:4, rate:800,}]
	    image:Upload
	  })
	  {
	    success
	    product{
	      id
	      brand
	      model
	      description
	      stock
	      condition
	      size{
		id
		productSize
	      }
	      productType{
		id
		name
	      }
	      shop{
		id
	      }

	      productrateSet{
		id
		product{
		  id
		}
		rateType{
		  id
		}
		rate
	      }
	      image

	    }
	  }
	}
  


## Delete Product 
        mutation{
          deleteProduct(id:2){
            success
          }
        }



## Get Products By Price Range

	query{
	  getProductsByPriceRange(min: 50, max: 100) {
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
	 
	    image
	    size{
	      id
	      productSize
	    }
	    productrateSet {
	      id
	      rate
	      rateType {
		id
		name
	      }
	    }
	    rating
	    totalReviews
	    stock
	    description
	    isAvailable
	    createdAt
	  }
	}




## Product search and filter query: 

	query{
	  products(
		  model: ""
		  brand: ""
		  shopLocation: ""
		  productTypeId: "1"
		  productRateTypeId:"1"
		  date : "2023-03-20"
		  riders: 5
	  ) {
	    edges {
	      node {
		id
		model
		brand
		shop {
		  id
		  name
		  state
		  street

		}
		productType {
		  id
		  name
		}
		size{
		      id
		      productSize
		    }
		
		productrateSet {
		  id
		  rate
		  rateType {
		    id
		    name
		  }
		}
		image
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


  

## Get all product review


	query{
	  productReviews{
	    id
	    product{
	      id
	      brand
	      model
	      image
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
	      image
	     
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
	      image
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


## get cart by user id 

	query{
	  carts(userId:"1"){
	    edges{
	      node{
		id
		cartitemSet{
		  edges{
		    node{
		      id
		      quantity
		      price
		      product{
			id
			model
			brand
			stock
		      }
		    }
		  }
		}
	      }
	    }
	  }
	}



## Order module:


#### Recent bike hires

	query{
	  latestOrder{
	    id
	    quantity
	    price
	    product{
	       id
		model
		brand
		shop {
		  id
		  name
		  state
		  street

		}
		productType {
		  id
		  name
		}
		image
		size{
		      id
		      productSize
		    }
		productrateSet {
		  id
		  rate
		  rateType {
		    id
		    name
		  }
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



### Order by user id 

	
	query{
	  orderByUserId(userId:4){
	    id
	    user{
	      id
	      username

	    }
	    paymentMethod
	    status
	    isPaid
	    isDelivered
	    totalPrice
	    paidAt
	    deliveredAt
	    returnedAt


	    orderitemSet{
	      product{
	       id
		model
		brand
		shop {
		  id
		  name
		  state
		  street

		}
		productType {
		  id
		  name
		}
		image
		size{
	    productSize
	  }
		productrateSet {
		  id
		  rate
		  rateType {
		    id
		    name
		  }
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


## Update Order

	mutation{
	  updateOrder(id:14, input:{
	    paymentMethod:"bank"
	    isCancelled: false
	    refundRequested: true


	  }){
	    order{
	      id

	      paymentMethod
	      status
	      orderitemSet{

		id
		product{
		  id
		  shop{
		    id
		    owner{
		      id
		    }
		  }
		}
		quantity
	      }
	    }
	  }
	}


## Order Item by Order ID 

	query{
	  orderItemByOrderId(orderId: 15) {
	    id
	    price
	    quantity
	    order {
	      id
	    }
	    product {
	      id
	      model
	      brand
	      shop {
		id
		name
		state
		street
	      }
	      productType {
		id
		name
	      }
	      image
	      size {
		productSize
	      }
	      productrateSet {
		id
		rate
		rateType {
		  id
		  name
		}
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

## Order Refunds 

	query{
	  refunds{
	    id
	    order{
	      id
	      status
	      orderitemSet{
		id
		product{
		  id
		  brand
		  productType{
		    id
		  }
		}
	      }
	    }
	    reason
	    status
	    createdAt

	  }
	}


## Create refund request 

	mutation{
	  createRefund(input:{
	    orderId:15
	    reason:"refund request"

	  })
	  {
	    success
	    refund{
	      id

	      reason
	      status
	    }
	  }
	}


## Delete refund 

	mutation{
	  deleteRefund(id:3){
	    success
	  }
	}



## Refund by oser id 


	query{
	  refundByUserId(userId:1){
	    id
	    order{
	      id
	      user{
		id
	      }
	      status
	      orderitemSet{
		id
		product{
		  id
		  brand
		  productType{
		    id
		  }
		}
	      }
	    }
	    reason
	    status
	    createdAt

	  }
	}









