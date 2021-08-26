---
description: L' <searchConnectorDescriptionType> élément est le conteneur de niveau supérieur pour la définition de connecteur de recherche.
ms.assetid: a6b45864-210d-4099-804d-7548fd8eb562
title: Élément searchConnectorDescriptionType (schéma du connecteur de recherche)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f228097e905ea6e60bb9197bcf8b8b381671a52f3375849af992f903df6e8b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119937909"
---
# <a name="searchconnectordescriptiontype-element-search-connector-schema"></a>Élément searchConnectorDescriptionType (schéma du connecteur de recherche)

L' <searchConnectorDescriptionType> élément est le conteneur de niveau supérieur pour la définition de connecteur de recherche.

-   [Syntaxe](#syntax)
-   [Informations sur les éléments](#element-information)
-   [Attributs](#attributes)
-   [Remarques](#remarks)
-   [Exemple de fichier de description de connecteur de recherche](#example-of-a-search-connector-description-file)
-   [Rubriques connexes](#related-topics)

## <a name="syntax"></a>Syntaxe


```
<!-- searchConnectorDescriptionType -->
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



| Élément parent | Éléments enfants                                                                                                           |
|----------------|--------------------------------------------------------------------------------------------------------------------------|
|                | [Élément isSearchOnlyItem (schéma du connecteur de recherche)](search-schema-sconn-issearchonlyitem.md)                           |
|                | [Élément isDefaultSaveLocation (schéma du connecteur de recherche)](search-schema-sconn-isdefaultsavelocation.md)                 |
|                | [Élément isDefaultNonOwnerSaveLocation (schéma du connecteur de recherche)](search-schema-sconn-isdefaultnonownersavelocation.md) |
|                | [Description, élément (schéma du connecteur de recherche)](search-schema-sconn-description.md)                                     |
|                | [Élément iconReference (schéma du connecteur de recherche)](search-schema-sconn-iconreference.md)                                 |
|                | [Élément imageLink (schéma du connecteur de recherche)](search-schema-sconn-imagelink.md)                                         |
|                | [auteur, élément (schéma du connecteur de recherche)](search-schema-sconn-author.md)                                               |
|                | [Élément dateCreated (schéma du connecteur de recherche)](search-schema-sconn-datecreated.md)                                     |
|                | [Élément templateInfo (schéma du connecteur de recherche)](search-schema-sconn-templateinfo.md)                                   |
|                | [Élément locationProvider (schéma du connecteur de recherche)](search-schema-sconn-locationprovider.md)                           |
|                | [Élément Scope (schéma du connecteur de recherche)](search-schema-sconn-scope.md)                                                 |
|                | [Élément propertyStore (schéma du connecteur de recherche)](search-schema-sconn-propertystore.md)                                 |
|                | [Élément includeInStartMenuScope (schéma du connecteur de recherche)](search-schema-sconn-includeinstartmenuscope.md)             |
|                | [Élément de domaine (schéma de connecteur de recherche)](search-schema-sconn-domain.md)                                               |
|                | [Élément supportsAdvancedQuerySyntax (schéma du connecteur de recherche)](search-schema-sconn-supportsadvancedquerysyntax.md)     |
|                | [Élément isIndexed (schéma du connecteur de recherche)](search-schema-sconn-isindexed.md)                                         |



 

## <a name="attributes"></a>Attributs



| Attribut | Description                                                                      |
|-----------|----------------------------------------------------------------------------------|
| publisher | Facultatif. Nom complet du serveur de publication qui fournit le connecteur de recherche.      |
| product   | Facultatif. Nom complet du produit auquel le connecteur de recherche s’applique. |



 

## <a name="remarks"></a>Remarques

Les connecteurs de recherche pour la recherche fédérée ne peuvent pas être utilisés dans les bibliothèques. Le schéma pour les connecteurs de recherche de bibliothèque est une extension du schéma décrit ici et contient des informations spécifiques aux bibliothèques.

## <a name="example-of-a-search-connector-description-file"></a>Exemple de fichier de description de connecteur de recherche

Voici un exemple de fichier de description de connecteur de recherche pour un service Web de recherche fédérée.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



Voici un exemple de fichier de description de connecteur de recherche pour un gestionnaire de protocole MAPI.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Vue d’ensemble du schéma de description du connecteur de recherche](search-sconn-desc-schema-entry.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Recherche fédérée dans Windows](-search-federated-search-overview.md)
</dt> </dl>

 

 



