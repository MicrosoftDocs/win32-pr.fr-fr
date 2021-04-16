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
# <a name="wcs-color-device-model-profile-schema-and-algorithms"></a>Algorithmes et schéma de profil de modèle d’appareil de couleur WCS

Cette rubrique fournit des informations sur le schéma de profil de modèle de périphérique de couleur WCS et les algorithmes qui lui sont associés.

Cette rubrique contient les sections suivantes :

-   [Vue d’ensemble](#overview)
-   [Architecture du profil de modèle de périphérique en couleurs](#color-device-model-profile-architecture)
-   [Schéma CDMP](#the-cdmp-schema)
-   [Ajout d’étalonnage à WCS CDMP v 2.0](#wcs-cdmp-v20-calibration-addition)
-   [Éléments du schéma CDMP](#the-cdmp-schema-elements)
    -   [ColorDeviceModelProfile](#colordevicemodelprofile)
    -   [ColorDeviceModel](#colordevicemodelprofile)
    -   [NamespaceVersion](#namespaceversion)
    -   [Version](#namespaceversion)
    -   [Documentation](#documentation)
    -   [Élément CRTDevice](#crtdevice-element)
    -   [Élément LCDDevice](#lcddevice-element)
    -   [Élément ProjectorDevice](#projectordevice-element)
    -   [Élément ScannerDevice](#scannerdevice-element)
    -   [Élément CameraDevice](#cameradevice-element)
    -   [Élément RGBPrinterDevice](#rgbprinterdevice-element)
    -   [Élément CMYKPrinterDevice](#cmykprinterdevice-element)
    -   [Élément RGBVirtualDevice](#rgbvirtualdevice-element)
    -   [PlugInDeviceType](#plugindevicetype)
    -   [RGBVirtualMeasurementType](#rgbvirtualmeasurementtype)
    -   [GammaType](#gammatype)
    -   [GammaOffsetGainType](#gammaoffsetgaintype)
    -   [GammaOffsetGainLinearGainType](#gammaoffsetgainlineargaintype)
    -   [ToneResponseCurvesType](#toneresponsecurvestype)
    -   [GamutBoundarySamplesType](#gamutboundarysamplestype)
    -   [FloatPairList](#floatpairlist)
    -   [CMYKPrinterMeasurementType](#cmykprintermeasurementtype)
    -   [RGBPrinterMeasurementType](#rgbprintermeasurementtype)
    -   [RGBCaptureMeasurementType](#rgbcapturemeasurementtype)
    -   [OneBasedIndex](#onebasedindex)
    -   [RGBProjectorMeasurementType](#rgbprojectormeasurementtype)
    -   [DisplayMeasurementType](#displaymeasurementtype)
    -   [MeasurementConditionsType](#measurementconditionstype)
    -   [GeometryType](#geometrytype)
    -   [RGBPrimariesGroup](#rgbprimariesgroup)
    -   [NonNegativeCMYKSampleType](#nonnegativecmyksampletype)
    -   [NonNegativeRGBSampleType](#nonnegativergbsampletype)
    -   [NonNegativeCMYKType](#nonnegativecmyktype)
    -   [NonNegativeRGBType](#nonnegativergbtype)
    -   [ExtensionType](#extensiontype)
    -   [NonNegativeXYZType](#nonnegativexyztype)
    -   [XYZType](#nonnegativexyztype)
-   [Algorithmes de base CDMP](#the-cdmp-baseline-algorithms)
    -   [Ligne de base du modèle de périphérique CRT](#crt-device-model-baseline)
    -   [Ligne de base du modèle d’appareil LCD](#lcd-device-model-baseline)
    -   [Ligne de base du modèle d’imprimante RVB](#rgb-printer-device-model-baseline)
    -   [Ligne de base du modèle d’appareil virtuel RGB](#rgb-virtual-device-model-baseline)
    -   [Ligne de base modèle de périphérique d’imprimante CMJN](#cmyk-printer-device-model-baseline)
    -   [Ligne de base du modèle d’appareil projecteur RVB](#rgb-projector-device-model-baseline)
    -   [Ligne de base du modèle d’appareil ICC](#icc-device-model-baseline)
-   [Rubriques connexes](#related-topics)

## <a name="overview"></a>Vue d’ensemble

Ce schéma est utilisé pour spécifier le contenu d’un profil de modèle de périphérique en couleurs (CDMP). Les algorithmes de base de référence associés sont décrits ci-dessous.

Le schéma DMP (Device Model Profile) de base se compose des données de mesure d’échantillonnage.

Le composant d’échantillonnage du schéma XML DMP assure la prise en charge des cibles de mesure de couleur de base, en se concentrant sur des cibles standard et des cibles optimisées pour les modèles d’appareil de base.

En outre, le profil d’appareil fournit des informations spécifiques sur le modèle d’appareil ciblé et fournit une stratégie que le modèle d’appareil de secours de base peut utiliser si le modèle ciblé n’est pas disponible. Les instances de profil peuvent inclure des extensions privées à l’aide de mécanismes d’extension XML standard.

## <a name="color-device-model-profile-architecture"></a>Architecture du profil de modèle de périphérique en couleurs

![Diagramme qui affiche les informations qui constituent un profil de modèle d’appareil.](images/cdmp-image002new.png)

## <a name="the-cdmp-schema"></a>Schéma CDMP


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



## <a name="wcs-cdmp-v20-calibration-addition"></a>Ajout d’étalonnage à WCS CDMP v 2.0

L’élément **ColorDeviceModel** du schéma CDMP a été mis à jour dans Windows 7 pour inclure le nouvel élément d’étalonnage. L’exemple suivant montre la modification apportée au schéma CDMP.


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



## <a name="the-cdmp-schema-elements"></a>Éléments du schéma CDMP

> [!Note]  
> Les primaires sont des exemples principaux de rouge, vert, bleu, noir et blanc. Une rampe principale est une rampe tonale de la luminance la plus faible à la valeur principale complète. Le nombre maximal d’entrées dans une rampe de fréquences est 4096.

 

> [!Note]  
> Les données de mesure doivent être DMPs.

 

### <a name="colordevicemodelprofile"></a>ColorDeviceModelProfile

Cet élément est de type ColorDeviceModel.

**Conditions de validation :** Chaque sous-élément est validé par son propre type.

### <a name="colordevicemodel"></a>ColorDeviceModel

Cet élément est une séquence des sous-éléments suivants

1.  Chaîne ProfileName,
2.  chaîne de description facultative,
3.  chaîne d’auteur facultative,
4.  MeasurementConditions facultatif MeasurementConditionsType,
5.  Self-Luminous valeur booléenne,
6.  MaxColorant float,
7.  MinColorant float,
8.  Choix des éléments
    1.  CRTDevice,
    2.  LCDDevice,
    3.  RGBProjectorDevice,
    4.  ScannerDevice,
    5.  CameraDevice,
    6.  RGBPrinterDevice,
    7.  CMYKPrinterDevice,
    8.  RGBVirtualDevice,
9.  PlugInDevice,
10. ExtensionType d’extension facultatif

**Conditions de validation :** Chaque sous-élément est validé par son propre type. Les sous-éléments de chaîne ont un maximum de 10 000 caractères. Le sous-élément MaxColorant doit être supérieur ou égal à zéro (0) et supérieur au sous-élément MinColorant. Le MinColorant peut être négatif.

### <a name="namespaceversion"></a>NamespaceVersion

xmlns : CDM = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel "

### <a name="version"></a>Version

Version = « 1,0 » avec Windows Vista.

**Conditions de validation :** Toute valeur de version &gt; 0,1 ou &lt; = 2,0 est valide pour prendre en charge des modifications sans rupture au format.

### <a name="documentation"></a>Documentation

Schéma de profil de modèle d’appareil.

Copyright (C) Microsoft. Tous droits réservés.

### <a name="crtdevice-element"></a>Élément CRTDevice

Cet élément est une séquence de sous-éléments d’un DisplayMeasurementType MeasurementData.

**Conditions de validation :** Chaque sous-élément est validé par son propre type.

### <a name="lcddevice-element"></a>Élément LCDDevice

Cet élément est une séquence de sous-éléments d’un DisplayMeasurementType MeasurementData.

**Conditions de validation :** Chaque sous-élément est validé par son propre type.

### <a name="projectordevice-element"></a>Élément ProjectorDevice

Cet élément est une séquence de sous-éléments d’un RGBProjectorMeasurementType MeasurementData.

**Conditions de validation :** Chaque sous-élément est validé par son propre type.

### <a name="scannerdevice-element"></a>Élément ScannerDevice

Cet élément est une séquence de sous-éléments d’un RGBCaptureMeasurementType MeasurementData

**Conditions de validation :** Chaque sous-élément est validé par son propre type.

### <a name="cameradevice-element"></a>Élément CameraDevice

Cet élément est une séquence de sous-éléments d’un RGBCaptureMeasurementType MeasurementData

**Conditions de validation :** Chaque sous-élément est validé par son propre type.

### <a name="rgbprinterdevice-element"></a>Élément RGBPrinterDevice

Cet élément est une séquence de sous-éléments d’un RGBPrinterMeasurementType MeasurementData.

**Conditions de validation :** Chaque sous-élément est validé par son propre type.

### <a name="cmykprinterdevice-element"></a>Élément CMYKPrinterDevice

Cet élément est une séquence de sous-éléments d’un CMYKPrinterMeasurementType MeasurementData.

**Conditions de validation :** Chaque sous-élément est validé par son propre type.

### <a name="rgbvirtualdevice-element"></a>Élément RGBVirtualDevice

Cet élément est une séquence de sous-éléments d’un RGBVirtualMeasurementDataType.

**Conditions de validation :** Chaque sous-élément est validé par son propre type.

### <a name="plugindevicetype"></a>PlugInDeviceType

Cet élément est une séquence d’un GUID GUIDType et de tous les sous-éléments.

**Conditions de validation :** Le GUID est utilisé pour faire correspondre le GUID de la dll du plug-in DM. Il y a un maximum de 100 000 sous-éléments personnalisés.

### <a name="rgbvirtualmeasurementtype"></a>RGBVirtualMeasurementType

Cet élément est une séquence composée de

1.  Groupe RGBPrimariesGroup
2.  Choix de
3.  -   Gamma
    -   GammaOffsetGain
    -   GammaOffsetGainLinearGam
    -   Éléments ToneResponseCurves

4.  GamutBoundarySamples facultatif GamutBoundarySamplesType
5.  Date/heure TimeStamp

**Conditions de validation :** Chaque sous-élément de ces types a ses propres conditions de validation.

### <a name="gammatype"></a>GammaType

Cet élément est un type complexe constitué de l’attribut

-   NonNegativeFloatType gamma

**Conditions de validation :** À déterminer à partir des commentaires du secteur.

### <a name="gammaoffsetgaintype"></a>GammaOffsetGainType

Cet élément est un type complexe constitué des attributs

-   NonNegativeFloatType gamma
-   Décalage NonNegativeFloatType
-   Obtenir NonNegativeFloatType

**Conditions de validation :** À déterminer à partir des commentaires du secteur.

### <a name="gammaoffsetgainlineargaintype"></a>GammaOffsetGainLinearGainType

Cet élément est un type complexe constitué des attributs

-   NonNegativeFloatType gamma
-   Décalage NonNegativeFloatType
-   Obtenir NonNegativeFloatType
-   LinearGain NonNegativeFloatType
-   TransitionPoint NonNegativeFloatType.

**Conditions de validation :** À déterminer à partir des commentaires du secteur.

### <a name="toneresponsecurvestype"></a>ToneResponseCurvesType

Cet élément est une séquence de

1.  RedTRC FloatPairList
2.  GreenTRC FloatPairList
3.  BlueTRC FloatPairList

L’élément a également un attribut TRCLength de type unsignedInt.

**Conditions de validation :** À déterminer à partir des commentaires du secteur.

### <a name="gamutboundarysamplestype"></a>GamutBoundarySamplesType

Cet élément est une séquence de RGBTypes RVB.

**Conditions de validation :** Les occurrences maximales non liées sont actuellement limitées en fonction des commentaires du secteur.

### <a name="floatpairlist"></a>FloatPairList

Cet élément est un type simple de liste de paires de valeurs float.

**Conditions de validation :** À déterminer à partir des commentaires du secteur.

### <a name="cmykprintermeasurementtype"></a>CMYKPrinterMeasurementType

Cet élément est un

1. séquence de l’élément ColorCube constitué d’une séquence d’exemples de NonNegativeCMYKSampleType

2. Attribut dateTime TimeStamp.

**Conditions de validation :** À déterminer à partir des commentaires du secteur.

### <a name="rgbprintermeasurementtype"></a>RGBPrinterMeasurementType

Cet élément est un

1. séquence de l’élément ColorCube constitué d’une séquence d’exemples de NonNegativeRGBSampleType

2. Attribut dateTime TimeStamp.

**Conditions de validation :** À déterminer à partir des commentaires du secteur.

### <a name="rgbcapturemeasurementtype"></a>RGBCaptureMeasurementType

Cet élément est une séquence de

1.  ComplexType PrimaryIndex de
2.  1.  OneBasedIndex blanc
    2.  OneBasedIndex noir facultatif
    3.  OneBasedIndex rouge facultatif
    4.  OneBasedIndex vert facultatif
    5.  OneBasedIndex bleu facultatif
    6.  OneBasedIndex cyan facultatif
    7.  OneBasedIndex magenta facultatif
    8.  OneBasedIndex jaune facultatif

3.  NeutralIndices de lignes de OneBasedIndex
4.  Séquence ColorSamples de l’exemple de NonNegativeRGBSampleType

L’élément a également un attribut dateTime TimeStamp.

**Conditions de validation :** À déterminer à partir des commentaires du secteur.

### <a name="onebasedindex"></a>OneBasedIndex

Cet élément est un type simple de base de restriction unsigned int avec la valeur minInclusive = "1."

**Conditions de validation :** À déterminer à partir des commentaires du secteur.

### <a name="rgbprojectormeasurementtype"></a>RGBProjectorMeasurementType

Cet élément est une séquence de

1.  Groupe RGBPrimariesGroup
2.  élément ColorSamples constitué d’une séquence d’exemples de NonNegativeRGBSampleType

L’élément a également un attribut dateTime TimeStamp.

**Conditions de validation :** À déterminer à partir des commentaires du secteur.

### <a name="displaymeasurementtype"></a>DisplayMeasurementType

Cet élément est une séquence de

1.  RGBPrimariesGroup de groupe
2.  GrayRamp de la séquence de l’exemple de NonNegativeRGBType
3.  RedRamp de la séquence de l’exemple de NonNegativeRGBType
4.  GreenRamp de la séquence de l’exemple de NonNegativeRGBType
5.  BlueRamp de la séquence de l’exemple de NonNegativeRGBType

L’élément DisplayMeasurementType a également un attribut dateTime TimeStamp.

**Conditions de validation :** À déterminer à partir des commentaires du secteur.

### <a name="measurementconditionstype"></a>MeasurementConditionsType

Le MeasurementConditionsType est une séquence de sous-éléments qui contient :

1.  Valeur d’énumération de chaîne restreinte ColorSpace « CIEXYZ »
2.  choix facultatif de l’énumération de chaînes WhitePoint NonNegativeXYZType ou WhitePointName de valeurs D50, D65, A ou F2
3.  GeometryType Geometry
4.  Entier ApertureSize en millimètres

Valeurs par défaut :

1.  Imprimantes RVB et CMJN :
    1.  CIEXYZ MeasurementSpaceType
    2.  WhitePointValue D50
    3.  0/45 GeometryType
    4.  10mm ApertureSize
2.  Scanneurs
    1.  CIEXYZ MeasurementSpaceType
    2.  WhitePointValue D50
    3.  0/45 GeometryType
    4.  10mm ApertureSize
3.  Affiche et appareil virtuel RGB :
    1.  CIEXYZ MeasurementSpaceType
    2.  D65 WhitePointValue
    3.  0/45 GeometryType
    4.  10mm ApertureSize
4.  Appareil
    1.  CIEXYZ MeasurementSpaceType
    2.  D65 WhitePointValue
    3.  GeometryType directe
    4.  10mm ApertureSize

**Conditions de validation :** La validation de chaque sous-élément est déterminée par les conditions de validation pour ces sous-éléments. Si un sous-élément est manquant, le type de modèle d’appareil spécifique par défaut est utilisé.

### <a name="geometrytype"></a>GeometryType

String

Valeurs d’énumération :

-   « 0/45 »
-   « 0/diffus »
-   « diffuse/0 »
-   Directe

**Conditions de validation :** Toute valeur, à l’exception des valeurs enumberation listées, n’est pas valide. Ces informations ne modifient pas le comportement de traitement de la ligne de base.

### <a name="rgbprimariesgroup"></a>RGBPrimariesGroup

Cet élément est une séquence de

1.  WhitePrimary NonNegativeXYZType
2.  RedPrimary NonNegativeXYZType
3.  GreenPrimary NonNegativeXYZType
4.  BluePrimary NonNegativeXYZTYpe
5.  BlackPrimary NonNegativeXYZType

**Conditions de validation :** À déterminer à partir des commentaires du secteur.

### <a name="nonnegativecmyksampletype"></a>NonNegativeCMYKSampleType

Cet élément est une séquence de

1.  NonNegativeCMYKType CMJN
2.  CIEXYZ NonNegativeXYZType

L’élément a également une chaîne d’étiquette d’attribut facultative

**Conditions de validation :** À déterminer à partir des commentaires du secteur.

### <a name="nonnegativergbsampletype"></a>NonNegativeRGBSampleType

Cet élément est une séquence de

1.  NonNegativeRGBType RVB
2.  CIEXYZ NonNegativeXYZType

L’élément a également une chaîne d’étiquette d’attribut facultative

**Conditions de validation :** À déterminer à partir des commentaires du secteur.

### <a name="nonnegativecmyktype"></a>NonNegativeCMYKType

Cet élément se compose d’attributs

1.  Virgule flottante C
2.  Virgule flottante
3.  Virgule flottante Y
4.  Virgule flottante

**Conditions de validation :** À déterminer à partir des commentaires du secteur.

### <a name="nonnegativergbtype"></a>NonNegativeRGBType

Cet élément se compose d’attributs

1.  Valeur float R
2.  Virgule flottante G
3.  Virgule flottante B

**Conditions de validation :** À déterminer à partir des commentaires du secteur.

### <a name="extensiontype"></a>ExtensionType

L’élément ExtensionType est une séquence de tout type de sous-élément et est utilisé pour les informations propriétaires d’applications non-Microsoft.

**Conditions de validation :** Cet élément est facultatif. Il peut y avoir un maximum de 1000 sous-éléments d’extension.

### <a name="nonnegativexyztype"></a>NonNegativeXYZType

L’élément NonNegativeXYZType est composé de NonNegativeFloatType trois éléments à virgule flottante IEEE simple précision nommés « X », « Y » et « Z ». Ces valeurs sont limitées aux valeurs de mesure des profils DMP. Ces mesures peuvent être absolues (non relatives) CIEXYZ 1931 valeurs réfléchissantes ou valeurs réfléchies absolues (non relatives) CIEXYZ 1931 (transmissif) dans candelas par unités au carré du compteur.

**Conditions de validation :** Seules les valeurs réelles sont valides, et les valeurs de mesure CIEXYZ négatives ne sont pas valides. Comme il s’agit de valeurs absolues, les valeurs peuvent être supérieures à 1,0 f. Limite raisonnable pour n’importe quel « X », « Y » ou « Z ». la valeur est arbitrairement définie sur 10000.0 f.

### <a name="xyztype"></a>XYZType

L’élément XYZType est composé de trois valeurs à virgule flottante IEEE simple précision : « X », « Y » et « Z ».

## <a name="the-cdmp-baseline-algorithms"></a>Algorithmes de base CDMP

### <a name="crt-device-model-baseline"></a>Ligne de base du modèle de périphérique CRT

Pour comprendre ce modèle, vous devez prendre en compte le processus de caractérisation et la modélisation de l’appareil. Dans le processus de caractérisation, les mesures XYZ sont d’abord effectuées sur les couleurs obtenues en remplissant la mémoire tampon d’affichage d’un périphérique d’affichage CRT. Les exemples de valeurs suivants génèrent des données correctes pour le modèle d’appareil CRT de base de référence :

Rouge : R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Vert : G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Blue : B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutres : R = G = B = 0, 8, 16, 32, 64, 128, 192, 255

Vous pouvez également utiliser des incréments autres que 15 et des incréments non linéaires. Chaque rampe rouge, verte, bleue et neutre doit contenir au moins trois échantillons, mais il est recommandé de fournir un plus grand nombre d’échantillons. Vous devez fournir des échantillons pour le rouge pur, le vert, le bleu, le noir et le blanc. Il n’est pas nécessaire que les exemples soient uniformément espacés.

Le processus de création de la matrice tristimulus se compose de deux étapes. Tout d’abord, évaluez la valeur du point noir XYZ ou le halo. Cette étape est principalement basée sur le travail de Bernes \[ 3 \] avec une fonction d’objectif légèrement modifiée pour l’optimisation non linéaire. Ensuite, calculez la matrice tristimulus en fonction du résultat de l’étape 1 et également d’un calcul de la moyenne sur toutes les mesures par canal, pas seulement celle du nombre maximal d’unités numériques.

Chacune de ces étapes contient des procédures détaillées. Le point de départ correspond aux rampes (17 étapes dans notre exemple) pour chacun des canaux R, G et B. Lorsque les mesures XYZ sont tracées sur le plan *XY* chromatique, une situation typique est illustrée à la figure 1. La première étape consiste à résoudre un problème d’optimisation non linéaire afin de trouver le point noir le mieux adapté qui réduira la valeur de la chromatique en traversant les canaux R, G et B. En se basant sur les Bernes \[ 3 \] , nous cherchons ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>k</sub>* ) qui minimise la fonction d’objectif suivante :

![Affiche la fonction objective où SR, SG et SB sont l’ensemble de points de données sur les canaux R, G et B.](images/cdmp-formula1.png)

où *s <sub>R</sub>*,*s <sub>G</sub>* et *s <sub>B</sub>* sont l’ensemble de points de données correspondant aux points sur les canaux R, G et b. Pour tous les *ensembles, définissez :*

![Affiche une formule pour la définition de n’importe quel jeu de.](images/cdmp-formula2.png)

Dans le précédent, \| *s* \| est la cardinalité de *s*, c.-à-d., le nombre de points dans le jeu *S*. ![ Affiche une formule pour la chromatique d’un point.](images/cdmp-formula3.png) les coordonnées chromatiques du point ![ montrent un formaula pour un point.](images/cdmp-formula4.png) , ![ affiche donc une formule pour la moyenne ou le centre de masse. ](images/cdmp-formula5.png) , est la moyenne, ou le centre de la masse, de tous les points du jeu *S* dans le plan chromatique. Par conséquent, ![ affiche une formule pour la somme d’un deuxième instant de points.](images/cdmp-formula6.png) somme des deuxièmes moments des points du centre de masse et mesure de la façon dont les points sont répartis. Enfin, ![ affiche une formule pour la mesure totale de la répartition de trois clusters de points.](images/cdmp-formula7.png) est une mesure totale de la répartition des trois clusters de points sur leurs centres respectifs de masse.

Dans, le calcul de ![ affiche une formule f (X, Y, Z ; XK, YK, ZK).](images/cdmp-formula8.png) , si ![ affiche une formule pour X. ](images/cdmp-formula9.png) , le calcul est ignoré et la cardinalité des *S* est ajustée en conséquence.

En dépit de la complexité apparente de la fonction d’objectif, il s’agit d’une somme des carrés de nombreuses fonctions dérivables dans *X <sub>k</sub>*,*Y <sub>k</sub>Z <sub>k</sub>* (17 points 2 *XY* -Components 3 canaux = 102, dans l’exemple) et, par conséquent, est visible pour les techniques de moindres carrés non linéaires standard, telles que l’algorithme Levenberg-Marquardt, qui est l’algorithme Notez que la fonction objective précédente est différente de celle suggérée dans les Bernes \[ 3 \] en ce que cette dernière mesure la variance des distances par rapport au centre de masse, de sorte que la variance soit égale à zéro lorsque les points sont éloignés du centre de masse, même s’ils peuvent l’être. Dans l’exemple, la dispersion des points est convertie directement à l’aide du deuxième instant.

Comme avec n’importe quel algorithme itératif pour le problème des moindres carrés non linéaires, Levenberg-Marquardt nécessite une estimation initiale. Il existe deux candidats évidents. L’un est (0, 0, 0); l’autre est le point noir mesuré. Pour la CTE, le point noir mesuré est utilisé pour la première fois comme estimation initiale. Si un maximum de 100 itérations est dépassé sans atteindre un seuil d’une distance moyenne de 0,001 de chaque point à partir de son centre de masse (qui correspond à une valeur de seuil de (0,001) 17 3 = 0,000051 pour la fonction d’objectif), un autre nombre d’itérations avec l’estimation initiale de (0, 0, 0) est effectué. L’estimation obtenue du point noir est XYZ comparée à la meilleure estimation de l’ancien cycle d’itérations (avec le point noir mesuré comme estimation initiale). Utilisez l’estimation qui donne la plus petite valeur pour la fonction objective. Le choix entre 100 itérations et la distance d’erreur 0,001 ont été sélectionnés de façon empirique. Dans les versions ultérieures, il peut être raisonnable de paramétrer la distance d’erreur.

Le résultat de l’étape 1 est le point noir estimé ( *X <sub>k</sub>*,*Y <sub>k</sub>*,*Z <sub>k</sub>* ). L’étape 2 consiste à déterminer la matrice tristimulus en calculant la moyenne de la chromatique des points dans les trois clusters obtenus à l’étape 1. Pour les CRT, cette opération est effectuée principalement pour réduire les effets des erreurs de mesure. Les points utilisés dans la moyenne de la chromatique doivent être les mêmes que ceux utilisés dans l’optimisation de l’étape 1. En d’autres termes, si le premier point (nombre numérique 15, dans l’exemple) dans chaque rampe est ignoré lors de l’étape d’optimisation, vous devez le faire dans le calcul de la moyenne. Si ![ affiche des formules de la chromatique moyenne pour les coordonnées des canaux rouge et vert.](images/cdmp-formula10.png) , et ![ affiche une formule de la chromatique moyenne des coordonnées dans le canal bleu.](images/cdmp-formula11.png) sont les coordonnées chromatiques moyennes des canaux rouge, vert et bleu, puis la procédure suivante détermine la matrice tristimulus. Tout d’abord, résolvez le système linéaire 3 ? 3 :

![Affiche la première partie de la procédure permettant de résoudre un système linéaire 3 ? 3.](images/cdmp-formula12.png)

![Affiche la deuxième partie du système linéaire 3 ? 3.](images/cdmp-formula13.gif)![Affichez la valeur t indice b à la fin de la deuxième partie du système linéaire 3 ? 3.](images/cdmp-formula14.gif)

*X <sub>w</sub>*,*Y <sub>w</sub>*,*Z <sub>w</sub>*

![Affiche la dernière partie de la procédure permettant de résoudre un système linéaire 3 ? 3.](images/cdmp-formula15.png)

Une fois la matrice tristimulus déterminée, la détermination des courbes de tonalité suit l’approche standard. Pour les affichages CRT, les canaux individuels sont supposés suivre le modèle « GOG » :

![Affiche la formule pour le modèle « G O G ».](images/cdmp-formula16.png)

où *k <sub>g</sub>* est le « gain », 1-*k <sub>g</sub>* est le « décalage », et ? est le « gamma ». La matrice inverse de la matrice tristimulus est appliquée aux données XYZ des neutres pour obtenir les données RVB linéaires, qui sont ensuite corrélées avec les valeurs RVB numériques à l’aide de la régression linéaire sur le modèle GOG. Ces caractéristiques n’ont pas besoin d’être identiques pour les canaux R, G et B, et ne sont généralement pas identiques.

Bernes \[ 1 \] : Bernes, *Billmeyer et Saltzman, principes de la technologie des couleurs*, 3 <sub>rd</sub> Ed. John Wiley & fils (2000).

Bernes \[ 2 \] : Bernes et Katoh, la fonction de transfert numérique à radiométrique pour les affichages CRT contrôlés par ordinateur, le *Congrès d’experts Cie 97 normes de couleur pour la technologie d’imagerie, du* 1997 novembre.

Bernes \[ 3 \] : Bernes, Fernandez et Taplin, estimation Black-Level émissions de Computer-Controlled des affichages, *recherche en couleurs et application*, 28:379-383 Wiley periods, Inc. (2003)

Kang \[ 1 \] : Kang, *technologie de couleur pour les appareils de création d’images électroniques*, SPIE (1997)

Katoh \[ 1 \] : Katoh, Deguchi et Bernes, caractérisation exacte de la proposition du moniteur CRT (II) pour une extension de la méthode Cie et de sa vérification, *opt. Rev.* 8:397-408 (2001)

### <a name="lcd-device-model-baseline"></a>Ligne de base du modèle d’appareil LCD

La ligne de base du modèle d’appareil LCD est semblable à la ligne de base du modèle de périphérique CRT. Cette section explique les différentes façons dont la modélisation LCD diffère de la modélisation CRT.

L’une des différences est que vous ne pouvez pas supposer que les écrans LCD suivent le modèle GOG utilisé pour les CRT, et les courbes de ton sont obtenues par interpolation de données mesurées. Pour cette raison, l’axe neutre de l’appareil doit être échantillonné plus fréquemment.

Voici quelques exemples de valeurs typiques qui peuvent générer de bonnes données pour la ligne de base du modèle d’appareil LCD :

Rouge : R = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, G = B = 0

Vert : G = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = B = 0

Blue : B = 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255, R = G = 0

Neutres : R = G = B = 0, 15, 30, 45, 60, 75, 90, 105, 120, 135, 150, 165, 180, 195, 210, 225, 240, 255.

Le processus de calcul de la moyenne des chromatiques de couleur mesurées pour obtenir les chromatiques des principaux de l’appareil est plus important pour les écrans LCD que pour les écrans CRT. Quand la mesure XYZ est tracée sur le plan *XY* chromatique, une situation classique est illustrée à la figure 1. Notez que la chromatique est dérive vers le point noir. Cela est dû au fait que tous les écrans LCD présentent une certaine perte de lumière.

![Diagramme qui affiche un graphique de la chromatique à l’aide de données brutes sans correction.](images/cdmp-lcd-dmp-figure1.png)

**Figure 1** : diagramme de la chromatique utilisant des données brutes sans correction

Lorsque cela est soustrait des mesures XYZ brutes, une situation classique est représentée à la figure 2. Les points sont maintenant mis en cluster sur trois centres, même s’ils ne sont pas identiques. La méthode de calcul de la moyenne décrite pour les écrans CRT améliore considérablement les résultats des écrans LCD.

![Diagramme qui montre un graphique de la chromatique à l’aide de données brutes avec un point noir ajusté.](images/cdmp-lcd-dmp-figure2.png)

**Figure 2** : diagramme chromatique utilisant des données avec le point noir ajusté

### <a name="rgb-capture-device-model-baseline"></a>Ligne de base du modèle d’appareil de capture RVB

Le modèle de périphérique de capture RVB de base est une sous-classe de la classe IDeviceModel. Dans la caractérisation colorimétrique des appareils de capture des couleurs, tels que les scanneurs et les appareils photo numériques, l’approche suivante est utilisée. Une cible composée de correctifs de couleurs avec des valeurs CIEXYZ connues est capturée à l’aide de l’appareil de capture. Le résultat de la capture est une image bitmap RVB dans laquelle la couleur de chaque correctif est encodée dans une valeur RVB. Ces valeurs RVB d’appareil sont spécifiques à un périphérique de capture particulier. L’objectif de la caractérisation colorimétrique est d’établir une relation empirique entre les valeurs RGB des appareils et les valeurs CIEXYZ, ou une transformation mathématique de RVB à XYZ, qui modélise aussi précisément que possible le comportement de l’appareil de capture.

Une telle transformation mathématique peut être modélisée raisonnablement par des polynomes de faible degré. Cette procédure est détaillée dans la documentation, par exemple Kang \[ 92 \] , Kang \[ 97 \] . Dans Kang \[ 97 \] , une approche est signalée qui utilise un ensemble de trois polynômes avec 3, 6, 8, 9, 11, 14 ou 20 termes dans les variables R, G et B, tandis que les trois Polynomials régresient respectivement dans les composants X, Y et Z de l’espace CIEXYZ. Pour le polynôme à 20 termes, le formulaire est le suivant :

![Affiche le polynôme à 20 termes.](images/cdmp-formula20.png)

Il existe des expressions similaires pour Y et Z. La technique mathématique pour l’ajustement des polynômes se trouve dans la « régression linéaire multivariable » et est décrite dans tout texte élémentaire dans les statistiques.

Cette méthode de régression linéaire souffre de ne pas réduire la fonction d’objectif « Right ». Par défaut, la régression linéaire recherche la solution la moins carrée, ce qui implique que les coefficients obtenus réduisent la somme totale des carrés des erreurs dans l’espace sous-jacent, ou équivalente à la somme des carrés des distances euclidienne. Dans la pratique, vous souhaitez réduire la somme des carrés de ? Es, où ? E est l’une des normes acceptées comme CIE94. La réduction de cette fonction d’objectif est un problème de régression non linéaire.

Dans le nouveau moteur, le laboratoire à XYZ est l’espace de couleurs CIE qui est régressé dans et le polynôme à 20 termes, le polynôme cubique, est utilisé comme modèle pour l’appareil de capture, ou coefficients ls, par exemple BS, de telle sorte que les polynômes suivantes réduisent la somme des carrés de ? E <sub>CIE94</sub> s.

![Affiche un ensemble de formules polynomiaux.](images/cdmp-formula21.png)

La solution ( *l <sub>i</sub>*, *a <sub>i</sub>*, *b <sub>i</sub>* ) dans l’espace de chiffre réel 60 dimensionnel **R** 203 doit être telle que l’erreur totale suivante est réduite :

![Affiche l’erreur totale à réduire.](images/cdmp-formula22.png)

où la somme se fait via toutes les paires de points de données (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>*;*L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* ) dans le jeu de données échantillonnées plus des points de contrôle supplémentaires à prendre en détail dans les éléments suivants. Il s’agit d’un problème de régression non linéaire, car les paramètres *?<sub> Je</sub>*, *a <sub></sub>* i, * <sub>i</sub>* Enter dans la fonction objective de manière non linéaire (pas augmentera).

En raison de la fonction objective ? la fonction est-elle linéaire (et non quadratique) des paramètres *?<sub> Je</sub>*, *a <sub>i</sub>* et * <sub>i</sub>*, vous devez recourir à des techniques itératives pour résoudre le problème d’optimisation. Comme la forme de la fonction objective est une somme des carrés, une technique d’optimisation standard appelée algorithme Levenberg-Marquardt est utilisée. Il est considéré comme la méthode de choix pour les problèmes de moindres carrés non linéaires. Pour les algorithmes itératifs tels que Levenberg-Marquardt, vous devez fournir une estimation initiale. Une bonne hypothèse initiale est généralement essentielle pour trouver la valeur minimale correcte. Dans ce cas, un bon candidat pour l’estimation initiale est la solution du problème de régression linéaire. Tout d’abord, réduisez la somme du carré des distances euclidienne dans l’espace de laboratoire en définissant une fonction d’objectif quadratique :

![Affiche une fonction d’objectif quadratique définie.](images/cdmp-formula23.png)

La solution mathématique de ce type de problème est bien connue. Car *?<sub> Je</sub>* n’apparais qu’dans  la modélisation L *,<sub>je</sub>* n’apparaît que dans la modélisation *u* et * <sub>i</sub>* uniquement dans la modélisation *v* . le problème d’optimisation peut être décomposé en trois sous-problèmes : un pour *L*, un pour *u* et un pour *v*. Examinez les équations *l* . (Les équations *u* et les équations *v* suivent exactement le même argument.) Le problème de la réduction de la somme des carrés des erreurs dans *L* peut être indiqué par la résolution de l’équation matricielle suivante dans le sens le moins évident :

![Affiche une équation de matrice pour L.](images/cdmp-formula24.png)

où *N* est le nombre total de points de données (points d’échantillonnage originaux et points de contrôle créés de la manière décrite ci-dessous). En règle générale, *N* est bien supérieur à 20, donc l’équation précédente est dépendante, ce qui nécessite une solution de moindres carrés. Une solution de formulaire fermée pour **?** est disponible :

![Affiche une solution de formulaire fermée.](images/cdmp-formula25.png)

Dans la pratique, l’évaluation directe à l’aide de la solution de formulaire fermée n’est pas utilisée, car elle comporte des propriétés numériques médiocres. Au lieu de cela, un certain type d’algorithme de factorisation de matrice est appliqué à la matrice de coefficient qui réduit le système d’équations à une forme canonique. Dans l’implémentation actuelle, la décomposition de la valeur singulière (MVP) est appliquée à la matrice **R** , puis le système décomposé résultant est résolu.

La solution au problème de régression linéaire, dénotée par ![ montre la solution au problème de régression linéaire.](images/cdmp-formula26.png) , est utilisé comme point de départ de l’algorithme Levenberg-Marquardt. Dans cet algorithme, une étape d’essai est calculée et doit déplacer le point plus près de la solution optimale. L’étape d’essai remplit un ensemble d’équations linéaires dépendant de la valeur fonctionnelle et des valeurs des dérivés au point actuel. Pour cette raison, les dérivés de la fonction objective ? en ce qui concerne les paramètres *?<sub></sub>j'* ai *besoin <sub></sub> <sub></sub> d’entrées* pour l’algorithme Levenberg-Marquardt. Bien qu’il y ait 60 paramètres, il existe un raccourci qui vous permet de calculer beaucoup moins. Par la règle de chaîne de calcul,

![Affiche une équation qui autorise un raccourci à l’aide de la règle de chaîne de calcul.](images/cdmp-formula27.png)

où *j* = 1, 2,, 20, *L <sub>i</sub>*,*u <sub>i</sub>*,*v <sub>i</sub>* sont la valeur CIELAB du point d’échantillonnage *i* et *R <sub>IJ</sub>* est l’entrée (*i*,*j* ) Th de la matrice **R** définie ci-dessus. Ainsi, au lieu de calculer les dérivés pour les paramètres 60, vous pouvez calculer les dérivés pour *L*, a et *b* à l’aide de *la* différenciation par progression numérique.

Il est également nécessaire de configurer un critère d’arrêt pour les algorithmes itératifs. Dans l’implémentation actuelle, les itérations sont terminées si le DECIE94 carré moyen est inférieur à 1, ou si le nombre d’itérations effectuées a dépassé 10. Le nombre 10 provient de l’expérience pratique selon laquelle si les premières itérations ne réduisent pas de manière significative l’erreur, les itérations supplémentaires ne sont pas encore plus utiles que le déplacement du point de manière oscillatoire, c’est-à-dire que l’algorithme peut ne pas converger. Même dans le cas où l’algorithme divergent, nous pouvons nous assurer que le DECIE94 n’est pas pire que ce que nous avons commencé, c’est-à-dire avec les paramètres obtenus à partir de la régression linéaire.

Même avec la méthode précédente de régression linéaire, il y a plusieurs problèmes avec le raccord. L’un des problèmes est que les polynômes ont tendance à dépasser ou à défaire au-delà des points de données. Les maxima et minima locaux artificiels peuvent être introduits dans le processus de montage. Cela peut être réduit en utilisant des polynômes de faible degré, ce qui est la raison pour laquelle vous ne devez pas utiliser une valeur supérieure à trois degrés. Un aspect plus sérieux du dépassement ou du dépassement est que, même si un polynomial peut prendre une valeur réelle théoriquement, l’espace qu’il tente de modéliser a généralement des contraintes physiques et pratiques. CIEXYZ doit avoir toutes les valeurs X, Y, Z non négatives, qui sont des contraintes physiques. Dans la pratique, elles prennent uniquement des valeurs dans l’amplitude de centaines, pas de milliers ou plus. De même, CIELAB ou CIELUV a ses propres contraintes physiques et pratiques. Lorsque l’espace RVB est suffisamment rempli avec des points d’échantillonnage, le problème de dépassement ou de dépassement n’est pas grave. Toutefois, les points RVB capturés à partir de l’appareil de capture ne remplissent généralement pas l’espace RVB uniformément. Les points peuvent remplir uniquement les 80% du cube RGB, ou pire, ils peuvent résider dans un collecteur dimensionnel inférieur. Dans ce cas, les polynômes régressés peuvent faire une mauvaise tâche pour extrapoler les valeurs au-delà des points de données, renvoyant parfois des prédictions irréalistes. Vous souhaitez un modèle qui retourne toujours des valeurs raisonnablement réalistes. Cela nécessite une méthode qui permet de contrôler efficacement le comportement de la limite des polynomes de régression en imposant des coûts supplémentaires à ceux qui se comportent de façon erratique près de la limite du cube RGB. Une mesure supplémentaire pour s’assurer que les polynômes renvoient toujours des valeurs réalistes est appliquée en découpant la sortie vers dans le locus spectral CIE.

C’est à ce stade que la modélisation du scanneur et la modélisation de la caméra divergent les unes des autres. Le modèle d’appareil photo est supposé extrapoler aux régions situées au-delà des points échantillonnés, y compris les « surbrillances spéculaires », la même extrapolation n’est pas requise pour le modèle de scanneur. La cible du scanneur est supposée couvrir une caractérisation similaire aux documents imprimés à analyser. Le modèle de scanneur doit toujours être robuste dans le sens où il ne doit pas retourner de valeurs inréalistes, mais l’extrapolation bien au-delà de la cible de caractérisation n’est pas obligatoire. Pour garantir la robustesse, l-polynomial ci-dessus est coupé à 100, autrement dit, le modèle polynomial est forcé à ne pas extrapoler au-delà de « Dmin » de la cible du scanneur.

Le modèle d’appareil photo est supposé extrapoler à des surbrillances spéculaires, de sorte que le découpage à 100 n’est pas souhaitable. À la place, l’algorithme suivant est utilisé.

Des points de contrôle artificiels sont introduits pour contrôler le comportement des polynômes dans les régions avec un échantillonnage insuffisant. En plaçant stratégiquement ces points de contrôle avec les valeurs appropriées, elles servent à « tirer » les polynômes dans le sens requis. Dans l’implémentation actuelle, huit points de contrôle correspondant aux angles du cube RGB sont utilisés. Si les valeurs de l’appareil sont normalisées en Unity, les points suivants sont :

*R* = 0, *G* = 0, *B* = 0

*R* = 0, *G* = 0, *B* = 1

*R* = 0, *G* = 1, *B* = 0

*R* = 0. *G* = 1, *B* = 1

*R* = 1, *G* = 0, *B* = 0

*R* = 1, *G* = 0, *B* = 1

*R* = 1, *G* = 1, *B* = 0

*R* = 1, *G* = 1, *B* = 1

À l’exception du *R*  = *G*  = *B* = 1, qui est associé à une valeur CIELAB de *L* = 100, *u*  = *v* = 0, l’algorithme d’extrapolation suivant est utilisé pour déterminer la valeur CIELAB appropriée à associer. En général, pour un donné (*r*,*g*,*b* ), un poids est associé à chacun des (*r <sub>i</sub>*,*g <sub>i</sub>*,*b <sub>i</sub>* ) dans le jeu de données échantillonné. Il y a deux objectifs pour assigner le poids. Tout d’abord, le poids est inversement proportionnel à la distance entre (*r*,*g*,*b* ) et (*r <sub>i</sub>*,*g <sub>i</sub>*,*B <sub>i</sub>* ). Ensuite, vous souhaitez ignorer ou affecter la pondération 0 aux points qui ont une teinte différente du point donné (*R*,*G*,*B* ). Pour prendre en compte la teinte, envisagez des points qui se trouvent dans un cône dont le vertex est à (0,0), dont l’axe coïncide avec la jonction de la ligne (0, 0, 0) à (*R*,*G*,*B* ) et dont l’angle est semi-vertical ? est conforme à cos ? = 0,9. Voir la figure 3 pour une illustration de ce cône.

![Diagramme qui affiche la forme du voisinage.](images/cdmp-lcd-dmp-figure3.png)

**Figure 3** : filtrage des points d’échantillonnage par angle et distance. La forme du voisinage représenté est à titre d’illustration uniquement. La forme réelle dépend de la distance utilisée ; Il s’agit d’un voisinage en forme de losange si la norme 1 est utilisée.

Dans ce cône, un deuxième filtrage est effectué en fonction de la distance RVB, qui utilise la norme 1-normal, définie par

![Affiche la formule pour le deuxième filtrage dans le cône.](images/cdmp-formula28.png)

Avec le cône actuel, la recherche initiale concerne les points situés à une distance de 0,1 (*R*,*G*,*B* ). Si aucun point n’est trouvé dans ce rayon, le rayon est augmenté de 0,1 et la recherche est redémarrée. Si les réseaux d’arrondis suivants ne pointent pas non plus, le rayon est augmenté de 0,1. Ce processus se poursuit jusqu’à ce que le rayon dépasse MaxDist/5, où MaxDist = 3, dans le cas de 1-normal. Si aucun point n’est trouvé, le cône est agrandi en diminuant les co ? par 0,05, autrement dit, vous augmentiez l’angle ? et le redémarrage de l’ensemble du processus avec un rayon de plus en plus important. Ce processus se poursuit jusqu’à ce qu’un ensemble de points non vide soit trouvé ou cos ? atteint 0, autrement dit, le cône s’est ouvert pour devenir un plan. À ce stade, la recherche est redémarrée en renforçant le rayon, sauf que la recherche se poursuit jusqu’à ce que le rayon atteigne MaxDist. Cela garantit que, dans le pire des cas, un ensemble de points non vide est trouvé. L’algorithme est résumé dans le diagramme de flow de la figure 4.

![Diagramme qui montre le déroulement de l’algorithme.](images/cdmp-lcd-dmp-figure4.png)

**Figure 4** : diagramme de Flow permettant de déterminer le jeu de points d’échantillonnage utilisé dans l’extrapolation pour une valeur RVB d’entrée

En supposant que le processus précédent génère *un ensemble non* vide de points (*R <sub>i</sub>*,*G <sub>i</sub>*,*B <sub>i</sub>* ) et correspondant (*L <sub>i</sub>*,*<sub>i</sub>*,*b <sub>i</sub>* ), puis, pour chaque point, un poids *w <sub></sub>* affecté, donné par

![Affiche la formule pour un poids pour chaque point.](images/cdmp-formula29.png)

Enfin, extrapolant est défini par

![Affiche la définition de extrapolant.](images/cdmp-formula30.png)

Les équations précédentes constituent une instance des « méthodes pondérées à distance inverse », communément appelées méthodes Shepard. En exécutant chacun des huit points à partir de EQ (6) à l’algorithme, huit points de contrôle sont obtenus, chacun avec des valeurs *R*,*G*,*B* et *L*,*a*,*b* , qui sont placées dans le pool avec les exemples de données d’origine.

Pour vous assurer que le modèle produit toujours des valeurs de couleur valides et pour l’intégrité du système et pour stabiliser le pipeline de traitement des couleurs, vous devez effectuer un découpage final dans la sortie du modèle polynomial. La gamme d’éléments visuels CIE est décrite par le composant Achromatic (*Y* ou *L* ) et le composant chromatique (*XY* ou *a’b*), qui sont associés à l’espace XYZ par une transformation projective. Dans l’implémentation actuelle, la valeur chromatique *a’b* est utilisée car elle est directement liée à l’espace CIELUV. Pour toute valeur *CIELAB* , premier clip *L* à une valeur non négative :

![Affiche le découpage de L à une valeur non négative.](images/cdmp-formula31.png)

Pour permettre l’extrapolation pour les surbrillances spéculaires, *l* n’est pas coupé à 100, la limite supérieure « conventionnelle » pour *l* dans l’espace Lab.

Ensuite, si *L* = 0, *a* et *b* sont découpés, de sorte que a *= b =* 0. Si *L* ? 0, calculer

![Affiche la formule si L = 0.](images/cdmp-formula32.png)

Il s’agit des composants d’un vecteur dans le diagramme du *a’b'* du point blanc (*u ? '*,*v ? '* ) à la couleur en question. Définir le locus spectral CIE comme la coque convexe de tous les points (*a'*,*b'* ), paramétrés par la longueur d’onde ?:

![Affiche la formule de la longueur d’onde.](images/cdmp-formula33.png)

où ![ affiche les fonctions pour la correspondance des couleurs Cie.](images/cdmp-formula34.png) sont les fonctions de correspondance de couleur CIE pour l’observateur à 2 degrés. Si le vecteur se trouve en dehors du locus CIE, la couleur est découpée au point sur le locus CIE qui est l’intersection du locus et la ligne définie par le vecteur. Voir figure 5. Si le découpage s’est produit, la valeur *a* et *b* est reconstruite en soustrayant *d’abord un ?* et *b ?»* entre *a* et *b* découpés, puis multiplié par 13 *L*.

![Diagramme qui montre le graphique de l’algorithme de découpage.](images/cdmp-lcd-dmp-figure5.png)

**Figure 5** : algorithme de découpage pour les valeurs Lab qui se trouvent en dehors de la gamme d’éléments visuels Cie

Dans l’implémentation actuelle, le locus spectral CIE dans le plan *a’b* est représenté par une courbe linéaire par morceaux avec 35 segments (correspondant à une longueur d’onde comprise entre 360 nm et 700 nm inclus). En classant les segments de ligne de sorte que leurs angles sous-tendus au niveau du point blanc soient croissants, ce qui équivaut aux longueurs d’onde décroissantes, le segment de ligne qui croise le rayon formé par le vecteur ci-dessus peut être trouvé par une simple recherche binaire.

### <a name="rgb-printer-device-model-baseline"></a>Ligne de base du modèle d’imprimante RVB

Une caractérisation d’appareil d’une imprimante RVB consiste à construire un modèle empirique de l’appareil qui prédit la couleur CIELUV indépendante du périphérique pour toute valeur RVB donnée.

Il existe deux façons de construire le modèle empirique. L’une des méthodes consiste à utiliser les données de l’appareil pour une imprimante RVB, et l’autre à utiliser les données de paramètres analytiques. Dans le premier, les données de mesure fournies par un utilisateur pour un périphérique d’imprimante RVB sont utilisées pour construire une table de recherche 3D (LUT). Les données de mesure se composent de valeurs XYZ pour les correctifs RGB à échantillonnage uniforme. Les tailles d’échantillonnage standard sont 9 ou 17 pour chaque composant. Chaque patch est mesuré à l’aide d’un colorimeter ou d’un spectrophotomètre dans l’espace CIEXYZ. La valeur XYZ d’un correctif est ensuite convertie en valeur CIELUV, formant un LUT 3D. Dans le modèle d’appareil, la méthode d’interpolation tetrahedral de Sakamoto est appliquée au LUT 3D afin de prédire les données CIELUV pour une donnée RVB donnée. (Conférer le brevet 4275413 (Sakamoto et al.), US brevet 4511989 (Sakamoto), Kang \[ 1 \] . Les deux brevets mentionnés ont expiré.). Les données de paramètres analytiques passées dans la deuxième méthode sont simplement un LUT qui a été créé précédemment. En règle générale, cet LUT a été créé à l’aide de la première méthode, bien qu’il puisse être créé manuellement.

Dans la gestion des couleurs actuelle, le mappage source est défini en tant que carte qui passe de l’espace RVB à un espace de couleurs CIEXYZ indépendant du périphérique. La carte de destination est définie en tant que carte qui passe de l’espace de couleurs CIEXYZ indépendant du périphérique à l’espace RVB. Il s’agit de l’inverse du mappage source.

Le modèle empirique est directement utilisé dans le mappage source. En premier lieu, il mappe une donnée RVB donnée dans des données CIELUV, qui sont converties en données XYZ. Dans le mappage de destination, les données CIEXYZ indépendantes du périphérique sont d’abord converties en données CIELUV. Ensuite, le modèle empirique et la méthode de Newton-Raphson classique sont utilisés pour prédire les meilleures données RVB pour les données CIELUV. Les détails de la conversion de CieLUV en données RVB sont les suivants :

Après la génération d’un LUT 3D à partir de RGB vers CieLUV, la carte de RVB à LUV est créée à l’aide de l’interpolation tetrahedral sur RVB. Ce mappage est indiqué par les équations suivantes :

![Affiche les équations de la carte comprise entre R G B et L U V.](images/cdmp-image125.png)

L’inversion de la carte consiste à résoudre, pour toutes les couleurs ![Affiche L U V.](images/cdmp-image127.png) , le système suivant d’équations non linéaires :

![Affiche les équations non linéaires pour lolving toute couleur L U V.](images/cdmp-image129.png)

Une équation non linéaire basée sur la méthode Newton-Raphson classique est utilisée dans la nouvelle CTE. Pour obtenir une estimation initiale, ou *un* précédent, vous obtenez des s <sub>antérieurs</sub> -(R 0, v 0, B 0) en effectuant une recherche dans une « matrice de départ » comprenant une grille 8x8x8 uniforme de paires précalculées (RVB, Luv). Le Luv correspondant RVB le plus proche de L \* u \* v \* est choisi. Chaque point de la matrice de valeur initiale correspond au centre d’une cellule afin que les itérations ne commencent pas par un point sur la face frontière du cube RGB. En d’autres termes, la couleur RVB des graines est définie par : étape = 1/8 s <sub>IJK</sub> = (étape/2 + (i-1) étape, étape/2 + (j-1) étape, étape/2 + (k-1) étape) avec i, j, k = 1... 8 à l’étape *i* de Newton-Raphson, l’estimation suivante ![ affiche les variables pour l’estimation suivante.](images/cdmp-image133.png) est obtenu par la formule :

![Affiche la formule de l’estimation.](images/cdmp-image135.png)

L’itération s’arrête lorsque l’erreur (distance dans l’espace CIELUV) est inférieure à un niveau de tolérance prédéfini (0,1 dans la CTE) ou lorsque le nombre d’itérations a dépassé le nombre maximal d’itérations autorisé (10 dans la CTE). Les valeurs de la tolérance et du nombre d’itérations ont été déterminées de manière empirique pour être effectives. Dans les versions ultérieures, la valeur de tolérance peut être modifiée.

La matrice de Jacob est calculée à l’aide de la différence directe, sauf à un point limite (un ou plusieurs des R, G, B est 1) où la différence descendante est utilisée à la place. Au lieu de calculer l’inverse de la matrice de Jacob, le système linéaire est résolu directement à l’aide de Gauss-Jordan élimination avec le pivotement complet.

À la fin des itérations, la convergence n’est peut-être pas possible, car Newton-Raphson est un algorithme « local », c’est-à-dire qu’elle fonctionne uniquement si vous démarrez avec une estimation initiale qui est proche de la véritable solution. Si, à la fin de l' Newton-Raphson itérations, la convergence au sein de la tolérance d’erreur prédéfinie n’a pas été effectuée, les itérations sont redémarrées avec un nouvel ensemble de graines, défini comme suit.

Par exemple, la meilleure solution obtenue jusqu’à présent est (r, g, b). À partir de cette solution, N a les graines postérieures sont dérivées, où N = 4. Intuitivement, la solution est déplacée « vers le centre » dans une taille d’étape qui dépend de N. Voir figure 6.

![Diagramme qui montre les directions de perturbation de la solution.](images/cdmp-image136.png)

**Figure 6** : la direction de la perturbation de la solution dépend de la Octant dans laquelle elle se trouve.

En d’autres termes, si r &gt; 0,5, la valeur sur le canal r est diminuée, sinon la valeur est augmentée. Il existe une logique similaire pour les canaux G et B. Les définitions précises sont les suivantes :

PERTURBATION = 0,5/(N + 1)

Dir (r) =-1 si r &gt; 0,5 ; + 1 dans le cas contraire. De même pour dir (g) et dir (b)

Le JTH a POSTERIEURE, s ????, est (r + Rép (r) \* j \* perturbation, g + Rép (g) \* j \* perturbation, b + Rép (b) \* j \* perturbation)

Essayez les premières s ???? et s’il fournit une nouvelle solution dans la tolérance d’erreur, vous pouvez arrêter. Dans le cas contraire, essayez les deuxième s ???? et ainsi de suite jusqu’au nième ????.

Les schémas de l’algorithme entier sont illustrés à la figure 7.

![Diagramme qui montre le déroulement de l’inversion du modèle d’appareil.](images/cdmp-image138.png)

**Figure 7** : schémas d’inversion du modèle d’appareil

### <a name="rgb-virtual-device-model-baseline"></a>Ligne de base du modèle d’appareil virtuel RGB

Ce modèle de périphérique (DM) est un algorithme de reproduction simple de matrice/ton. La matrice est dérivée du point blanc et des primaires à l’aide d’algorithmes de science des couleurs standard. La courbe de reproduction des tons est dérivée des paramètres de mesure en fonction des descriptions ICC de CurveType et ParametricType (ou inversées selon les besoins). Les détails des algorithmes internes seront fournis après une validation supplémentaire des problèmes de plage dynamique élevée.

Le modèle d’appareil virtuel RGB est une courbe de reproduction de matrice/ton idéale RVB similaire à la conception de profil basé sur la matrice ICC à trois composants. Les paramètres de « mesure virtuelle » du DM incluent une valeur de point blanc (Absolute CIEXYZ), des valeurs RVB primaires (CIEXYZ absolues) et une courbe de reproduction des tons basée sur le ParametricCurveType ICC et CurveType dans la mise en forme XML cohérente avec les schémas DMP.

L’encodage de type de fonction ICC parametricCurveType et la prise en charge correspondante dans IRGBVirtualDeviceModelBase sont indiqués dans le tableau suivant.



| Type de fonction                                         | Paramètres                          | Type                                     | Remarque                                           |
|------------------------------------------|---------------------------|--------------------------------------|--------------------------------------------|
| ![Affiche la fonction « GammaType ».](images/cdmp-image154.png)<br/> | g<br/>              | GammaType<br/>                 | Implémentation courante<br/>           |
| ![Affiche la fonction « GammaOffsetGainType ».](images/cdmp-image156.png)<br/> | GA b<br/>           | GammaOffsetGainType<br/>       | CIE 122-1966<br/>                    |
| ![Affiche la fonction « GammaOffsetGainOffsetType ».](images/cdmp-image158.png)<br/> | GA b c<br/>         | GammaOffsetGainOffsetType<br/> | IEC 61966-3<br/>                     |
| ![Affiche la fonction « GammaOffsetGainGainType ».](images/cdmp-image160.png)<br/> | GA b c d<br/>       | GammaOffsetGainGainType<br/>   | IEC 61966-2.1<br/> sRVB<br/> |
| ![Affiche une fonction pour les paramètres’g a b c d e f'.](images/cdmp-image162.png)<br/> | GA b c d e f<br/>   | N/A<br/>                       | Non pris en charge dans WCS<br/>            |



 

La courbe de tonalité pour les appareils virtuels RGB est appliquée dans DeviceToColorimetric entre les données d’entrée, pDeviceColors et la matrice multiplier. Pour ColorimetricToDevice, une méthode doit être utilisée pour inverser la courbe tonale. Dans l’implémentation de base, cette opération est effectuée par interpolation directe dans la même courbe de tonalité utilisée pour DeviceToColorimetric.

Les courbes doivent être spécifiées dans les profils sous forme de paires de nombres dans l’espace flottant. Le premier nombre représente des valeurs dans pDeviceColors. Le deuxième nombre représente la sortie de la courbe de tonalité. Toutes les valeurs de la courbe tonale doivent être comprises entre minColorantUsed et maxColorantUsed. Les courbes de tons doivent contenir au moins deux entrées : une pour minColorantUsed et une pour maxColorantUsed. Le nombre maximal d’entrées dans le ToneCurve est 2048. En général, plus le nombre d’entrées dans la table est grand, plus le modèle de courbure est précis. Une interpolation linéaire par morceaux est effectuée entre les entrées.

Vous pouvez envisager d’autres méthodes d’interpolation. Si vous connaissez le comportement sous-jacent de l’appareil, vous pouvez utiliser moins d’échantillons et de modèles avec une plus grande courbe d’ordre. Toutefois, si vous utilisez un type de courbe incorrect, vous serez très imprécis. Sans plus d’informations, vous ne pouvez pas deviner le type de courbe. Par conséquent, utilisez l’interpolation linéaire et fournissez de nombreux points de données.

### <a name="cmyk-printer-device-model-baseline"></a>Ligne de base modèle de périphérique d’imprimante CMJN

Une caractérisation d’appareil d’une imprimante CMJN consiste à construire un modèle empirique de l’appareil qui prédit la couleur imprimée pour une valeur CMJN donnée. La caractérisation comprend également l’inversion de ce modèle afin qu’une prescription de la valeur CMYK à nous pour une couleur donnée à imprimer puisse être fournie. Cela est généralement défini en termes de valeur CIEXYZ ou CIELAB.

En règle générale, une cible IT 8.7/3 contenant des correctifs CMJN est utilisée. Les correctifs consistent en un échantillonnage de l’espace CMJN de manière bien définie, de sorte qu’une grille rectangulaire (avec un espacement non uniforme en C, M, Y et K) soit formée. Chaque patch est ensuite mesuré à l’aide d’un colorimeter ou d’un spectrophotomètre. Les mesures dans les valeurs CIEXYZ forment ensuite une table de recherche (LUT), à partir de laquelle un modèle empirique de l’imprimante est créé à l’aide de la méthode d’interpolation de Sakamoto. Brevet américain 4275413 (Sakamoto et al.), brevet américain 4511989 (Sakamoto), Kang \[ 1 \] . Les deux brevets mentionnés ont expiré.

Les exigences spécifiques pour les exemples de mesures CMJN nécessaires à l’acceptation d’un profil de modèle d’appareil comme valide par le modèle d’appareil de ligne de base d’imprimante CMJN sont les suivantes. (Le jeu d’échantillons est plus clairement décrit comme un ensemble d’exemples de cubes CMJ, chacun étant associé à un niveau K spécifique.)

-   Au minimum, les cubes CMJ valides doivent être fournis pour les niveaux K = 0 et K = 100.
-   Les niveaux K intermédiaires peuvent être espacés de façon non uniforme.
-   Tout niveau K intermédiaire sans un cube CMJ valide sera ignoré.
-   Les cubes CMJ peuvent utiliser des intervalles d’échantillonnage non uniformes (espacement de la grille), mais le même jeu d’intervalles d’échantillonnage doit être utilisé dans toutes les dimensions C, M et Y du cube CMJ pour un niveau K donné.
-   Chaque cube de niveau K peut utiliser un nombre et un espacement différents d’intervalles d’échantillonnage.
-   Tous les cubes CMJ doivent contenir les « angles » du cube CMJ, c’est-à-dire les exemples CMJ à 0, 0, 0, 0, 0100 \[ \] \[ \] , \[ 0100, 0 \] , 100, 0, 0, \[ \] \[ 0100 100 \] , 100, \[ 0100 \] , \[ 100 100, 0 \] , \[ 100 100 100 \] .
-   Tous les niveaux de grille CMJ intermédiaires doivent être intégralement échantillonnés dans chaque canal. En d’autres termes, un échantillon doit exister à chaque intersection de grille 3D dans le cube CMJ.
-   Pour les cubes K = 0 et K = 100 CMJ, les cubes 2x2x2 « Corners only » sont le minimum accepté comme valide.

    \[Remarque : pour K = 0 et K = 100 niveaux, un cube 3x3x3 CMJ est traité comme un cube 2x2x2 « Corners only ». le niveau d’échantillonnage intermédiaire est ignoré. les 4x4x4 et les cubes plus volumineux auront tous des échantillons sur la grille utilisés.\]

-   Pour les niveaux K intermédiaires, les cubes 4x4x4 CMJ sont la valeur minimale acceptée comme valide.

Un profil de haute qualité utilise des grilles d’échantillonnage plus fines que le minimum requis pour la validité, généralement 9x9x9x9 ou supérieur. Les exemples des cibles IT 8.7/3, IT 8.7/4 et ECI produisent des profils de modèle d’appareil (DMPs) valides pour le modèle d’appareil de base d’imprimante CMJN. Bien que ce modèle d’appareil soit en mesure d’ignorer les exemples étrangers (hors grille) dans ces cibles, il n’est pas garanti qu’il puisse le faire pour d’autres cibles, et par conséquent, il est recommandé de supprimer les exemples superflus des ensembles de mesures entrant dans des profils pour ce modèle d’appareil.

L’inversion du modèle d’imprimante présente davantage de difficultés. Étant donné une couleur d’entrée dans CIECAM, il est question de savoir si cette couleur est dans la gamme d’imprimantes. Il y a également un problème concernant la disposition des points dans l’espace d’apparence de la couleur. Bien que nous puissions organiser les valeurs CMJN pour les faire tomber sur une grille rectangulaire, comme c’est le cas dans la cible IT 8.7/3, il n’est pas possible d’avoir la même valeur pour les couleurs imprimées, car elles sont situées dans l’espace d’apparence de couleur. En général, ils sont disséminés dans l’espace d’apparence de couleur sans modèle particulier.

Il existe généralement deux approches pour le problème d’inversion de points dispersés. Une approche consiste à utiliser une sous-division géométrique de la gamme d’imprimantes à l’aide de solides unidimensionnels élémentaires, tels que tetrahedra. Une sous-division de la gamme d’imprimantes dans l’espace d’apparence des couleurs peut être induite à partir de la sous-division correspondante de l’espace CMJ (K), consultez \[ 93 \] , Kang \[ 97 \] . Cette approche présente l’avantage de la simplicité de calcul. Dans le cas d’un tétraèdres, seuls quatre points sont utilisés dans une interpolation. D’un autre côté, le résultat dépend fortement de quelques points, ce qui signifie qu’une erreur de mesure aura un effet significatif sur le résultat. L’interpolation a également tendance à ne pas être aussi lisse. La deuxième approche ne suppose pas de sous-division et est basée sur la technique d’interpolation de données éparpillée. Un exemple classique est la technique de l’interpolation Shepard ou la méthode pondérée inversée (voir Shepard \[ 68 \] ). Ici, plusieurs points entourant le point d’entrée sont choisis d’une certaine manière, chacun affecté un poids, généralement inversement proportionnel à la distance, et l’interpolation est considérée comme la moyenne pondérée des points voisins. Dans cette approche, le choix des points voisins est primordial pour les performances. Bien que trop peu de points puissent rendre l’interpolation inexacte et non lisse, un trop grand nombre de points imposent un coût de calcul élevé, car les poids sont généralement des fonctions non linéaires et coûteuses à calculer.

Les deux approches décrites ci-dessus rencontrent des problèmes. L’approche de la sous-division dépend de manière critique des données qui sont raisonnablement vides et, en général, l’interpolation n’est pas très lisse. L’interpolation de données éparpillée est plus tolérante au bruit des données et donne généralement une interpolation plus lisse, mais elle est plus coûteuse en termes de calcul.

La nouvelle CTE adopte une autre approche. L’appareil CMJN est traité comme une collection de plusieurs appareils CMJ, chacun d’entre eux ayant une valeur spécifique de noir (K). À l’aide d’un algorithme de sélection qui prend comme claire et chroma des paramètres, un niveau de noir est choisi. Les valeurs CMJ sont obtenues par inversion de la table CMJ vers Luv correspondante à l’aide des méthodes Newton utilisées ailleurs par l’algorithme d’imprimante RVB.

Effectuez les étapes suivantes.

1.  Imprimez la cible de caractérisation, qui est soit la cible IT 8.7/3, soit une cible contenant l’échantillonnage de l’espace CMJN à intervalles réguliers ou irréguliers.
2.  Mesurez la cible à l’aide d’un spectrophotomètre et convertissez les mesures en espace CIELUV.
3.  Construisez la carte de transfert de l’image CMJN vers Luv.
4.  Utilisez la carte de transfert pour construire un ensemble de CMJ à Luv Maps pour une plage de valeurs K.
5.  Pour toute valeur Luv d’entrée, la valeur CMJN correspondante est obtenue en sélectionnant l’une des cartes construites à l’étape 4 ci-dessus et en l’inversant à l’aide de la méthode de Newton pour obtenir un jeu de couleurs CMJ pour accompagner la valeur K sélectionnée.

Les étapes 1 et 2, qui sont des procédures standard, sont effectuées par un programme de profilage qui ne fait pas partie de la nouvelle CTE. La cible IT 8.7/3 contient un échantillonnage raisonnablement détaillé de toutes les valeurs CMJN à différents niveaux de C, M, Y et K. vous pouvez également utiliser une cible personnalisée avec un échantillonnage uniforme des canaux C, M, Y et K. Une fois la cible imprimée, un spectrophotomètre ou un colorimeter peut être utilisé pour mesurer la valeur XYZ de chaque correctif, et la valeur XYZ peut être convertie en valeur Luv à l’aide du modèle CIELUV.

L’étape 3, la construction de la carte de transfert de type CMJN à Luv, peut être obtenue en appliquant une technique d’interpolation connue, telle que tetrahedral ou une méthode multilinéaire, sur la grille rectangulaire de l’espace CMJN. Dans la nouvelle CTE, une interpolation tetrahedral à quatre dimensions est utilisée. Étant donné que les grilles d’échantillonnage CMJ sont généralement différentes à chaque niveau de K, toutefois, nous utilisons une technique de Super-échantillonnage, comme indiqué ci-dessous. Pour un point CMJN donné, les niveaux d’intercalaire K sont déterminés en priorité en fonction de la valeur K. Introduisez ensuite une « super-grille » sur chaque niveau K qui est une Union des grilles de CMJ sur chacun des deux niveaux K. À chaque niveau K, la valeur Luv de tout nouveau point de grille récemment introduit est obtenue par une interpolation tetrahedral à 3 dimensions dans ce niveau K. Enfin, une interpolation tetrahedral à quatre dimensions pour le point CMJN spécifique est effectuée sur cette nouvelle grille.

![Diagramme illustrant l’échantillonnage.](images/cdmp-image163.png)

**Figure 8** : superéchantillonnage

L’étape 4 crée un ensemble de tables de recherche de CMJ à Luv (LUTs). La carte de transfert construite à l’étape 3 est appelée à plusieurs reprises pour rééchantillonner l’espace CMJN. L’espace colorimétrique CMJN est échantillonné à l’aide d’un espacement pair de K et d’un autre, mais toujours espacés, de manière uniforme, par échantillonnage de CMJ.

L’étape 5 est une procédure permettant d’obtenir la valeur CMYK à l’aide du LUTs construit à l’étape 4 pour tout point de Luv d’entrée. La valeur appropriée de K est choisie en analysant la clarté et le degré de couleur dans le Luv demandé. Une fois la table sélectionnée, les valeurs CMJ sont obtenues à partir de la table à l’aide de la méthode de Newton (comme indiqué dans le modèle de périphérique d’imprimante RVB plus haut).

L’espace CIELUV est utilisé dans le modèle d’imprimante au lieu de CIEJab, car le modèle d’appareil doit être basé uniquement sur des données colorimétriques disponibles dans DMP. Le DMP contient des données colorimétriques pour chaque correctif mesuré, y compris le point blanc du média. il est donc possible de convertir les données CIEXYZ en données CIELUV. Toutefois, il n’est pas possible de convertir en CIECAM02 JCh ou Jab, car il n’y a pas accès aux informations de condition d’affichage dans le DMP.

### <a name="rgb-projector-device-model-baseline"></a>Ligne de base du modèle d’appareil projecteur RVB

Remarque : un grand nombre de projecteurs RGB ont plusieurs modes d’opération. Dans un mode, qui est souvent la valeur par défaut et peut être appelé « présentation », la réponse couleur du projecteur est optimisée pour une luminosité maximale. Toutefois, dans ce mode, le projecteur perd la capacité de reproduire des couleurs légères, légèrement chromatiques, telles que des jaunes pâles et des tons chair. Dans un autre mode, souvent appelé « film », « vidéo » ou « sRVB », le projecteur est optimisé pour la reproduction d’images réalistes et de scènes naturelles. Dans ce mode, la luminosité maximale est compromise pour améliorer la qualité globale de la reproduction des couleurs. Pour obtenir une reproduction des couleurs satisfaisante avec les projecteurs RGB, il est nécessaire de placer le projecteur dans un mode dans lequel une gamme lisse de couleurs peut être reproduite.

![Diagramme illustrant un modèle d’appareil D L P.](images/cdmp-image167.png)

**Figure 9** : modèle d’appareil DLP

Une valeur RVB entrante passe par deux chemins de calcul. La première est le modèle de matrice, qui produit une valeur XYZ. Cela est immédiatement suivi par la conversion de XYZ en Luv. La seconde est l’interpolation de LUT non uniforme à l’aide de l’interpolation tetrahedral. La sortie de l’interpolation est déjà dans Luv Space par construction. Les deux sorties sont ajoutées pour obtenir la valeur Luv prédite. Elle est finalement convertie en XYZ, qui est la sortie attendue du modèle de colorimétrie pour l’appareil DLP.

Étant donné que les projecteurs sont des appareils d’affichage, ils prennent également en charge l’inversion du modèle, autrement dit, la transformation de XYZ en RVB. Étant donné que le modèle d’appareil transforme l’espace RVB en espace XYZ, qui sont tous deux unidimensionnels, l’inversion est équivalente à la résolution de trois équations non linéaires en trois inconnues. Cela peut être effectué par des techniques de résolution d’équations standard, telles que Newton-Raphson. Toutefois, il est préférable de convertir d’abord XYZ en Luv, puis d’inverser la transformation Luv en RGB, car l’espace Luv est plus RECEPTEUR que l’espace XYZ.

### <a name="icc-device-model-baseline"></a>Ligne de base du modèle d’appareil ICC

L’interopérabilité du flux de travail ICC est activée en créant un profil de modèle de ligne de base d’appareil ICC spécial qui stocke l’objet de profil et crée une transformation ICC à l’aide d’un profil non-op XYZ. Cette transformation est ensuite utilisée pour la conversion entre les couleurs des appareils et des CIEXYZ.

![Diagramme illustrant l’interopérabilité du flux de travail c I T e I c.](images/cdmp-image168.png)

**Figure 10** : citez l’interopérabilité des flux de travail ICC

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de base de la gestion des couleurs](basic-color-management-concepts.md)
</dt> <dt>

[Schémas et algorithmes du système de couleurs Windows](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





