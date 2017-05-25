---
layout: post
title: "Bezier Curve"
post_author: Arno Alexander
date: 2017-05-24
categories: article
---
<p>Dalam aplikasi pengolahan grafis berbasis vektor, salah satu kemampuan dasar yang harus dimiliki adalah membuat kurva. Pembuatan kurva tidak dilakukan secara langsung, melainkan dengan memindahkan titik-titik tertentu yang disebut juga <em>control point</em>, hingga kurva yang diinginkan terbentuk. Kurva dihasilkan dari perhitungan matematis berdasarkan posisi titik-titik yang telah disebutkan sebelumnya. Teknik penggambaran kurva ini disebut <em>Bézier curve</em> karena dipopulerkan oleh seorang matematikawan bernama Pierre Bézier.</p><!--endofpreview-->
<img src="{{ site.url }}/assets/posts/2017-05-24-bezier-curve/quad_benzier.jpg" alt="bezier-types" class="img-responsive" style="display: block; margin-left: auto; margin-right: auto">
<p><em>Bézier curve</em> memiliki atribut berupa derajat yang besarnya ditentukan oleh banyaknya <em>control point</em>. Jika sebuah <em>Bézier curve</em> memiliki n <em>control point</em>, maka derajatnya adalah n-1. </p>