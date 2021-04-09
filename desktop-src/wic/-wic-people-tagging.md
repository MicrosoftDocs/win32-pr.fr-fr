---
description: Cette rubrique présente le nouveau schéma XMP (Extensible Metadata Platform) et la propriété photo Windows 7 System. photo. PeopleNames qui permet d’étiqueter des individus dans une photo numérique.
ms.assetid: 557c3e9a-1756-4abb-8465-b12195ecbc91
title: Vue d’ensemble du balisage des personnes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64f2080e51d4d340474e0610fcce9512fc72429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115778"
---
# <a name="people-tagging-overview"></a>Vue d’ensemble du balisage des personnes

Cette rubrique présente le nouveau schéma XMP (Extensible Metadata Platform) et la propriété photo Windows 7 [System. photo. PeopleNames](../properties/props-system-photo-peoplenames.md) qui permet d’étiqueter des individus dans une photo numérique. Cette rubrique explique également comment utiliser l’API WIC (Windows Imaging Component) pour lire et écrire les métadonnées nécessaires au balisage des personnes.

Cette rubrique contient les sections suivantes.

-   [Conditions préalables](#prerequisites)
-   [Introduction](#introduction)
-   [Balisage de personnes](#people-tagging-overview)
    -   [Noms de personnes](#people-names)
    -   [Rectangles de personnes](#people-rectangles)
-   [Référence du schéma](#schema-reference)
    -   [Schéma Microsoft Photo 1,2](#microsoft-photo-12-schema)
    -   [Schéma de l’RegionInfo Microsoft Photo](#microsoft-photo-regioninfo-schema)
    -   [Schéma de la région de photo Microsoft](#microsoft-photo-regioninfo-schema)
    -   [Exemples de métadonnées](#sample-metadata)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

Pour comprendre cette rubrique, vous devez être familiarisé avec les interfaces de décodeur WIC et les composants COM (Component Object Model) associés, comme décrit dans la [vue d’ensemble du composant de création d’images Windows](-wic-about-windows-imaging-codec.md). Il permet également d’avoir une connaissance générale des métadonnées d’acquisition d’images, en particulier XMP.

## <a name="introduction"></a>Introduction

Microsoft a créé un nouveau schéma XMP pour baliser les personnes au sein d’une image numérique. Ce schéma permet aux applications de stocker les noms et les emplacements des individus qui se trouvent dans l’image en tant que métadonnées dans l’image. Outre le nouveau schéma, la nouvelle propriété photo [System. photo. PeopleNames](../properties/props-system-photo-peoplenames.md) est disponible dans Windows 7. Cette nouvelle propriété permet aux applications de lire les noms individuels stockés dans les métadonnées de l’image. WIC utilise ces nouvelles fonctionnalités en permettant aux applications de lire et d’écrire facilement des métadonnées de balisage sur des photos numériques.

## <a name="people-tagging"></a>Balisage de personnes

WIC fournit aux développeurs d’applications des composants COM qui lisent les données d’image, ainsi que les métadonnées d’image. Pour la lecture et l’écriture de métadonnées, telles que la nouvelle fonctionnalité de balisage de personnes, WIC fournit les interfaces [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) et [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) . Ces interfaces permettent aux applications d’utiliser le [langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md) pour écrire des métadonnées dans les frames individuels d’une image. La section suivante montre comment lire et écrire les métadonnées de balisage des personnes dans les métadonnées d’une image à l’aide de lecteurs et de Writers de requêtes WIC.

### <a name="people-names"></a>Noms de personnes

Une partie de la fonctionnalité de balisage des personnes est la possibilité de simplement obtenir une liste des noms des personnes marquées dans l’image. Cette partie de la fonctionnalité est prise en charge par les gestionnaires de métadonnées [System. photo. PeopleNames](../properties/props-system-photo-peoplenames.md) et WIC. L’interface [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) , conjointement à la propriété System. photo. PeopleNames, est utilisée pour lire les noms des personnes identifiées dans une image et stockées dans les métadonnées de l’image.

L’exemple de code suivant montre un lecteur de requête obtenu à partir d’un frame d’image pour interroger les métadonnées d’une image pour les noms avec balises de la propriété [System. photo. PeopleNames](../properties/props-system-photo-peoplenames.md) .


```C++
// Not shown: image decoding, retrieving an image frame. 
...
PROPVARIANT value;
IWICMetadataQueryReader *pQueryReader = NULL;
...
// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

// Query for the System.Photo.PeopleNames property.
if (SUCCEEDED(hr))
{
    // Get the property metadata by property name.
    hr = pQueryReader->GetMetadataByName(L"System.Photo.PeopleNames", &value);
}
```



L’expression de requête « System. photo. PeopleNames » interroge le frame pour la propriété. Si les métadonnées de balisage de personnes existent et contiennent des noms de personnes, la valeur [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) est définie sur VT \_ LPWStr et la valeur des données contient la liste des noms avec balises. Pour plus d’informations sur la lecture des métadonnées d’image, consultez [vue d’ensemble de la lecture et de l’écriture de métadonnées d’image](-wic-codec-readingwritingmetadata.md).

L’interrogation de la balise People Names n’est utile que si l’image contient réellement les métadonnées de balisage. Pour que cela se produise, une application doit d’abord l’avoir écrite. Pour écrire les métadonnées de noms de personnes, utilisez un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) et le chemin d’accès XMP explicite des métadonnées. L’exemple de code suivant illustre l’utilisation d’un générateur de requêtes pour écrire un nom dans le chemin d’accès de la requête.


```C++
// Not shown: image encoding, retrieving/creating the image frame,
// creating the IWICImagingFactory 
...
IWICImagingFactory *pFactory = NULL;
IWICMetadataQueryWriter *pQueryWriter = NULL;
...
// Get the query writer from the image frame.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pQueryWriter);
}

// A query writer specifically for this person's XMP struct
IWICMetadataQueryWriter *pXMPStructQueryWriter = NULL;

// Create a query writer specifically for an XMP Struct
hr = pFactory->CreateQueryWriter(
    GUID_MetadataFormatXMPStruct,
    NULL,
    &pXMPStructQueryWriter
    );

// Create a variant representing the structure created above
PROPVARIANT xmpStruct;
PropVariantInit(&xmpStruct);

// VT_UNKNOWN indicates that we're setting a COM object, in this case a XMPStruct
// which will hold the name and rectangle
xmpStruct.vt = VT_UNKNOWN; 
xmpStruct.punkVal = pXMPStructQueryWriter;

if(SUCCEEDED(hr))
{
    // WIC will automatically create the xmp base, the RegionInfo struct, and the Regions
    // bag (an unordered array) but structs within that bag need to be explicitly created.
    // The {ulong=0} in the query means to insert the new struct at the start of the bag,
    // {} could also be used to insert at the end of the bag.
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions/{ulong=0}",
        &xmpStruct
        );
}

// Set up the PROPVARIANT with the name information
PROPVARIANT personName;
PropVariantInit(&personName);
personName.vt = VT_LPWSTR;
personName.pwszVal = L"John Doe";

if(SUCCEEDED(hr))
{
    // Set the name metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:PersonDisplayName",
        &personName
        );  
}
```



Notez l’étape qui consiste à construire la structure XMP et à la définir sous `MPRI:Regions/{ulong=0}` . Sans cette étape, le WIC ne peut pas identifier où placer `PersonDisplayName` ultérieurement. Notez également que le chemin de requête explicite est utilisé à la place de [System. photo. PeopleNames](-wic-photoprop-system-photo-peoplenames.md), dont la stratégie de métadonnées ne prend pas en charge l’écriture de métadonnées.

### <a name="people-rectangles"></a>Rectangles de personnes

Toutefois, les noms des personnes font uniquement partie de la fonctionnalité de balisage des personnes. Outre le stockage des noms des personnes dans les métadonnées, le schéma prend également en charge les informations de région qui identifient la zone spécifique (un rectangle) que la personne affiche dans l’image.

Les informations de rectangle sont représentées par quatre valeurs décimales délimitées par des virgules, telles que « 0,25, 0,25, 0,25, 0,25 ». Les deux premières valeurs spécifient la coordonnée supérieure gauche ; les deux derniers spécifient la hauteur et la largeur du rectangle. Les dimensions de l’image dans le cadre de la définition des rectangles de personnes sont normalisées à 1, ce qui signifie que dans l’exemple « 0,25, 0,25, 0,25, 0,25 », le rectangle démarre 1/4 de la distance à partir du haut et de 1/4 de la distance à partir de la gauche de l’image. La hauteur et la largeur du rectangle sont 1/4 de la taille de leurs dimensions d’image respectives.

Les informations de rectangle qui identifient les individus sont écrites de la même façon que les noms des personnes, au sein de la même structure. Pour écrire les métadonnées de rectangle, utilisez un [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) et le chemin d’accès XMP explicite des métadonnées. L’exemple de code suivant poursuit l’exemple précédent et ajoute un rectangle représentant « John Doe » aux métadonnées de l’image. Notez qu’il utilise le même `{ulong=0}` index pour associer ce rectangle à « John Doe ».


```C++
// Set up the PROPVARIANT with the rectangle information
PROPVARIANT rectangle;
PropVariantInit(&rectangle);
rectangle.vt = VT_LPWSTR;
rectangle.pwszVal = L"0.0,0.0,0.25,0.25";

if(SUCCEEDED(hr))
{
    // Set the rectangle metadata
    hr = pQueryWriter->SetMetadataByName(
        L"/xmp/MP:RegionInfo/MPRI:Regions/{ulong=0}/MPReg:Rectangle",
        &rectangle
        );
}
```



## <a name="schema-reference"></a>Référence du schéma

Les schémas XMP Microsoft pour les balises de personnes définissent un ensemble de propriétés pour baliser des personnes dans des photos numériques.

Les sections suivantes fournissent les définitions de schéma nécessaires pour le balisage des personnes. Dans la mesure du possible, les définitions de schéma utilisent les conventions fournies par les [spécifications XMP (Extensible Metadata Platform) d’Adobe](https://www.adobe.com/devnet/xmp/). Les définitions de schéma de cette rubrique indiquent l’espace de noms XML Uniform Resource Identifier (URI) qui identifie le schéma et le préfixe d’espace de noms de schéma par défaut, suivis d’un tableau qui répertorie toutes les propriétés définies pour le schéma. Chaque table contient les colonnes suivantes :

-   **Property** -le nom de la propriété, y compris le préfixe d’espace de noms préféré.

-   **Type de valeur** : type de valeur de la propriété. Les schémas de prise en charge du balisage des personnes utilisent les types de valeur XMP chaque fois que cela est possible, y compris la date et le texte. Les types de tableau sont précédés du type de conteneur : `alt` , `bag` ou `seq` .

-   **Category** -les propriétés de schéma sont internes ou externes :

    -   Les métadonnées internes doivent être définies par l’application.

    -   Les métadonnées externes doivent être définies par l’utilisateur et sont indépendantes du contenu du document.

-   **Description** : description de la propriété.

### <a name="microsoft-photo-12-schema"></a>Schéma Microsoft Photo 1,2

Le schéma Microsoft Photo 1,2 fournit un ensemble de propriétés pour les zones d’image.

-   L’URI de l’espace de noms du schéma est `https://ns.microsoft.com/photo/1.2/` .
-   Le préfixe de l’espace de noms du schéma par défaut est `MP` .



| Propriété      | Type de valeur | Category | Description                                                                                                                     |
|---------------|------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| MP : RegionInfo | RegionInfo | Interne | **obligatoire** : stocke la racine des métadonnées de balisage des personnes. Consultez la section relative au schéma Microsoft Photo RegionInfo qui suit. |



 

### <a name="microsoft-photo-regioninfo-schema"></a>Schéma de l’RegionInfo Microsoft Photo

Le schéma Microsoft Photo RegionInfo 1,2 fournit un ensemble de propriétés pour les informations de région.

-   L’URI de l’espace de noms du schéma est `https://ns.microsoft.com/photo/1.2/t/RegionInfo#` .
-   Le préfixe de l’espace de noms du schéma par défaut est `MPRI` .



| Propriété              | Type de valeur | Category | Description                                                                                                    |
|-----------------------|------------|----------|----------------------------------------------------------------------------------------------------------------|
| MPRI:DateRegionsValid | Date       | Externe | **facultatif** : date de création de la dernière région.                                                          |
| MPRI : régions          | Région de sac | Externe | **obligatoire** : stocke les régions de marquage des personnes. Consultez la section schéma de la zone de photo Microsoft qui suit. |



 

### <a name="microsoft-photo-region-schema"></a>Schéma de la région de photo Microsoft

Le schéma de la zone de photo Microsoft 1,2 fournit un ensemble de propriétés pour les régions d’image.

-   L’URI de l’espace de noms du schéma est `https://ns.microsoft.com/photo/1.2/t/Region#` .
-   Le préfixe de l’espace de noms du schéma par défaut est `MPReg` .



| MPReg : propriété          | Type de valeur | Category | Description                                                                                                                                                                                                                                                                                                     |
|-------------------------|------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MPReg:PersonDisplayName | Texte       | Externe | **Required** : stocke le nom de la personne dans le rectangle donné.                                                                                                                                                                                                                                            |
| MPReg : rectangle         | Texte       | Externe | **facultatif** : stocke le rectangle qui identifie la personne au sein de la photo. Le rectangle est stocké sous la forme de quatre valeurs décimales délimitées par des virgules. Les deux premières valeurs spécifient la coordonnée supérieure gauche ; les deux derniers spécifient la hauteur et la largeur du rectangle. Les valeurs décimales doivent être normalisées en 1. |
| MPReg:PersonEmailDigest | Texte       | Externe | **facultatif** : stocke le hachage de message SHA-1 chiffré de l’adresse de messagerie en direct de la personne.                                                                                                                                                                                                                     |
| MPReg:PersonLiveIdCID   | Texte       | Externe | **facultatif** : stocke la représentation décimale signée du CID actif de la personne, un entier 64 bits qui identifie publiquement une identité active.                                                                                                                                                                     |



 

### <a name="sample-metadata"></a>Exemples de métadonnées

Voici une représentation des métadonnées XMP pour le balisage des personnes.

``` syntax
<rdf:Description rdf:about="" xmlns:MP="https://ns.microsoft.com/photo/1.2/">
<MP:RegionInfo> 
<rdf:Description xmlns:MPRI="https://ns.microsoft.com/photo/1.2/t/RegionInfo#">
   <MPRI:Regions> 
       <rdf:Bag> 
          <rdf:li> 
       <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#"> 
           <MPReg:Rectangle>0.790650, 0.441734, 0.209350, 0.279133
           </MPReg:Rectangle>
           <MPReg:PersonDisplayName>John Doe</MPReg:PersonDisplayName> 
           <MPReg:PersonEmailDigest>2FD4E1C67A2D28FCED849EE1BB76E7391B93EB13</MPReg:PersonEmailDigest> 
           <MPReg:PersonLiveIdCID>1234567890123456789</MPReg:PersonLiveIdCID> 
       </rdf:Description> 
         </rdf:li> 
         <rdf:li>
             <rdf:Description xmlns:MPReg="https://ns.microsoft.com/photo/1.2/t/Region#">
                  <MPReg:Rectangle>0.222656, 0.302083, 0.378906, 0.505208</MPReg:Rectangle> 
                  <MPReg:PersonDisplayName>Jane Doe</MPReg:PersonDisplayName> 
              </rdf:Description> 
         </rdf:li> 
<!-- Addition Regions --> ... 
<rdf:li>...
</rdf:li> 
</rdf:Bag> 
</MPRI:Regions> </rdf:Description> </MP:RegionInfo> </rdf:Description>
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Vue d’ensemble des métadonnées WIC](-wic-about-metadata.md)
</dt> <dt>

[Vue d’ensemble de la lecture et de l’écriture des métadonnées d’image](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Vue d’ensemble du langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md)
</dt> </dl>

 

 
