

<h5><span style="color:#000000"><strong>Models</strong></span><br>
<br>
<span style="color:#000000"><a href="https://stepswithcode.s3.us-west-2.amazonaws.com/introduction/models.png" target="_blank"><img src="https://stepswithcode.s3.us-west-2.amazonaws.com/introduction/models.png" style="height:426px; width:591px"></a></span></h5>

<p><span style="color:#000000">This project will consist of 6 Models, so let's summarize each one:</span></p>

<p><span style="color:#000000">1. <strong>USER </strong>- Built in Django user model,&nbsp; instance created for each customer who registers.</span></p>

<p><span style="color:#000000">2. <strong>CUSTOMER </strong>- Along with a User model, each customer will contain a Customer model that holds a one to one relationship to each user. (OneToOneFied)</span></p>

<p><span style="color:#000000">3. <strong>PRODUCT </strong>- The product model represents product types&nbsp;we have in store.</span></p>

<p><span style="color:#000000">4. <strong>ORDER </strong>- The order model will represent a transaction that is placed or pending. The model will hold information such as the transaction ID, data completed and order status. This model will be a child or the customer model but a parent to Order Items.</span></p>

<p><span style="color:#000000">5. <strong>ORDERITEM</strong> - An order Item is one item with an order. For example, a shopping cart may consist of many items but is all part of one order. Therfore the OrderItem model will be a child of the PRODUCT model AND the ORDER Model.</span></p>

