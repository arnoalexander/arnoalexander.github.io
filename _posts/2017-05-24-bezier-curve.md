---
layout: post
title: "Bezier Curve"
post_author: Arno Alexander
date: 2017-05-24
categories: article
---
<p>Dalam aplikasi pengolahan grafis berbasis vektor, salah satu kemampuan dasar yang harus dimiliki adalah membuat kurva. Pembuatan kurva tidak dilakukan secara langsung, melainkan dengan memindahkan titik-titik tertentu yang disebut juga <em>control point</em>, hingga kurva yang diinginkan terbentuk. Kurva dihasilkan dari perhitungan matematis berdasarkan posisi titik-titik yang telah disebutkan sebelumnya. Teknik penggambaran kurva ini disebut <em>Bézier curve</em> karena dipopulerkan oleh seorang matematikawan bernama Pierre Bézier.</p><!--endofpreview-->
<img src="{{ site.url }}/assets/posts/2017-05-24-bezier-curve/quad_benzier.jpg" title="jenis bezier" class="img-responsive" style="display: block; margin-left: auto; margin-right: auto">
<p><em>Bézier curve</em> memiliki atribut berupa derajat yang besarnya sebanding dengan banyaknya <em>control point</em>. Jika sebuah <em>Bézier curve</em> memiliki derajat n, maka banyaknya <em>control point</em> adalah n+1. Derajat tersebut merupakan derajat dari polinomial yang merepresentasikan <em>Bézier curve</em>. Berikut persamaannya:</p>
<img src="https://latex.codecogs.com/gif.latex?r(t)=\sum_{i=0}^{n}\binom{n}{i}(1-t)^{n-i}t^{i}P_{i}" title="polinom bezier" class="img-responsive" style="display: block; margin-left: auto; margin-right: auto"/>
<p>Dalam persamaan tersebut, n menyatakan derajat dan P<sub>i</sub> menyatakan posisi <em>control point</em> ke-i. Kurva yang terbentuk sebenarnya adalah himpunan dari tak hingga titik yang terbentuk oleh r(t) untuk setiap bilangan real t di antara 0 hingga 1. Menurut persamaan tersebut, selama t bergerak dari 0 ke 1, titik yang dihasilkan bergerak mulai dari berhimpit dengan P<sub>0</sub> saat t=0, kemudian bergerak mendekati P<sub>1</sub>, P<sub>2</sub>, P<sub>3</sub>, dan seterusnya hingga akhirnya berhimpit dengan P<sub>n</sub> saat t=n. Gambar di bawah menunjukkan animasi kurva yang terbentuk pada <em>Bézier curve</em> berderajat 3.</p>
<img src="{{ site.url }}/assets/posts/2017-05-24-bezier-curve/bezier3.gif" title="animasi bezier derajat 3" class="img-responsive" style="display: block; margin-left: auto; margin-right: auto"/>