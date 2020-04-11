// ---------------------------------------
// Copyright 2020
// Created and Designed by Rifqi Ardhian
// Authentic Design
// User Interface Mid Test
// ---------------------------------------

<template>
    <div class="home">
        <div>
            <b-carousel id="carousel-1"
                :interval="4000"
                controls
                indicators
                img-width="1024"
                img-height="480"
            >
                <b-carousel-slide v-for="(data, index) in slider" :key="index">
                    <template v-slot:img>
                    <img
                        class="d-block img-fluid w-100 img-banner"
                        :src="require(`../assets/images/${data.foto}`)"
                        alt="image slot"
                    >
                    </template>
                    <h4 class="title">{{data.title}}</h4>
                    <p class="subtitle">{{data.subtitle}}</p>
                </b-carousel-slide>
            </b-carousel>
        </div>
        <section class="product text-center">
            <div class="container-fluid">
                <div class="row mt-5">
                    <div class="col-md-12 text-center">
                        <h4><b>Our Products</b></h4>
                        <p>
                            With over 10 luxury brands around the world.
                            More luxurious and guaranted</p>
                    </div>
                </div>
            </div>
            <b-tabs
                align="center"
                no-key-nav
                class="mt-3"
                no-nav-style
                small
                active-nav-item-class="category-item-active text-secondary font-weight-bold"
                >
                <b-tab>
                    <template v-slot:title>
                        <div class="category-item">All</div>
                    </template>
                    <div class="container-fluid container-product">
                        <div class="row row-product">
                            <div class="col-md-3" v-for="(data, index) in products" :key="index">
                                <div class="product-item">
                                    <div class="product-img text-center">
                                        <img
                                            :src="require(`../assets/images/${data.foto}`)"
                                            class="img-product"
                                        >
                                    </div>
                                    <div class="product-detail text-center">
                                        <h5><b>{{data.merk}}</b></h5>
                                        <h6>{{data.harga}}</h6>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </b-tab>
                <b-tab>
                    <template v-slot:title>
                        <div class="category-item">Men Watch</div>
                    </template>
                    <div class="container-fluid container-product">
                        <div class="row row-product">
                            <div class="col-md-3" v-for="(data, index) in menwatch" :key="index">
                                <div class="product-item">
                                    <div class="product-img text-center">
                                        <img
                                            :src="require(`../assets/images/${data.foto}`)"
                                            class="img-product"
                                        >
                                    </div>
                                    <div class="product-detail text-center">
                                        <h5><b>{{data.merk}}</b></h5>
                                        <h6>{{data.harga}}</h6>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </b-tab>
                <b-tab>
                    <template v-slot:title>
                        <div class="category-item">Women Watch</div>
                    </template>
                    <div class="container-fluid container-product">
                        <div class="row row-product">
                            <div class="col-md-3" v-for="(data, index) in womenwatch" :key="index">
                                <div class="product-item">
                                    <div class="product-img text-center">
                                        <img
                                            :src="require(`../assets/images/${data.foto}`)"
                                            class="img-product"
                                        >
                                    </div>
                                    <div class="product-detail text-center">
                                        <h5><b>{{data.merk}}</b></h5>
                                        <h6>{{data.harga}}</h6>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </b-tab>
            </b-tabs>
            <div class="container-fluid">
                <div class="row text-center">
                    <div class="col-md-12 text-center">
                        <button type="button" class="btn btn-load-more mb-5">LOAD MORE</button>
                    </div>
                </div>
            </div>
        </section>
        <section class="newsletter">
            <div class="container-fluid">
                <div class="row m-5">
                    <div class="col-md-12 text-center">
                        <h4><b>Newsletter</b></h4>
                        <p>Get the weekly promotions after you subscribe below</p>
                        <div class="input-group mb-3">
                            <input
                                type="text"
                                class="form-control input-subscribe"
                                placeholder="Enter your email address"
                                aria-label="email address"
                                aria-describedby="button-subscribe"
                            >
                            <div class="input-group-append">
                                <button
                                    class="btn btn-outline-secondary btn-subscribe"
                                    type="button"
                                    id="button-subscribe">
                                    <b>Subscribe</b>
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <section id="contact">
            <footer class="footer-contact">
                <div class="row row-contact">
                    <div class="col-md-4">
                    <img src="../assets/images/logojam.png" class="logo-footer img-fluid">
                        <br/>
                        <p class="link-footer">House of Time Indonesia</p>
                    </div>
                    <div class="col-md-4">
                        <p class="link-footer"><b>Quick Links</b></p>
                        <div class="row">
                            <div class="col-6">
                                <a href="/" class="link-footer"><p>Home</p></a>
                                <a href="#services" class="link-footer"><p>Men Watch</p></a>
                            </div>
                            <div class="col-6">
                                <a href="#about" class="link-footer"><p>About</p></a>
                                <a href="#education" class="link-footer"><p>Women Watch</p></a>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <p class="link-footer"><b>Contact Us</b></p>
                        <span><i class="fab fa-whatsapp link-footer pr-2"></i></span>
                        <span><i class="fab fa-instagram link-footer p-2"></i></span>
                        <span><i class="fab fa-twitter link-footer p-2"></i></span>
                        <span><i class="fas fa-envelope link-footer pl-2"></i></span>
                    </div>
                </div>
                <br/><br/>
                <p class="text-center link-footer">
                    Copyright &copy;2020 House of Time Indonesia. All Rights Reserved
                    <br/>
                    Created by Rifqi Ardhian
                </p>
            </footer>
        </section>
    </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      slider: [],
      products: [],
      menwatch: [],
      womenwatch: [],
      slide: 0,
    };
  },
  async created() {
    const BASEURI = 'https://my-json-server.typicode.com/rifqiiardhian/dbuts/db';
    axios.get(BASEURI).then((result) => {
      this.slider = result.data.slider;
      this.products = result.data.products;
      this.menwatch = result.data.menwatch;
      this.womenwatch = result.data.womenwatch;
    });
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import '../css/style.css';
</style>
