# Assignment: Server admin

## Campaign

We’re organising a campaign starting on LINE Hot Deal. LINE will display our banner for their 30 mil. users within 30 seconds. We can expect around 1 mil. users to click on our banner within 1 minute. 

On our site, users will be able to buy a voucher with a big discount. We’ll offer 90% discount to the first 1000 buyers. 70% discount to next 9000 buyers. And 50% discount for the rest of the buyers - maximum 20.000 vouchers. After all these vouchers are sold, we’ll display a message “Sold out.” 

Users will be able to buy these vouchers using our application written in PHP which we need to write specially for this purpose from scratch.

We assume one payment gateway can process only ~100 transactions per second. We can use 3 of them, but one has significantly better conditions than the other two.

LINE will not show our banner 2nd time, thus we have unique opportunity to serve hundreds of thousands of visitors. If our servers crash, we’re doomed. Cannot afford it.

## Application

A user needs to be able to buy a voucher, thus there’ll be a simple page with a checkout form (credit card details). Some other pages will be static (i.e. terms & conditions).

The application will be written in PHP, reading & saving data to MySQL. Payment gateway is also written in PHP and communicates with 3rd parties (i.e. PayPal).

Voucher codes are unique and are pre-generated in advance. We’ll need to store customer’s data in database (info about the purchase, transaction history, payment info).

It can use synchronous or asynchronous connection, it can possibly use NoSQL database, cache, … it’s up to you to pick the right components.

## Request

You need to use AWS for all services (unless they don’t support a feature you need).

 1. Prepare server architecture for this campaign
  * Design a chart showing components of the infrastructure
  * Describe why did you chose each component
 2. Make sure the architecture is bullet-proof - it cannot crash
  * How would you test it? Prepare plan for load testing of the whole system and each component.
  * How would you make sure the system will be available even if one of the Amazon’s data centre goes down? (i.e. electricity is off)
  * How would you set up monitoring of the system?
  * What and how would you monitor to ensure it’s all OK?

## Output
Prepare output in whatever form you prefer and submit back to us.
