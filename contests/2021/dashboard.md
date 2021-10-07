---
layout: contests/2021/base_decorated
title: Dashboard
edition: "2021"
---

<hr>
<!-- Content Boxes -->
<div class="card shadow mb-4">
  <div class="card-body">
    {% include index_boxes.html %}
  </div>
</div>

<hr>

<div class="row">
  <div class="col-12 mb-2">
    <h3 class="text-gray-800">Challenges</h3>
  </div>
</div>

<div class="row">
  <div class="col-12 mb-4">

    {% if programs %}
    <div class="card shadow mb-2">
      <div class="card-header py-3">
        <h4 id="challenges" class="m-0 font-weight-bold text-primary">Challenges ranking by strawberry scores</h4>
      </div>
      <div class="card-body">
        {% include 'table_challenges.html' %}
      </div>
    </div>
    {% else %}
    <p class="lead">
      There aren't any challenges submitted yet.
      Be the first to submit one by clicking on the <mark>Submit a Challenge</mark> link in the menu bar.
    </p>
    <div class="text-center">
      <img class="img-fluid px-3 px-sm-4 mt-3 mb-4" style="width: 25rem;"
           src="../static/2021/images/undraw_uploading.svg" alt="">
    </div>
    {% endif %}

  </div>
</div><!-- row -->

{% if programs_to_plot %}

<div class="card shadow mb-4">
  <div class="card-header py-3">
    <h4 id="challenges" class="m-0 font-weight-bold text-primary">Strawberry scores over time</h4>
  </div>
  <div class="card-body">
    <div id="strawberryholder" style="height: 500px;"></div>
  </div>
</div>
{% endif %}

<hr />

{% if users %}

<div class="row">
  <div class="col-12">
    <h3 class="text-gray-800">Banana Scores</h3>
  </div>
</div>

<div class="row">

  <div class="col-sm-12 col-md-10 col-lg-6">
    <div class="card shadow mb-4">
      <div class="card-header py-3">
        <h4 id="challenges" class="m-0 font-weight-bold text-primary">Banana ranking</h4>
      </div>
      <div class="card-body">
        <div class="table-responsive">
          {% include 'table_bananas_ranking.html' %}
        </div>
      </div>
    </div>
  </div>

  <div class="col-sm-12 col-md-10 col-lg-6">
    {% if programs %}

    <div class="card shadow mb-4">
      <div class="card-header py-3">
        <h4 id="challenges" class="m-0 font-weight-bold text-primary">All challenge breaks</h4>
      </div>
      <div class="card-body">
        {% if wb_breaks %}
        <div class="table-responsive">
          {% include 'table_breaks.html' %}
        </div>
        {% else %}
        <h2>No Challenge break Yet!</h2>
        {% endif %}
      </div>
    </div>

    {% endif %}

  </div>

</div><!-- row -->

{% endif %}
