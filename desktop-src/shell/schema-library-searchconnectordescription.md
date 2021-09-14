---
description: L' &lt; &gt; élément searchConnectorDescription est l’élément conteneur de niveau supérieur d’une définition de connecteur de recherche.
ms.assetid: 383CAA20-56CA-4bdc-AC79-E57A1D59785C
title: Élément searchConnectorDescription (schéma de bibliothèque)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eddf7c2795f5c87009bc17b5fa3899d339ceed3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196444"
---
# <a name="searchconnectordescription-element-library-schema"></a>Élément searchConnectorDescription (schéma de bibliothèque)

L' &lt; &gt; élément searchConnectorDescription est l’élément conteneur de niveau supérieur d’une définition de connecteur de recherche. l' &lt; &gt; élément searchConnectorDescription est une extension du &lt; type d' &gt; élément searchConnectorDescriptionType associé à Windows les connecteurs de recherche fédérés ; toutefois, vous ne pouvez pas inclure de connecteurs de recherche pour Windows recherche fédérée ou des gestionnaires de protocole dans une bibliothèque.

## <a name="syntax"></a>Syntaxe

``` syntax
<!-- searchConnectorDescription -->
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema" elementFormDefault="qualified" attributeFormDefault="unqualified">
   <xs:complexType name="searchConnectorDescriptionType">
      <xs:all>
         <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
         <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/
         <xs:element name="description" type="xs:string" minOccurs="0"/>
         <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
         <xs:element name="imageLink" minOccurs="0">
            <xs:complexType>
               <xs:sequence>
                  <xs:element name="url" type="xs:anyURI"/>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="author" type="xs:string" minOccurs="0"/>
         <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
         <xs:element name="templateInfo" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="folderType" minOccurs="0"/>
               </xs:all>
            </xs:complexType>
         </xs:element>
         <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0"/>
         <xs:element name="locationProvider" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
               </xs:all>
               <xs:attribute name="clsid" use="required"/>
               <xs:attribute name="codebase" type="xs:string"/>
            </xs:complexType>
         </xs:element>
         <xs:element name="scope" minOccurs="0">
            <xs:complexType>
               <xs:sequence minOccurs="0">
                  <xs:element name="scopeItem" maxOccurs="unbounded">
                     <xs:complexType>
                        <xs:all>
                           <xs:element name="mode" default="Include">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Include"/>
                                    <xs:enumeration value="Exclude"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="depth" default="Shallow" minOccurs="0">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Shallow"/>
                                    <xs:enumeration value="Deep"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="url" type="xs:anyURI"/>
                        </xs:all>
                     </xs:complexType>
                  </xs:element>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0"/>
         <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="domain" type="xs:string" minOccurs="0"/>
         <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isIndexed" type="xs:boolean" minOccurs="0"/>
      </xs:all>
      <xs:attribute name="publisher" type="xs:string"/>
      <xs:attribute name="product" type="xs:string"/>
   </xs:complexType>
</xs:schema>
```

## <a name="element-information"></a>Informations sur les éléments

reportez-vous à la documentation du schéma dans [Windows Search](/previous-versions/bb268030(v=msdn.10))



| Élément parent                                                                                               | Éléments enfants                        |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [Élément searchConnectorDescriptionList (schéma de bibliothèque)](schema-library-searchconnectordescriptionlist.md) | <isSearchOnlyI. TEM>             |
|                                                                                                              | &lt;description&gt;                   |
|                                                                                                              | &lt;iconReference&gt;                 |
|                                                                                                              | &lt;imageLink&gt;                     |
|                                                                                                              | &lt;auteur&gt;                        |
|                                                                                                              | &lt;dateCreated&gt;                   |
|                                                                                                              | &lt;templateInfo&gt;                  |
|                                                                                                              | &lt;locationProvider&gt;              |
|                                                                                                              | &lt;scope&gt;                         |
|                                                                                                              | &lt;propertyStore&gt;                 |
|                                                                                                              | &lt;domaine&gt;                        |
|                                                                                                              | &lt;supportsAdvancedQuerySyntax&gt;   |
|                                                                                                              | &lt;isDefaultSaveLocation&gt;         |
|                                                                                                              | &lt;isDefaultNonOwnerSaveLocation&gt; |
|                                                                                                              | &lt;isIndexed&gt;                     |
|                                                                                                              | &lt;simpleLocation&gt;                |
|                                                                                                              | &lt;includeInStartMenu&gt;            |



 

## <a name="attributes"></a>Attributs



| Attribut | Description                                                                      |
|-----------|----------------------------------------------------------------------------------|
| publisher | Optionnel. Nom complet du serveur de publication qui fournit le connecteur de recherche.      |
| product   | Optionnel. Nom complet du produit auquel le connecteur de recherche s’applique. |



 

## <a name="remarks"></a>Notes

l' &lt; &gt; élément searchConnectorDescription d’une bibliothèque utilise la même définition de schéma que le &lt; searchConnectorDescription &gt; pour Windows recherche fédérée. bien qu’ils utilisent les mêmes schémas, les connecteurs de recherche pour Windows la recherche fédérée ne peuvent pas être inclus dans une bibliothèque.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Schéma de description de la bibliothèque](library-schema-entry.md)
</dt> <dt>

[Schéma de la description du connecteur de recherche](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
