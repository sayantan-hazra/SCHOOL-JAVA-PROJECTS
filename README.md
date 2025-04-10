# WELCOME

HI I AM SAYANTAN HAZRA, STUDENT OF CLASS 12

I AM A CODE LOVER, TRIES TO WORK WITH DIFFERENT PROBLEMS TO FIND IT'S ANSWER

CURRENTLY I AM FOCUSING ON SCHOOL PROJECTS

THIS YEAR MEANS 2023 - 2024 IS A CRUCIAL YEAR FOR ME BECAUSE OF ISC EXAM

<<< -------     E     N     D     ------- >>>





<!DOCTYPE html>
<html ng-app="layoutApp">
<head>
  <script src="https://ajax.googleapis.com/ajax/libs/angularjs/1.8.2/angular.min.js"></script>
  <style>
    .container {
      border: 2px solid black;
      width: 500px;
      margin-bottom: 50px;
    }
    .header, .footer {
      border: 1px solid black;
      padding: 10px;
      text-align: center;
      font-weight: bold;
    }
    .row {
      display: flex;
    }
    .left, .right {
      flex: 1;
      border: 1px solid black;
      padding: 20px;
      text-align: center;
      font-weight: bold;
    }

    /* Second layout colors */
    .layout2 .header { background-color: cyan; }
    .layout2 .left { background-color: chartreuse; }
    .layout2 .right { background-color: blueviolet; }
    .layout2 .footer { background-color: palevioletred; }
  </style>
</head>
<body ng-controller="LayoutController">

  <!-- Layout 1 -->
  <div class="container" ng-if="showLayout1">
    <div class="header">{{layout1.header}}</div>
    <div class="row">
      <div class="left">{{layout1.left}}</div>
      <div class="right">{{layout1.right}}</div>
    </div>
    <div class="footer">{{layout1.footer}}</div>
  </div>

  <!-- Layout 2 -->
  <div class="container layout2" ng-if="showLayout2">
    <div class="header">{{layout2.header}}</div>
    <div class="row">
      <div class="left">{{layout2.left}}</div>
      <div class="right">{{layout2.right}}</div>
    </div>
    <div class="footer">{{layout2.footer}}</div>
  </div>

  <script>
    angular.module('layoutApp', [])
      .controller('LayoutController', function($scope) {
        $scope.showLayout1 = true;
        $scope.showLayout2 = true;

        $scope.layout1 = {
          header: 'HEADER',
          left: 'LEFT',
          right: 'RIGHT',
          footer: 'FOOTER'
        };

        $scope.layout2 = {
          header: 'HEADER',
          left: 'LEFT',
          right: 'RIGHT',
          footer: 'FOOTER'
        };
      });
  </script>
</body>
</html>