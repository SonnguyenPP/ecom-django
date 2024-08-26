<div class="col-lg-12">
                <br>
                <div style="background-color: " class="module-title">
                <h3>Project Overview</h3>
            </div>
                <div style="border:1px solid " class="module-desctription">
                

                <br>
                <p><strong>Source code by module:</strong></p>

<p><a href="https://github.com/divanov11/ecommerce_django_mod1" target="_blank">Module #1</a> | <a href="https://github.com/divanov11/ecommerce_django_mod2" target="_blank">Module #2</a> | <a href="https://github.com/divanov11/ecommerce_django_mod3" target="_blank">Module #3</a>&nbsp;| <a href="https://github.com/divanov11/ecommerce_django_mod4" target="_blank">Module #4</a>&nbsp;| <a href="https://github.com/divanov11/django_ecommerce_mod5/" target="_blank">Module #5</a></p>

<p>This project will be a fully functional eCommerece website with user and guest checkout capabilities. We will start first by setting up our templates and data structure in the first two modules, then moving on to adding user checkout flow with payment integration.</p>

<p>After we complete basic checkout with a logged in user, we will add in the ability for users to checkout as a guest using cookies.</p>

<h3><span style="color:#000000"><strong>What We Are Building</strong></span></h3>

<p><span style="color:#000000"><strong><a href="https://stepswithcode.s3-us-west-2.amazonaws.com/introduction/1+the+product.png" target="_blank"><img src="https://stepswithcode.s3-us-west-2.amazonaws.com/introduction/1+the+product.png" style="height:376px; width:700px"></a></strong></span></p>

<p><span style="color:#000000">This product will be a fully functioning eCommerce website from start to checkout functionality. Users will have the ability to add multiple products to cart, varying from physical to digital products.</span></p>

<p>&nbsp;</p>

<h5><span style="color:#000000"><strong>Payment Integration</strong></span></h5>

<p><span style="color:#000000"><a href="https://stepswithcode.s3-us-west-2.amazonaws.com/introduction/2+payment+page.png" target="_blank"><img src="https://stepswithcode.s3-us-west-2.amazonaws.com/introduction/2+payment+page.png" style="height:295px; width:600px"></a></span></p>

<p><span style="color:#000000">Payment integration will be handled with PayPal offering the ability to checkout with a PayPal account and checkout with PayPal debit/credit card. Stripe integration is simple to add but for the purpose of international transactions we will focus on PayPal for international availability and security.</span></p>

<p><span style="color:#000000"><a href="https://stepswithcode.s3-us-west-2.amazonaws.com/introduction/3+checkout+page.png" target="_blank"><img src="https://stepswithcode.s3-us-west-2.amazonaws.com/introduction/3+checkout+page.png" style="height:270px; width:600px"></a></span></p>

<p>&nbsp;</p>

<hr>
<h3><span style="color:#000000"><strong>User/Guest Checkout</strong></span></h3>

<p><span style="color:#000000">The main focus of this eCommerce project will be to integrate guest checkout ability along with user accounts. Many eCommerce tutorials/demo’s have one or the other but I could not find any at this time that contain both.</span></p>

<p><span style="color:#000000">As I posted on twitter in April 2020 “</span><span style="color:#000000"><em>A good eCommerce website should always give the user the ability to checkout without creating an account.</em></span><span style="color:#000000">“&nbsp;</span></p>

<p><span style="color:#000000"><a href="https://stepswithcode.s3-us-west-2.amazonaws.com/introduction/4+twitter+post.png" target="_blank"><img src="https://stepswithcode.s3-us-west-2.amazonaws.com/introduction/4+twitter+post.png" style="height:114px; width:710px"></a></span></p>

<p><span style="color:#000000">This kind of functionality has come to be expected by users and forcing them&nbsp;to create an account can affect sales significantly as any resistance does.</span></p>

<h5><span style="color:#000000"><strong>Authenticated User Vs Guest Checkout</strong></span></h5>

<p><span style="color:#000000">Authenticated users &amp; guests&nbsp;have virtually the same process with slight differences. Users with accounts will have the ability to view pending and previous orders while guests will have items stored in cookies and will have the option to create account after a successful purchase.</span></p>

<p><span style="color:#000000"><u>Authenticated User Process</u></span></p>

<ol>
	<li style="list-style-type:decimal"><span style="color:#000000">Add item to cart → Edit Order → Checkout</span></li>
	<li style="list-style-type:decimal"><span style="color:#000000">View pending and previous orders + Order details&nbsp;</span></li>
</ol>

<p><span style="color:#000000"><u>Guest Checkout Process</u></span></p>

<ol>
	<li style="list-style-type:decimal"><span style="color:#000000">Add item to cart → Edit Order → Checkout</span></li>
	<li style="list-style-type:decimal"><span style="color:#000000">Create Account to view Order</span></li>
</ol>

<hr>
<p>&nbsp;</p>

<h3><strong><span style="color:#000000">Project Structure</span></strong></h3>

<p><span style="color:#000000">Before we start building,&nbsp;let's go over the core structure of this project. I’ll first go over templates and what each one will handle and then we’ll cover our models and page functionality.</span></p>

<h3>&nbsp;</h3>

<h5><span style="color:#000000"><strong>Templates</strong></span></h5>

<p><span style="color:#000000">This project will focus on 3 main templates, store.html, cart.html and checkout.html.&nbsp;</span></p>

<p><span style="color:#000000"><a href="https://stepswithcode.s3-us-west-2.amazonaws.com/introduction/5%2Btemplate%2Bdiagram.png" target="_blank"><img src="https://stepswithcode.s3-us-west-2.amazonaws.com/introduction/5%2Btemplate%2Bdiagram.png" style="height:265px; width:763px"></a></span></p>

<p>&nbsp;</p>

<div>
<table cellspacing="0" style="border-collapse:collapse; border:none; table-layout:fixed; width:624px">
	<tbody>
		<tr>
			<td>
			<p><span style="color:#000000"><strong>Store.html</strong></span><span style="color:#000000"><strong><a href="https://stepswithcode.s3-us-west-2.amazonaws.com/introduction/6+strore.png" target="_blank"><img src="https://stepswithcode.s3-us-west-2.amazonaws.com/introduction/6+strore.png" style="height:187px; width:267px"></a></strong></span></p>
			</td>
			<td>
			<p><strong><span style="color:#000000">Cart.html</span></strong></p>

			<p><span style="color:#000000"><a href="https://stepswithcode.s3-us-west-2.amazonaws.com/introduction/7+cart.png" target="_blank"><img src="https://stepswithcode.s3-us-west-2.amazonaws.com/introduction/7+cart.png" style="height:157px; width:300px"></a></span></p>
			</td>
		</tr>
		<tr>
			<td>
			<p><span style="color:#000000"><strong>Checkout.html</strong></span></p>

			<p><span style="color:#000000"><strong><a href="https://stepswithcode.s3-us-west-2.amazonaws.com/introduction/8+checkout.png" target="_blank"><img src="https://stepswithcode.s3-us-west-2.amazonaws.com/introduction/8+checkout.png" style="height:208px; width:400px"></a></strong></span></p>
			</td>
			<td>&nbsp;</td>
		</tr>
	</tbody>
</table>
</div>

<h3>&nbsp;</h3>

<h5><span style="color:#000000"><strong>Models</strong></span><br>
<br>
<span style="color:#000000"><a href="https://stepswithcode.s3.us-west-2.amazonaws.com/introduction/models.png" target="_blank"><img src="https://stepswithcode.s3.us-west-2.amazonaws.com/introduction/models.png" style="height:426px; width:591px"></a></span></h5>

<p><span style="color:#000000">This project will consist of 6 Models, so let's summarize each one:</span></p>

<p><span style="color:#000000">1. <strong>USER </strong>- Built in Django user model,&nbsp; instance created for each customer who registers.</span></p>

<p><span style="color:#000000">2. <strong>CUSTOMER </strong>- Along with a User model, each customer will contain a Customer model that holds a one to one relationship to each user. (OneToOneFied)</span></p>

<p><span style="color:#000000">3. <strong>PRODUCT </strong>- The product model represents product types&nbsp;we have in store.</span></p>

<p><span style="color:#000000">4. <strong>ORDER </strong>- The order model will represent a transaction that is placed or pending. The model will hold information such as the transaction ID, data completed and order status. This model will be a child or the customer model but a parent to Order Items.</span></p>

<p><span style="color:#000000">5. <strong>ORDERITEM</strong> - An order Item is one item with an order. For example, a shopping cart may consist of many items but is all part of one order. Therfore the OrderItem model will be a child of the PRODUCT model AND the ORDER Model.</span></p>

<p><span style="color:#000000">6. <strong>SHIPPING </strong>- Not every order will need shipping information. For orders containing physical products that need to be shipping we will need to create an instance of the shipping model to know where to send the order. Shipping will simply be a child of the order model when necessary.</span></p>

<p>&nbsp;</p>
                </div>

            </div>
