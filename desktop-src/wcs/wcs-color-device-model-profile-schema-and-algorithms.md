---
title: Algorithmes et schéma de profil de modèle d’appareil de couleur WCS
description: Cette rubrique fournit des informations sur le schéma de profil de modèle de périphérique de couleur WCS et les algorithmes qui lui sont associés. Cette rubrique contient les sections suivantes OverviewColor Device Model Profile ArchitectureThe CDMP SchemaWCS CDMP v 2.0 étalonnage AdditionThe CDMP Schema ElementsColorDeviceModelProfileColorDeviceModelNamespaceVersionVersionDocumentationCRTDevice elementLCDDevice elementProjectorDevice elementScannerDevice elementCameraDevice elementRGBPrinterDevice elementCMYKPrinterDevice elementRGBVirtualDevice elementPlugInDeviceTypeRGBVirtualMeasurementTypeGammaTypeGammaOffsetGainTypeGammaOffsetGainLinearGainTypeToneResponseCurvesTypeGamutBoundarySamplesTypeFloatPairListCMYKPrinterMeasurementTypeRGBPrinterMeasurementTypeRGBCaptureMeasurementTypeOneBasedIndexRGBProjectorMeasurementTypeDisplayMeasurementTy peMeasurementConditionsTypeGeometryTypeRGBPrimariesGroupNonNegativeCMYKSampleTypeNonNegativeRGBSampleTypeNonNegativeCMYKTypeNonNegativeRGBTypeExtensionTypeNonNegativeXYZTypeXYZTypeThe CDMP Baseline AlgorithmsCRT modèle d’appareil BaselineLCD modèle d’appareil BaselineRGB imprimante modèle d’appareil BaselineRGB modèle d’appareil BaselineCMYK imprimante modèle de périphérique BaselineRGB projecteur périphérique BaselineICC modèle d’appareil BaselineRelated rubriques
ms.assetid: bbb3b50d-75fc-476d-a011-af7dcc2ac520
keywords:
- Système de couleurs Windows (WCS), profil de modèle de périphérique en couleurs (CDMP)
- WCS (système de couleurs Windows), profil de modèle de périphérique en couleurs (CDMP)
- gestion des couleurs des images, profil de modèle de périphérique en couleurs (CDMP)
- gestion des couleurs, profil de modèle de périphérique en couleurs (CDMP)
- couleurs, profil de modèle de périphérique en couleurs (CDMP)
- Système de couleurs Windows (WCS), profils
- WCS (système de couleurs Windows), profils
- gestion des couleurs des images, profils
- gestion des couleurs, profils
- couleurs, profils
- schémas, modèle de modèle de périphérique de couleurs (CDMP)
- algorithmes, profil de modèle de périphérique en couleurs (CDMP)
- Profil de modèle de périphérique en couleurs (CDMP)
- CDMP (profil de modèle de périphérique en couleur)
- Profil de modèle de périphérique de couleur WCS
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b671bf97625b00c99060e65be4d39c44e5b35f
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104551796"
---
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a><span data-ttu-id="e004e-118">Algorithmes et schéma de profil de modèle d’appareil de couleur WCS</span><span class="sxs-lookup"><span data-stu-id="e004e-118">WCS Color Device Model Profile Schema and Algorithms</span></span>

<span data-ttu-id="e004e-119">Cette rubrique fournit des informations sur le schéma de profil de modèle de périphérique de couleur WCS et les algorithmes qui lui sont associés.</span><span class="sxs-lookup"><span data-stu-id="e004e-119">This topic provides information about the WCS Color Device Model Profile Schema and its associated algorithms.</span></span>

<span data-ttu-id="e004e-120">Cette rubrique contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="e004e-120">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="e004e-121">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="e004e-121">Overview</span></span>](#overview)
-   [<span data-ttu-id="e004e-122">Architecture du profil de modèle de périphérique en couleurs</span><span class="sxs-lookup"><span data-stu-id="e004e-122">Color Device Model Profile Architecture</span></span>](#color-device-model-profile-architecture)
-   [<span data-ttu-id="e004e-123">Schéma CDMP</span><span class="sxs-lookup"><span data-stu-id="e004e-123">The CDMP Schema</span></span>](#the-cdmp-schema)
-   [<span data-ttu-id="e004e-124">Ajout d’étalonnage à WCS CDMP v 2.0</span><span class="sxs-lookup"><span data-stu-id="e004e-124">WCS CDMP v2.0 Calibration Addition</span></span>](#wcs-cdmp-v20-calibration-addition)
-   [<span data-ttu-id="e004e-125">Éléments du schéma CDMP</span><span class="sxs-lookup"><span data-stu-id="e004e-125">The CDMP Schema Elements</span></span>](#the-cdmp-schema-elements)
    -   [<span data-ttu-id="e004e-126">ColorDeviceModelProfile</span><span class="sxs-lookup"><span data-stu-id="e004e-126">ColorDeviceModelProfile</span></span>](#colordevicemodelprofile)
    -   [<span data-ttu-id="e004e-127">ColorDeviceModel</span><span class="sxs-lookup"><span data-stu-id="e004e-127">ColorDeviceModel</span></span>](#colordevicemodelprofile)
    -   [<span data-ttu-id="e004e-128">NamespaceVersion</span><span class="sxs-lookup"><span data-stu-id="e004e-128">NamespaceVersion</span></span>](#namespaceversion)
    -   [<span data-ttu-id="e004e-129">Version</span><span class="sxs-lookup"><span data-stu-id="e004e-129">Version</span></span>](#namespaceversion)
    -   [<span data-ttu-id="e004e-130">Documentation</span><span class="sxs-lookup"><span data-stu-id="e004e-130">Documentation</span></span>](#documentation)
    -   [<span data-ttu-id="e004e-131">Élément CRTDevice</span><span class="sxs-lookup"><span data-stu-id="e004e-131">CRTDevice element</span></span>](#crtdevice-element)
    -   [<span data-ttu-id="e004e-132">Élément LCDDevice</span><span class="sxs-lookup"><span data-stu-id="e004e-132">LCDDevice element</span></span>](#lcddevice-element)
    -   [<span data-ttu-id="e004e-133">Élément ProjectorDevice</span><span class="sxs-lookup"><span data-stu-id="e004e-133">ProjectorDevice element</span></span>](#projectordevice-element)
    -   [<span data-ttu-id="e004e-134">Élément ScannerDevice</span><span class="sxs-lookup"><span data-stu-id="e004e-134">ScannerDevice element</span></span>](#scannerdevice-element)
    -   [<span data-ttu-id="e004e-135">Élément CameraDevice</span><span class="sxs-lookup"><span data-stu-id="e004e-135">CameraDevice element</span></span>](#cameradevice-element)
    -   [<span data-ttu-id="e004e-136">Élément RGBPrinterDevice</span><span class="sxs-lookup"><span data-stu-id="e004e-136">RGBPrinterDevice element</span></span>](#rgbprinterdevice-element)
    -   [<span data-ttu-id="e004e-137">Élément CMYKPrinterDevice</span><span class="sxs-lookup"><span data-stu-id="e004e-137">CMYKPrinterDevice element</span></span>](#cmykprinterdevice-element)
    -   [<span data-ttu-id="e004e-138">Élément RGBVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="e004e-138">RGBVirtualDevice element</span></span>](#rgbvirtualdevice-element)
    -   [<span data-ttu-id="e004e-139">PlugInDeviceType</span><span class="sxs-lookup"><span data-stu-id="e004e-139">PlugInDeviceType</span></span>](#plugindevicetype)
    -   [<span data-ttu-id="e004e-140">RGBVirtualMeasurementType</span><span class="sxs-lookup"><span data-stu-id="e004e-140">RGBVirtualMeasurementType</span></span>](#rgbvirtualmeasurementtype)
    -   [<span data-ttu-id="e004e-141">GammaType</span><span class="sxs-lookup"><span data-stu-id="e004e-141">GammaType</span></span>](#gammatype)
    -   [<span data-ttu-id="e004e-142">GammaOffsetGainType</span><span class="sxs-lookup"><span data-stu-id="e004e-142">GammaOffsetGainType</span></span>](#gammaoffsetgaintype)
    -   [<span data-ttu-id="e004e-143">GammaOffsetGainLinearGainType</span><span class="sxs-lookup"><span data-stu-id="e004e-143">GammaOffsetGainLinearGainType</span></span>](#gammaoffsetgainlineargaintype)
    -   [<span data-ttu-id="e004e-144">ToneResponseCurvesType</span><span class="sxs-lookup"><span data-stu-id="e004e-144">ToneResponseCurvesType</span></span>](#toneresponsecurvestype)
    -   [<span data-ttu-id="e004e-145">GamutBoundarySamplesType</span><span class="sxs-lookup"><span data-stu-id="e004e-145">GamutBoundarySamplesType</span></span>](#gamutboundarysamplestype)
    -   [<span data-ttu-id="e004e-146">FloatPairList</span><span class="sxs-lookup"><span data-stu-id="e004e-146">FloatPairList</span></span>](#floatpairlist)
    -   [<span data-ttu-id="e004e-147">CMYKPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="e004e-147">CMYKPrinterMeasurementType</span></span>](#cmykprintermeasurementtype)
    -   [<span data-ttu-id="e004e-148">RGBPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="e004e-148">RGBPrinterMeasurementType</span></span>](#rgbprintermeasurementtype)
    -   [<span data-ttu-id="e004e-149">RGBCaptureMeasurementType</span><span class="sxs-lookup"><span data-stu-id="e004e-149">RGBCaptureMeasurementType</span></span>](#rgbcapturemeasurementtype)
    -   [<span data-ttu-id="e004e-150">OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="e004e-150">OneBasedIndex</span></span>](#onebasedindex)
    -   [<span data-ttu-id="e004e-151">RGBProjectorMeasurementType</span><span class="sxs-lookup"><span data-stu-id="e004e-151">RGBProjectorMeasurementType</span></span>](#rgbprojectormeasurementtype)
    -   [<span data-ttu-id="e004e-152">DisplayMeasurementType</span><span class="sxs-lookup"><span data-stu-id="e004e-152">DisplayMeasurementType</span></span>](#displaymeasurementtype)
    -   [<span data-ttu-id="e004e-153">MeasurementConditionsType</span><span class="sxs-lookup"><span data-stu-id="e004e-153">MeasurementConditionsType</span></span>](#measurementconditionstype)
    -   [<span data-ttu-id="e004e-154">GeometryType</span><span class="sxs-lookup"><span data-stu-id="e004e-154">GeometryType</span></span>](#geometrytype)
    -   [<span data-ttu-id="e004e-155">RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="e004e-155">RGBPrimariesGroup</span></span>](#rgbprimariesgroup)
    -   [<span data-ttu-id="e004e-156">NonNegativeCMYKSampleType</span><span class="sxs-lookup"><span data-stu-id="e004e-156">NonNegativeCMYKSampleType</span></span>](#nonnegativecmyksampletype)
    -   [<span data-ttu-id="e004e-157">NonNegativeRGBSampleType</span><span class="sxs-lookup"><span data-stu-id="e004e-157">NonNegativeRGBSampleType</span></span>](#nonnegativergbsampletype)
    -   [<span data-ttu-id="e004e-158">NonNegativeCMYKType</span><span class="sxs-lookup"><span data-stu-id="e004e-158">NonNegativeCMYKType</span></span>](#nonnegativecmyktype)
    -   [<span data-ttu-id="e004e-159">NonNegativeRGBType</span><span class="sxs-lookup"><span data-stu-id="e004e-159">NonNegativeRGBType</span></span>](#nonnegativergbtype)
    -   [<span data-ttu-id="e004e-160">ExtensionType</span><span class="sxs-lookup"><span data-stu-id="e004e-160">ExtensionType</span></span>](#extensiontype)
    -   [<span data-ttu-id="e004e-161">NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="e004e-161">NonNegativeXYZType</span></span>](#nonnegativexyztype)
    -   [<span data-ttu-id="e004e-162">XYZType</span><span class="sxs-lookup"><span data-stu-id="e004e-162">XYZType</span></span>](#nonnegativexyztype)
-   [<span data-ttu-id="e004e-163">Algorithmes de base CDMP</span><span class="sxs-lookup"><span data-stu-id="e004e-163">The CDMP Baseline Algorithms</span></span>](#the-cdmp-baseline-algorithms)
    -   [<span data-ttu-id="e004e-164">Ligne de base du modèle de périphérique CRT</span><span class="sxs-lookup"><span data-stu-id="e004e-164">CRT Device Model Baseline</span></span>](#crt-device-model-baseline)
    -   [<span data-ttu-id="e004e-165">Ligne de base du modèle d’appareil LCD</span><span class="sxs-lookup"><span data-stu-id="e004e-165">LCD Device Model Baseline</span></span>](#lcd-device-model-baseline)
    -   [<span data-ttu-id="e004e-166">Ligne de base du modèle d’imprimante RVB</span><span class="sxs-lookup"><span data-stu-id="e004e-166">RGB Printer Device Model Baseline</span></span>](#rgb-printer-device-model-baseline)
    -   [<span data-ttu-id="e004e-167">Ligne de base du modèle d’appareil virtuel RGB</span><span class="sxs-lookup"><span data-stu-id="e004e-167">RGB Virtual Device Model Baseline</span></span>](#rgb-virtual-device-model-baseline)
    -   [<span data-ttu-id="e004e-168">Ligne de base modèle de périphérique d’imprimante CMJN</span><span class="sxs-lookup"><span data-stu-id="e004e-168">CMYK Printer Device Model Baseline</span></span>](#cmyk-printer-device-model-baseline)
    -   [<span data-ttu-id="e004e-169">Ligne de base du modèle d’appareil projecteur RVB</span><span class="sxs-lookup"><span data-stu-id="e004e-169">RGB Projector Device Model Baseline</span></span>](#rgb-projector-device-model-baseline)
    -   [<span data-ttu-id="e004e-170">Ligne de base du modèle d’appareil ICC</span><span class="sxs-lookup"><span data-stu-id="e004e-170">ICC Device Model Baseline</span></span>](#icc-device-model-baseline)
-   [<span data-ttu-id="e004e-171">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e004e-171">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="e004e-172">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="e004e-172">Overview</span></span>

<span data-ttu-id="e004e-173">Ce schéma est utilisé pour spécifier le contenu d’un profil de modèle de périphérique en couleurs (CDMP).</span><span class="sxs-lookup"><span data-stu-id="e004e-173">This schema is used to specify the content of a color device model profile(CDMP).</span></span> <span data-ttu-id="e004e-174">Les algorithmes de base de référence associés sont décrits ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e004e-174">The associated baseline algorithms are described below.</span></span>

<span data-ttu-id="e004e-175">Le schéma DMP (Device Model Profile) de base se compose des données de mesure d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="e004e-175">The basic device model profile (DMP) schema consists of the sampling measurement data.</span></span>

<span data-ttu-id="e004e-176">Le composant d’échantillonnage du schéma XML DMP assure la prise en charge des cibles de mesure de couleur de base, en se concentrant sur des cibles standard et des cibles optimisées pour les modèles d’appareil de base.</span><span class="sxs-lookup"><span data-stu-id="e004e-176">The sampling component of the DMP XML schema provides support for basic color measurement targets, focusing on common standard targets and targets optimized for the baseline device models.</span></span>

<span data-ttu-id="e004e-177">En outre, le profil d’appareil fournit des informations spécifiques sur le modèle d’appareil ciblé et fournit une stratégie que le modèle d’appareil de secours de base peut utiliser si le modèle ciblé n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="e004e-177">In addition, the device profile provides specific information on the targeted device model and provides a policy that the baseline fallback device model can use if the targeted model is unavailable.</span></span> <span data-ttu-id="e004e-178">Les instances de profil peuvent inclure des extensions privées à l’aide de mécanismes d’extension XML standard.</span><span class="sxs-lookup"><span data-stu-id="e004e-178">The profile instances can include private extensions using standard XML extension mechanisms.</span></span>

## <a name="color-device-model-profile-architecture"></a><span data-ttu-id="e004e-179">Architecture du profil de modèle de périphérique en couleurs</span><span class="sxs-lookup"><span data-stu-id="e004e-179">Color Device Model Profile Architecture</span></span>

![Diagramme qui affiche les informations qui constituent un profil de modèle d’appareil.](images/cdmp-image002new.png)

## <a name="the-cdmp-schema"></a><span data-ttu-id="e004e-181">Schéma CDMP</span><span class="sxs-lookup"><span data-stu-id="e004e-181">The CDMP Schema</span></span>


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema 
  xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Device Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:complexType name="RGBType">
    <xs:attribute name="R" type="xs:float" use="required"/>
    <xs:attribute name="G" type="xs:float" use="required"/>
    <xs:attribute name="B" type="xs:float" use="required"/>
  </xs:complexType>

  <xs:complexType name="NonNegativeRGBType">
    <xs:attribute name="R" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="G" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="B" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:complexType name="NonNegativeCMYKType">
    <xs:attribute name="C" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="M" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Y" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="K" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:complexType name="NonNegativeRGBSampleType">
    <xs:sequence>
      <xs:element name="RGB" type="cdm:NonNegativeRGBType"/>
      <xs:element name="CIEXYZ" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
    <xs:attribute name="Tag" type="xs:string" use="optional"/>
  </xs:complexType>
  
  <xs:complexType name="NonNegativeCMYKSampleType">
    <xs:sequence>
      <xs:element name="CMYK" type="cdm:NonNegativeCMYKType"/>
      <xs:element name="CIEXYZ" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
    <xs:attribute name="Tag" type="xs:string" use="optional"/>
  </xs:complexType>
  
  <xs:group name="RGBPrimariesGroup">
    <xs:sequence>
      <xs:element name="WhitePrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="RedPrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="GreenPrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="BluePrimary" type="wcs:NonNegativeCIEXYZType"/>
      <xs:element name="BlackPrimary" type="wcs:NonNegativeCIEXYZType"/>
    </xs:sequence>
  </xs:group> 
  
  <xs:complexType name="MeasurementConditionsType">
    <xs:annotation>
      <xs:documentation>
      Optional measurement conditions. 
       
      We only support CIEXYZ for measurement color space in this version. 
      If the white point value from the measurement conditions is not available, 
      the default processing will use
        - "D50" for printer and scanners
        - "D65" for camera and displays.          
      </xs:documentation>
    </xs:annotation>
    <xs:sequence>
      <xs:element name="ColorSpace" minOccurs="0">
        <xs:simpleType>
          <xs:restriction base="xs:string">
            <xs:enumeration value="CIEXYZ"/>
          </xs:restriction>
        </xs:simpleType>    
      </xs:element>
      <xs:choice minOccurs="0">
        <xs:element name="WhitePoint" type="wcs:NonNegativeCIEXYZType"/>
        <xs:element name="WhitePointName">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="D50"/>
              <xs:enumeration value="D65"/>
              <xs:enumeration value="A"/>
              <xs:enumeration value="F2"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
      </xs:choice>
      <xs:element name="Geometry" minOccurs="0">
        <xs:simpleType>
          <xs:restriction base="xs:string">
            <xs:enumeration value="0/45"/>
            <xs:enumeration value="0/diffuse"/>
            <xs:enumeration value="diffuse/0"/>
            <xs:enumeration value="direct"/>
          </xs:restriction>
        </xs:simpleType>   
      </xs:element>
      <xs:element name="ApertureSize" type="xs:int" minOccurs="0"/>
    </xs:sequence>
  </xs:complexType>
  
  <xs:complexType name="DisplayMeasurementType">
    <xs:sequence>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:element name="GrayRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="RedRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="GreenRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
      <xs:element name="BlueRamp">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="4096"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="RGBProjectorMeasurementType">
    <xs:sequence>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:element name="ColorSamples">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:simpleType name="OneBasedIndex">
    <xs:restriction base="xs:int">
      <xs:minInclusive value="1"/>
    </xs:restriction>
  </xs:simpleType>
    
  <xs:complexType name="RGBCaptureMeasurementType">
    <xs:sequence>
      <xs:element name="PrimaryIndex">
        <xs:complexType>
          <xs:all>
            <xs:element name="White" type="cdm:OneBasedIndex"/>
            <xs:element name="Black" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Red" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Green" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Blue" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Cyan" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Magenta" type="cdm:OneBasedIndex" minOccurs="0"/>
            <xs:element name="Yellow" type="cdm:OneBasedIndex" minOccurs="0"/>
          </xs:all>
        </xs:complexType>
      </xs:element>
      <xs:element name="NeutralIndices">
        <xs:simpleType>
          <xs:list itemType="cdm:OneBasedIndex"/>
        </xs:simpleType>
      </xs:element>
      <xs:element name="ColorSamples">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="RGBPrinterMeasurementType">
    <xs:sequence>
      <xs:element name="ColorCube">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeRGBSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>       
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>
  
  <xs:complexType name="CMYKPrinterMeasurementType">
    <xs:sequence>
      <xs:element name="ColorCube">
        <xs:complexType>
          <xs:sequence>
            <xs:element name="Sample" type="cdm:NonNegativeCMYKSampleType" maxOccurs="unbounded"/> 
          </xs:sequence>
        </xs:complexType>
      </xs:element>       
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>

  <xs:complexType name="GammaType">
    <xs:attribute name="value" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:complexType name="GammaOffsetGainType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:complexType name="GammaOffsetGainLinearGainType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="LinearGain" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="TransitionPoint" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>
  
  <xs:simpleType name="FloatList">
    <xs:list itemType="xs:float"/>
  </xs:simpleType>

  <xs:complexType name="OneDimensionLutType">
    <xs:sequence>
      <xs:element name="Input" type="cdm:FloatList"/>
      <xs:element name="Output" type="cdm:FloatList"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="HDRToneResponseCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="cdm:OneDimensionLutType"/>
      <xs:element name="GreenTRC" type="cdm:OneDimensionLutType"/>
      <xs:element name="BlueTRC" type="cdm:OneDimensionLutType"/>
    </xs:sequence>
    <xs:attribute name="TRCLength" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:int">
          <xs:minInclusive value="0" />
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
  
  <xs:complexType name="GamutBoundarySamplesType">
    <xs:sequence>
      <xs:element name="RGB" type="cdm:RGBType" maxOccurs="unbounded"/>
    </xs:sequence>
  </xs:complexType>
  
  <xs:complexType name="RGBVirtualMeasurementType">
    <xs:sequence>
      <xs:element name="MaxColorantUsed" type="xs:float"/>
      <xs:element name="MinColorantUsed" type="xs:float"/>
      <xs:group ref="cdm:RGBPrimariesGroup"/>
      <xs:choice>
        <xs:element name="Gamma" type="cdm:GammaType"/>
        <xs:element name="GammaOffsetGain" type="cdm:GammaOffsetGainType"/>
        <xs:element name="GammaOffsetGainLinearGain" type="cdm:GammaOffsetGainLinearGainType"/>
        <xs:element name="HDRToneResponseCurves" type="cdm:HDRToneResponseCurvesType"/>
      </xs:choice>
      <xs:element name="GamutBoundarySamples" type="cdm:GamutBoundarySamplesType" minOccurs="0"/>
    </xs:sequence>
    <xs:attribute name="TimeStamp" type="xs:dateTime"/>
  </xs:complexType>
  
  <xs:element name="ColorDeviceModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="MeasurementConditions" type="cdm:MeasurementConditionsType" minOccurs="0"/>
        <xs:element name="SelfLuminous" type="xs:boolean" />
        <xs:element name="MaxColorant" type="xs:float"/>
        <xs:element name="MinColorant" type="xs:float"/>
        <xs:choice>
          <xs:element name="CRTDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:DisplayMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="LCDDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:DisplayMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBProjectorDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBProjectorMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="ScannerDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBCaptureMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="CameraDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBCaptureMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBPrinterDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBPrinterMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="CMYKPrinterDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:CMYKPrinterMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
          <xs:element name="RGBVirtualDevice">
            <xs:complexType>
              <xs:sequence>
                <xs:element name="MeasurementData" type="cdm:RGBVirtualMeasurementType"/>
              </xs:sequence>
            </xs:complexType>
          </xs:element>
        </xs:choice>
        <xs:element name="PlugInDevice" minOccurs="0">
          <xs:complexType>
            <xs:sequence>
              <xs:any namespace="##other" processContents="skip"
                minOccurs="0" maxOccurs="unbounded" />
            </xs:sequence>
            <xs:attribute name="GUID" type="wcs:GUIDType" use="required"/>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>

```



## <a name="wcs-cdmp-v20-calibration-addition"></a><span data-ttu-id="e004e-182">Ajout d’étalonnage à WCS CDMP v 2.0</span><span class="sxs-lookup"><span data-stu-id="e004e-182">WCS CDMP v2.0 Calibration Addition</span></span>

<span data-ttu-id="e004e-183">L’élément **ColorDeviceModel** du schéma CDMP a été mis à jour dans Windows 7 pour inclure le nouvel élément d’étalonnage.</span><span class="sxs-lookup"><span data-stu-id="e004e-183">The **ColorDeviceModel** element of the CDMP schema has been updated in Windows 7 to include the new calibration element.</span></span> <span data-ttu-id="e004e-184">L’exemple suivant montre la modification apportée au schéma CDMP.</span><span class="sxs-lookup"><span data-stu-id="e004e-184">The following shows the change to the CDMP schema.</span></span>


```C++
  ...
  <xs:element name="ColorDeviceModel">
    <xs:complexType>
      <xs:sequence>
        ...
        <xs:element name="PlugInDevice" minOccurs="0">
             ...
        </xs:element>
        <xs:element name="Calibration" type="cal:Calibration" minOccurs="0"/>
        ...
      <xs:sequence>
    ...
    <xs:complexType>
  ...
```



## <a name="the-cdmp-schema-elements"></a><span data-ttu-id="e004e-185">Éléments du schéma CDMP</span><span class="sxs-lookup"><span data-stu-id="e004e-185">The CDMP Schema Elements</span></span>

> [!Note]  
> <span data-ttu-id="e004e-186">Les primaires sont des exemples principaux de rouge, vert, bleu, noir et blanc.</span><span class="sxs-lookup"><span data-stu-id="e004e-186">Primaries are primary samples of red, green, blue, black, and white.</span></span> <span data-ttu-id="e004e-187">Une rampe principale est une rampe tonale de la luminance la plus faible à la valeur principale complète.</span><span class="sxs-lookup"><span data-stu-id="e004e-187">A primary ramp is a tonal ramp from least luminance to full primary value.</span></span> <span data-ttu-id="e004e-188">Le nombre maximal d’entrées dans une rampe de fréquences est 4096.</span><span class="sxs-lookup"><span data-stu-id="e004e-188">The maximum number of entries in a tone ramp is 4096.</span></span>

 

> [!Note]  
> <span data-ttu-id="e004e-189">Les données de mesure doivent être DMPs.</span><span class="sxs-lookup"><span data-stu-id="e004e-189">DMPs are required to have measurement data.</span></span>

 

### <a name="colordevicemodelprofile"></a><span data-ttu-id="e004e-190">ColorDeviceModelProfile</span><span class="sxs-lookup"><span data-stu-id="e004e-190">ColorDeviceModelProfile</span></span>

<span data-ttu-id="e004e-191">Cet élément est de type ColorDeviceModel.</span><span class="sxs-lookup"><span data-stu-id="e004e-191">This element is of type ColorDeviceModel.</span></span>

<span data-ttu-id="e004e-192">**Conditions de validation :** Chaque sous-élément est validé par son propre type.</span><span class="sxs-lookup"><span data-stu-id="e004e-192">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="colordevicemodel"></a><span data-ttu-id="e004e-193">ColorDeviceModel</span><span class="sxs-lookup"><span data-stu-id="e004e-193">ColorDeviceModel</span></span>

<span data-ttu-id="e004e-194">Cet élément est une séquence des sous-éléments suivants</span><span class="sxs-lookup"><span data-stu-id="e004e-194">This element is a sequence of the following sub-elements</span></span>

1.  <span data-ttu-id="e004e-195">Chaîne ProfileName,</span><span class="sxs-lookup"><span data-stu-id="e004e-195">ProfileName string,</span></span>
2.  <span data-ttu-id="e004e-196">chaîne de description facultative,</span><span class="sxs-lookup"><span data-stu-id="e004e-196">optional Description string,</span></span>
3.  <span data-ttu-id="e004e-197">chaîne d’auteur facultative,</span><span class="sxs-lookup"><span data-stu-id="e004e-197">optional Author string,</span></span>
4.  <span data-ttu-id="e004e-198">MeasurementConditions facultatif MeasurementConditionsType,</span><span class="sxs-lookup"><span data-stu-id="e004e-198">optional MeasurementConditions MeasurementConditionsType,</span></span>
5.  <span data-ttu-id="e004e-199">Self-Luminous valeur booléenne,</span><span class="sxs-lookup"><span data-stu-id="e004e-199">Self-Luminous Boolean,</span></span>
6.  <span data-ttu-id="e004e-200">MaxColorant float,</span><span class="sxs-lookup"><span data-stu-id="e004e-200">MaxColorant float,</span></span>
7.  <span data-ttu-id="e004e-201">MinColorant float,</span><span class="sxs-lookup"><span data-stu-id="e004e-201">MinColorant float,</span></span>
8.  <span data-ttu-id="e004e-202">Choix des éléments</span><span class="sxs-lookup"><span data-stu-id="e004e-202">Choice of elements</span></span>
    1.  <span data-ttu-id="e004e-203">CRTDevice,</span><span class="sxs-lookup"><span data-stu-id="e004e-203">CRTDevice,</span></span>
    2.  <span data-ttu-id="e004e-204">LCDDevice,</span><span class="sxs-lookup"><span data-stu-id="e004e-204">LCDDevice,</span></span>
    3.  <span data-ttu-id="e004e-205">RGBProjectorDevice,</span><span class="sxs-lookup"><span data-stu-id="e004e-205">RGBProjectorDevice,</span></span>
    4.  <span data-ttu-id="e004e-206">ScannerDevice,</span><span class="sxs-lookup"><span data-stu-id="e004e-206">ScannerDevice,</span></span>
    5.  <span data-ttu-id="e004e-207">CameraDevice,</span><span class="sxs-lookup"><span data-stu-id="e004e-207">CameraDevice,</span></span>
    6.  <span data-ttu-id="e004e-208">RGBPrinterDevice,</span><span class="sxs-lookup"><span data-stu-id="e004e-208">RGBPrinterDevice,</span></span>
    7.  <span data-ttu-id="e004e-209">CMYKPrinterDevice,</span><span class="sxs-lookup"><span data-stu-id="e004e-209">CMYKPrinterDevice,</span></span>
    8.  <span data-ttu-id="e004e-210">RGBVirtualDevice,</span><span class="sxs-lookup"><span data-stu-id="e004e-210">RGBVirtualDevice,</span></span>
9.  <span data-ttu-id="e004e-211">PlugInDevice,</span><span class="sxs-lookup"><span data-stu-id="e004e-211">PlugInDevice,</span></span>
10. <span data-ttu-id="e004e-212">ExtensionType d’extension facultatif</span><span class="sxs-lookup"><span data-stu-id="e004e-212">optional Extension ExtensionType</span></span>

<span data-ttu-id="e004e-213">**Conditions de validation :** Chaque sous-élément est validé par son propre type.</span><span class="sxs-lookup"><span data-stu-id="e004e-213">**Validation conditions:** Each sub-element is validated by its own type.</span></span> <span data-ttu-id="e004e-214">Les sous-éléments de chaîne ont un maximum de 10 000 caractères.</span><span class="sxs-lookup"><span data-stu-id="e004e-214">String sub-elements have a maximum of 10,000 characters.</span></span> <span data-ttu-id="e004e-215">Le sous-élément MaxColorant doit être supérieur ou égal à zéro (0) et supérieur au sous-élément MinColorant.</span><span class="sxs-lookup"><span data-stu-id="e004e-215">The MaxColorant sub-element must be greater than or equal to zero (0) and greater than the MinColorant sub-element.</span></span> <span data-ttu-id="e004e-216">Le MinColorant peut être négatif.</span><span class="sxs-lookup"><span data-stu-id="e004e-216">The MinColorant can be negative.</span></span>

### <a name="namespaceversion"></a><span data-ttu-id="e004e-217">NamespaceVersion</span><span class="sxs-lookup"><span data-stu-id="e004e-217">NamespaceVersion</span></span>

<span data-ttu-id="e004e-218">xmlns : CDM = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "</span><span class="sxs-lookup"><span data-stu-id="e004e-218">xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"</span></span>

<span data-ttu-id="e004e-219">targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "</span><span class="sxs-lookup"><span data-stu-id="e004e-219">targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"</span></span>

### <a name="version"></a><span data-ttu-id="e004e-220">Version</span><span class="sxs-lookup"><span data-stu-id="e004e-220">Version</span></span>

<span data-ttu-id="e004e-221">Version = « 1,0 » avec Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e004e-221">Version = "1.0" with Windows Vista.</span></span>

<span data-ttu-id="e004e-222">**Conditions de validation :** Toute valeur de version &gt; 0,1 ou &lt; = 2,0 est valide pour prendre en charge des modifications sans rupture au format.</span><span class="sxs-lookup"><span data-stu-id="e004e-222">**Validation conditions:** Any version value &gt;0.1 or &lt;=2.0 is valid to support non-breaking changes to the format.</span></span>

### <a name="documentation"></a><span data-ttu-id="e004e-223">Documentation</span><span class="sxs-lookup"><span data-stu-id="e004e-223">Documentation</span></span>

<span data-ttu-id="e004e-224">Schéma de profil de modèle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="e004e-224">Device Model Profile schema.</span></span>

<span data-ttu-id="e004e-225">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e004e-225">Copyright (C) Microsoft.</span></span> <span data-ttu-id="e004e-226">Tous droits réservés.</span><span class="sxs-lookup"><span data-stu-id="e004e-226">All rights reserved.</span></span>

### <a name="crtdevice-element"></a><span data-ttu-id="e004e-227">Élément CRTDevice</span><span class="sxs-lookup"><span data-stu-id="e004e-227">CRTDevice element</span></span>

<span data-ttu-id="e004e-228">Cet élément est une séquence de sous-éléments d’un DisplayMeasurementType MeasurementData.</span><span class="sxs-lookup"><span data-stu-id="e004e-228">This element is a sequence of sub-elements of a MeasurementData DisplayMeasurementType.</span></span>

<span data-ttu-id="e004e-229">**Conditions de validation :** Chaque sous-élément est validé par son propre type.</span><span class="sxs-lookup"><span data-stu-id="e004e-229">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="lcddevice-element"></a><span data-ttu-id="e004e-230">Élément LCDDevice</span><span class="sxs-lookup"><span data-stu-id="e004e-230">LCDDevice element</span></span>

<span data-ttu-id="e004e-231">Cet élément est une séquence de sous-éléments d’un DisplayMeasurementType MeasurementData.</span><span class="sxs-lookup"><span data-stu-id="e004e-231">This element is a sequence of sub-elements of a MeasurementData DisplayMeasurementType.</span></span>

<span data-ttu-id="e004e-232">**Conditions de validation :** Chaque sous-élément est validé par son propre type.</span><span class="sxs-lookup"><span data-stu-id="e004e-232">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="projectordevice-element"></a><span data-ttu-id="e004e-233">Élément ProjectorDevice</span><span class="sxs-lookup"><span data-stu-id="e004e-233">ProjectorDevice element</span></span>

<span data-ttu-id="e004e-234">Cet élément est une séquence de sous-éléments d’un RGBProjectorMeasurementType MeasurementData.</span><span class="sxs-lookup"><span data-stu-id="e004e-234">This element is a sequence of sub-elements of a MeasurementData RGBProjectorMeasurementType.</span></span>

<span data-ttu-id="e004e-235">**Conditions de validation :** Chaque sous-élément est validé par son propre type.</span><span class="sxs-lookup"><span data-stu-id="e004e-235">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="scannerdevice-element"></a><span data-ttu-id="e004e-236">Élément ScannerDevice</span><span class="sxs-lookup"><span data-stu-id="e004e-236">ScannerDevice element</span></span>

<span data-ttu-id="e004e-237">Cet élément est une séquence de sous-éléments d’un RGBCaptureMeasurementType MeasurementData</span><span class="sxs-lookup"><span data-stu-id="e004e-237">This element is a sequence of sub-elements of a MeasurementData RGBCaptureMeasurementType</span></span>

<span data-ttu-id="e004e-238">**Conditions de validation :** Chaque sous-élément est validé par son propre type.</span><span class="sxs-lookup"><span data-stu-id="e004e-238">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="cameradevice-element"></a><span data-ttu-id="e004e-239">Élément CameraDevice</span><span class="sxs-lookup"><span data-stu-id="e004e-239">CameraDevice element</span></span>

<span data-ttu-id="e004e-240">Cet élément est une séquence de sous-éléments d’un RGBCaptureMeasurementType MeasurementData</span><span class="sxs-lookup"><span data-stu-id="e004e-240">This element is a sequence of sub-elements of a MeasurementData RGBCaptureMeasurementType</span></span>

<span data-ttu-id="e004e-241">**Conditions de validation :** Chaque sous-élément est validé par son propre type.</span><span class="sxs-lookup"><span data-stu-id="e004e-241">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="rgbprinterdevice-element"></a><span data-ttu-id="e004e-242">Élément RGBPrinterDevice</span><span class="sxs-lookup"><span data-stu-id="e004e-242">RGBPrinterDevice element</span></span>

<span data-ttu-id="e004e-243">Cet élément est une séquence de sous-éléments d’un RGBPrinterMeasurementType MeasurementData.</span><span class="sxs-lookup"><span data-stu-id="e004e-243">This element is a sequence of sub-elements of a MeasurementData RGBPrinterMeasurementType.</span></span>

<span data-ttu-id="e004e-244">**Conditions de validation :** Chaque sous-élément est validé par son propre type.</span><span class="sxs-lookup"><span data-stu-id="e004e-244">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="cmykprinterdevice-element"></a><span data-ttu-id="e004e-245">Élément CMYKPrinterDevice</span><span class="sxs-lookup"><span data-stu-id="e004e-245">CMYKPrinterDevice element</span></span>

<span data-ttu-id="e004e-246">Cet élément est une séquence de sous-éléments d’un CMYKPrinterMeasurementType MeasurementData.</span><span class="sxs-lookup"><span data-stu-id="e004e-246">This element is a sequence of sub-elements of a MeasurementData CMYKPrinterMeasurementType.</span></span>

<span data-ttu-id="e004e-247">**Conditions de validation :** Chaque sous-élément est validé par son propre type.</span><span class="sxs-lookup"><span data-stu-id="e004e-247">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="rgbvirtualdevice-element"></a><span data-ttu-id="e004e-248">Élément RGBVirtualDevice</span><span class="sxs-lookup"><span data-stu-id="e004e-248">RGBVirtualDevice element</span></span>

<span data-ttu-id="e004e-249">Cet élément est une séquence de sous-éléments d’un RGBVirtualMeasurementDataType.</span><span class="sxs-lookup"><span data-stu-id="e004e-249">This element is a sequence of sub-elements of a RGBVirtualMeasurementDataType.</span></span>

<span data-ttu-id="e004e-250">**Conditions de validation :** Chaque sous-élément est validé par son propre type.</span><span class="sxs-lookup"><span data-stu-id="e004e-250">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

### <a name="plugindevicetype"></a><span data-ttu-id="e004e-251">PlugInDeviceType</span><span class="sxs-lookup"><span data-stu-id="e004e-251">PlugInDeviceType</span></span>

<span data-ttu-id="e004e-252">Cet élément est une séquence d’un GUID GUIDType et de tous les sous-éléments.</span><span class="sxs-lookup"><span data-stu-id="e004e-252">This element is a sequence of a GUID GUIDType and any sub-elements.</span></span>

<span data-ttu-id="e004e-253">**Conditions de validation :** Le GUID est utilisé pour faire correspondre le GUID de la dll du plug-in DM.</span><span class="sxs-lookup"><span data-stu-id="e004e-253">**Validation conditions:** The GUID is used to match the DM PlugIn Dll GUID.</span></span> <span data-ttu-id="e004e-254">Il y a un maximum de 100 000 sous-éléments personnalisés.</span><span class="sxs-lookup"><span data-stu-id="e004e-254">There are a maximum of 100,000 custom sub-elements.</span></span>

### <a name="rgbvirtualmeasurementtype"></a><span data-ttu-id="e004e-255">RGBVirtualMeasurementType</span><span class="sxs-lookup"><span data-stu-id="e004e-255">RGBVirtualMeasurementType</span></span>

<span data-ttu-id="e004e-256">Cet élément est une séquence composée de</span><span class="sxs-lookup"><span data-stu-id="e004e-256">This element is a sequence consisting of</span></span>

1.  <span data-ttu-id="e004e-257">Groupe RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="e004e-257">RGBPrimariesGroup group</span></span>
2.  <span data-ttu-id="e004e-258">Choix de</span><span class="sxs-lookup"><span data-stu-id="e004e-258">A choice of</span></span>
3.  -   <span data-ttu-id="e004e-259">Gamma</span><span class="sxs-lookup"><span data-stu-id="e004e-259">Gamma</span></span>
    -   <span data-ttu-id="e004e-260">GammaOffsetGain</span><span class="sxs-lookup"><span data-stu-id="e004e-260">GammaOffsetGain</span></span>
    -   <span data-ttu-id="e004e-261">GammaOffsetGainLinearGam</span><span class="sxs-lookup"><span data-stu-id="e004e-261">GammaOffsetGainLinearGam</span></span>
    -   <span data-ttu-id="e004e-262">Éléments ToneResponseCurves</span><span class="sxs-lookup"><span data-stu-id="e004e-262">ToneResponseCurves elements</span></span>

4.  <span data-ttu-id="e004e-263">GamutBoundarySamples facultatif GamutBoundarySamplesType</span><span class="sxs-lookup"><span data-stu-id="e004e-263">optional GamutBoundarySamples GamutBoundarySamplesType</span></span>
5.  <span data-ttu-id="e004e-264">Date/heure TimeStamp</span><span class="sxs-lookup"><span data-stu-id="e004e-264">TimeStamp dateTime</span></span>

<span data-ttu-id="e004e-265">**Conditions de validation :** Chaque sous-élément de ces types a ses propres conditions de validation.</span><span class="sxs-lookup"><span data-stu-id="e004e-265">**Validation conditions:** Each sub-element of these types has its own validation conditions.</span></span>

### <a name="gammatype"></a><span data-ttu-id="e004e-266">GammaType</span><span class="sxs-lookup"><span data-stu-id="e004e-266">GammaType</span></span>

<span data-ttu-id="e004e-267">Cet élément est un type complexe constitué de l’attribut</span><span class="sxs-lookup"><span data-stu-id="e004e-267">This element is a complex type consisting of the attribute</span></span>

-   <span data-ttu-id="e004e-268">NonNegativeFloatType gamma</span><span class="sxs-lookup"><span data-stu-id="e004e-268">Gamma NonNegativeFloatType</span></span>

<span data-ttu-id="e004e-269">**Conditions de validation :** À déterminer à partir des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-269">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gammaoffsetgaintype"></a><span data-ttu-id="e004e-270">GammaOffsetGainType</span><span class="sxs-lookup"><span data-stu-id="e004e-270">GammaOffsetGainType</span></span>

<span data-ttu-id="e004e-271">Cet élément est un type complexe constitué des attributs</span><span class="sxs-lookup"><span data-stu-id="e004e-271">This element is a complex type consisting of the attributes</span></span>

-   <span data-ttu-id="e004e-272">NonNegativeFloatType gamma</span><span class="sxs-lookup"><span data-stu-id="e004e-272">Gamma NonNegativeFloatType</span></span>
-   <span data-ttu-id="e004e-273">Décalage NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="e004e-273">Offset NonNegativeFloatType</span></span>
-   <span data-ttu-id="e004e-274">Obtenir NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="e004e-274">Gain NonNegativeFloatType</span></span>

<span data-ttu-id="e004e-275">**Conditions de validation :** À déterminer à partir des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-275">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gammaoffsetgainlineargaintype"></a><span data-ttu-id="e004e-276">GammaOffsetGainLinearGainType</span><span class="sxs-lookup"><span data-stu-id="e004e-276">GammaOffsetGainLinearGainType</span></span>

<span data-ttu-id="e004e-277">Cet élément est un type complexe constitué des attributs</span><span class="sxs-lookup"><span data-stu-id="e004e-277">This element is a complex type consisting of the attributes</span></span>

-   <span data-ttu-id="e004e-278">NonNegativeFloatType gamma</span><span class="sxs-lookup"><span data-stu-id="e004e-278">Gamma NonNegativeFloatType</span></span>
-   <span data-ttu-id="e004e-279">Décalage NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="e004e-279">Offset NonNegativeFloatType</span></span>
-   <span data-ttu-id="e004e-280">Obtenir NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="e004e-280">Gain NonNegativeFloatType</span></span>
-   <span data-ttu-id="e004e-281">LinearGain NonNegativeFloatType</span><span class="sxs-lookup"><span data-stu-id="e004e-281">LinearGain NonNegativeFloatType</span></span>
-   <span data-ttu-id="e004e-282">TransitionPoint NonNegativeFloatType.</span><span class="sxs-lookup"><span data-stu-id="e004e-282">TransitionPoint NonNegativeFloatType.</span></span>

<span data-ttu-id="e004e-283">**Conditions de validation :** À déterminer à partir des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-283">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="toneresponsecurvestype"></a><span data-ttu-id="e004e-284">ToneResponseCurvesType</span><span class="sxs-lookup"><span data-stu-id="e004e-284">ToneResponseCurvesType</span></span>

<span data-ttu-id="e004e-285">Cet élément est une séquence de</span><span class="sxs-lookup"><span data-stu-id="e004e-285">This element is a sequence of</span></span>

1.  <span data-ttu-id="e004e-286">RedTRC FloatPairList</span><span class="sxs-lookup"><span data-stu-id="e004e-286">RedTRC FloatPairList</span></span>
2.  <span data-ttu-id="e004e-287">GreenTRC FloatPairList</span><span class="sxs-lookup"><span data-stu-id="e004e-287">GreenTRC FloatPairList</span></span>
3.  <span data-ttu-id="e004e-288">BlueTRC FloatPairList</span><span class="sxs-lookup"><span data-stu-id="e004e-288">BlueTRC FloatPairList</span></span>

<span data-ttu-id="e004e-289">L’élément a également un attribut TRCLength de type unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e004e-289">The element also has an attribute TRCLength of unsignedint type.</span></span>

<span data-ttu-id="e004e-290">**Conditions de validation :** À déterminer à partir des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-290">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="gamutboundarysamplestype"></a><span data-ttu-id="e004e-291">GamutBoundarySamplesType</span><span class="sxs-lookup"><span data-stu-id="e004e-291">GamutBoundarySamplesType</span></span>

<span data-ttu-id="e004e-292">Cet élément est une séquence de RGBTypes RVB.</span><span class="sxs-lookup"><span data-stu-id="e004e-292">This element is a sequence of RGB RGBTypes.</span></span>

<span data-ttu-id="e004e-293">**Conditions de validation :** Les occurrences maximales non liées sont actuellement limitées en fonction des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-293">**Validation conditions:** Currently unbounded maximum occurences, to be capped based on industry feedback.</span></span>

### <a name="floatpairlist"></a><span data-ttu-id="e004e-294">FloatPairList</span><span class="sxs-lookup"><span data-stu-id="e004e-294">FloatPairList</span></span>

<span data-ttu-id="e004e-295">Cet élément est un type simple de liste de paires de valeurs float.</span><span class="sxs-lookup"><span data-stu-id="e004e-295">This element is a simple type of list of pairs of floats.</span></span>

<span data-ttu-id="e004e-296">**Conditions de validation :** À déterminer à partir des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-296">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="cmykprintermeasurementtype"></a><span data-ttu-id="e004e-297">CMYKPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="e004e-297">CMYKPrinterMeasurementType</span></span>

<span data-ttu-id="e004e-298">Cet élément est un</span><span class="sxs-lookup"><span data-stu-id="e004e-298">This element is a</span></span>

1. <span data-ttu-id="e004e-299">séquence de l’élément ColorCube constitué d’une séquence d’exemples de NonNegativeCMYKSampleType</span><span class="sxs-lookup"><span data-stu-id="e004e-299">sequence of ColorCube element consisting of a sequence of Sample NonNegativeCMYKSampleType</span></span>

2. <span data-ttu-id="e004e-300">Attribut dateTime TimeStamp.</span><span class="sxs-lookup"><span data-stu-id="e004e-300">TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="e004e-301">**Conditions de validation :** À déterminer à partir des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-301">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbprintermeasurementtype"></a><span data-ttu-id="e004e-302">RGBPrinterMeasurementType</span><span class="sxs-lookup"><span data-stu-id="e004e-302">RGBPrinterMeasurementType</span></span>

<span data-ttu-id="e004e-303">Cet élément est un</span><span class="sxs-lookup"><span data-stu-id="e004e-303">This element is a</span></span>

1. <span data-ttu-id="e004e-304">séquence de l’élément ColorCube constitué d’une séquence d’exemples de NonNegativeRGBSampleType</span><span class="sxs-lookup"><span data-stu-id="e004e-304">sequence of ColorCube element consisting of a sequence of Sample NonNegativeRGBSampleType</span></span>

2. <span data-ttu-id="e004e-305">Attribut dateTime TimeStamp.</span><span class="sxs-lookup"><span data-stu-id="e004e-305">TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="e004e-306">**Conditions de validation :** À déterminer à partir des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-306">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbcapturemeasurementtype"></a><span data-ttu-id="e004e-307">RGBCaptureMeasurementType</span><span class="sxs-lookup"><span data-stu-id="e004e-307">RGBCaptureMeasurementType</span></span>

<span data-ttu-id="e004e-308">Cet élément est une séquence de</span><span class="sxs-lookup"><span data-stu-id="e004e-308">This element is a sequence of</span></span>

1.  <span data-ttu-id="e004e-309">ComplexType PrimaryIndex de</span><span class="sxs-lookup"><span data-stu-id="e004e-309">PrimaryIndex complexType of</span></span>
2.  1.  <span data-ttu-id="e004e-310">OneBasedIndex blanc</span><span class="sxs-lookup"><span data-stu-id="e004e-310">White OneBasedIndex</span></span>
    2.  <span data-ttu-id="e004e-311">OneBasedIndex noir facultatif</span><span class="sxs-lookup"><span data-stu-id="e004e-311">Optional Black OneBasedIndex</span></span>
    3.  <span data-ttu-id="e004e-312">OneBasedIndex rouge facultatif</span><span class="sxs-lookup"><span data-stu-id="e004e-312">Optional Red OneBasedIndex</span></span>
    4.  <span data-ttu-id="e004e-313">OneBasedIndex vert facultatif</span><span class="sxs-lookup"><span data-stu-id="e004e-313">Optional Green OneBasedIndex</span></span>
    5.  <span data-ttu-id="e004e-314">OneBasedIndex bleu facultatif</span><span class="sxs-lookup"><span data-stu-id="e004e-314">Optional Blue OneBasedIndex</span></span>
    6.  <span data-ttu-id="e004e-315">OneBasedIndex cyan facultatif</span><span class="sxs-lookup"><span data-stu-id="e004e-315">Optional Cyan OneBasedIndex</span></span>
    7.  <span data-ttu-id="e004e-316">OneBasedIndex magenta facultatif</span><span class="sxs-lookup"><span data-stu-id="e004e-316">Optional Magenta OneBasedIndex</span></span>
    8.  <span data-ttu-id="e004e-317">OneBasedIndex jaune facultatif</span><span class="sxs-lookup"><span data-stu-id="e004e-317">Optional Yellow OneBasedIndex</span></span>

3.  <span data-ttu-id="e004e-318">NeutralIndices de lignes de OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="e004e-318">NeutralIndices of lines of OneBasedIndex</span></span>
4.  <span data-ttu-id="e004e-319">Séquence ColorSamples de l’exemple de NonNegativeRGBSampleType</span><span class="sxs-lookup"><span data-stu-id="e004e-319">ColorSamples sequence of Sample NonNegativeRGBSampleType</span></span>

<span data-ttu-id="e004e-320">L’élément a également un attribut dateTime TimeStamp.</span><span class="sxs-lookup"><span data-stu-id="e004e-320">The element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="e004e-321">**Conditions de validation :** À déterminer à partir des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-321">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="onebasedindex"></a><span data-ttu-id="e004e-322">OneBasedIndex</span><span class="sxs-lookup"><span data-stu-id="e004e-322">OneBasedIndex</span></span>

<span data-ttu-id="e004e-323">Cet élément est un type simple de base de restriction unsigned int avec la valeur minInclusive = "1."</span><span class="sxs-lookup"><span data-stu-id="e004e-323">This element is a simple type of restriction base unsigned int with minInclusive value = "1."</span></span>

<span data-ttu-id="e004e-324">**Conditions de validation :** À déterminer à partir des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-324">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="rgbprojectormeasurementtype"></a><span data-ttu-id="e004e-325">RGBProjectorMeasurementType</span><span class="sxs-lookup"><span data-stu-id="e004e-325">RGBProjectorMeasurementType</span></span>

<span data-ttu-id="e004e-326">Cet élément est une séquence de</span><span class="sxs-lookup"><span data-stu-id="e004e-326">This element is a sequence of</span></span>

1.  <span data-ttu-id="e004e-327">Groupe RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="e004e-327">RGBPrimariesGroup group</span></span>
2.  <span data-ttu-id="e004e-328">élément ColorSamples constitué d’une séquence d’exemples de NonNegativeRGBSampleType</span><span class="sxs-lookup"><span data-stu-id="e004e-328">element ColorSamples consisting of sequence of Sample NonNegativeRGBSampleType</span></span>

<span data-ttu-id="e004e-329">L’élément a également un attribut dateTime TimeStamp.</span><span class="sxs-lookup"><span data-stu-id="e004e-329">The element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="e004e-330">**Conditions de validation :** À déterminer à partir des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-330">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="displaymeasurementtype"></a><span data-ttu-id="e004e-331">DisplayMeasurementType</span><span class="sxs-lookup"><span data-stu-id="e004e-331">DisplayMeasurementType</span></span>

<span data-ttu-id="e004e-332">Cet élément est une séquence de</span><span class="sxs-lookup"><span data-stu-id="e004e-332">This element is a sequence of</span></span>

1.  <span data-ttu-id="e004e-333">RGBPrimariesGroup de groupe</span><span class="sxs-lookup"><span data-stu-id="e004e-333">group RGBPrimariesGroup</span></span>
2.  <span data-ttu-id="e004e-334">GrayRamp de la séquence de l’exemple de NonNegativeRGBType</span><span class="sxs-lookup"><span data-stu-id="e004e-334">GrayRamp of sequence of Sample NonNegativeRGBType</span></span>
3.  <span data-ttu-id="e004e-335">RedRamp de la séquence de l’exemple de NonNegativeRGBType</span><span class="sxs-lookup"><span data-stu-id="e004e-335">RedRamp of sequence of Sample NonNegativeRGBType</span></span>
4.  <span data-ttu-id="e004e-336">GreenRamp de la séquence de l’exemple de NonNegativeRGBType</span><span class="sxs-lookup"><span data-stu-id="e004e-336">GreenRamp of sequence of Sample NonNegativeRGBType</span></span>
5.  <span data-ttu-id="e004e-337">BlueRamp de la séquence de l’exemple de NonNegativeRGBType</span><span class="sxs-lookup"><span data-stu-id="e004e-337">BlueRamp of sequence of Sample NonNegativeRGBType</span></span>

<span data-ttu-id="e004e-338">L’élément DisplayMeasurementType a également un attribut dateTime TimeStamp.</span><span class="sxs-lookup"><span data-stu-id="e004e-338">The DisplayMeasurementType element also has a TimeStamp dateTime attribute.</span></span>

<span data-ttu-id="e004e-339">**Conditions de validation :** À déterminer à partir des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-339">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="measurementconditionstype"></a><span data-ttu-id="e004e-340">MeasurementConditionsType</span><span class="sxs-lookup"><span data-stu-id="e004e-340">MeasurementConditionsType</span></span>

<span data-ttu-id="e004e-341">Le MeasurementConditionsType est une séquence de sous-éléments qui contient :</span><span class="sxs-lookup"><span data-stu-id="e004e-341">The MeasurementConditionsType is a sequence of sub-elements that contains:</span></span>

1.  <span data-ttu-id="e004e-342">Valeur d’énumération de chaîne restreinte ColorSpace « CIEXYZ »</span><span class="sxs-lookup"><span data-stu-id="e004e-342">ColorSpace restricted string enumeration value of "CIEXYZ"</span></span>
2.  <span data-ttu-id="e004e-343">choix facultatif de l’énumération de chaînes WhitePoint NonNegativeXYZType ou WhitePointName de valeurs D50, D65, A ou F2</span><span class="sxs-lookup"><span data-stu-id="e004e-343">optional choice of WhitePoint NonNegativeXYZType or WhitePointName string enumeration of values D50, D65, A, or F2</span></span>
3.  <span data-ttu-id="e004e-344">GeometryType Geometry</span><span class="sxs-lookup"><span data-stu-id="e004e-344">Geometry GeometryType</span></span>
4.  <span data-ttu-id="e004e-345">Entier ApertureSize en millimètres</span><span class="sxs-lookup"><span data-stu-id="e004e-345">ApertureSize integer in millimeters</span></span>

<span data-ttu-id="e004e-346">Valeurs par défaut :</span><span class="sxs-lookup"><span data-stu-id="e004e-346">Defaults are:</span></span>

1.  <span data-ttu-id="e004e-347">Imprimantes RVB et CMJN :</span><span class="sxs-lookup"><span data-stu-id="e004e-347">RGB and CMYK Printers:</span></span>
    1.  <span data-ttu-id="e004e-348">CIEXYZ MeasurementSpaceType</span><span class="sxs-lookup"><span data-stu-id="e004e-348">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="e004e-349">WhitePointValue D50</span><span class="sxs-lookup"><span data-stu-id="e004e-349">D50 WhitePointValue</span></span>
    3.  <span data-ttu-id="e004e-350">0/45 GeometryType</span><span class="sxs-lookup"><span data-stu-id="e004e-350">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="e004e-351">10mm ApertureSize</span><span class="sxs-lookup"><span data-stu-id="e004e-351">10mm ApertureSize</span></span>
2.  <span data-ttu-id="e004e-352">Scanneurs</span><span class="sxs-lookup"><span data-stu-id="e004e-352">Scanners:</span></span>
    1.  <span data-ttu-id="e004e-353">CIEXYZ MeasurementSpaceType</span><span class="sxs-lookup"><span data-stu-id="e004e-353">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="e004e-354">WhitePointValue D50</span><span class="sxs-lookup"><span data-stu-id="e004e-354">D50 WhitePointValue</span></span>
    3.  <span data-ttu-id="e004e-355">0/45 GeometryType</span><span class="sxs-lookup"><span data-stu-id="e004e-355">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="e004e-356">10mm ApertureSize</span><span class="sxs-lookup"><span data-stu-id="e004e-356">10mm ApertureSize</span></span>
3.  <span data-ttu-id="e004e-357">Affiche et appareil virtuel RGB :</span><span class="sxs-lookup"><span data-stu-id="e004e-357">Displays and RGB Virtual Device:</span></span>
    1.  <span data-ttu-id="e004e-358">CIEXYZ MeasurementSpaceType</span><span class="sxs-lookup"><span data-stu-id="e004e-358">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="e004e-359">D65 WhitePointValue</span><span class="sxs-lookup"><span data-stu-id="e004e-359">D65 WhitePointValue</span></span>
    3.  <span data-ttu-id="e004e-360">0/45 GeometryType</span><span class="sxs-lookup"><span data-stu-id="e004e-360">0/45 GeometryType</span></span>
    4.  <span data-ttu-id="e004e-361">10mm ApertureSize</span><span class="sxs-lookup"><span data-stu-id="e004e-361">10mm ApertureSize</span></span>
4.  <span data-ttu-id="e004e-362">Appareil</span><span class="sxs-lookup"><span data-stu-id="e004e-362">Cameras:</span></span>
    1.  <span data-ttu-id="e004e-363">CIEXYZ MeasurementSpaceType</span><span class="sxs-lookup"><span data-stu-id="e004e-363">CIEXYZ MeasurementSpaceType</span></span>
    2.  <span data-ttu-id="e004e-364">D65 WhitePointValue</span><span class="sxs-lookup"><span data-stu-id="e004e-364">D65 WhitePointValue</span></span>
    3.  <span data-ttu-id="e004e-365">GeometryType directe</span><span class="sxs-lookup"><span data-stu-id="e004e-365">Direct GeometryType</span></span>
    4.  <span data-ttu-id="e004e-366">10mm ApertureSize</span><span class="sxs-lookup"><span data-stu-id="e004e-366">10mm ApertureSize</span></span>

<span data-ttu-id="e004e-367">**Conditions de validation :** La validation de chaque sous-élément est déterminée par les conditions de validation pour ces sous-éléments.</span><span class="sxs-lookup"><span data-stu-id="e004e-367">**Validation conditions:** Validation of each sub-element is determined by validation conditions for those sub-elements.</span></span> <span data-ttu-id="e004e-368">Si un sous-élément est manquant, le type de modèle d’appareil spécifique par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e004e-368">If any sub-element is missing, the device model type specific default is used.</span></span>

### <a name="geometrytype"></a><span data-ttu-id="e004e-369">GeometryType</span><span class="sxs-lookup"><span data-stu-id="e004e-369">GeometryType</span></span>

<span data-ttu-id="e004e-370">String</span><span class="sxs-lookup"><span data-stu-id="e004e-370">String</span></span>

<span data-ttu-id="e004e-371">Valeurs d’énumération :</span><span class="sxs-lookup"><span data-stu-id="e004e-371">Enumeration values:</span></span>

-   <span data-ttu-id="e004e-372">« 0/45 »</span><span class="sxs-lookup"><span data-stu-id="e004e-372">"0/45"</span></span>
-   <span data-ttu-id="e004e-373">« 0/diffus »</span><span class="sxs-lookup"><span data-stu-id="e004e-373">"0/diffuse"</span></span>
-   <span data-ttu-id="e004e-374">« diffuse/0 »</span><span class="sxs-lookup"><span data-stu-id="e004e-374">"diffuse/0"</span></span>
-   <span data-ttu-id="e004e-375">Directe</span><span class="sxs-lookup"><span data-stu-id="e004e-375">"Direct"</span></span>

<span data-ttu-id="e004e-376">**Conditions de validation :** Toute valeur, à l’exception des valeurs enumberation listées, n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e004e-376">**Validation conditions:** Any value except the enumberation values listed is invalid.</span></span> <span data-ttu-id="e004e-377">Ces informations ne modifient pas le comportement de traitement de la ligne de base.</span><span class="sxs-lookup"><span data-stu-id="e004e-377">This information will not change baseline processing behavior.</span></span>

### <a name="rgbprimariesgroup"></a><span data-ttu-id="e004e-378">RGBPrimariesGroup</span><span class="sxs-lookup"><span data-stu-id="e004e-378">RGBPrimariesGroup</span></span>

<span data-ttu-id="e004e-379">Cet élément est une séquence de</span><span class="sxs-lookup"><span data-stu-id="e004e-379">This element is a sequence of</span></span>

1.  <span data-ttu-id="e004e-380">WhitePrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="e004e-380">WhitePrimary NonNegativeXYZType</span></span>
2.  <span data-ttu-id="e004e-381">RedPrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="e004e-381">RedPrimary NonNegativeXYZType</span></span>
3.  <span data-ttu-id="e004e-382">GreenPrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="e004e-382">GreenPrimary NonNegativeXYZType</span></span>
4.  <span data-ttu-id="e004e-383">BluePrimary NonNegativeXYZTYpe</span><span class="sxs-lookup"><span data-stu-id="e004e-383">BluePrimary NonNegativeXYZTYpe</span></span>
5.  <span data-ttu-id="e004e-384">BlackPrimary NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="e004e-384">BlackPrimary NonNegativeXYZType</span></span>

<span data-ttu-id="e004e-385">**Conditions de validation :** À déterminer à partir des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-385">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativecmyksampletype"></a><span data-ttu-id="e004e-386">NonNegativeCMYKSampleType</span><span class="sxs-lookup"><span data-stu-id="e004e-386">NonNegativeCMYKSampleType</span></span>

<span data-ttu-id="e004e-387">Cet élément est une séquence de</span><span class="sxs-lookup"><span data-stu-id="e004e-387">This element is a sequence of</span></span>

1.  <span data-ttu-id="e004e-388">NonNegativeCMYKType CMJN</span><span class="sxs-lookup"><span data-stu-id="e004e-388">CMYK NonNegativeCMYKType</span></span>
2.  <span data-ttu-id="e004e-389">CIEXYZ NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="e004e-389">CIEXYZ NonNegativeXYZType</span></span>

<span data-ttu-id="e004e-390">L’élément a également une chaîne d’étiquette d’attribut facultative</span><span class="sxs-lookup"><span data-stu-id="e004e-390">The element also has an optional attribute Tag string</span></span>

<span data-ttu-id="e004e-391">**Conditions de validation :** À déterminer à partir des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-391">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativergbsampletype"></a><span data-ttu-id="e004e-392">NonNegativeRGBSampleType</span><span class="sxs-lookup"><span data-stu-id="e004e-392">NonNegativeRGBSampleType</span></span>

<span data-ttu-id="e004e-393">Cet élément est une séquence de</span><span class="sxs-lookup"><span data-stu-id="e004e-393">This element is a sequence of</span></span>

1.  <span data-ttu-id="e004e-394">NonNegativeRGBType RVB</span><span class="sxs-lookup"><span data-stu-id="e004e-394">RGB NonNegativeRGBType</span></span>
2.  <span data-ttu-id="e004e-395">CIEXYZ NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="e004e-395">CIEXYZ NonNegativeXYZType</span></span>

<span data-ttu-id="e004e-396">L’élément a également une chaîne d’étiquette d’attribut facultative</span><span class="sxs-lookup"><span data-stu-id="e004e-396">The element also has an optional attribute Tag string</span></span>

<span data-ttu-id="e004e-397">**Conditions de validation :** À déterminer à partir des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-397">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativecmyktype"></a><span data-ttu-id="e004e-398">NonNegativeCMYKType</span><span class="sxs-lookup"><span data-stu-id="e004e-398">NonNegativeCMYKType</span></span>

<span data-ttu-id="e004e-399">Cet élément se compose d’attributs</span><span class="sxs-lookup"><span data-stu-id="e004e-399">This element consisting of attributes</span></span>

1.  <span data-ttu-id="e004e-400">Virgule flottante C</span><span class="sxs-lookup"><span data-stu-id="e004e-400">C float</span></span>
2.  <span data-ttu-id="e004e-401">Virgule flottante</span><span class="sxs-lookup"><span data-stu-id="e004e-401">M float</span></span>
3.  <span data-ttu-id="e004e-402">Virgule flottante Y</span><span class="sxs-lookup"><span data-stu-id="e004e-402">Y float</span></span>
4.  <span data-ttu-id="e004e-403">Virgule flottante</span><span class="sxs-lookup"><span data-stu-id="e004e-403">K float</span></span>

<span data-ttu-id="e004e-404">**Conditions de validation :** À déterminer à partir des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-404">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="nonnegativergbtype"></a><span data-ttu-id="e004e-405">NonNegativeRGBType</span><span class="sxs-lookup"><span data-stu-id="e004e-405">NonNegativeRGBType</span></span>

<span data-ttu-id="e004e-406">Cet élément se compose d’attributs</span><span class="sxs-lookup"><span data-stu-id="e004e-406">This element consisting of attributes</span></span>

1.  <span data-ttu-id="e004e-407">Valeur float R</span><span class="sxs-lookup"><span data-stu-id="e004e-407">R float</span></span>
2.  <span data-ttu-id="e004e-408">Virgule flottante G</span><span class="sxs-lookup"><span data-stu-id="e004e-408">G float</span></span>
3.  <span data-ttu-id="e004e-409">Virgule flottante B</span><span class="sxs-lookup"><span data-stu-id="e004e-409">B float</span></span>

<span data-ttu-id="e004e-410">**Conditions de validation :** À déterminer à partir des commentaires du secteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-410">**Validation conditions:** To be determined from industry feedback.</span></span>

### <a name="extensiontype"></a><span data-ttu-id="e004e-411">ExtensionType</span><span class="sxs-lookup"><span data-stu-id="e004e-411">ExtensionType</span></span>

<span data-ttu-id="e004e-412">L’élément ExtensionType est une séquence de tout type de sous-élément et est utilisé pour les informations propriétaires d’applications non-Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e004e-412">The ExtensionType element is a sequence of any sub-element type and is used for proprietary information from non-Microsoft applications.</span></span>

<span data-ttu-id="e004e-413">**Conditions de validation :** Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="e004e-413">**Validation conditions:** This element is optional.</span></span> <span data-ttu-id="e004e-414">Il peut y avoir un maximum de 1000 sous-éléments d’extension.</span><span class="sxs-lookup"><span data-stu-id="e004e-414">There can be a maximum of 1000 extension sub-elements.</span></span>

### <a name="nonnegativexyztype"></a><span data-ttu-id="e004e-415">NonNegativeXYZType</span><span class="sxs-lookup"><span data-stu-id="e004e-415">NonNegativeXYZType</span></span>

<span data-ttu-id="e004e-416">L’élément NonNegativeXYZType est composé de NonNegativeFloatType trois éléments à virgule flottante IEEE simple précision nommés « X », « Y » et « Z ».</span><span class="sxs-lookup"><span data-stu-id="e004e-416">The NonNegativeXYZType element is composed of NonNegativeFloatType three single-precision IEEE floating-point elements named "X," "Y," and "Z."</span></span> <span data-ttu-id="e004e-417">Ces valeurs sont limitées aux valeurs de mesure des profils DMP.</span><span class="sxs-lookup"><span data-stu-id="e004e-417">These values are limited to the DMP profiles measurement values.</span></span> <span data-ttu-id="e004e-418">Ces mesures peuvent être absolues (non relatives) CIEXYZ 1931 valeurs réfléchissantes ou valeurs réfléchies absolues (non relatives) CIEXYZ 1931 (transmissif) dans candelas par unités au carré du compteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-418">These measurements can be either absolute (not relative) CIEXYZ 1931 reflective values or absolute (not relative) CIEXYZ 1931 direct (transmissive) values in candelas per meter squared units.</span></span>

<span data-ttu-id="e004e-419">**Conditions de validation :** Seules les valeurs réelles sont valides, et les valeurs de mesure CIEXYZ négatives ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e004e-419">**Validation conditions:** Only real-world values are valid, and negative CIEXYZ measurement values are invalid.</span></span> <span data-ttu-id="e004e-420">Comme il s’agit de valeurs absolues, les valeurs peuvent être supérieures à 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="e004e-420">Because these are absolute values, values can be greater than 1.0f.</span></span> <span data-ttu-id="e004e-421">Limite raisonnable pour n’importe quel « X », « Y » ou « Z ».</span><span class="sxs-lookup"><span data-stu-id="e004e-421">A reasonable limit for any "X," "Y," or "Z."</span></span> <span data-ttu-id="e004e-422">la valeur est arbitrairement définie sur 10000.0 f.</span><span class="sxs-lookup"><span data-stu-id="e004e-422">value is arbitrarily set to 10000.0f.</span></span>

### <a name="xyztype"></a><span data-ttu-id="e004e-423">XYZType</span><span class="sxs-lookup"><span data-stu-id="e004e-423">XYZType</span></span>

<span data-ttu-id="e004e-424">L’élément XYZType est composé de trois valeurs à virgule flottante IEEE simple précision : « X », « Y » et « Z ».</span><span class="sxs-lookup"><span data-stu-id="e004e-424">The XYZType element is composed of three single-precision IEEE floating-point values: "X," "Y," and "Z."</span></span>

## <a name="the-cdmp-baseline-algorithms"></a><span data-ttu-id="e004e-425">Algorithmes de base CDMP</span><span class="sxs-lookup"><span data-stu-id="e004e-425">The CDMP Baseline Algorithms</span></span>

### <a name="crt-device-model-baseline"></a><span data-ttu-id="e004e-426">Ligne de base du modèle de périphérique CRT</span><span class="sxs-lookup"><span data-stu-id="e004e-426">CRT Device Model Baseline</span></span>

<span data-ttu-id="e004e-427">Pour comprendre ce modèle, vous devez prendre en compte le processus de caractérisation et la modélisation de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e004e-427">To understand this model, you must consider both the characterization process and the device modeling.</span></span> <span data-ttu-id="e004e-428">Dans le processus de caractérisation, les mesures XYZ sont d’abord effectuées sur les couleurs obtenues en remplissant la mémoire tampon d’affichage d’un périphérique d’affichage CRT.</span><span class="sxs-lookup"><span data-stu-id="e004e-428">In the characterization process, XYZ measurements are first performed on the colors obtained by filling the display buffer of a CRT display device.</span></span> <span data-ttu-id="e004e-429">Les exemples de valeurs suivants génèrent des données correctes pour le modèle d’appareil CRT de base de référence :</span><span class="sxs-lookup"><span data-stu-id="e004e-429">The following example values will generate good data for the baseline CRT device model:</span></span>

<span data-ttu-id="e004e-430">Rouge : R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span><span class="sxs-lookup"><span data-stu-id="e004e-430">Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span></span>

<span data-ttu-id="e004e-431">Vert : G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span><span class="sxs-lookup"><span data-stu-id="e004e-431">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span></span>

<span data-ttu-id="e004e-432">Blue : B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span><span class="sxs-lookup"><span data-stu-id="e004e-432">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span></span>

<span data-ttu-id="e004e-433">Neutres : R = G = B = 0, 8, 16, 32, 64, 128, 192, 255</span><span class="sxs-lookup"><span data-stu-id="e004e-433">Neutrals: R = G= B = 0, 8, 16, 32, 64, 128, 192, 255</span></span>

<span data-ttu-id="e004e-434">Vous pouvez également utiliser des incréments autres que 15 et des incréments non linéaires.</span><span class="sxs-lookup"><span data-stu-id="e004e-434">Increments other than 15 and nonlinear increments can also be used.</span></span> <span data-ttu-id="e004e-435">Chaque rampe rouge, verte, bleue et neutre doit contenir au moins trois échantillons, mais il est recommandé de fournir un plus grand nombre d’échantillons.</span><span class="sxs-lookup"><span data-stu-id="e004e-435">Each red, green, blue, and neutral ramp must contain at least three samples, but providing more samples is recommended.</span></span> <span data-ttu-id="e004e-436">Vous devez fournir des échantillons pour le rouge pur, le vert, le bleu, le noir et le blanc.</span><span class="sxs-lookup"><span data-stu-id="e004e-436">You must provide samples for pure red, green, blue, black, and white.</span></span> <span data-ttu-id="e004e-437">Il n’est pas nécessaire que les exemples soient uniformément espacés.</span><span class="sxs-lookup"><span data-stu-id="e004e-437">The samples do not have to be uniformly spaced.</span></span>

<span data-ttu-id="e004e-438">Le processus de création de la matrice tristimulus se compose de deux étapes.</span><span class="sxs-lookup"><span data-stu-id="e004e-438">The process of building the tristimulus matrix consists of two steps.</span></span> <span data-ttu-id="e004e-439">Tout d’abord, évaluez la valeur du point noir XYZ ou le halo.</span><span class="sxs-lookup"><span data-stu-id="e004e-439">First, estimate the black point XYZ value, or the flare.</span></span> <span data-ttu-id="e004e-440">Cette étape est principalement basée sur le travail de Bernes \[ 3 \] avec une fonction d’objectif légèrement modifiée pour l’optimisation non linéaire.</span><span class="sxs-lookup"><span data-stu-id="e004e-440">This step is based largely on work of Berns\[3\] with a slightly modified objective function for the nonlinear optimization.</span></span> <span data-ttu-id="e004e-441">Ensuite, calculez la matrice tristimulus en fonction du résultat de l’étape 1 et également d’un calcul de la moyenne sur toutes les mesures par canal, pas seulement celle du nombre maximal d’unités numériques.</span><span class="sxs-lookup"><span data-stu-id="e004e-441">Second, calculate tristimulus matrix based on the result from step one and also from an averaging calculation on all of the per-channel measurements, not just the one for maximum digital count.</span></span>

<span data-ttu-id="e004e-442">Chacune de ces étapes contient des procédures détaillées.</span><span class="sxs-lookup"><span data-stu-id="e004e-442">Each of these steps contains detailed procedures.</span></span> <span data-ttu-id="e004e-443">Le point de départ correspond aux rampes (17 étapes dans notre exemple) pour chacun des canaux R, G et B.</span><span class="sxs-lookup"><span data-stu-id="e004e-443">The starting point is the ramps (17 steps in our example) for each of R, G, and B channels.</span></span> <span data-ttu-id="e004e-444">Lorsque les mesures XYZ sont tracées sur le plan *XY* chromatique, une situation typique est illustrée à la figure 1.</span><span class="sxs-lookup"><span data-stu-id="e004e-444">When the XYZ measurements are plotted on the chromaticity *xy* -plane, a typical situation is shown in Figure 1.</span></span> <span data-ttu-id="e004e-445">La première étape consiste à résoudre un problème d’optimisation non linéaire afin de trouver le point noir le mieux adapté qui réduira la valeur de la chromatique en traversant les canaux R, G et B.</span><span class="sxs-lookup"><span data-stu-id="e004e-445">Step one consists of solving a nonlinear optimization problem to find the "best fit" black point that will minimize the drift in chromaticity as one traverses along the R, G, and B channels.</span></span> <span data-ttu-id="e004e-446">En se basant sur les Bernes \[ 3 \] , nous cherchons ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>k</sub>* ) qui minimise la fonction d’objectif suivante :</span><span class="sxs-lookup"><span data-stu-id="e004e-446">Based on Berns\[3\], we seek ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z<sub>K</sub>* ) that minimizes the following objective function:</span></span>

![Affiche la fonction objective où SR, SG et SB sont l’ensemble de points de données sur les canaux R, G et B.](images/cdmp-formula1.png)

<span data-ttu-id="e004e-448">où *s <sub>R</sub>*,*s <sub>G</sub>* et *s <sub>B</sub>* sont l’ensemble de points de données correspondant aux points sur les canaux R, G et b.</span><span class="sxs-lookup"><span data-stu-id="e004e-448">where *S <sub>R</sub>*,*S <sub>G</sub>*, and *S<sub>B</sub>* are the set of data points corresponding to the points on the R, G, and B channels.</span></span> <span data-ttu-id="e004e-449">Pour tous les *ensembles, définissez :*</span><span class="sxs-lookup"><span data-stu-id="e004e-449">For any set *S*, define:</span></span>

![Affiche une formule pour la définition de n’importe quel jeu de.](images/cdmp-formula2.png)

<span data-ttu-id="e004e-451">Dans le précédent, \| *s* \| est la cardinalité de *s*, c.-à-d., le nombre de points dans le jeu *S*. ![ Affiche une formule pour la chromatique d’un point.](images/cdmp-formula3.png)</span><span class="sxs-lookup"><span data-stu-id="e004e-451">In the preceding, \| *S* \| is the cardinality of *S*, i.e., the number of points in the set *S*. ![Shows a formula for the chromaticity of a point.](images/cdmp-formula3.png)</span></span> <span data-ttu-id="e004e-452">les coordonnées chromatiques du point ![ montrent un formaula pour un point.](images/cdmp-formula4.png)</span><span class="sxs-lookup"><span data-stu-id="e004e-452">is the chromaticity coordinates of the point ![Shows a formaula for a point.](images/cdmp-formula4.png)</span></span> <span data-ttu-id="e004e-453">, ![ affiche donc une formule pour la moyenne ou le centre de masse. ](images/cdmp-formula5.png) , est la moyenne, ou le centre de la masse, de tous les points du jeu *S* dans le plan chromatique.</span><span class="sxs-lookup"><span data-stu-id="e004e-453">, so ![Shows a formula for the average or center of mass.](images/cdmp-formula5.png), is the average, or center of mass, of all the points in the set *S* in the chromaticity plane.</span></span> <span data-ttu-id="e004e-454">Par conséquent, ![ affiche une formule pour la somme d’un deuxième instant de points.](images/cdmp-formula6.png)</span><span class="sxs-lookup"><span data-stu-id="e004e-454">Thus, ![Shows a formula for the sum of a second moments of points.](images/cdmp-formula6.png)</span></span> <span data-ttu-id="e004e-455">somme des deuxièmes moments des points du centre de masse et mesure de la façon dont les points sont répartis.</span><span class="sxs-lookup"><span data-stu-id="e004e-455">is the sum of second moments of the points about the center of mass and is a measure of how spread out the points are about it.</span></span> <span data-ttu-id="e004e-456">Enfin, ![ affiche une formule pour la mesure totale de la répartition de trois clusters de points.](images/cdmp-formula7.png)</span><span class="sxs-lookup"><span data-stu-id="e004e-456">Finally, ![Shows a formula for the total measure of the spread of three clusters of points.](images/cdmp-formula7.png)</span></span> <span data-ttu-id="e004e-457">est une mesure totale de la répartition des trois clusters de points sur leurs centres respectifs de masse.</span><span class="sxs-lookup"><span data-stu-id="e004e-457">is a total measure of how spread out the three clusters of points are about their respective centers of mass.</span></span>

<span data-ttu-id="e004e-458">Dans, le calcul de ![ affiche une formule f (X, Y, Z ; XK, YK, ZK).](images/cdmp-formula8.png)</span><span class="sxs-lookup"><span data-stu-id="e004e-458">In the calculation of ![Shows a formula of f(X,Y,Z; Xk, Yk, Zk).](images/cdmp-formula8.png)</span></span> <span data-ttu-id="e004e-459">, si ![ affiche une formule pour X. ](images/cdmp-formula9.png) , le calcul est ignoré et la cardinalité des *S* est ajustée en conséquence.</span><span class="sxs-lookup"><span data-stu-id="e004e-459">, if ![Shows a formula for X.](images/cdmp-formula9.png) , then the calculation is skipped, and the cardinality of *S* is adjusted accordingly.</span></span>

<span data-ttu-id="e004e-460">En dépit de la complexité apparente de la fonction d’objectif, il s’agit d’une somme des carrés de nombreuses fonctions dérivables dans *X <sub>k</sub>*,*Y <sub>k</sub>Z <sub>k</sub>* (17 points 2 *XY* -Components 3 canaux = 102, dans l’exemple) et, par conséquent, est visible pour les techniques de moindres carrés non linéaires standard, telles que l’algorithme Levenberg-Marquardt, qui est l’algorithme</span><span class="sxs-lookup"><span data-stu-id="e004e-460">Despite the apparent complexity of the objective function, it is a sum of the squares of many differentiable functions in *X <sub>K</sub>*,*Y <sub>K</sub>Z <sub>K</sub>* (17 points   2 *xy* -components   3 channels = 102, in the example), and, therefore, is amenable to standard nonlinear least squares techniques, such as the Levenberg-Marquardt algorithm, which is the algorithm used in WCS.</span></span> <span data-ttu-id="e004e-461">Notez que la fonction objective précédente est différente de celle suggérée dans les Bernes \[ 3 \] en ce que cette dernière mesure la variance des distances par rapport au centre de masse, de sorte que la variance soit égale à zéro lorsque les points sont éloignés du centre de masse, même s’ils peuvent l’être.</span><span class="sxs-lookup"><span data-stu-id="e004e-461">Note that the preceding objective function is different from the one suggested in Berns\[3\] in that the latter function measures the variance of the distances from the center of mass, so that the variance is zero when the points are equidistant from the center of mass, even though they may spread out quite a bit about it.</span></span> <span data-ttu-id="e004e-462">Dans l’exemple, la dispersion des points est convertie directement à l’aide du deuxième instant.</span><span class="sxs-lookup"><span data-stu-id="e004e-462">In the example, the dispersion of points is contolled directly using the second moments.</span></span>

<span data-ttu-id="e004e-463">Comme avec n’importe quel algorithme itératif pour le problème des moindres carrés non linéaires, Levenberg-Marquardt nécessite une estimation initiale.</span><span class="sxs-lookup"><span data-stu-id="e004e-463">As with any iterative algorithm for the nonlinear least squares problem, Levenberg-Marquardt requires an initial guess.</span></span> <span data-ttu-id="e004e-464">Il existe deux candidats évidents.</span><span class="sxs-lookup"><span data-stu-id="e004e-464">There are two obvious candidates.</span></span> <span data-ttu-id="e004e-465">L’un est (0, 0, 0); l’autre est le point noir mesuré.</span><span class="sxs-lookup"><span data-stu-id="e004e-465">One is (0, 0, 0); the other is the measured black point.</span></span> <span data-ttu-id="e004e-466">Pour la CTE, le point noir mesuré est utilisé pour la première fois comme estimation initiale.</span><span class="sxs-lookup"><span data-stu-id="e004e-466">For the CTE, the measured black point is first used as the initial guess.</span></span> <span data-ttu-id="e004e-467">Si un maximum de 100 itérations est dépassé sans atteindre un seuil d’une distance moyenne de 0,001 de chaque point à partir de son centre de masse (qui correspond à une valeur de seuil de (0,001) 17 3 = 0,000051 pour la fonction d’objectif), un autre nombre d’itérations avec l’estimation initiale de (0, 0, 0) est effectué.</span><span class="sxs-lookup"><span data-stu-id="e004e-467">If a maximum of 100 iterations is exceeded without achieving a threshold of an average distance of 0.001 of each point from its center of mass (which corresponds to a threshold value of (0.001)    17   3 = 0.000051 for the objective function), then another round of iterations with the initial guess of (0, 0, 0) is performed.</span></span> <span data-ttu-id="e004e-468">L’estimation obtenue du point noir est XYZ comparée à la meilleure estimation de l’ancien cycle d’itérations (avec le point noir mesuré comme estimation initiale).</span><span class="sxs-lookup"><span data-stu-id="e004e-468">The resulting estimate of the black point is XYZ compared with the best estimate from the previous round of iterations (with the measured black point as the initial guess).</span></span> <span data-ttu-id="e004e-469">Utilisez l’estimation qui donne la plus petite valeur pour la fonction objective.</span><span class="sxs-lookup"><span data-stu-id="e004e-469">Use the estimate that gives the smallest value for the objective function.</span></span> <span data-ttu-id="e004e-470">Le choix entre 100 itérations et la distance d’erreur 0,001 ont été sélectionnés de façon empirique.</span><span class="sxs-lookup"><span data-stu-id="e004e-470">The choice of 100 iterations and the error distance of 0.001 were each selected empirically.</span></span> <span data-ttu-id="e004e-471">Dans les versions ultérieures, il peut être raisonnable de paramétrer la distance d’erreur.</span><span class="sxs-lookup"><span data-stu-id="e004e-471">In future versions, it might be reasonable to parameterize the error distance.</span></span>

<span data-ttu-id="e004e-472">Le résultat de l’étape 1 est le point noir estimé ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>k</sub>* ).</span><span class="sxs-lookup"><span data-stu-id="e004e-472">The result of step one is the estimated black point ( *X <sub>K</sub>*,*Y <sub>K</sub>*,*Z<sub>K</sub>* ).</span></span> <span data-ttu-id="e004e-473">L’étape 2 consiste à déterminer la matrice tristimulus en calculant la moyenne de la chromatique des points dans les trois clusters obtenus à l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="e004e-473">Step two consists of determining the tristimulus matrix by averaging the chromaticity of the points in the three clusters obtained in step one.</span></span> <span data-ttu-id="e004e-474">Pour les CRT, cette opération est effectuée principalement pour réduire les effets des erreurs de mesure.</span><span class="sxs-lookup"><span data-stu-id="e004e-474">For CRTs, this is done primarily to minimize the effects of measurement errors.</span></span> <span data-ttu-id="e004e-475">Les points utilisés dans la moyenne de la chromatique doivent être les mêmes que ceux utilisés dans l’optimisation de l’étape 1.</span><span class="sxs-lookup"><span data-stu-id="e004e-475">The points used in averaging the chromaticity must be the same points used in the optimization in step one.</span></span> <span data-ttu-id="e004e-476">En d’autres termes, si le premier point (nombre numérique 15, dans l’exemple) dans chaque rampe est ignoré lors de l’étape d’optimisation, vous devez le faire dans le calcul de la moyenne.</span><span class="sxs-lookup"><span data-stu-id="e004e-476">In other words, if the first point (digital count 15, in the example) in each ramp is discarded in the optimization step, then the same must be done in the averaging.</span></span> <span data-ttu-id="e004e-477">Si ![ affiche des formules de la chromatique moyenne pour les coordonnées des canaux rouge et vert.](images/cdmp-formula10.png)</span><span class="sxs-lookup"><span data-stu-id="e004e-477">If ![Shows formulas of averaged chromaticity for coordinates in the red and green channels.](images/cdmp-formula10.png)</span></span> <span data-ttu-id="e004e-478">, et ![ affiche une formule de la chromatique moyenne des coordonnées dans le canal bleu.](images/cdmp-formula11.png)</span><span class="sxs-lookup"><span data-stu-id="e004e-478">, and ![Shows a formula of averaged chromaticity for coordinates in the blue channel.](images/cdmp-formula11.png)</span></span> <span data-ttu-id="e004e-479">sont les coordonnées chromatiques moyennes des canaux rouge, vert et bleu, puis la procédure suivante détermine la matrice tristimulus.</span><span class="sxs-lookup"><span data-stu-id="e004e-479">are the averaged chromaticity coordinates of the red, green, and blue channels, then the following procedure determines the tristimulus matrix.</span></span> <span data-ttu-id="e004e-480">Tout d’abord, résolvez le système linéaire 3 ? 3 :</span><span class="sxs-lookup"><span data-stu-id="e004e-480">First, solve the 3?3 linear system:</span></span>

![Affiche la première partie de la procédure permettant de résoudre un système linéaire 3 ? 3.](images/cdmp-formula12.png)

![Affiche la deuxième partie du système linéaire 3 ? 3.](images/cdmp-formula13.gif)![Affichez la valeur t indice b à la fin de la deuxième partie du système linéaire 3 ? 3.](images/cdmp-formula14.gif)

<span data-ttu-id="e004e-484">*X <sub>w</sub>*,*Y <sub>w</sub>*,*Z <sub>w</sub>*</span><span class="sxs-lookup"><span data-stu-id="e004e-484">*X <sub>W</sub>*,*Y <sub>W</sub>*,*Z<sub>W</sub>*</span></span>

![Affiche la dernière partie de la procédure permettant de résoudre un système linéaire 3 ? 3.](images/cdmp-formula15.png)

<span data-ttu-id="e004e-486">Une fois la matrice tristimulus déterminée, la détermination des courbes de tonalité suit l’approche standard.</span><span class="sxs-lookup"><span data-stu-id="e004e-486">After the tristimulus matrix is determined, the determination of tone curves follows the standard approach.</span></span> <span data-ttu-id="e004e-487">Pour les affichages CRT, les canaux individuels sont supposés suivre le modèle « GOG » :</span><span class="sxs-lookup"><span data-stu-id="e004e-487">For CRT displays, the individual channels are assumed to follow the "GOG" model:</span></span>

![Affiche la formule pour le modèle « G O G ».](images/cdmp-formula16.png)

<span data-ttu-id="e004e-489">où *k <sub>g</sub>* est le « gain », 1-*k <sub>g</sub>* est le « décalage », et ?</span><span class="sxs-lookup"><span data-stu-id="e004e-489">where *k <sub>g</sub>* is the "gain",1 -*k<sub>g</sub>* is the "offset", and ?</span></span> <span data-ttu-id="e004e-490">est le « gamma ».</span><span class="sxs-lookup"><span data-stu-id="e004e-490">is the "gamma."</span></span> <span data-ttu-id="e004e-491">La matrice inverse de la matrice tristimulus est appliquée aux données XYZ des neutres pour obtenir les données RVB linéaires, qui sont ensuite corrélées avec les valeurs RVB numériques à l’aide de la régression linéaire sur le modèle GOG.</span><span class="sxs-lookup"><span data-stu-id="e004e-491">The inverse matrix of the tristimulus matrix is applied to the XYZ data of the neutrals to obtain the linear RGB data, which is then correlated with the digital RGB values using nonlinear regression on the GOG model.</span></span> <span data-ttu-id="e004e-492">Ces caractéristiques n’ont pas besoin d’être identiques pour les canaux R, G et B, et ne sont généralement pas identiques.</span><span class="sxs-lookup"><span data-stu-id="e004e-492">These characteristics do not have to be the same for the R, G, and B channels, and generally are not the same.</span></span>

<span data-ttu-id="e004e-493">Bernes \[ 1 \] : Bernes, *Billmeyer et Saltzman, principes de la technologie des couleurs*, 3 <sub>rd</sub> Ed.</span><span class="sxs-lookup"><span data-stu-id="e004e-493">Berns\[1\]: Berns, *Billmeyer and Saltzman's Principles of Color Technology*, 3 <sub>rd</sub> Ed.</span></span> <span data-ttu-id="e004e-494">John Wiley & fils (2000).</span><span class="sxs-lookup"><span data-stu-id="e004e-494">John Wiley & Sons (2000).</span></span>

<span data-ttu-id="e004e-495">Bernes \[ 2 \] : Bernes et Katoh, la fonction de transfert numérique à radiométrique pour les affichages CRT contrôlés par ordinateur, le *Congrès d’experts Cie 97 normes de couleur pour la technologie d’imagerie, du* 1997 novembre.</span><span class="sxs-lookup"><span data-stu-id="e004e-495">Berns\[2\]: Berns and Katoh, The digital to radiometric transfer function for computer controlled CRT displays, *CIE Expert Symposium '97 Colour Standards for Imaging Technology*, Nov. 1997.</span></span>

<span data-ttu-id="e004e-496">Bernes \[ 3 \] : Bernes, Fernandez et Taplin, estimation Black-Level émissions de Computer-Controlled des affichages, *recherche en couleurs et application*, 28:379-383 Wiley periods, Inc. (2003)</span><span class="sxs-lookup"><span data-stu-id="e004e-496">Berns\[3\]: Berns, Fernandez and Taplin, Estimating Black-Level Emissions of Computer-Controlled Displays, *Color Research and Application*, 28: 379-383 Wiley Periodicals, Inc. (2003)</span></span>

<span data-ttu-id="e004e-497">Kang \[ 1 \] : Kang, *technologie de couleur pour les appareils de création d’images électroniques*, SPIE (1997)</span><span class="sxs-lookup"><span data-stu-id="e004e-497">Kang\[1\]: Kang, *Color Technology for Electronic Imaging Devices*, SPIE (1997)</span></span>

<span data-ttu-id="e004e-498">Katoh \[ 1 \] : Katoh, Deguchi et Bernes, caractérisation exacte de la proposition du moniteur CRT (II) pour une extension de la méthode Cie et de sa vérification, *opt. Rev.* 8:397-408 (2001)</span><span class="sxs-lookup"><span data-stu-id="e004e-498">Katoh\[1\]: Katoh, Deguchi and Berns, An accurate characterization of CRT monitor (II) proposal for an extension to CIE method and its verification, *Opt. Rev.* 8: 397-408 (2001)</span></span>

### <a name="lcd-device-model-baseline"></a><span data-ttu-id="e004e-499">Ligne de base du modèle d’appareil LCD</span><span class="sxs-lookup"><span data-stu-id="e004e-499">LCD Device Model Baseline</span></span>

<span data-ttu-id="e004e-500">La ligne de base du modèle d’appareil LCD est semblable à la ligne de base du modèle de périphérique CRT.</span><span class="sxs-lookup"><span data-stu-id="e004e-500">The LCD Device Model Baseline is similar to the CRT Device Model Baseline.</span></span> <span data-ttu-id="e004e-501">Cette section explique les différentes façons dont la modélisation LCD diffère de la modélisation CRT.</span><span class="sxs-lookup"><span data-stu-id="e004e-501">This section will explain the ways in which LCD modeling differs from CRT modeling.</span></span>

<span data-ttu-id="e004e-502">L’une des différences est que vous ne pouvez pas supposer que les écrans LCD suivent le modèle GOG utilisé pour les CRT, et les courbes de ton sont obtenues par interpolation de données mesurées.</span><span class="sxs-lookup"><span data-stu-id="e004e-502">One difference is that you cannot assume that LCD displays follow the GOG model used for CRTs, and the tone curves are obtained by interpolation of measured data.</span></span> <span data-ttu-id="e004e-503">Pour cette raison, l’axe neutre de l’appareil doit être échantillonné plus fréquemment.</span><span class="sxs-lookup"><span data-stu-id="e004e-503">Because of that, the device neutral axis should be sampled more frequently.</span></span>

<span data-ttu-id="e004e-504">Voici quelques exemples de valeurs typiques qui peuvent générer de bonnes données pour la ligne de base du modèle d’appareil LCD :</span><span class="sxs-lookup"><span data-stu-id="e004e-504">Here are some typical example values that can generate good data for the LCD device model baseline:</span></span>

<span data-ttu-id="e004e-505">Rouge : R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span><span class="sxs-lookup"><span data-stu-id="e004e-505">Red: R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0</span></span>

<span data-ttu-id="e004e-506">Vert : G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span><span class="sxs-lookup"><span data-stu-id="e004e-506">Green: G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0</span></span>

<span data-ttu-id="e004e-507">Blue : B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span><span class="sxs-lookup"><span data-stu-id="e004e-507">Blue: B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0</span></span>

<span data-ttu-id="e004e-508">Neutres : R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.</span><span class="sxs-lookup"><span data-stu-id="e004e-508">Neutrals: R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.</span></span>

<span data-ttu-id="e004e-509">Le processus de calcul de la moyenne des chromatiques de couleur mesurées pour obtenir les chromatiques des principaux de l’appareil est plus important pour les écrans LCD que pour les écrans CRT.</span><span class="sxs-lookup"><span data-stu-id="e004e-509">The process of averaging measured color chromaticies to obtain the chromaticities for the device primaries is more critical for LCDs than it is for CRTs.</span></span> <span data-ttu-id="e004e-510">Quand la mesure XYZ est tracée sur le plan *XY* chromatique, une situation classique est illustrée à la figure 1.</span><span class="sxs-lookup"><span data-stu-id="e004e-510">When XYZ measurements are plotted on the chromaticity *xy* -plane, a typical situation is shown in Figure 1.</span></span> <span data-ttu-id="e004e-511">Notez que la chromatique est dérive vers le point noir.</span><span class="sxs-lookup"><span data-stu-id="e004e-511">Notice how the chromaticity drifts toward the black point.</span></span> <span data-ttu-id="e004e-512">Cela est dû au fait que tous les écrans LCD présentent une certaine perte de lumière.</span><span class="sxs-lookup"><span data-stu-id="e004e-512">This is because all LCDs have a certain amount of light leakage.</span></span>

![Diagramme qui affiche un graphique de la chromatique à l’aide de données brutes sans correction.](images/cdmp-lcd-dmp-figure1.png)

<span data-ttu-id="e004e-514">**Figure 1** : diagramme de la chromatique utilisant des données brutes sans correction</span><span class="sxs-lookup"><span data-stu-id="e004e-514">**Figure 1** : The chromaticity diagram using raw data with no correction</span></span>

<span data-ttu-id="e004e-515">Lorsque cela est soustrait des mesures XYZ brutes, une situation classique est représentée à la figure 2.</span><span class="sxs-lookup"><span data-stu-id="e004e-515">When this is subtracted from the raw XYZ measurements, a typical situation is depicted in Figure 2.</span></span> <span data-ttu-id="e004e-516">Les points sont maintenant mis en cluster sur trois centres, même s’ils ne sont pas identiques.</span><span class="sxs-lookup"><span data-stu-id="e004e-516">Tthe points are now clustered about three centers, although they don't fall identically on them.</span></span> <span data-ttu-id="e004e-517">La méthode de calcul de la moyenne décrite pour les écrans CRT améliore considérablement les résultats des écrans LCD.</span><span class="sxs-lookup"><span data-stu-id="e004e-517">The averaging process described for CRTs greatly improves the results for LCDs.</span></span>

![Diagramme qui montre un graphique de la chromatique à l’aide de données brutes avec un point noir ajusté.](images/cdmp-lcd-dmp-figure2.png)

<span data-ttu-id="e004e-519">**Figure 2** : diagramme chromatique utilisant des données avec le point noir ajusté</span><span class="sxs-lookup"><span data-stu-id="e004e-519">**Figure 2** : The chromaticity diagram using data with adjusted black point</span></span>

### <a name="rgb-capture-device-model-baseline"></a><span data-ttu-id="e004e-520">Ligne de base du modèle d’appareil de capture RVB</span><span class="sxs-lookup"><span data-stu-id="e004e-520">RGB Capture Device Model Baseline</span></span>

<span data-ttu-id="e004e-521">Le modèle de périphérique de capture RVB de base est une sous-classe de la classe IDeviceModel.</span><span class="sxs-lookup"><span data-stu-id="e004e-521">The baseline RGB capture device model is a subclass of the IDeviceModel class.</span></span> <span data-ttu-id="e004e-522">Dans la caractérisation colorimétrique des appareils de capture des couleurs, tels que les scanneurs et les appareils photo numériques, l’approche suivante est utilisée.</span><span class="sxs-lookup"><span data-stu-id="e004e-522">In the colorimetric characterization of color capture devices, such as scanners and digital cameras, the following approach is used.</span></span> <span data-ttu-id="e004e-523">Une cible composée de correctifs de couleurs avec des valeurs CIEXYZ connues est capturée à l’aide de l’appareil de capture.</span><span class="sxs-lookup"><span data-stu-id="e004e-523">A target consisting of color patches with known CIEXYZ values is captured using the capture device.</span></span> <span data-ttu-id="e004e-524">Le résultat de la capture est une image bitmap RVB dans laquelle la couleur de chaque correctif est encodée dans une valeur RVB.</span><span class="sxs-lookup"><span data-stu-id="e004e-524">The result of the capture is an RGB bitmap image in which the color of each patch is encoded in an RGB value.</span></span> <span data-ttu-id="e004e-525">Ces valeurs RVB d’appareil sont spécifiques à un périphérique de capture particulier.</span><span class="sxs-lookup"><span data-stu-id="e004e-525">These device RGB values are specific to a particular capture device.</span></span> <span data-ttu-id="e004e-526">L’objectif de la caractérisation colorimétrique est d’établir une relation empirique entre les valeurs RGB des appareils et les valeurs CIEXYZ, ou une transformation mathématique de RVB à XYZ, qui modélise aussi précisément que possible le comportement de l’appareil de capture.</span><span class="sxs-lookup"><span data-stu-id="e004e-526">The goal of colorimetric characterization is to establish an empirical relationship between the device RGB values and CIEXYZ values, or a mathematical transformation from RGB to XYZ that models as accurately as possible the behavior of the capture device.</span></span>

<span data-ttu-id="e004e-527">Une telle transformation mathématique peut être modélisée raisonnablement par des polynomes de faible degré.</span><span class="sxs-lookup"><span data-stu-id="e004e-527">Such a mathematical transformation can be modeled reasonably by polynomials of low degrees.</span></span> <span data-ttu-id="e004e-528">Cette procédure est détaillée dans la documentation, par exemple Kang \[ 92 \] , Kang \[ 97 \] .</span><span class="sxs-lookup"><span data-stu-id="e004e-528">This procedure is detailed in the literature, for example Kang\[92\], Kang\[97\].</span></span> <span data-ttu-id="e004e-529">Dans Kang \[ 97 \] , une approche est signalée qui utilise un ensemble de trois polynômes avec 3, 6, 8, 9, 11, 14 ou 20 termes dans les variables R, G et B, tandis que les trois Polynomials régresient respectivement dans les composants X, Y et Z de l’espace CIEXYZ.</span><span class="sxs-lookup"><span data-stu-id="e004e-529">In Kang\[97\], an approach is reported that uses a set of three polynomials with 3, 6, 8, 9, 11, 14 or 20 terms in the R, G, and B variables, while the three polynomials regress respectively into the X, Y, Z components of the CIEXYZ space.</span></span> <span data-ttu-id="e004e-530">Pour le polynôme à 20 termes, le formulaire est le suivant :</span><span class="sxs-lookup"><span data-stu-id="e004e-530">For the 20-term polynomial, the form is:</span></span>

![Affiche le polynôme à 20 termes.](images/cdmp-formula20.png)

<span data-ttu-id="e004e-532">Il existe des expressions similaires pour Y et Z. La technique mathématique pour l’ajustement des polynômes se trouve dans la « régression linéaire multivariable » et est décrite dans tout texte élémentaire dans les statistiques.</span><span class="sxs-lookup"><span data-stu-id="e004e-532">There are similar expressions for Y and Z. The mathematical technique for fitting the polynomials falls within "Multivariate Linear Regression" and is described in any elementary text in Statistics.</span></span>

<span data-ttu-id="e004e-533">Cette méthode de régression linéaire souffre de ne pas réduire la fonction d’objectif « Right ».</span><span class="sxs-lookup"><span data-stu-id="e004e-533">This method of linear regression suffers from not minimizing the "right" objective function.</span></span> <span data-ttu-id="e004e-534">Par défaut, la régression linéaire recherche la solution la moins carrée, ce qui implique que les coefficients obtenus réduisent la somme totale des carrés des erreurs dans l’espace sous-jacent, ou équivalente à la somme des carrés des distances euclidienne.</span><span class="sxs-lookup"><span data-stu-id="e004e-534">By design, linear regression finds the least squares solution, which implies that the coefficients obtained will minimize the total sum of squares of errors in the underlying space, or equivalently, the sum of squares of the Euclidean distances.</span></span> <span data-ttu-id="e004e-535">Dans la pratique, vous souhaitez réduire la somme des carrés de ? Es, où ? E est l’une des normes acceptées comme CIE94.</span><span class="sxs-lookup"><span data-stu-id="e004e-535">In practice, you want to minimize the sum of squares of ?Es, where ?E is one of the accepted standards such as CIE94.</span></span> <span data-ttu-id="e004e-536">La réduction de cette fonction d’objectif est un problème de régression non linéaire.</span><span class="sxs-lookup"><span data-stu-id="e004e-536">Minimizing this objective function is a nonlinear regression problem.</span></span>

<span data-ttu-id="e004e-537">Dans le nouveau moteur, le laboratoire à XYZ est l’espace de couleurs CIE qui est régressé dans et le polynôme à 20 termes, le polynôme cubique, est utilisé comme modèle pour l’appareil de capture, ou coefficients ls, par exemple BS, de telle sorte que les polynômes suivantes réduisent la somme des carrés de ? E <sub>CIE94</sub> s.</span><span class="sxs-lookup"><span data-stu-id="e004e-537">In the new engine, Lab to XYZ is the CIE color space that is regressed into, and the 20-term cubic polynomial is used as the model for the capture device, or coefficients ls,as,bs such that the following polynomials minimize the sum of squares of ?E <sub>CIE94</sub> s.</span></span>

![Affiche un ensemble de formules polynomiaux.](images/cdmp-formula21.png)

<span data-ttu-id="e004e-539">La solution ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) dans l’espace de chiffre réel 60 dimensionnel **R** 203 doit être telle que l’erreur totale suivante est réduite :</span><span class="sxs-lookup"><span data-stu-id="e004e-539">The solution ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) in the 60-dimensional real numeric space **R** 203 must be such that the following total error is minimized:</span></span>

![Affiche l’erreur totale à réduire.](images/cdmp-formula22.png)

<span data-ttu-id="e004e-541">où la somme se fait via toutes les paires de points de données (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* ) dans le jeu de données échantillonnées plus des points de contrôle supplémentaires à prendre en détail dans les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="e004e-541">where the summation is through all the data point pairs (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub>i</sub>*,*v<sub>i</sub>* ) in the sampled data set plus additional control points to be detailed in the following.</span></span> <span data-ttu-id="e004e-542">Il s’agit d’un problème de régression non linéaire, car les paramètres *?<sub> Je</sub>*, *a <sub></sub>* i, \* <sub>i</sub>\* Enter dans la fonction objective de manière non linéaire (pas augmentera).</span><span class="sxs-lookup"><span data-stu-id="e004e-542">This is a nonlinear regression problem because the parameters *?<sub>i</sub>*, *a<sub>i</sub>*, \* <sub>i</sub>\* enter into the objective function in a nonlinear way (not quadratically).</span></span>

<span data-ttu-id="e004e-543">En raison de la fonction objective ?</span><span class="sxs-lookup"><span data-stu-id="e004e-543">Because the objective function ?</span></span> <span data-ttu-id="e004e-544">la fonction est-elle linéaire (et non quadratique) des paramètres *?<sub> Je</sub>*, *a <sub>i</sub>* et \* <sub>i</sub>\*, vous devez recourir à des techniques itératives pour résoudre le problème d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="e004e-544">is a nonlinear (and nonquadratic) function of the parameters *?<sub>i</sub>*, *a<sub>i</sub>* and \* <sub>i</sub>\*, you must resort to iterative techniques to solve the optimization problem.</span></span> <span data-ttu-id="e004e-545">Comme la forme de la fonction objective est une somme des carrés, une technique d’optimisation standard appelée algorithme Levenberg-Marquardt est utilisée.</span><span class="sxs-lookup"><span data-stu-id="e004e-545">Because the form of the objective function is a sum of squares, a standard optimization technique called the Levenberg-Marquardt algorithm is used.</span></span> <span data-ttu-id="e004e-546">Il est considéré comme la méthode de choix pour les problèmes de moindres carrés non linéaires.</span><span class="sxs-lookup"><span data-stu-id="e004e-546">It is considered the method of choice for nonlinear least squares problems.</span></span> <span data-ttu-id="e004e-547">Pour les algorithmes itératifs tels que Levenberg-Marquardt, vous devez fournir une estimation initiale.</span><span class="sxs-lookup"><span data-stu-id="e004e-547">For iterative algorithms such as Levenberg-Marquardt, you must supply an initial guess.</span></span> <span data-ttu-id="e004e-548">Une bonne hypothèse initiale est généralement essentielle pour trouver la valeur minimale correcte.</span><span class="sxs-lookup"><span data-stu-id="e004e-548">A good initial guess is usually critical in finding the correct minimum value.</span></span> <span data-ttu-id="e004e-549">Dans ce cas, un bon candidat pour l’estimation initiale est la solution du problème de régression linéaire.</span><span class="sxs-lookup"><span data-stu-id="e004e-549">In this case, one good candidate for the initial guess is the solution of the linear regression problem.</span></span> <span data-ttu-id="e004e-550">Tout d’abord, réduisez la somme du carré des distances euclidienne dans l’espace de laboratoire en définissant une fonction d’objectif quadratique :</span><span class="sxs-lookup"><span data-stu-id="e004e-550">First, minimize the sum of the square of Euclidean distances in Lab space, by defining a quadratic objective function:</span></span>

![Affiche une fonction d’objectif quadratique définie.](images/cdmp-formula23.png)

<span data-ttu-id="e004e-552">La solution mathématique de ce type de problème est bien connue.</span><span class="sxs-lookup"><span data-stu-id="e004e-552">The mathematical solution to such "linear least squares" problem is well known.</span></span> <span data-ttu-id="e004e-553">Car *?<sub> Je</sub>* n’apparais qu’dans  la modélisation L *,<sub>je</sub>* n’apparaît que dans la modélisation *u* et \* <sub>i</sub>\* uniquement dans la modélisation *v* . le problème d’optimisation peut être décomposé en trois sous-problèmes : un pour *L*, un pour *u* et un pour *v*.</span><span class="sxs-lookup"><span data-stu-id="e004e-553">Because *?<sub>i</sub>* only appears in the *L* modeling, *a <sub>i</sub>* only appears in the *u* modeling, and \* <sub>i</sub>\* only appears in the *v* modeling; the optimization problem can be decomposed into three subproblems: one for *L*, one for *u* and one for *v*.</span></span> <span data-ttu-id="e004e-554">Examinez les équations *l* .</span><span class="sxs-lookup"><span data-stu-id="e004e-554">Consider the *L* equations.</span></span> <span data-ttu-id="e004e-555">(Les équations *u* et les équations *v* suivent exactement le même argument.) Le problème de la réduction de la somme des carrés des erreurs dans *L* peut être indiqué par la résolution de l’équation matricielle suivante dans le sens le moins évident :</span><span class="sxs-lookup"><span data-stu-id="e004e-555">(The *u* equations and the *v* equations follow exactly the same argument.) The problem of minimizing the sum of squares of errors in *L* can be stated as solving the following matrix equation in the least squares sense:</span></span>

![Affiche une équation de matrice pour L.](images/cdmp-formula24.png)

<span data-ttu-id="e004e-557">où *N* est le nombre total de points de données (points d’échantillonnage originaux et points de contrôle créés de la manière décrite ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="e004e-557">where *N* is the total number of data points (original sampled points plus control points created in a manner described below).</span></span> <span data-ttu-id="e004e-558">En règle générale, *N* est bien supérieur à 20, donc l’équation précédente est dépendante, ce qui nécessite une solution de moindres carrés.</span><span class="sxs-lookup"><span data-stu-id="e004e-558">Typically, *N* is much larger than 20, so the preceding equation is over-determined, requiring a least squares solution.</span></span> <span data-ttu-id="e004e-559">Une solution de formulaire fermée pour **?**</span><span class="sxs-lookup"><span data-stu-id="e004e-559">A closed form solution for **?**</span></span> <span data-ttu-id="e004e-560">est disponible :</span><span class="sxs-lookup"><span data-stu-id="e004e-560">is available:</span></span>

![Affiche une solution de formulaire fermée.](images/cdmp-formula25.png)

<span data-ttu-id="e004e-562">Dans la pratique, l’évaluation directe à l’aide de la solution de formulaire fermée n’est pas utilisée, car elle comporte des propriétés numériques médiocres.</span><span class="sxs-lookup"><span data-stu-id="e004e-562">In practice, direct evaluation using the closed form solution is not used because it has poor numerical properties.</span></span> <span data-ttu-id="e004e-563">Au lieu de cela, un certain type d’algorithme de factorisation de matrice est appliqué à la matrice de coefficient qui réduit le système d’équations à une forme canonique.</span><span class="sxs-lookup"><span data-stu-id="e004e-563">Instead, some kind of matrix factorization algorithm is applied to the coefficient matrix which reduces the system of equations to a canonical form.</span></span> <span data-ttu-id="e004e-564">Dans l’implémentation actuelle, la décomposition de la valeur singulière (MVP) est appliquée à la matrice **R** , puis le système décomposé résultant est résolu.</span><span class="sxs-lookup"><span data-stu-id="e004e-564">In the current implementation, Singular Value Decomposition (SVD) is applied to the matrix **R** and then the resulting decomposed system is solved.</span></span>

<span data-ttu-id="e004e-565">La solution au problème de régression linéaire, dénotée par ![ montre la solution au problème de régression linéaire.](images/cdmp-formula26.png)</span><span class="sxs-lookup"><span data-stu-id="e004e-565">The solution to the linear regression problem, denoted by ![Shows the solution to the linear regression problem.](images/cdmp-formula26.png)</span></span> <span data-ttu-id="e004e-566">, est utilisé comme point de départ de l’algorithme Levenberg-Marquardt.</span><span class="sxs-lookup"><span data-stu-id="e004e-566">, is used as the starting point of the Levenberg-Marquardt algorithm.</span></span> <span data-ttu-id="e004e-567">Dans cet algorithme, une étape d’essai est calculée et doit déplacer le point plus près de la solution optimale.</span><span class="sxs-lookup"><span data-stu-id="e004e-567">In this algorithm, a trial step is computed that should move the point closer to the optimal solution.</span></span> <span data-ttu-id="e004e-568">L’étape d’essai remplit un ensemble d’équations linéaires dépendant de la valeur fonctionnelle et des valeurs des dérivés au point actuel.</span><span class="sxs-lookup"><span data-stu-id="e004e-568">The trial step satisfies a set of linear equations dependent on the functional value and values of the derivatives at the current point.</span></span> <span data-ttu-id="e004e-569">Pour cette raison, les dérivés de la fonction objective ?</span><span class="sxs-lookup"><span data-stu-id="e004e-569">For this reason, the derivatives of the objective function ?</span></span> <span data-ttu-id="e004e-570">en ce qui concerne les paramètres *?<sub></sub>j'* ai *besoin <sub></sub> <sub></sub> d’entrées* pour l’algorithme Levenberg-Marquardt.</span><span class="sxs-lookup"><span data-stu-id="e004e-570">with respect to the parameters *?<sub>i</sub>*, *a<sub>i</sub> <sub>i</sub>* are required inputs to the Levenberg-Marquardt algorithm.</span></span> <span data-ttu-id="e004e-571">Bien qu’il y ait 60 paramètres, il existe un raccourci qui vous permet de calculer beaucoup moins.</span><span class="sxs-lookup"><span data-stu-id="e004e-571">Although there are 60 parameters, there is a shortcut that allows you to compute a lot less.</span></span> <span data-ttu-id="e004e-572">Par la règle de chaîne de calcul,</span><span class="sxs-lookup"><span data-stu-id="e004e-572">By the Chain Rule of Calculus,</span></span>

![Affiche une équation qui autorise un raccourci à l’aide de la règle de chaîne de calcul.](images/cdmp-formula27.png)

<span data-ttu-id="e004e-574">où *j* = 1, 2,, 20, *L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* sont la valeur CIELAB du point d’échantillonnage *i* et *R <sub>IJ</sub>* est l’entrée (*i*,*j* ) Th de la matrice **R** définie ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="e004e-574">where *j* = 1, 2,  , 20, *L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* are the CIELAB value of the *i* th sample point, and *R <sub>ij</sub>* is the (*i*,*j* )th entry of the matrix **R** defined above.</span></span> <span data-ttu-id="e004e-575">Ainsi, au lieu de calculer les dérivés pour les paramètres 60, vous pouvez calculer les dérivés pour *L*, a et *b* à l’aide de *la* différenciation par progression numérique.</span><span class="sxs-lookup"><span data-stu-id="e004e-575">So instead of computing derivatives for 60 parameters, you can compute derivatives for *L*,*a*, and *b* using numerical forward differencing.</span></span>

<span data-ttu-id="e004e-576">Il est également nécessaire de configurer un critère d’arrêt pour les algorithmes itératifs.</span><span class="sxs-lookup"><span data-stu-id="e004e-576">It is also necessary to set up a stopping criterion for iterative algorithms.</span></span> <span data-ttu-id="e004e-577">Dans l’implémentation actuelle, les itérations sont terminées si le DECIE94 carré moyen est inférieur à 1, ou si le nombre d’itérations effectuées a dépassé 10.</span><span class="sxs-lookup"><span data-stu-id="e004e-577">In the current implementation, the iterations are terminated if the mean square DECIE94 is less than 1, or the number of iterations performed has exceeded 10.</span></span> <span data-ttu-id="e004e-578">Le nombre 10 provient de l’expérience pratique selon laquelle si les premières itérations ne réduisent pas de manière significative l’erreur, les itérations supplémentaires ne sont pas encore plus utiles que le déplacement du point de manière oscillatoire, c’est-à-dire que l’algorithme peut ne pas converger.</span><span class="sxs-lookup"><span data-stu-id="e004e-578">The number 10 comes from the practical experience that if the first few iterations do not reduce the error significantly, further iterations would not help much other than moving the point in an oscillatory manner, i.e., the algorithm may not converge.</span></span> <span data-ttu-id="e004e-579">Même dans le cas où l’algorithme divergent, nous pouvons nous assurer que le DECIE94 n’est pas pire que ce que nous avons commencé, c’est-à-dire avec les paramètres obtenus à partir de la régression linéaire.</span><span class="sxs-lookup"><span data-stu-id="e004e-579">Even in the case that the algorithm diverges, we can be sure that the DECIE94 is no worse than what we started, i.e. with the parameters obtained from linear regression.</span></span>

<span data-ttu-id="e004e-580">Même avec la méthode précédente de régression linéaire, il y a plusieurs problèmes avec le raccord.</span><span class="sxs-lookup"><span data-stu-id="e004e-580">Even with the preceding method of nonlinear regression, there are several problems with the fitting.</span></span> <span data-ttu-id="e004e-581">L’un des problèmes est que les polynômes ont tendance à dépasser ou à défaire au-delà des points de données.</span><span class="sxs-lookup"><span data-stu-id="e004e-581">One problem is that the polynomials tend to overshoot or undershoot beyond the data points.</span></span> <span data-ttu-id="e004e-582">Les maxima et minima locaux artificiels peuvent être introduits dans le processus de montage.</span><span class="sxs-lookup"><span data-stu-id="e004e-582">Artificial local maxima and minima may be introduced in the fitting process.</span></span> <span data-ttu-id="e004e-583">Cela peut être réduit en utilisant des polynômes de faible degré, ce qui est la raison pour laquelle vous ne devez pas utiliser une valeur supérieure à trois degrés.</span><span class="sxs-lookup"><span data-stu-id="e004e-583">This can be counteracted by using polynomials of low degree, which is the reason you should not use higher than three degrees.</span></span> <span data-ttu-id="e004e-584">Un aspect plus sérieux du dépassement ou du dépassement est que, même si un polynomial peut prendre une valeur réelle théoriquement, l’espace qu’il tente de modéliser a généralement des contraintes physiques et pratiques.</span><span class="sxs-lookup"><span data-stu-id="e004e-584">A more serious aspect of overshooting or undershooting is that, while a polynomial can take any real value theoretically, the space it tries to model typically has physical constraints and practical constraints.</span></span> <span data-ttu-id="e004e-585">CIEXYZ doit avoir toutes les valeurs X, Y, Z non négatives, qui sont des contraintes physiques.</span><span class="sxs-lookup"><span data-stu-id="e004e-585">CIEXYZ must have all of X, Y, Z non-negative, which is a physical constraint.</span></span> <span data-ttu-id="e004e-586">Dans la pratique, elles prennent uniquement des valeurs dans l’amplitude de centaines, pas de milliers ou plus.</span><span class="sxs-lookup"><span data-stu-id="e004e-586">In practice, they only take values in the magnitude of hundreds, not thousands or higher.</span></span> <span data-ttu-id="e004e-587">De même, CIELAB ou CIELUV a ses propres contraintes physiques et pratiques.</span><span class="sxs-lookup"><span data-stu-id="e004e-587">Similarly, CIELAB or CIELUV has its own physical and practical constraints.</span></span> <span data-ttu-id="e004e-588">Lorsque l’espace RVB est suffisamment rempli avec des points d’échantillonnage, le problème de dépassement ou de dépassement n’est pas grave.</span><span class="sxs-lookup"><span data-stu-id="e004e-588">When the RGB space is filled sufficiently with sample points, the problem of overshooting or undershooting is not serious.</span></span> <span data-ttu-id="e004e-589">Toutefois, les points RVB capturés à partir de l’appareil de capture ne remplissent généralement pas l’espace RVB uniformément.</span><span class="sxs-lookup"><span data-stu-id="e004e-589">However, the captured RGB points from the capture device do not usually fill up the RGB space uniformly.</span></span> <span data-ttu-id="e004e-590">Les points peuvent remplir uniquement les 80% du cube RGB, ou pire, ils peuvent résider dans un collecteur dimensionnel inférieur.</span><span class="sxs-lookup"><span data-stu-id="e004e-590">The points may fill up only inner the 80% of the RGB cube, or worse, they may reside in a lower dimensional manifold.</span></span> <span data-ttu-id="e004e-591">Dans ce cas, les polynômes régressés peuvent faire une mauvaise tâche pour extrapoler les valeurs au-delà des points de données, renvoyant parfois des prédictions irréalistes.</span><span class="sxs-lookup"><span data-stu-id="e004e-591">When this happens, the regressed polynomials may do a poor job at extrapolating the values beyond the data points, sometimes returning unrealistic predictions.</span></span> <span data-ttu-id="e004e-592">Vous souhaitez un modèle qui retourne toujours des valeurs raisonnablement réalistes.</span><span class="sxs-lookup"><span data-stu-id="e004e-592">You want a model that always returns reasonably realistic values.</span></span> <span data-ttu-id="e004e-593">Cela nécessite une méthode qui permet de contrôler efficacement le comportement de la limite des polynomes de régression en imposant des coûts supplémentaires à ceux qui se comportent de façon erratique près de la limite du cube RGB.</span><span class="sxs-lookup"><span data-stu-id="e004e-593">This requires a method that can effectively control the boundary behavior of regression polynomials by imposing additional cost to those polynomials that behave erratically near the boundary of the RGB cube.</span></span> <span data-ttu-id="e004e-594">Une mesure supplémentaire pour s’assurer que les polynômes renvoient toujours des valeurs réalistes est appliquée en découpant la sortie vers dans le locus spectral CIE.</span><span class="sxs-lookup"><span data-stu-id="e004e-594">A further measure to ensure that the polynomials always return realistic values is applied by clipping the output to within the CIE spectral locus.</span></span>

<span data-ttu-id="e004e-595">C’est à ce stade que la modélisation du scanneur et la modélisation de la caméra divergent les unes des autres.</span><span class="sxs-lookup"><span data-stu-id="e004e-595">It is at this point that the scanner modeling and camera modeling diverge from each other.</span></span> <span data-ttu-id="e004e-596">Le modèle d’appareil photo est supposé extrapoler aux régions situées au-delà des points échantillonnés, y compris les « surbrillances spéculaires », la même extrapolation n’est pas requise pour le modèle de scanneur.</span><span class="sxs-lookup"><span data-stu-id="e004e-596">The camera model is expected to extrapolate to regions beyond the sampled points including the "specular highlights," the same extrapolation is not required for the scanner model.</span></span> <span data-ttu-id="e004e-597">La cible du scanneur est supposée couvrir une caractérisation similaire aux documents imprimés à analyser.</span><span class="sxs-lookup"><span data-stu-id="e004e-597">The scanner target is expected to cover a characterization that is similar to the printed materials to be scanned.</span></span> <span data-ttu-id="e004e-598">Le modèle de scanneur doit toujours être robuste dans le sens où il ne doit pas retourner de valeurs inréalistes, mais l’extrapolation bien au-delà de la cible de caractérisation n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e004e-598">The scanner model is still required to be robust in the sense that it should not return unrealistic values, but extrapolation far beyond the characterization target is not required.</span></span> <span data-ttu-id="e004e-599">Pour garantir la robustesse, l-polynomial ci-dessus est coupé à 100, autrement dit, le modèle polynomial est forcé à ne pas extrapoler au-delà de « Dmin » de la cible du scanneur.</span><span class="sxs-lookup"><span data-stu-id="e004e-599">To ensure robustness, the L-polynomial above is clipped at 100, that is, the polynomial model is forced not to extrapolate beyond "Dmin" of the scanner target.</span></span>

<span data-ttu-id="e004e-600">Le modèle d’appareil photo est supposé extrapoler à des surbrillances spéculaires, de sorte que le découpage à 100 n’est pas souhaitable.</span><span class="sxs-lookup"><span data-stu-id="e004e-600">The camera model is expected to extrapolate to specular highlights, so clipping at 100 is undesirable.</span></span> <span data-ttu-id="e004e-601">À la place, l’algorithme suivant est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e004e-601">Instead, the following algorithm is used.</span></span>

<span data-ttu-id="e004e-602">Des points de contrôle artificiels sont introduits pour contrôler le comportement des polynômes dans les régions avec un échantillonnage insuffisant.</span><span class="sxs-lookup"><span data-stu-id="e004e-602">Artificial control points are introduced to control the behavior of the polynomials in regions with insufficient sampling.</span></span> <span data-ttu-id="e004e-603">En plaçant stratégiquement ces points de contrôle avec les valeurs appropriées, elles servent à « tirer » les polynômes dans le sens requis.</span><span class="sxs-lookup"><span data-stu-id="e004e-603">By strategically placing these control points with appropriate values, they serve to "pull" the polynomials in the required direction.</span></span> <span data-ttu-id="e004e-604">Dans l’implémentation actuelle, huit points de contrôle correspondant aux angles du cube RGB sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="e004e-604">In the current implementation, eight control points corresponding to the corners of the RGB cube are used.</span></span> <span data-ttu-id="e004e-605">Si les valeurs de l’appareil sont normalisées en Unity, les points suivants sont :</span><span class="sxs-lookup"><span data-stu-id="e004e-605">If the device values are normalized to unity, then these points are:</span></span>

<span data-ttu-id="e004e-606">*R* = 0, *G* = 0, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="e004e-606">*R* = 0, *G* = 0, *B* = 0</span></span>

<span data-ttu-id="e004e-607">*R* = 0, *G* = 0, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="e004e-607">*R* = 0, *G* = 0, *B* = 1</span></span>

<span data-ttu-id="e004e-608">*R* = 0, *G* = 1, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="e004e-608">*R* = 0, *G* = 1, *B* = 0</span></span>

<span data-ttu-id="e004e-609">*R* = 0.</span><span class="sxs-lookup"><span data-stu-id="e004e-609">*R* = 0.</span></span> <span data-ttu-id="e004e-610">*G* = 1, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="e004e-610">*G* = 1, *B* = 1</span></span>

<span data-ttu-id="e004e-611">*R* = 1, *G* = 0, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="e004e-611">*R* = 1, *G* = 0, *B* = 0</span></span>

<span data-ttu-id="e004e-612">*R* = 1, *G* = 0, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="e004e-612">*R* = 1, *G* = 0, *B* = 1</span></span>

<span data-ttu-id="e004e-613">*R* = 1, *G* = 1, *B* = 0</span><span class="sxs-lookup"><span data-stu-id="e004e-613">*R* = 1, *G* = 1, *B* = 0</span></span>

<span data-ttu-id="e004e-614">*R* = 1, *G* = 1, *B* = 1</span><span class="sxs-lookup"><span data-stu-id="e004e-614">*R* = 1, *G* = 1, *B* = 1</span></span>

<span data-ttu-id="e004e-615">À l’exception du *R*  = *G*  = *B* = 1, qui est associé à une valeur CIELAB de *L* = 100, *u*  = *v* = 0, l’algorithme d’extrapolation suivant est utilisé pour déterminer la valeur CIELAB appropriée à associer.</span><span class="sxs-lookup"><span data-stu-id="e004e-615">Except for the white *R* =*G* =*B* = 1, which is associated with a CIELAB value of *L* = 100, *u* =*v* = 0, the following extrapolation algorithm is used to determine the appropriate CIELAB value to be associated with.</span></span> <span data-ttu-id="e004e-616">En général, pour un donné (*r*,*g*,*b* ), un poids est associé à chacun des (*r <sub>i</sub>*,*g <sub>i</sub>*,*b <sub>i</sub>* ) dans le jeu de données échantillonné.</span><span class="sxs-lookup"><span data-stu-id="e004e-616">Generally, for a given (*R*,*G*,*B* ), a weight is associated with each of the (*R <sub>i</sub>*,*G <sub>i</sub>*,*B<sub>i</sub>* ) in the sampled data set.</span></span> <span data-ttu-id="e004e-617">Il y a deux objectifs pour assigner le poids.</span><span class="sxs-lookup"><span data-stu-id="e004e-617">There are two goals to assigning the weight.</span></span> <span data-ttu-id="e004e-618">Tout d’abord, le poids est inversement proportionnel à la distance entre (*r*,*g*,*b* ) et (*r <sub>i</sub>*,*g <sub>i</sub>*,*B <sub>i</sub>* ).</span><span class="sxs-lookup"><span data-stu-id="e004e-618">First, the weight is inversely proportional to the distance between (*R*,*G*,*B* ) and (*R <sub>i</sub>*,*G <sub>i</sub>*,*B<sub>i</sub>* ).</span></span> <span data-ttu-id="e004e-619">Ensuite, vous souhaitez ignorer ou affecter la pondération 0 aux points qui ont une teinte différente du point donné (*R*,*G*,*B* ).</span><span class="sxs-lookup"><span data-stu-id="e004e-619">Second, you want to discard, or assign weight 0 to, points that have a different hue than the given point (*R*,*G*,*B* ).</span></span> <span data-ttu-id="e004e-620">Pour prendre en compte la teinte, envisagez des points qui se trouvent dans un cône dont le vertex est à (0,0), dont l’axe coïncide avec la jonction de la ligne (0, 0, 0) à (*R*,*G*,*B* ) et dont l’angle est semi-vertical ?</span><span class="sxs-lookup"><span data-stu-id="e004e-620">To take the hue into account, consider points that lie within a cone whose vertex is at (0, 0, 0), whose axis coincides with the line joining (0, 0, 0) to (*R*,*G*,*B* ), and whose semi-vertical angle ?</span></span> <span data-ttu-id="e004e-621">est conforme à cos ?</span><span class="sxs-lookup"><span data-stu-id="e004e-621">satisfies cos ?</span></span> <span data-ttu-id="e004e-622">= 0,9.</span><span class="sxs-lookup"><span data-stu-id="e004e-622">= 0.9.</span></span> <span data-ttu-id="e004e-623">Voir la figure 3 pour une illustration de ce cône.</span><span class="sxs-lookup"><span data-stu-id="e004e-623">See Figure 3 for an illustration of this cone.</span></span>

![Diagramme qui affiche la forme du voisinage.](images/cdmp-lcd-dmp-figure3.png)

<span data-ttu-id="e004e-625">**Figure 3** : filtrage des points d’échantillonnage par angle et distance.</span><span class="sxs-lookup"><span data-stu-id="e004e-625">**Figure 3** : Filtering the sample points by angle and distance.</span></span> <span data-ttu-id="e004e-626">La forme du voisinage représenté est à titre d’illustration uniquement.</span><span class="sxs-lookup"><span data-stu-id="e004e-626">The shape of the neighborhood depicted is for illustration purpose only.</span></span> <span data-ttu-id="e004e-627">La forme réelle dépend de la distance utilisée ; Il s’agit d’un voisinage en forme de losange si la norme 1 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="e004e-627">The actual shape depends on the distance used; it is a diamond-shaped neighborhood if the 1-norm is used.</span></span>

<span data-ttu-id="e004e-628">Dans ce cône, un deuxième filtrage est effectué en fonction de la distance RVB, qui utilise la norme 1-normal, définie par</span><span class="sxs-lookup"><span data-stu-id="e004e-628">Within this cone, a second filtering is performed that is based on the RGB distance, which uses the 1-norm, defined by</span></span>

![Affiche la formule pour le deuxième filtrage dans le cône.](images/cdmp-formula28.png)

<span data-ttu-id="e004e-630">Avec le cône actuel, la recherche initiale concerne les points situés à une distance de 0,1 (*R*,*G*,*B* ).</span><span class="sxs-lookup"><span data-stu-id="e004e-630">With the current cone, the initial search is for points that are within a distance of 0.1 from (*R*,*G*,*B* ).</span></span> <span data-ttu-id="e004e-631">Si aucun point n’est trouvé dans ce rayon, le rayon est augmenté de 0,1 et la recherche est redémarrée.</span><span class="sxs-lookup"><span data-stu-id="e004e-631">If no point is found within this radius, the radius is increased by 0.1, and the search is restarted.</span></span> <span data-ttu-id="e004e-632">Si les réseaux d’arrondis suivants ne pointent pas non plus, le rayon est augmenté de 0,1.</span><span class="sxs-lookup"><span data-stu-id="e004e-632">If the next round nets no point either, the radius is increased by 0.1.</span></span> <span data-ttu-id="e004e-633">Ce processus se poursuit jusqu’à ce que le rayon dépasse MaxDist/5, où MaxDist = 3, dans le cas de 1-normal.</span><span class="sxs-lookup"><span data-stu-id="e004e-633">This process continues until the radius exceeds MaxDist/5, where MaxDist = 3, in the case of 1-norm.</span></span> <span data-ttu-id="e004e-634">Si aucun point n’est trouvé, le cône est agrandi en diminuant les co ?</span><span class="sxs-lookup"><span data-stu-id="e004e-634">If no point is found, the cone is enlarged by decreasing the cos ?</span></span> <span data-ttu-id="e004e-635">par 0,05, autrement dit, vous augmentiez l’angle ?</span><span class="sxs-lookup"><span data-stu-id="e004e-635">by 0.05, that is, increasing the angle ?</span></span> <span data-ttu-id="e004e-636">et le redémarrage de l’ensemble du processus avec un rayon de plus en plus important.</span><span class="sxs-lookup"><span data-stu-id="e004e-636">and restarting the whole process with an increasing radius.</span></span> <span data-ttu-id="e004e-637">Ce processus se poursuit jusqu’à ce qu’un ensemble de points non vide soit trouvé ou cos ?</span><span class="sxs-lookup"><span data-stu-id="e004e-637">This process continues until a non-empty set of points is found, or cos ?</span></span> <span data-ttu-id="e004e-638">atteint 0, autrement dit, le cône s’est ouvert pour devenir un plan.</span><span class="sxs-lookup"><span data-stu-id="e004e-638">reaches 0, that is, the cone has opened up to become a plane.</span></span> <span data-ttu-id="e004e-639">À ce stade, la recherche est redémarrée en renforçant le rayon, sauf que la recherche se poursuit jusqu’à ce que le rayon atteigne MaxDist.</span><span class="sxs-lookup"><span data-stu-id="e004e-639">At this point, the search is restarted by increasing the radius, except that the search continues until the radius reaches MaxDist.</span></span> <span data-ttu-id="e004e-640">Cela garantit que, dans le pire des cas, un ensemble de points non vide est trouvé.</span><span class="sxs-lookup"><span data-stu-id="e004e-640">This guarantees that in the worst-case scenario, a non-empty set of points will be found.</span></span> <span data-ttu-id="e004e-641">L’algorithme est résumé dans le diagramme de flow de la figure 4.</span><span class="sxs-lookup"><span data-stu-id="e004e-641">The algorithm is summarized in the flow diagram in Figure 4.</span></span>

![Diagramme qui montre le déroulement de l’algorithme.](images/cdmp-lcd-dmp-figure4.png)

<span data-ttu-id="e004e-643">**Figure 4** : diagramme de Flow permettant de déterminer le jeu de points d’échantillonnage utilisé dans l’extrapolation pour une valeur RVB d’entrée</span><span class="sxs-lookup"><span data-stu-id="e004e-643">**Figure 4** : Flow diagram for determining the set S of sample points used in the extrapolation for an input RGB value</span></span>

<span data-ttu-id="e004e-644">En supposant que le processus précédent génère *un ensemble non* vide de points (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) et correspondant (*L <sub>i</sub>*,*<sub>i</sub>*,*b <sub>i</sub>* ), puis, pour chaque point, un poids *w <sub></sub>* affecté, donné par</span><span class="sxs-lookup"><span data-stu-id="e004e-644">Assuming that the preceding process yields a non-empty set *S* of points (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) and corresponding (*L <sub>i</sub>*,*a <sub>i</sub>*,*b <sub>i</sub>* ), then for each such point, a weight *w<sub>i</sub>* is assigned, given by</span></span>

![Affiche la formule pour un poids pour chaque point.](images/cdmp-formula29.png)

<span data-ttu-id="e004e-646">Enfin, extrapolant est défini par</span><span class="sxs-lookup"><span data-stu-id="e004e-646">Finally, the extrapolant is defined by</span></span>

![Affiche la définition de extrapolant.](images/cdmp-formula30.png)

<span data-ttu-id="e004e-648">Les équations précédentes constituent une instance des « méthodes pondérées à distance inverse », communément appelées méthodes Shepard.</span><span class="sxs-lookup"><span data-stu-id="e004e-648">The preceding equations constitute an instance of the "inverse-distance weighted methods," commonly called the Shepard methods.</span></span> <span data-ttu-id="e004e-649">En exécutant chacun des huit points à partir de EQ (6) à l’algorithme, huit points de contrôle sont obtenus, chacun avec des valeurs *R*,*G*,*B* et *L*,*a*,*b* , qui sont placées dans le pool avec les exemples de données d’origine.</span><span class="sxs-lookup"><span data-stu-id="e004e-649">By running each of the eight points from eq (6) through the algorithm, eight control points are obtained, each with *R*,*G*,*B* and *L*,*a*,*b* values, which are put into the pool with the original sample data.</span></span>

<span data-ttu-id="e004e-650">Pour vous assurer que le modèle produit toujours des valeurs de couleur valides et pour l’intégrité du système et pour stabiliser le pipeline de traitement des couleurs, vous devez effectuer un découpage final dans la sortie du modèle polynomial.</span><span class="sxs-lookup"><span data-stu-id="e004e-650">To ensure that the model always produces valid color values and for system integrity and stability down the whole color processing pipeline, you must perform a final clipping to the output of the polynomial model.</span></span> <span data-ttu-id="e004e-651">La gamme d’éléments visuels CIE est décrite par le composant Achromatic (*Y* ou *L* ) et le composant chromatique (*XY* ou *a’b*), qui sont associés à l’espace XYZ par une transformation projective.</span><span class="sxs-lookup"><span data-stu-id="e004e-651">The CIE visual gamut is described by the achromatic component (*Y* or *L* ) and the chromatic component (*xy* or *a'b'*, which are related to the XYZ space by a projective transformation).</span></span> <span data-ttu-id="e004e-652">Dans l’implémentation actuelle, la valeur chromatique *a’b* est utilisée car elle est directement liée à l’espace CIELUV.</span><span class="sxs-lookup"><span data-stu-id="e004e-652">In the current implementation, the *a'b'* chromaticity is used because it is directly related to the CIELUV space.</span></span> <span data-ttu-id="e004e-653">Pour toute valeur *CIELAB* , premier clip *L* à une valeur non négative :</span><span class="sxs-lookup"><span data-stu-id="e004e-653">For any *CIELAB* value, first clip *L* to a non-negative value:</span></span>

![Affiche le découpage de L à une valeur non négative.](images/cdmp-formula31.png)

<span data-ttu-id="e004e-655">Pour permettre l’extrapolation pour les surbrillances spéculaires, *l* n’est pas coupé à 100, la limite supérieure « conventionnelle » pour *l* dans l’espace Lab.</span><span class="sxs-lookup"><span data-stu-id="e004e-655">To allow extrapolation for specular highlights, *L* is not clipped at 100, the "conventional" upper bound for *L* in Lab space.</span></span>

<span data-ttu-id="e004e-656">Ensuite, si *L* = 0, *a* et *b* sont découpés, de sorte que a *= b =* 0.</span><span class="sxs-lookup"><span data-stu-id="e004e-656">Next, if *L* = 0, then *a* and *b* are clipped such that a *= b =* 0.</span></span> <span data-ttu-id="e004e-657">Si *L* ?</span><span class="sxs-lookup"><span data-stu-id="e004e-657">If *L* ?</span></span> <span data-ttu-id="e004e-658">0, calculer</span><span class="sxs-lookup"><span data-stu-id="e004e-658">0, calculate</span></span>

![Affiche la formule si L = 0.](images/cdmp-formula32.png)

<span data-ttu-id="e004e-660">Il s’agit des composants d’un vecteur dans le diagramme du *a’b'* du point blanc (*u ? '*,*v ? '*</span><span class="sxs-lookup"><span data-stu-id="e004e-660">These are the components of a vector in the *a'b'* diagram from the white point (*u?'*,*v?'*</span></span> <span data-ttu-id="e004e-661">) à la couleur en question.</span><span class="sxs-lookup"><span data-stu-id="e004e-661">) to the color in question.</span></span> <span data-ttu-id="e004e-662">Définir le locus spectral CIE comme la coque convexe de tous les points (*a'*,*b'* ), paramétrés par la longueur d’onde ?:</span><span class="sxs-lookup"><span data-stu-id="e004e-662">Define the CIE spectral locus as the convex hull of all the points (*a'*,*b'* ), parameterized by the wavelength ?:</span></span>

![Affiche la formule de la longueur d’onde.](images/cdmp-formula33.png)

<span data-ttu-id="e004e-664">où ![ affiche les fonctions pour la correspondance des couleurs Cie.](images/cdmp-formula34.png)</span><span class="sxs-lookup"><span data-stu-id="e004e-664">where ![Shows the functions for CIE color-matching.](images/cdmp-formula34.png)</span></span> <span data-ttu-id="e004e-665">sont les fonctions de correspondance de couleur CIE pour l’observateur à 2 degrés.</span><span class="sxs-lookup"><span data-stu-id="e004e-665">are the CIE color-matching functions for the 2-degree observer.</span></span> <span data-ttu-id="e004e-666">Si le vecteur se trouve en dehors du locus CIE, la couleur est découpée au point sur le locus CIE qui est l’intersection du locus et la ligne définie par le vecteur.</span><span class="sxs-lookup"><span data-stu-id="e004e-666">If the vector lies outside the CIE locus, the color is clipped to the point on the CIE locus that is the intersection of the locus and the line defined by the vector.</span></span> <span data-ttu-id="e004e-667">Voir figure 5.</span><span class="sxs-lookup"><span data-stu-id="e004e-667">See Figure 5.</span></span> <span data-ttu-id="e004e-668">Si le découpage s’est produit, la valeur *a* et *b* est reconstruite en soustrayant *d’abord un ?*</span><span class="sxs-lookup"><span data-stu-id="e004e-668">If clipping has occurred, the *a* and *b* value is reconstructed by first subtracting *a?'*</span></span> <span data-ttu-id="e004e-669">et *b ?»*</span><span class="sxs-lookup"><span data-stu-id="e004e-669">and *b?'*</span></span> <span data-ttu-id="e004e-670">entre *a* et *b* découpés, puis multiplié par 13 *L*.</span><span class="sxs-lookup"><span data-stu-id="e004e-670">from the clipped *a'* and *b'*, and then multiplying by 13 *L*.</span></span>

![Diagramme qui montre le graphique de l’algorithme de découpage.](images/cdmp-lcd-dmp-figure5.png)

<span data-ttu-id="e004e-672">**Figure 5** : algorithme de découpage pour les valeurs Lab qui se trouvent en dehors de la gamme d’éléments visuels Cie</span><span class="sxs-lookup"><span data-stu-id="e004e-672">**Figure 5** : Clipping algorithm for Lab values that are outside the CIE visual gamut</span></span>

<span data-ttu-id="e004e-673">Dans l’implémentation actuelle, le locus spectral CIE dans le plan *a’b* est représenté par une courbe linéaire par morceaux avec 35 segments (correspondant à une longueur d’onde comprise entre 360 nm et 700 nm inclus).</span><span class="sxs-lookup"><span data-stu-id="e004e-673">In the current implementation, the CIE spectral locus in the *a'b'* plane is represented by a piecewise linear curve with 35 segments (corresponding to a wavelength from 360 nm to 700 nm inclusive).</span></span> <span data-ttu-id="e004e-674">En classant les segments de ligne de sorte que leurs angles sous-tendus au niveau du point blanc soient croissants, ce qui équivaut aux longueurs d’onde décroissantes, le segment de ligne qui croise le rayon formé par le vecteur ci-dessus peut être trouvé par une simple recherche binaire.</span><span class="sxs-lookup"><span data-stu-id="e004e-674">By ordering the line segments so that their subtended angles at the white point are ascending, which is equivalent to descending wavelengths, the line segment that intersects with the ray formed by the above vector can be found by a simple binary search.</span></span>

### <a name="rgb-printer-device-model-baseline"></a><span data-ttu-id="e004e-675">Ligne de base du modèle d’imprimante RVB</span><span class="sxs-lookup"><span data-stu-id="e004e-675">RGB Printer Device Model Baseline</span></span>

<span data-ttu-id="e004e-676">Une caractérisation d’appareil d’une imprimante RVB consiste à construire un modèle empirique de l’appareil qui prédit la couleur CIELUV indépendante du périphérique pour toute valeur RVB donnée.</span><span class="sxs-lookup"><span data-stu-id="e004e-676">A device characterization of a RGB printer consists of constructing an empirical model of the device that predicts the device-independent CIELUV color for any given RGB value</span></span>

<span data-ttu-id="e004e-677">Il existe deux façons de construire le modèle empirique.</span><span class="sxs-lookup"><span data-stu-id="e004e-677">There are two ways to construct the empirical model.</span></span> <span data-ttu-id="e004e-678">L’une des méthodes consiste à utiliser les données de l’appareil pour une imprimante RVB, et l’autre à utiliser les données de paramètres analytiques.</span><span class="sxs-lookup"><span data-stu-id="e004e-678">One way is to use the device data for a RGB printer, and the other is to use analytical parameter data.</span></span> <span data-ttu-id="e004e-679">Dans le premier, les données de mesure fournies par un utilisateur pour un périphérique d’imprimante RVB sont utilisées pour construire une table de recherche 3D (LUT).</span><span class="sxs-lookup"><span data-stu-id="e004e-679">In the first one, measurement data provided by a user for a RGB printer device is used to construct 3-D lookup table (LUT).</span></span> <span data-ttu-id="e004e-680">Les données de mesure se composent de valeurs XYZ pour les correctifs RGB à échantillonnage uniforme.</span><span class="sxs-lookup"><span data-stu-id="e004e-680">The measurement data consists of XYZ values for uniformly sampled RGB patches.</span></span> <span data-ttu-id="e004e-681">Les tailles d’échantillonnage standard sont 9 ou 17 pour chaque composant.</span><span class="sxs-lookup"><span data-stu-id="e004e-681">Typical sampling sizes are 9 or 17 for each component.</span></span> <span data-ttu-id="e004e-682">Chaque patch est mesuré à l’aide d’un colorimeter ou d’un spectrophotomètre dans l’espace CIEXYZ.</span><span class="sxs-lookup"><span data-stu-id="e004e-682">Each patch is measured with a colorimeter or spectrophotometer in CIEXYZ space.</span></span> <span data-ttu-id="e004e-683">La valeur XYZ d’un correctif est ensuite convertie en valeur CIELUV, formant un LUT 3D.</span><span class="sxs-lookup"><span data-stu-id="e004e-683">The XYZ value for a patch is then converted into CIELUV value, forming a 3-D LUT.</span></span> <span data-ttu-id="e004e-684">Dans le modèle d’appareil, la méthode d’interpolation tetrahedral de Sakamoto est appliquée au LUT 3D afin de prédire les données CIELUV pour une donnée RVB donnée.</span><span class="sxs-lookup"><span data-stu-id="e004e-684">In the device model, the Sakamoto's tetrahedral interpolation method is applied to the 3-D LUT in order to predict the CIELUV data for a given RGB data.</span></span> <span data-ttu-id="e004e-685">(Conférer le brevet 4275413 (Sakamoto et al.), US brevet 4511989 (Sakamoto), Kang \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="e004e-685">(Confer US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[1\].</span></span> <span data-ttu-id="e004e-686">Les deux brevets mentionnés ont expiré.).</span><span class="sxs-lookup"><span data-stu-id="e004e-686">The two patents mentioned have expired.).</span></span> <span data-ttu-id="e004e-687">Les données de paramètres analytiques passées dans la deuxième méthode sont simplement un LUT qui a été créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="e004e-687">The analytical parameter data passed in the second method is simply a LUT that was built previously.</span></span> <span data-ttu-id="e004e-688">En règle générale, cet LUT a été créé à l’aide de la première méthode, bien qu’il puisse être créé manuellement.</span><span class="sxs-lookup"><span data-stu-id="e004e-688">Typically, that LUT was built using the first method, although it could be hand-built.</span></span>

<span data-ttu-id="e004e-689">Dans la gestion des couleurs actuelle, le mappage source est défini en tant que carte qui passe de l’espace RVB à un espace de couleurs CIEXYZ indépendant du périphérique.</span><span class="sxs-lookup"><span data-stu-id="e004e-689">In the current color management, the source map is defined as the map that goes from RGB space to a device-independent CIEXYZ color space.</span></span> <span data-ttu-id="e004e-690">La carte de destination est définie en tant que carte qui passe de l’espace de couleurs CIEXYZ indépendant du périphérique à l’espace RVB.</span><span class="sxs-lookup"><span data-stu-id="e004e-690">The destination map is defined as the map that goes from the device-independent CIEXYZ color space to RGB space.</span></span> <span data-ttu-id="e004e-691">Il s’agit de l’inverse du mappage source.</span><span class="sxs-lookup"><span data-stu-id="e004e-691">It is the inverse of the source map.</span></span>

<span data-ttu-id="e004e-692">Le modèle empirique est directement utilisé dans le mappage source.</span><span class="sxs-lookup"><span data-stu-id="e004e-692">The empirical model is directly used in the source map.</span></span> <span data-ttu-id="e004e-693">En premier lieu, il mappe une donnée RVB donnée dans des données CIELUV, qui sont converties en données XYZ.</span><span class="sxs-lookup"><span data-stu-id="e004e-693">It first maps a given RGB data into a CIELUV data, which is converted into XYZ data.</span></span> <span data-ttu-id="e004e-694">Dans le mappage de destination, les données CIEXYZ indépendantes du périphérique sont d’abord converties en données CIELUV.</span><span class="sxs-lookup"><span data-stu-id="e004e-694">In the destination map, device-independent CIEXYZ data is first converted into CIELUV data.</span></span> <span data-ttu-id="e004e-695">Ensuite, le modèle empirique et la méthode de Newton-Raphson classique sont utilisés pour prédire les meilleures données RVB pour les données CIELUV.</span><span class="sxs-lookup"><span data-stu-id="e004e-695">Then, the empirical model and the classical Newton-Raphson method are used to predict the best RGB data for the CIELUV data.</span></span> <span data-ttu-id="e004e-696">Les détails de la conversion de CieLUV en données RVB sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="e004e-696">The details about conversion from CieLUV to RGB data are as follows:</span></span>

<span data-ttu-id="e004e-697">Après la génération d’un LUT 3D à partir de RGB vers CieLUV, la carte de RVB à LUV est créée à l’aide de l’interpolation tetrahedral sur RVB.</span><span class="sxs-lookup"><span data-stu-id="e004e-697">After generating a 3-D LUT from RGB to CieLUV, the map from RGB to LUV is built using tetrahedral interpolation on RGB.</span></span> <span data-ttu-id="e004e-698">Ce mappage est indiqué par les équations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e004e-698">This map is denoted by the following equations:</span></span>

![Affiche les équations de la carte comprise entre R G B et L U V.](images/cdmp-image125.png)

<span data-ttu-id="e004e-700">L’inversion de la carte consiste à résoudre, pour toutes les couleurs</span><span class="sxs-lookup"><span data-stu-id="e004e-700">Inversion of the map consists of solving, for any color</span></span> ![Affiche L U V.](images/cdmp-image127.png) <span data-ttu-id="e004e-702">, le système suivant d’équations non linéaires :</span><span class="sxs-lookup"><span data-stu-id="e004e-702">, the following system of nonlinear equations:</span></span>

![Affiche les équations non linéaires pour lolving toute couleur L U V.](images/cdmp-image129.png)

<span data-ttu-id="e004e-704">Une équation non linéaire basée sur la méthode Newton-Raphson classique est utilisée dans la nouvelle CTE.</span><span class="sxs-lookup"><span data-stu-id="e004e-704">A nonlinear equation that is based on the classical Newton-Raphson method is used in the new CTE.</span></span> <span data-ttu-id="e004e-705">Pour obtenir une estimation initiale, ou *un* précédent, vous obtenez des s <sub>antérieurs</sub> -(R 0, v 0, B 0) en effectuant une recherche dans une « matrice de départ » comprenant une grille 8x8x8 uniforme de paires précalculées (RVB, Luv).</span><span class="sxs-lookup"><span data-stu-id="e004e-705">An initial guess, or *a priori* see, s <sub>prior</sub> -(R 0, G 0, B 0 ) is obtained by searching through a "seed matrix" consisting of a uniform 8x8x8 grid of pre-computed (RGB,Luv) pairs.</span></span> <span data-ttu-id="e004e-706">Le Luv correspondant RVB le plus proche de L \* u \* v \* est choisi.</span><span class="sxs-lookup"><span data-stu-id="e004e-706">The RGB corresponding Luv that is closest to the L\*u\*v\* is chosen.</span></span> <span data-ttu-id="e004e-707">Chaque point de la matrice de valeur initiale correspond au centre d’une cellule afin que les itérations ne commencent pas par un point sur la face frontière du cube RGB.</span><span class="sxs-lookup"><span data-stu-id="e004e-707">Each point in the seed matrix corresponds to the center of a cell so that the iterations don't start with a point on the boundary face of the RGB cube.</span></span> <span data-ttu-id="e004e-708">En d’autres termes, la couleur RVB des graines est définie par : étape = 1/8 s <sub>IJK</sub> = (étape/2 + (i-1) étape, étape/2 + (j-1) étape, étape/2 + (k-1) étape) avec i, j, k = 1... 8 à l’étape *i* de Newton-Raphson, l’estimation suivante ![ affiche les variables pour l’estimation suivante.](images/cdmp-image133.png)</span><span class="sxs-lookup"><span data-stu-id="e004e-708">In other words, the RGB of the seeds is defined by: STEP = 1/8 s <sub>ijk</sub> = (STEP/2 + (i-1) STEP, STEP/2+(j-1)STEP, STEP/2+(k-1)STEP) with i,j,k = 1...8 At the *i* th step of Newton-Raphson, the next estimate ![Shows the variables for the next estimate.](images/cdmp-image133.png)</span></span> <span data-ttu-id="e004e-709">est obtenu par la formule :</span><span class="sxs-lookup"><span data-stu-id="e004e-709">is obtained by the formula:</span></span>

![Affiche la formule de l’estimation.](images/cdmp-image135.png)

<span data-ttu-id="e004e-711">L’itération s’arrête lorsque l’erreur (distance dans l’espace CIELUV) est inférieure à un niveau de tolérance prédéfini (0,1 dans la CTE) ou lorsque le nombre d’itérations a dépassé le nombre maximal d’itérations autorisé (10 dans la CTE).</span><span class="sxs-lookup"><span data-stu-id="e004e-711">Iteration stops when the error (distance in the CIELUV space) is less than a pre-set tolerance level (0.1 in the CTE), or when the number of iterations has exceeded the maximum allowed number of iterations (10 in the CTE).</span></span> <span data-ttu-id="e004e-712">Les valeurs de la tolérance et du nombre d’itérations ont été déterminées de manière empirique pour être effectives.</span><span class="sxs-lookup"><span data-stu-id="e004e-712">The values for the tolerance and the number of iterations were empirically determined to be effective.</span></span> <span data-ttu-id="e004e-713">Dans les versions ultérieures, la valeur de tolérance peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="e004e-713">In future versions, the tolerance value may be changed.</span></span>

<span data-ttu-id="e004e-714">La matrice de Jacob est calculée à l’aide de la différence directe, sauf à un point limite (un ou plusieurs des R, G, B est 1) où la différence descendante est utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="e004e-714">The Jacobian matrix is calculated using forward difference, except at a boundary point (one or more of the R, G, B is 1) where backward difference is used instead.</span></span> <span data-ttu-id="e004e-715">Au lieu de calculer l’inverse de la matrice de Jacob, le système linéaire est résolu directement à l’aide de Gauss-Jordan élimination avec le pivotement complet.</span><span class="sxs-lookup"><span data-stu-id="e004e-715">Instead of calculating the inverse of the Jacobian matrix, the linear system is solved directly using Gauss-Jordan elimination with full pivoting.</span></span>

<span data-ttu-id="e004e-716">À la fin des itérations, la convergence n’est peut-être pas possible, car Newton-Raphson est un algorithme « local », c’est-à-dire qu’elle fonctionne uniquement si vous démarrez avec une estimation initiale qui est proche de la véritable solution.</span><span class="sxs-lookup"><span data-stu-id="e004e-716">At the end of the iterations, convergence still might not be achieved because Newton-Raphson is a "local" algorithm, that is, it only works well if you start with an initial guess that is close to the true solution.</span></span> <span data-ttu-id="e004e-717">Si, à la fin de l' Newton-Raphson itérations, la convergence au sein de la tolérance d’erreur prédéfinie n’a pas été effectuée, les itérations sont redémarrées avec un nouvel ensemble de graines, défini comme suit.</span><span class="sxs-lookup"><span data-stu-id="e004e-717">If, at the end of the Newton-Raphson iterations, convergence within the pre-defined error tolerance has not been achieved, the iterations are restarted with a new set of seeds, defined as follows.</span></span>

<span data-ttu-id="e004e-718">Par exemple, la meilleure solution obtenue jusqu’à présent est (r, g, b).</span><span class="sxs-lookup"><span data-stu-id="e004e-718">For example, the best solution obtained so far is (r, g, b).</span></span> <span data-ttu-id="e004e-719">À partir de cette solution, N a les graines postérieures sont dérivées, où N = 4.</span><span class="sxs-lookup"><span data-stu-id="e004e-719">From this solution, N a posteriori seeds are derived, where N = 4.</span></span> <span data-ttu-id="e004e-720">Intuitivement, la solution est déplacée « vers le centre » dans une taille d’étape qui dépend de N. Voir figure 6.</span><span class="sxs-lookup"><span data-stu-id="e004e-720">Intuitively, the solution is moved "toward the center" in a step size that depends on N. See Figure 6.</span></span>

![Diagramme qui montre les directions de perturbation de la solution.](images/cdmp-image136.png)

<span data-ttu-id="e004e-722">**Figure 6** : la direction de la perturbation de la solution dépend de la Octant dans laquelle elle se trouve.</span><span class="sxs-lookup"><span data-stu-id="e004e-722">**Figure 6** : Perturbation direction of the solution depends on which octant it is in.</span></span>

<span data-ttu-id="e004e-723">En d’autres termes, si r &gt; 0,5, la valeur sur le canal r est diminuée, sinon la valeur est augmentée.</span><span class="sxs-lookup"><span data-stu-id="e004e-723">In other words, if r &gt; 0.5, the value on the R channel is decreased, otherwise the value is increased.</span></span> <span data-ttu-id="e004e-724">Il existe une logique similaire pour les canaux G et B.</span><span class="sxs-lookup"><span data-stu-id="e004e-724">There is similar logic for the G and B channels.</span></span> <span data-ttu-id="e004e-725">Les définitions précises sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="e004e-725">The precise definitions are:</span></span>

<span data-ttu-id="e004e-726">PERTURBATION = 0,5/(N + 1)</span><span class="sxs-lookup"><span data-stu-id="e004e-726">PERTURBATION = 0.5/(N+1)</span></span>

<span data-ttu-id="e004e-727">Dir (r) =-1 si r &gt; 0,5 ; + 1 dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e004e-727">Dir(r) = -1 if r &gt; 0.5; +1 otherwise.</span></span> <span data-ttu-id="e004e-728">De même pour dir (g) et dir (b)</span><span class="sxs-lookup"><span data-stu-id="e004e-728">Similarly for Dir(g) and Dir(b)</span></span>

<span data-ttu-id="e004e-729">Le JTH a POSTERIEURE, s ????, est (r + Rép (r) \* j \* perturbation, g + Rép (g) \* j \* perturbation, b + Rép (b) \* j \* perturbation)</span><span class="sxs-lookup"><span data-stu-id="e004e-729">The jth a posteriori seed, s ????, is (r + Dir(r) \*j \* PERTURBATION, g + Dir(g) \* j \* PERTURBATION, b + Dir(b) \* j \* PERTURBATION)</span></span>

<span data-ttu-id="e004e-730">Essayez les premières s ????</span><span class="sxs-lookup"><span data-stu-id="e004e-730">Try the first s ????</span></span> <span data-ttu-id="e004e-731">et s’il fournit une nouvelle solution dans la tolérance d’erreur, vous pouvez arrêter.</span><span class="sxs-lookup"><span data-stu-id="e004e-731">and if it gives a new solution within error tolerance, you can stop.</span></span> <span data-ttu-id="e004e-732">Dans le cas contraire, essayez les deuxième s ????</span><span class="sxs-lookup"><span data-stu-id="e004e-732">Otherwise, try the second s ????</span></span> <span data-ttu-id="e004e-733">et ainsi de suite jusqu’au nième ????.</span><span class="sxs-lookup"><span data-stu-id="e004e-733">and so on until the Nth s ????.</span></span>

<span data-ttu-id="e004e-734">Les schémas de l’algorithme entier sont illustrés à la figure 7.</span><span class="sxs-lookup"><span data-stu-id="e004e-734">The schematics of the whole algorithm is shown in Figure 7.</span></span>

![Diagramme qui montre le déroulement de l’inversion du modèle d’appareil.](images/cdmp-image138.png)

<span data-ttu-id="e004e-736">**Figure 7** : schémas d’inversion du modèle d’appareil</span><span class="sxs-lookup"><span data-stu-id="e004e-736">**Figure 7** : Schematics of inverting the device model</span></span>

### <a name="rgb-virtual-device-model-baseline"></a><span data-ttu-id="e004e-737">Ligne de base du modèle d’appareil virtuel RGB</span><span class="sxs-lookup"><span data-stu-id="e004e-737">RGB Virtual Device Model Baseline</span></span>

<span data-ttu-id="e004e-738">Ce modèle de périphérique (DM) est un algorithme de reproduction simple de matrice/ton.</span><span class="sxs-lookup"><span data-stu-id="e004e-738">This device model(DM) is a simple matrix/tone reproduction algorithm.</span></span> <span data-ttu-id="e004e-739">La matrice est dérivée du point blanc et des primaires à l’aide d’algorithmes de science des couleurs standard.</span><span class="sxs-lookup"><span data-stu-id="e004e-739">The matrix is derived from the white point and primaries using standard color science algorithms.</span></span> <span data-ttu-id="e004e-740">La courbe de reproduction des tons est dérivée des paramètres de mesure en fonction des descriptions ICC de CurveType et ParametricType (ou inversées selon les besoins).</span><span class="sxs-lookup"><span data-stu-id="e004e-740">The tone reproduction curve is derived from the measurement parameters according to the ICC descriptions of CurveType and ParametricType (or inverted as required).</span></span> <span data-ttu-id="e004e-741">Les détails des algorithmes internes seront fournis après une validation supplémentaire des problèmes de plage dynamique élevée.</span><span class="sxs-lookup"><span data-stu-id="e004e-741">Details of the internal algorithms will be provided after additional validation of high dynamic range issues.</span></span>

<span data-ttu-id="e004e-742">Le modèle d’appareil virtuel RGB est une courbe de reproduction de matrice/ton idéale RVB similaire à la conception de profil basé sur la matrice ICC à trois composants.</span><span class="sxs-lookup"><span data-stu-id="e004e-742">The RGB virtual device model is an idealized matrix/tone reproduction curve RGB similar to the ICC three-component matrix-based profile design.</span></span> <span data-ttu-id="e004e-743">Les paramètres de « mesure virtuelle » du DM incluent une valeur de point blanc (Absolute CIEXYZ), des valeurs RVB primaires (CIEXYZ absolues) et une courbe de reproduction des tons basée sur le ParametricCurveType ICC et CurveType dans la mise en forme XML cohérente avec les schémas DMP.</span><span class="sxs-lookup"><span data-stu-id="e004e-743">The "virtual measurement" parameters of the DM include a white point value (absolute CIEXYZ), RGB primary values (absolute CIEXYZ), and a tone reproduction curve that is based on the ICC ParametricCurveType and CurveType in XML formatting consistent with the DMP schemas.</span></span>

<span data-ttu-id="e004e-744">L’encodage de type de fonction ICC parametricCurveType et la prise en charge correspondante dans IRGBVirtualDeviceModelBase sont indiqués dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e004e-744">ICC parametricCurveType function type encoding and corresponding support in IRGBVirtualDeviceModelBase are shown in the following table.</span></span>



| <span data-ttu-id="e004e-745">Type de fonction</span><span class="sxs-lookup"><span data-stu-id="e004e-745">Function type</span></span>                                         | <span data-ttu-id="e004e-746">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e004e-746">Parameters</span></span>                          | <span data-ttu-id="e004e-747">Type</span><span class="sxs-lookup"><span data-stu-id="e004e-747">Type</span></span>                                     | <span data-ttu-id="e004e-748">Remarque</span><span class="sxs-lookup"><span data-stu-id="e004e-748">Note</span></span>                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![Affiche la fonction « GammaType ».](images/cdmp-image154.png)<br/> | <span data-ttu-id="e004e-750">g</span><span class="sxs-lookup"><span data-stu-id="e004e-750">g</span></span><br/>              | <span data-ttu-id="e004e-751">GammaType</span><span class="sxs-lookup"><span data-stu-id="e004e-751">GammaType</span></span><br/>                 | <span data-ttu-id="e004e-752">Implémentation courante</span><span class="sxs-lookup"><span data-stu-id="e004e-752">Common implementation</span></span><br/>           |
| ![Affiche la fonction « GammaOffsetGainType ».](images/cdmp-image156.png)<br/> | <span data-ttu-id="e004e-754">GA b</span><span class="sxs-lookup"><span data-stu-id="e004e-754">ga b</span></span><br/>           | <span data-ttu-id="e004e-755">GammaOffsetGainType</span><span class="sxs-lookup"><span data-stu-id="e004e-755">GammaOffsetGainType</span></span><br/>       | <span data-ttu-id="e004e-756">CIE 122-1966</span><span class="sxs-lookup"><span data-stu-id="e004e-756">CIE 122-1966</span></span><br/>                    |
| ![Affiche la fonction « GammaOffsetGainOffsetType ».](images/cdmp-image158.png)<br/> | <span data-ttu-id="e004e-758">GA b c</span><span class="sxs-lookup"><span data-stu-id="e004e-758">ga b c</span></span><br/>         | <span data-ttu-id="e004e-759">GammaOffsetGainOffsetType</span><span class="sxs-lookup"><span data-stu-id="e004e-759">GammaOffsetGainOffsetType</span></span><br/> | <span data-ttu-id="e004e-760">IEC 61966-3</span><span class="sxs-lookup"><span data-stu-id="e004e-760">IEC 61966-3</span></span><br/>                     |
| ![Affiche la fonction « GammaOffsetGainGainType ».](images/cdmp-image160.png)<br/> | <span data-ttu-id="e004e-762">GA b c d</span><span class="sxs-lookup"><span data-stu-id="e004e-762">ga b c d</span></span><br/>       | <span data-ttu-id="e004e-763">GammaOffsetGainGainType</span><span class="sxs-lookup"><span data-stu-id="e004e-763">GammaOffsetGainGainType</span></span><br/>   | <span data-ttu-id="e004e-764">IEC 61966-2.1</span><span class="sxs-lookup"><span data-stu-id="e004e-764">IEC 61966-2.1</span></span><br/> <span data-ttu-id="e004e-765">sRVB</span><span class="sxs-lookup"><span data-stu-id="e004e-765">(sRGB)</span></span><br/> |
| ![Affiche une fonction pour les paramètres’g a b c d e f'.](images/cdmp-image162.png)<br/> | <span data-ttu-id="e004e-767">GA b c d e f</span><span class="sxs-lookup"><span data-stu-id="e004e-767">ga b c d e f</span></span><br/>   | <span data-ttu-id="e004e-768">N/A</span><span class="sxs-lookup"><span data-stu-id="e004e-768">N/A</span></span><br/>                       | <span data-ttu-id="e004e-769">Non pris en charge dans WCS</span><span class="sxs-lookup"><span data-stu-id="e004e-769">Not supported in WCS</span></span><br/>            |



 

<span data-ttu-id="e004e-770">La courbe de tonalité pour les appareils virtuels RGB est appliquée dans DeviceToColorimetric entre les données d’entrée, pDeviceColors et la matrice multiplier.</span><span class="sxs-lookup"><span data-stu-id="e004e-770">The tone curve for RGB virtual devices is applied in DeviceToColorimetric between the input data, pDeviceColors, and the matrix multiply.</span></span> <span data-ttu-id="e004e-771">Pour ColorimetricToDevice, une méthode doit être utilisée pour inverser la courbe tonale.</span><span class="sxs-lookup"><span data-stu-id="e004e-771">For ColorimetricToDevice, a method must be used to invert the tone curve.</span></span> <span data-ttu-id="e004e-772">Dans l’implémentation de base, cette opération est effectuée par interpolation directe dans la même courbe de tonalité utilisée pour DeviceToColorimetric.</span><span class="sxs-lookup"><span data-stu-id="e004e-772">In the baseline implementation, this is done by direct interpolation in the same tone curve used for DeviceToColorimetric.</span></span>

<span data-ttu-id="e004e-773">Les courbes doivent être spécifiées dans les profils sous forme de paires de nombres dans l’espace flottant.</span><span class="sxs-lookup"><span data-stu-id="e004e-773">The curves should be specified in the profiles as pairs of numbers in float space.</span></span> <span data-ttu-id="e004e-774">Le premier nombre représente des valeurs dans pDeviceColors.</span><span class="sxs-lookup"><span data-stu-id="e004e-774">The first number represents values in pDeviceColors.</span></span> <span data-ttu-id="e004e-775">Le deuxième nombre représente la sortie de la courbe de tonalité.</span><span class="sxs-lookup"><span data-stu-id="e004e-775">The second number represents the output of the tone curve.</span></span> <span data-ttu-id="e004e-776">Toutes les valeurs de la courbe tonale doivent être comprises entre minColorantUsed et maxColorantUsed.</span><span class="sxs-lookup"><span data-stu-id="e004e-776">All values in the tone curve must be between minColorantUsed and maxColorantUsed.</span></span> <span data-ttu-id="e004e-777">Les courbes de tons doivent contenir au moins deux entrées : une pour minColorantUsed et une pour maxColorantUsed.</span><span class="sxs-lookup"><span data-stu-id="e004e-777">Tone curves must contain at least two entries: one for minColorantUsed and one for maxColorantUsed.</span></span> <span data-ttu-id="e004e-778">Le nombre maximal d’entrées dans le ToneCurve est 2048.</span><span class="sxs-lookup"><span data-stu-id="e004e-778">The maximum number of entries in the ToneCurve is 2048.</span></span> <span data-ttu-id="e004e-779">En général, plus le nombre d’entrées dans la table est grand, plus le modèle de courbure est précis.</span><span class="sxs-lookup"><span data-stu-id="e004e-779">In general, the more entries in the table, the more accurately you can model curvature.</span></span> <span data-ttu-id="e004e-780">Une interpolation linéaire par morceaux est effectuée entre les entrées.</span><span class="sxs-lookup"><span data-stu-id="e004e-780">A piecewise linear interpolation is performed between the entries.</span></span>

<span data-ttu-id="e004e-781">Vous pouvez envisager d’autres méthodes d’interpolation.</span><span class="sxs-lookup"><span data-stu-id="e004e-781">You might consider alternative interpolation methods.</span></span> <span data-ttu-id="e004e-782">Si vous connaissez le comportement sous-jacent de l’appareil, vous pouvez utiliser moins d’échantillons et de modèles avec une plus grande courbe d’ordre.</span><span class="sxs-lookup"><span data-stu-id="e004e-782">If you know something about the underlying behavior of the device, you can use fewer samples and model more accurately with a higher order curve.</span></span> <span data-ttu-id="e004e-783">Toutefois, si vous utilisez un type de courbe incorrect, vous serez très imprécis.</span><span class="sxs-lookup"><span data-stu-id="e004e-783">But if you use the wrong curve type, you will be very inaccurate.</span></span> <span data-ttu-id="e004e-784">Sans plus d’informations, vous ne pouvez pas deviner le type de courbe.</span><span class="sxs-lookup"><span data-stu-id="e004e-784">Without more information, you cannot guess the curve type.</span></span> <span data-ttu-id="e004e-785">Par conséquent, utilisez l’interpolation linéaire et fournissez de nombreux points de données.</span><span class="sxs-lookup"><span data-stu-id="e004e-785">So, use linear interpolation and provide many data points.</span></span>

### <a name="cmyk-printer-device-model-baseline"></a><span data-ttu-id="e004e-786">Ligne de base modèle de périphérique d’imprimante CMJN</span><span class="sxs-lookup"><span data-stu-id="e004e-786">CMYK Printer Device Model Baseline</span></span>

<span data-ttu-id="e004e-787">Une caractérisation d’appareil d’une imprimante CMJN consiste à construire un modèle empirique de l’appareil qui prédit la couleur imprimée pour une valeur CMJN donnée.</span><span class="sxs-lookup"><span data-stu-id="e004e-787">A device characterization of a CMYK printer consists of constructing an empirical model of the device that predicts the printed color for any given CMYK value.</span></span> <span data-ttu-id="e004e-788">La caractérisation comprend également l’inversion de ce modèle afin qu’une prescription de la valeur CMYK à nous pour une couleur donnée à imprimer puisse être fournie.</span><span class="sxs-lookup"><span data-stu-id="e004e-788">The characterization also includes the inversion of this model so that a prescription of the CMYK value to us for a given color to be printed can be given.</span></span> <span data-ttu-id="e004e-789">Cela est généralement défini en termes de valeur CIEXYZ ou CIELAB.</span><span class="sxs-lookup"><span data-stu-id="e004e-789">This is typically defined in terms of CIEXYZ or CIELAB value.</span></span>

<span data-ttu-id="e004e-790">En règle générale, une cible IT 8.7/3 contenant des correctifs CMJN est utilisée.</span><span class="sxs-lookup"><span data-stu-id="e004e-790">Typically, an IT8.7/3 target containing CMYK patches is used.</span></span> <span data-ttu-id="e004e-791">Les correctifs consistent en un échantillonnage de l’espace CMJN de manière bien définie, de sorte qu’une grille rectangulaire (avec un espacement non uniforme en C, M, Y et K) soit formée.</span><span class="sxs-lookup"><span data-stu-id="e004e-791">The patches consist of sampling of the CMYK space in a well-defined manner so that a rectangular grid (with non-uniform spacing in C, M, Y and K) is formed.</span></span> <span data-ttu-id="e004e-792">Chaque patch est ensuite mesuré à l’aide d’un colorimeter ou d’un spectrophotomètre.</span><span class="sxs-lookup"><span data-stu-id="e004e-792">Each patch is then measured with a colorimeter or spectrophotometer.</span></span> <span data-ttu-id="e004e-793">Les mesures dans les valeurs CIEXYZ forment ensuite une table de recherche (LUT), à partir de laquelle un modèle empirique de l’imprimante est créé à l’aide de la méthode d’interpolation de Sakamoto.</span><span class="sxs-lookup"><span data-stu-id="e004e-793">The measurements in CIEXYZ values then form a lookup table (LUT), from which an empirical model of the printer is built using Sakamoto's interpolation method.</span></span> <span data-ttu-id="e004e-794">Brevet américain 4275413 (Sakamoto et al.), brevet américain 4511989 (Sakamoto), Kang \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="e004e-794">US Patent 4275413 (Sakamoto et al.), US Patent 4511989 (Sakamoto), Kang \[1\].</span></span> <span data-ttu-id="e004e-795">Les deux brevets mentionnés ont expiré.</span><span class="sxs-lookup"><span data-stu-id="e004e-795">The two patents mentioned have expired.</span></span>

<span data-ttu-id="e004e-796">Les exigences spécifiques pour les exemples de mesures CMJN nécessaires à l’acceptation d’un profil de modèle d’appareil comme valide par le modèle d’appareil de ligne de base d’imprimante CMJN sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="e004e-796">Specific requirements for the CMYK measurement samples necessary for a device model profile to be accepted as valid by the CMYK printer baseline device model are as follows.</span></span> <span data-ttu-id="e004e-797">(Le jeu d’échantillons est plus clairement décrit comme un ensemble d’exemples de cubes CMJ, chacun étant associé à un niveau K spécifique.)</span><span class="sxs-lookup"><span data-stu-id="e004e-797">(The sample set is most clearly described as a set of CMY sample cubes, each associated with a specific K level.)</span></span>

-   <span data-ttu-id="e004e-798">Au minimum, les cubes CMJ valides doivent être fournis pour les niveaux K = 0 et K = 100.</span><span class="sxs-lookup"><span data-stu-id="e004e-798">At minimum, valid CMY cubes must be provided for the K = 0 and K = 100 levels.</span></span>
-   <span data-ttu-id="e004e-799">Les niveaux K intermédiaires peuvent être espacés de façon non uniforme.</span><span class="sxs-lookup"><span data-stu-id="e004e-799">Intermediate K levels may be non-uniformly spaced.</span></span>
-   <span data-ttu-id="e004e-800">Tout niveau K intermédiaire sans un cube CMJ valide sera ignoré.</span><span class="sxs-lookup"><span data-stu-id="e004e-800">Any intermediate K level without a valid CMY cube will be ignored.</span></span>
-   <span data-ttu-id="e004e-801">Les cubes CMJ peuvent utiliser des intervalles d’échantillonnage non uniformes (espacement de la grille), mais le même jeu d’intervalles d’échantillonnage doit être utilisé dans toutes les dimensions C, M et Y du cube CMJ pour un niveau K donné.</span><span class="sxs-lookup"><span data-stu-id="e004e-801">The CMY cubes may use non-uniform sample intervals (grid spacing), but the same set of sample intervals must be used in all of the C,M, and Y dimensions in the CMY cube for a given K level.</span></span>
-   <span data-ttu-id="e004e-802">Chaque cube de niveau K peut utiliser un nombre et un espacement différents d’intervalles d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="e004e-802">Each K level CMY cube can use a different number and spacing of sample intervals.</span></span>
-   <span data-ttu-id="e004e-803">Tous les cubes CMJ doivent contenir les « angles » du cube CMJ, c’est-à-dire les exemples CMJ à 0, 0, 0, 0, 0100 \[ \] \[ \] , \[ 0100, 0 \] , 100, 0, 0, \[ \] \[ 0100 100 \] , 100, \[ 0100 \] , \[ 100 100, 0 \] , \[ 100 100 100 \] .</span><span class="sxs-lookup"><span data-stu-id="e004e-803">All CMY cubes must contain the "corners" of the CMY cube, that is, CMY samples at \[0,0,0\], \[0,0,100\], \[0,100,0\], \[100,0,0\], \[0,100,100\], \[100,0,100\], \[100,100, 0\], \[100,100,100\].</span></span>
-   <span data-ttu-id="e004e-804">Tous les niveaux de grille CMJ intermédiaires doivent être intégralement échantillonnés dans chaque canal.</span><span class="sxs-lookup"><span data-stu-id="e004e-804">Any intermediate CMY grid levels must be fully sampled in each channel.</span></span> <span data-ttu-id="e004e-805">En d’autres termes, un échantillon doit exister à chaque intersection de grille 3D dans le cube CMJ.</span><span class="sxs-lookup"><span data-stu-id="e004e-805">In other words, a sample must exist at each 3-D grid intersection within the CMY cube.</span></span>
-   <span data-ttu-id="e004e-806">Pour les cubes K = 0 et K = 100 CMJ, les cubes 2x2x2 « Corners only » sont le minimum accepté comme valide.</span><span class="sxs-lookup"><span data-stu-id="e004e-806">For the K = 0 and K = 100 CMY cubes, 2x2x2 "corners-only" cubes are the minimum accepted as valid.</span></span>

    <span data-ttu-id="e004e-807">\[Remarque : pour K = 0 et K = 100 niveaux, un cube 3x3x3 CMJ est traité comme un cube 2x2x2 « Corners only ». le niveau d’échantillonnage intermédiaire est ignoré.</span><span class="sxs-lookup"><span data-stu-id="e004e-807">\[NOTE: for K=0 and K=100 levels, a 3x3x3 CMY cube will be processed as a 2x2x2 "corners-only" cube; the intermediate sample level is ignored.</span></span> <span data-ttu-id="e004e-808">les 4x4x4 et les cubes plus volumineux auront tous des échantillons sur la grille utilisés.\]</span><span class="sxs-lookup"><span data-stu-id="e004e-808">4x4x4 and larger cubes will have all on-grid samples used.\]</span></span>

-   <span data-ttu-id="e004e-809">Pour les niveaux K intermédiaires, les cubes 4x4x4 CMJ sont la valeur minimale acceptée comme valide.</span><span class="sxs-lookup"><span data-stu-id="e004e-809">For intermediate K levels, 4x4x4 CMY cubes are the minimum accepted as valid.</span></span>

<span data-ttu-id="e004e-810">Un profil de haute qualité utilise des grilles d’échantillonnage plus fines que le minimum requis pour la validité, généralement 9x9x9x9 ou supérieur.</span><span class="sxs-lookup"><span data-stu-id="e004e-810">A high-quality profile will use finer sampling grids than the minimum required for validity, usually 9x9x9x9 or higher.</span></span> <span data-ttu-id="e004e-811">Les exemples des cibles IT 8.7/3, IT 8.7/4 et ECI produisent des profils de modèle d’appareil (DMPs) valides pour le modèle d’appareil de base d’imprimante CMJN.</span><span class="sxs-lookup"><span data-stu-id="e004e-811">The samples from the IT8.7/3, IT8.7/4, and ECI targets produce valid device model profiles (DMPs)for the CMYK printer baseline device model.</span></span> <span data-ttu-id="e004e-812">Bien que ce modèle d’appareil soit en mesure d’ignorer les exemples étrangers (hors grille) dans ces cibles, il n’est pas garanti qu’il puisse le faire pour d’autres cibles, et par conséquent, il est recommandé de supprimer les exemples superflus des ensembles de mesures entrant dans des profils pour ce modèle d’appareil.</span><span class="sxs-lookup"><span data-stu-id="e004e-812">While this device model is able to ignore the extraneous (off-grid) samples in these targets, it is not guaranteed to be able to do so for other targets, and so, it is recommended that extraneous samples be removed from measurement sets going into profiles for this device model.</span></span>

<span data-ttu-id="e004e-813">L’inversion du modèle d’imprimante présente davantage de difficultés.</span><span class="sxs-lookup"><span data-stu-id="e004e-813">The inversion of the printer model presents more difficulties.</span></span> <span data-ttu-id="e004e-814">Étant donné une couleur d’entrée dans CIECAM, il est question de savoir si cette couleur est dans la gamme d’imprimantes.</span><span class="sxs-lookup"><span data-stu-id="e004e-814">Given an input color in CIECAM, there is a question of whether this color is within the printer gamut.</span></span> <span data-ttu-id="e004e-815">Il y a également un problème concernant la disposition des points dans l’espace d’apparence de la couleur.</span><span class="sxs-lookup"><span data-stu-id="e004e-815">There is also the issue regarding the arrangement of points in the color appearance space.</span></span> <span data-ttu-id="e004e-816">Bien que nous puissions organiser les valeurs CMJN pour les faire tomber sur une grille rectangulaire, comme c’est le cas dans la cible IT 8.7/3, il n’est pas possible d’avoir la même valeur pour les couleurs imprimées, car elles sont situées dans l’espace d’apparence de couleur.</span><span class="sxs-lookup"><span data-stu-id="e004e-816">While we can arrange the CMYK values to fall on a rectangular grid, as is done in the IT8.7/3 target, the same cannot be said of the resulting printed colors as they are situated in the color appearance space.</span></span> <span data-ttu-id="e004e-817">En général, ils sont disséminés dans l’espace d’apparence de couleur sans modèle particulier.</span><span class="sxs-lookup"><span data-stu-id="e004e-817">In general, they are scattered in the color appearance space with no particular pattern.</span></span>

<span data-ttu-id="e004e-818">Il existe généralement deux approches pour le problème d’inversion de points dispersés.</span><span class="sxs-lookup"><span data-stu-id="e004e-818">There are generally two approaches to the inversion problem of scattered points.</span></span> <span data-ttu-id="e004e-819">Une approche consiste à utiliser une sous-division géométrique de la gamme d’imprimantes à l’aide de solides unidimensionnels élémentaires, tels que tetrahedra.</span><span class="sxs-lookup"><span data-stu-id="e004e-819">One approach is to use a geometric subdivision of the printer gamut using elementary 3-dimensional solids, such as tetrahedra.</span></span> <span data-ttu-id="e004e-820">Une sous-division de la gamme d’imprimantes dans l’espace d’apparence des couleurs peut être induite à partir de la sous-division correspondante de l’espace CMJ (K), consultez \[ 93 \] , Kang \[ 97 \] . Cette approche présente l’avantage de la simplicité de calcul.</span><span class="sxs-lookup"><span data-stu-id="e004e-820">A subdivision of the printer gamut in the color appearance space can be induced from the corresponding subdivision of the CMY(K) space, see Hung\[93\], Kang\[97\].This approach has the advantage of computational simplicity.</span></span> <span data-ttu-id="e004e-821">Dans le cas d’un tétraèdres, seuls quatre points sont utilisés dans une interpolation.</span><span class="sxs-lookup"><span data-stu-id="e004e-821">In the case of a tetrahedron, only four points are used in an interpolation.</span></span> <span data-ttu-id="e004e-822">D’un autre côté, le résultat dépend fortement de quelques points, ce qui signifie qu’une erreur de mesure aura un effet significatif sur le résultat.</span><span class="sxs-lookup"><span data-stu-id="e004e-822">On the other hand, the result depends heavily on a few points, which means that a measurement error will have a significant effect on the result.</span></span> <span data-ttu-id="e004e-823">L’interpolation a également tendance à ne pas être aussi lisse.</span><span class="sxs-lookup"><span data-stu-id="e004e-823">The interpolant also tends to be not as smooth.</span></span> <span data-ttu-id="e004e-824">La deuxième approche ne suppose pas de sous-division et est basée sur la technique d’interpolation de données éparpillée.</span><span class="sxs-lookup"><span data-stu-id="e004e-824">The second approach does not assume any subdivision, and is based on the technique of scattered data interpolation.</span></span> <span data-ttu-id="e004e-825">Un exemple classique est la technique de l’interpolation Shepard ou la méthode pondérée inversée (voir Shepard \[ 68 \] ).</span><span class="sxs-lookup"><span data-stu-id="e004e-825">A classical example is the technique of Shepard interpolation, or inverse weighted method (See Shepard \[68\]).</span></span> <span data-ttu-id="e004e-826">Ici, plusieurs points entourant le point d’entrée sont choisis d’une certaine manière, chacun affecté un poids, généralement inversement proportionnel à la distance, et l’interpolation est considérée comme la moyenne pondérée des points voisins.</span><span class="sxs-lookup"><span data-stu-id="e004e-826">Here, several points surrounding the input point are chosen in some manner, each assigned a weight, usually inversely proportional to the distance, and the interpolant is taken as the weighted average of the neighboring points.</span></span> <span data-ttu-id="e004e-827">Dans cette approche, le choix des points voisins est primordial pour les performances.</span><span class="sxs-lookup"><span data-stu-id="e004e-827">In this approach, the choice of neighboring points is paramount to performance.</span></span> <span data-ttu-id="e004e-828">Bien que trop peu de points puissent rendre l’interpolation inexacte et non lisse, un trop grand nombre de points imposent un coût de calcul élevé, car les poids sont généralement des fonctions non linéaires et coûteuses à calculer.</span><span class="sxs-lookup"><span data-stu-id="e004e-828">While too few points can render the interpolant inaccurate and non-smooth, too many points impose a high computational cost, as the weights are typically non-linear functions and costly to compute.</span></span>

<span data-ttu-id="e004e-829">Les deux approches décrites ci-dessus rencontrent des problèmes.</span><span class="sxs-lookup"><span data-stu-id="e004e-829">The two approaches described above both have problems.</span></span> <span data-ttu-id="e004e-830">L’approche de la sous-division dépend de manière critique des données qui sont raisonnablement vides et, en général, l’interpolation n’est pas très lisse.</span><span class="sxs-lookup"><span data-stu-id="e004e-830">The subdivision approach depends critically on the data being reasonably void of noise, and generally the interpolant is not very smooth.</span></span> <span data-ttu-id="e004e-831">L’interpolation de données éparpillée est plus tolérante au bruit des données et donne généralement une interpolation plus lisse, mais elle est plus coûteuse en termes de calcul.</span><span class="sxs-lookup"><span data-stu-id="e004e-831">The scattered data interpolation is more tolerant to data noise, and generally gives a smoother interpolant, but it is computationally more expensive.</span></span>

<span data-ttu-id="e004e-832">La nouvelle CTE adopte une autre approche.</span><span class="sxs-lookup"><span data-stu-id="e004e-832">The new CTE takes an alternative approach.</span></span> <span data-ttu-id="e004e-833">L’appareil CMJN est traité comme une collection de plusieurs appareils CMJ, chacun d’entre eux ayant une valeur spécifique de noir (K).</span><span class="sxs-lookup"><span data-stu-id="e004e-833">The CMYK device is treated as a collection of several CMY devices, each of which has a specific value of black (K).</span></span> <span data-ttu-id="e004e-834">À l’aide d’un algorithme de sélection qui prend comme claire et chroma des paramètres, un niveau de noir est choisi.</span><span class="sxs-lookup"><span data-stu-id="e004e-834">Using a selection algorithm that takes as parameters lightness and chroma, a level of black is chosen.</span></span> <span data-ttu-id="e004e-835">Les valeurs CMJ sont obtenues par inversion de la table CMJ vers Luv correspondante à l’aide des méthodes Newton utilisées ailleurs par l’algorithme d’imprimante RVB.</span><span class="sxs-lookup"><span data-stu-id="e004e-835">The CMY values are obtained by inversion of the corresponding CMY to Luv table using the Newton methods employed elsewhere by the RGB printer algorithm.</span></span>

<span data-ttu-id="e004e-836">Effectuez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="e004e-836">Use the following steps.</span></span>

1.  <span data-ttu-id="e004e-837">Imprimez la cible de caractérisation, qui est soit la cible IT 8.7/3, soit une cible contenant l’échantillonnage de l’espace CMJN à intervalles réguliers ou irréguliers.</span><span class="sxs-lookup"><span data-stu-id="e004e-837">Print the characterization target, which is either the IT8.7/3 target, or a target containing sampling of the CMYK space at regularly or irregularly spaced intervals.</span></span>
2.  <span data-ttu-id="e004e-838">Mesurez la cible à l’aide d’un spectrophotomètre et convertissez les mesures en espace CIELUV.</span><span class="sxs-lookup"><span data-stu-id="e004e-838">Measure the target using a spectrophotometer, and convert the measurements to CIELUV space.</span></span>
3.  <span data-ttu-id="e004e-839">Construisez la carte de transfert de l’image CMJN vers Luv.</span><span class="sxs-lookup"><span data-stu-id="e004e-839">Construct the forward map from CMYK to Luv.</span></span>
4.  <span data-ttu-id="e004e-840">Utilisez la carte de transfert pour construire un ensemble de CMJ à Luv Maps pour une plage de valeurs K.</span><span class="sxs-lookup"><span data-stu-id="e004e-840">Use the forward map to construct a set of CMY to Luv maps for a range of K values.</span></span>
5.  <span data-ttu-id="e004e-841">Pour toute valeur Luv d’entrée, la valeur CMJN correspondante est obtenue en sélectionnant l’une des cartes construites à l’étape 4 ci-dessus et en l’inversant à l’aide de la méthode de Newton pour obtenir un jeu de couleurs CMJ pour accompagner la valeur K sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e004e-841">For any input Luv value, the corresponding CMYK value is obtained by selecting one of the maps constructed in step 4 above and inverting using Newton's method to obtain a CMY colorant set to accompany the K value selected.</span></span>

<span data-ttu-id="e004e-842">Les étapes 1 et 2, qui sont des procédures standard, sont effectuées par un programme de profilage qui ne fait pas partie de la nouvelle CTE.</span><span class="sxs-lookup"><span data-stu-id="e004e-842">Steps 1 and 2, which are standard procedures, are performed by a profiling program that is not part of the new CTE.</span></span> <span data-ttu-id="e004e-843">La cible IT 8.7/3 contient un échantillonnage raisonnablement détaillé de toutes les valeurs CMJN à différents niveaux de C, M, Y et K. vous pouvez également utiliser une cible personnalisée avec un échantillonnage uniforme des canaux C, M, Y et K.</span><span class="sxs-lookup"><span data-stu-id="e004e-843">The IT8.7/3 target contains a reasonably detailed sampling of all the CMYK values at various levels of C, M, Y, and K. Alternatively, a custom target with uniform sampling of the C, M, Y, and K channels can be used.</span></span> <span data-ttu-id="e004e-844">Une fois la cible imprimée, un spectrophotomètre ou un colorimeter peut être utilisé pour mesurer la valeur XYZ de chaque correctif, et la valeur XYZ peut être convertie en valeur Luv à l’aide du modèle CIELUV.</span><span class="sxs-lookup"><span data-stu-id="e004e-844">After the target is printed, a spectrophotometer or colorimeter can be used to measure the XYZ value of each patch, and the XYZ value can be converted to the Luv value using the CIELUV model.</span></span>

<span data-ttu-id="e004e-845">L’étape 3, la construction de la carte de transfert de type CMJN à Luv, peut être obtenue en appliquant une technique d’interpolation connue, telle que tetrahedral ou une méthode multilinéaire, sur la grille rectangulaire de l’espace CMJN.</span><span class="sxs-lookup"><span data-stu-id="e004e-845">Step 3, construction of the forward map from CMYK to Luv, can be achieved by applying any known interpolation technique, such as tetrahedral or multilinear method, on the rectangular grid in CMYK space.</span></span> <span data-ttu-id="e004e-846">Dans la nouvelle CTE, une interpolation tetrahedral à quatre dimensions est utilisée.</span><span class="sxs-lookup"><span data-stu-id="e004e-846">In the new CTE, a 4-dimensional tetrahedral interpolation is used.</span></span> <span data-ttu-id="e004e-847">Étant donné que les grilles d’échantillonnage CMJ sont généralement différentes à chaque niveau de K, toutefois, nous utilisons une technique de Super-échantillonnage, comme indiqué ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e004e-847">Because the CMY sampling grids are generally different on each level of K, however, we use a technique of super-sampling, as detailed below.</span></span> <span data-ttu-id="e004e-848">Pour un point CMJN donné, les niveaux d’intercalaire K sont déterminés en priorité en fonction de la valeur K.</span><span class="sxs-lookup"><span data-stu-id="e004e-848">For a given CMYK point, the sandwiching K levels are first determined based on the K value.</span></span> <span data-ttu-id="e004e-849">Introduisez ensuite une « super-grille » sur chaque niveau K qui est une Union des grilles de CMJ sur chacun des deux niveaux K.</span><span class="sxs-lookup"><span data-stu-id="e004e-849">Then introduce a "super-grid" on each K level that is a union of the CMY grids on each of the two K levels.</span></span> <span data-ttu-id="e004e-850">À chaque niveau K, la valeur Luv de tout nouveau point de grille récemment introduit est obtenue par une interpolation tetrahedral à 3 dimensions dans ce niveau K.</span><span class="sxs-lookup"><span data-stu-id="e004e-850">On each K level, the Luv value of any newly introduced grid point is obtained by a 3-dimensional tetrahedral interpolation within that K level.</span></span> <span data-ttu-id="e004e-851">Enfin, une interpolation tetrahedral à quatre dimensions pour le point CMJN spécifique est effectuée sur cette nouvelle grille.</span><span class="sxs-lookup"><span data-stu-id="e004e-851">Finally, a 4-dimensional tetrahedral interpolation for the specific CMYK point is performed on this new grid.</span></span>

![Diagramme illustrant l’échantillonnage.](images/cdmp-image163.png)

<span data-ttu-id="e004e-853">**Figure 8** : superéchantillonnage</span><span class="sxs-lookup"><span data-stu-id="e004e-853">**Figure 8** : Supersampling</span></span>

<span data-ttu-id="e004e-854">L’étape 4 crée un ensemble de tables de recherche de CMJ à Luv (LUTs).</span><span class="sxs-lookup"><span data-stu-id="e004e-854">Step 4 constructs a set of CMY-to-Luv lookup tables (LUTs).</span></span> <span data-ttu-id="e004e-855">La carte de transfert construite à l’étape 3 est appelée à plusieurs reprises pour rééchantillonner l’espace CMJN.</span><span class="sxs-lookup"><span data-stu-id="e004e-855">The forward map constructed in Step 3 is called repeatedly to resample the CMYK space.</span></span> <span data-ttu-id="e004e-856">L’espace colorimétrique CMJN est échantillonné à l’aide d’un espacement pair de K et d’un autre, mais toujours espacés, de manière uniforme, par échantillonnage de CMJ.</span><span class="sxs-lookup"><span data-stu-id="e004e-856">The CMYK color space is sampled using an even spacing of K and a different, but still evenly spaced, sampling of CMY.</span></span>

<span data-ttu-id="e004e-857">L’étape 5 est une procédure permettant d’obtenir la valeur CMYK à l’aide du LUTs construit à l’étape 4 pour tout point de Luv d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e004e-857">Step 5 is a procedure to obtain the CMYK value using the LUTs constructed in Step 4 for any input Luv point.</span></span> <span data-ttu-id="e004e-858">La valeur appropriée de K est choisie en analysant la clarté et le degré de couleur dans le Luv demandé.</span><span class="sxs-lookup"><span data-stu-id="e004e-858">The appropriate value of K is chosen by analyzing the lightness as well as the degree of color in the Luv requested.</span></span> <span data-ttu-id="e004e-859">Une fois la table sélectionnée, les valeurs CMJ sont obtenues à partir de la table à l’aide de la méthode de Newton (comme indiqué dans le modèle de périphérique d’imprimante RVB plus haut).</span><span class="sxs-lookup"><span data-stu-id="e004e-859">After the table is selected, the CMY values are obtained from the table by using Newton's method (as documented under the RGB printer device model earlier).</span></span>

<span data-ttu-id="e004e-860">L’espace CIELUV est utilisé dans le modèle d’imprimante au lieu de CIEJab, car le modèle d’appareil doit être basé uniquement sur des données colorimétriques disponibles dans DMP.</span><span class="sxs-lookup"><span data-stu-id="e004e-860">CIELUV space is used in the printer model instead of CIEJab because the device model should be based solely on colorimetric data available in the DMP.</span></span> <span data-ttu-id="e004e-861">Le DMP contient des données colorimétriques pour chaque correctif mesuré, y compris le point blanc du média. il est donc possible de convertir les données CIEXYZ en données CIELUV.</span><span class="sxs-lookup"><span data-stu-id="e004e-861">The DMP contains colorimetric data for each measured patch, including the media white point, so it is possible to convert CIEXYZ data into CIELUV data.</span></span> <span data-ttu-id="e004e-862">Toutefois, il n’est pas possible de convertir en CIECAM02 JCh ou Jab, car il n’y a pas accès aux informations de condition d’affichage dans le DMP.</span><span class="sxs-lookup"><span data-stu-id="e004e-862">However, it is not possible to convert to CIECAM02 JCh or Jab, because there is no access to the viewing condition information in the DMP.</span></span>

### <a name="rgb-projector-device-model-baseline"></a><span data-ttu-id="e004e-863">Ligne de base du modèle d’appareil projecteur RVB</span><span class="sxs-lookup"><span data-stu-id="e004e-863">RGB Projector Device Model Baseline</span></span>

<span data-ttu-id="e004e-864">Remarque : un grand nombre de projecteurs RGB ont plusieurs modes d’opération.</span><span class="sxs-lookup"><span data-stu-id="e004e-864">Note: Many RGB projectors have more than one operating mode.</span></span> <span data-ttu-id="e004e-865">Dans un mode, qui est souvent la valeur par défaut et peut être appelé « présentation », la réponse couleur du projecteur est optimisée pour une luminosité maximale.</span><span class="sxs-lookup"><span data-stu-id="e004e-865">In one mode, which is often the default and might be called something like "presentation," the color response of the projector is optimized for maximum brightness.</span></span> <span data-ttu-id="e004e-866">Toutefois, dans ce mode, le projecteur perd la capacité de reproduire des couleurs légères, légèrement chromatiques, telles que des jaunes pâles et des tons chair.</span><span class="sxs-lookup"><span data-stu-id="e004e-866">However, in this mode, the projector loses the ability to reproduce light, slightly chromatic colors such as pale yellows and some flesh tones.</span></span> <span data-ttu-id="e004e-867">Dans un autre mode, souvent appelé « film », « vidéo » ou « sRVB », le projecteur est optimisé pour la reproduction d’images réalistes et de scènes naturelles.</span><span class="sxs-lookup"><span data-stu-id="e004e-867">In another mode, often called "film," "video," or "sRGB," the projector is optimized for reproduction of realistic images and natural scenes.</span></span> <span data-ttu-id="e004e-868">Dans ce mode, la luminosité maximale est compromise pour améliorer la qualité globale de la reproduction des couleurs.</span><span class="sxs-lookup"><span data-stu-id="e004e-868">In this mode, maximum brightness is traded off to improve the overall quality of the color reproduction.</span></span> <span data-ttu-id="e004e-869">Pour obtenir une reproduction des couleurs satisfaisante avec les projecteurs RGB, il est nécessaire de placer le projecteur dans un mode dans lequel une gamme lisse de couleurs peut être reproduite.</span><span class="sxs-lookup"><span data-stu-id="e004e-869">To obtain satisfactory color reproduction with RGB projectors, it is necessary to place the projector in a mode where a smooth gamut of colors can be reproduced.</span></span>

![Diagramme illustrant un modèle d’appareil D L P.](images/cdmp-image167.png)

<span data-ttu-id="e004e-871">**Figure 9** : modèle d’appareil DLP</span><span class="sxs-lookup"><span data-stu-id="e004e-871">**Figure 9** : DLP device model</span></span>

<span data-ttu-id="e004e-872">Une valeur RVB entrante passe par deux chemins de calcul.</span><span class="sxs-lookup"><span data-stu-id="e004e-872">An incoming RGB value passes through two computational pathways.</span></span> <span data-ttu-id="e004e-873">La première est le modèle de matrice, qui produit une valeur XYZ.</span><span class="sxs-lookup"><span data-stu-id="e004e-873">The first is the matrix model, which results in an XYZ value.</span></span> <span data-ttu-id="e004e-874">Cela est immédiatement suivi par la conversion de XYZ en Luv.</span><span class="sxs-lookup"><span data-stu-id="e004e-874">This is immediately followed by the conversion from XYZ to Luv.</span></span> <span data-ttu-id="e004e-875">La seconde est l’interpolation de LUT non uniforme à l’aide de l’interpolation tetrahedral.</span><span class="sxs-lookup"><span data-stu-id="e004e-875">The second is the non-uniform LUT interpolation using tetrahedral interpolation.</span></span> <span data-ttu-id="e004e-876">La sortie de l’interpolation est déjà dans Luv Space par construction.</span><span class="sxs-lookup"><span data-stu-id="e004e-876">The output of the interpolation is already in Luv space by construction.</span></span> <span data-ttu-id="e004e-877">Les deux sorties sont ajoutées pour obtenir la valeur Luv prédite.</span><span class="sxs-lookup"><span data-stu-id="e004e-877">The two outputs are added to obtain the predicted Luv value.</span></span> <span data-ttu-id="e004e-878">Elle est finalement convertie en XYZ, qui est la sortie attendue du modèle de colorimétrie pour l’appareil DLP.</span><span class="sxs-lookup"><span data-stu-id="e004e-878">This is finally converted to XYZ, which is the expected output of the colorimetric model for the DLP device.</span></span>

<span data-ttu-id="e004e-879">Étant donné que les projecteurs sont des appareils d’affichage, ils prennent également en charge l’inversion du modèle, autrement dit, la transformation de XYZ en RVB.</span><span class="sxs-lookup"><span data-stu-id="e004e-879">Since projectors are display devices, they also support the inversion of the model, that is, the transform from XYZ to RGB.</span></span> <span data-ttu-id="e004e-880">Étant donné que le modèle d’appareil transforme l’espace RVB en espace XYZ, qui sont tous deux unidimensionnels, l’inversion est équivalente à la résolution de trois équations non linéaires en trois inconnues.</span><span class="sxs-lookup"><span data-stu-id="e004e-880">Because the device model transforms RGB space to XYZ space, which are both three dimensional, inversion is equivalent to solving three nonlinear equations in three unknowns.</span></span> <span data-ttu-id="e004e-881">Cela peut être effectué par des techniques de résolution d’équations standard, telles que Newton-Raphson.</span><span class="sxs-lookup"><span data-stu-id="e004e-881">This can done by standard equation solving techniques, such as Newton-Raphson.</span></span> <span data-ttu-id="e004e-882">Toutefois, il est préférable de convertir d’abord XYZ en Luv, puis d’inverser la transformation Luv en RGB, car l’espace Luv est plus RECEPTEUR que l’espace XYZ.</span><span class="sxs-lookup"><span data-stu-id="e004e-882">It is preferable, however, to first convert XYZ to Luv, and then invert the Luv To RGB transform, because Luv space is more perceptually linear than XYZ space.</span></span>

### <a name="icc-device-model-baseline"></a><span data-ttu-id="e004e-883">Ligne de base du modèle d’appareil ICC</span><span class="sxs-lookup"><span data-stu-id="e004e-883">ICC Device Model Baseline</span></span>

<span data-ttu-id="e004e-884">L’interopérabilité du flux de travail ICC est activée en créant un profil de modèle de ligne de base d’appareil ICC spécial qui stocke l’objet de profil et crée une transformation ICC à l’aide d’un profil non-op XYZ.</span><span class="sxs-lookup"><span data-stu-id="e004e-884">The CITE ICC workflow interoperability is enabled by creating a special ICC device baseline device model profile that stores the profile object and creates a ICC transform using a no-op XYZ profile.</span></span> <span data-ttu-id="e004e-885">Cette transformation est ensuite utilisée pour la conversion entre les couleurs des appareils et des CIEXYZ.</span><span class="sxs-lookup"><span data-stu-id="e004e-885">This transform is then used to translate between device and CIEXYZ colors.</span></span>

![Diagramme illustrant l’interopérabilité du flux de travail c I T e I c.](images/cdmp-image168.png)

<span data-ttu-id="e004e-887">**Figure 10** : citez l’interopérabilité des flux de travail ICC</span><span class="sxs-lookup"><span data-stu-id="e004e-887">**Figure 10** : CITE ICC Workflow Interoperability</span></span>

## <a name="related-topics"></a><span data-ttu-id="e004e-888">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e004e-888">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e004e-889">Concepts de base de la gestion des couleurs</span><span class="sxs-lookup"><span data-stu-id="e004e-889">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="e004e-890">Schémas et algorithmes du système de couleurs Windows</span><span class="sxs-lookup"><span data-stu-id="e004e-890">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





