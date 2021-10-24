{% extends 'app/base.html' %} {% load static %} {% block title %}Home{% endblock title %} {% block banner_slider %}
<!--Banner Slider-->
<div id="carouselExampleControls" class="carousel slide" data-bs-ride="carousel">
    <div class="carousel-inner">
        <div class="carousel-item active">

            <img src="{% static 'app/images/banner/b1.png' %}" class="d-block w-40 bg-dark bg-gradient" alt="...">
        </div>
        <!--   <div class="carousel-item">
            <img src="{% static 'app/images/banner/b2.jpg' %}" class="d-block w-100" alt="...">
        </div>
        <div class="carousel-item">
            <img src="{% static 'app/images/banner/b3.jpg' %}" class="d-block w-100" alt="...">
        </div>
        <div class="carousel-item">
            <img src="{% static 'app/images/banner/b4.jpg' %}" class="d-block w-100" alt="...">
        </div> -->
    </div>
    <!--  <a class="carousel-control-prev" href="#carouselExampleControls" role="button" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
    </a>
    <a class="carousel-control-next" href="#carouselExampleControls" role="button" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
    </a> -->
</div>
<!-- End Banner Slider -->
{% endblock banner_slider %} {% block livesale %}
<!-- Live Sale Section -->
<div class="container">
    <div class="row bg-danger text-center p-5 text-white border-bottom shadow">
        <h1>SALE IS LIVE NOW</h1>
        <!-- <span>5% Instant Discount on Axis Bank Credit and Debit Card</span> -->
        <small class="fw-lighter">Term and Condition Applied </small>
    </div>
</div>
<!-- End Live Sale Section -->
{% endblock livesale %} {% block main-content %}
<!-- 1st Product Slider -->
<div class="m-3">
    <h2>SHOP24's Bottom Wear</h2>
    <!-- Slider 1 -->
    <div class="owl-carousel" id="slider1">
        {% for b in bottomwears %}
        <a href="{% url 'product-detail' b.id %}" class="btn">
            <div class="item"><img src="{{b.product_image.url}}" alt="" height="300px"><span class="fw-bold">{{b.title}}</span><br><span class="fs-5">Rs. {{b.discounted_price}}</span></div>
        </a>
        {% endfor %}
    </div>
</div>
<!-- End 1st Product Slider -->



<!-- 2nd Product Slider -->
<div class="mx-3">
    <h2>SHOP24's Top Wear</h2>
    <!-- Slider 2 -->
    <div class="owl-carousel" id="slider2">
        {% for tp in topwears %}
        <a href="{% url 'product-detail' tp.id %}" class="btn">
            <div class="item"><img src="{{tp.product_image.url}}" alt="" height="300"><span class="fw-bold">{{tp.title}}</span><br><span class="fs-5">Rs. {{tp.discounted_price}}</span></div>
        </a>
        {% endfor %}
    </div>
</div>
<!-- End 2nd Product Slider -->

<!-- 3rd Product Slider -->
<div class="mx-3">
    <h2>SHOP24's Mobile</h2>
    <!-- Slider 3 -->
    <div class="owl-carousel" id="slider3">
        {% for m in mobiles %}
        <a href="{% url 'product-detail' m.id %}" class="btn">
            <div class="item"><img src="{{m.product_image.url}}" alt="" height="300"><span class="fw-bold">{{m.title}}</span><br><span class="fs-5">Rs. {{m.discounted_price}}</span></div>
        </a>
        {% endfor %}
    </div>
</div>
<!-- End 2nd Product Slider -->
{% endblock main-content %}
