---
layout: default
title: LmBox 1.0.0-RC2
parent: Release Notes
nav_order: 2
description: "LmBox 1.0.0-RC2"
permalink: lmbox-1-0-0-rc2
---

Release Notes - LmBox 1.0.0-RC2
===============================

    ** Feature
        * [LMB-161] - Implement volume discount system
        * [LMB-162] - Add "Paid Amount", "Discount" and "Currency" fields to the Transaction business entity
        * [LMB-163] - Add discounts entry to the LmBoxManage Product edit page (similar to custom properties)
        * [LMB-164] - Implement discounts validation in core
        * [LMB-165] - Add discounts calculation to LmBoxShop
        * [LMB-166] - Enable payment methods page
        * [LMB-168] - Feature expiration warning level in FeatureWithTimeVolume Licensing Model
        * [LMB-169] - Implement calculation of the warning level in FeatureWithTimeVolume Licensing Model
        * [LMB-173] - Paypal configuration instructions for vendor
        * [LMB-174] - Add read-only property to FEATURE license reporting current green/yellow/red status
        * [LMB-175] - Add custom properties to product module
        * [LMB-181] - Add product module properties "redTreshold", "yellowTreshold" (FeatureWithTimeVolume Licensing Model)
        * [LMB-183] - Documentation for vendor: redirect to LmBoxShop
        * [LMB-189] - Add "type" attribute to XML "info"
        * [LMB-192] - Introduce basic filter functionality for the list operations
        * [LMB-193] - Implement dynamic popup content on license add in LmBoxShop, that depends on selected license template
        * [LMB-198] - Prepare Licensing Model / License Template specific forms for the popup
        * [LMB-204] - Make entity tables number fields clickable
        * [LMB-205] - Introduce token service
        * [LMB-212] - Add filter controls to UI
        * [LMB-219] - Implement subtotals and discounts display
        * [LMB-239] - Return warnings for bad filter parameters
        * [LMB-251] - Shop confirmation page

    ** Bug
        * [LMB-136] - Frontend: In case of exception, the view is broken
        * [LMB-237] - Fix error 500 if shop is opened without token or with expired token
        * [LMB-249] - TimeEvaluation Licensing Model should only allow to purchase the feature once