---
description: Cette rubrique présente la prise en charge des métadonnées de création d’images fournie par le WIC (Windows Imaging Component).
ms.assetid: 35727810-3c4c-4c11-a4a2-3ae2cf3b8142
title: Vue d’ensemble des métadonnées WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f00e3a77eb74a3fb4a00db05ef9e00028f02ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556412"
---
# <a name="wic-metadata-overview"></a>Vue d’ensemble des métadonnées WIC

Cette rubrique présente la prise en charge des métadonnées de création d’images fournie par le WIC (Windows Imaging Component). Il fournit une présentation de la lecture et de l’écriture des métadonnées d’image, du langage de requête de métadonnées et de l’extensibilité du gestionnaire de métadonnées.

Les métadonnées d’image sont des données incorporées dans un fichier image qui fournit des informations supplémentaires sur l’image, telles que l’appareil utilisé pour capturer l’image ou les dimensions de l’image. Bien qu’elle soit contenue dans le fichier image lui-même, ces métadonnées ne font pas partie des données de rendu. WIC fournit des interfaces qui vous permettent de lire et d’écrire ces métadonnées pour plusieurs formats de métadonnées courants, notamment les formats de métadonnées XMP (Extensible Metadata Platform), EXIF (échanged image file) et png (texte).

Cette rubrique contient les sections suivantes.

-   [Conditions préalables](#prerequisites)
-   [Introduction](#introduction)
-   [Lecture des métadonnées de l’image](#reading-image-metadata)
-   [Écriture de métadonnées d’image](#writing-image-metadata)
-   [Extensibilité des métadonnées](#metadata-extensibility)
-   [Formats de métadonnées pris en charge](#supported-metadata-formats)
-   [Résumé du composant de métadonnées](#metadata-component-summary)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

Pour comprendre cette rubrique, vous devez être familiarisé avec l’encodeur et les interfaces de décodeur WIC et leurs composants COM (Component Object Model) associés, comme décrit dans [vue d’ensemble du composant de création d’images Windows](-wic-about-windows-imaging-codec.md). Il permet également d’avoir une connaissance générale de certains des formats de métadonnées de création d’images actuellement utilisés.

## <a name="introduction"></a>Introduction

Les métadonnées fournissent des informations étendues sur une image. Ces informations peuvent être utilisées de plusieurs façons. Une image peut contenir des métadonnées telles qu’une description, une évaluation, des balises de catégorie et des informations de copyright. L’accès aux métadonnées facilite l’exécution de tâches telles que la gestion des ressources, l’emplacement des fichiers ou la détermination des informations de copyright. Par exemple, la Galerie de photos Windows dans Windows Vista vous permet d’ajouter des descriptions et des balises de catégorie aux images. Cela permet une meilleure détectabilité des images et un moyen pratique de classer les images. À l’aide des API WIC et des formats de métadonnées courants, les applications peuvent facilement écrire ou lire ce type de métadonnées vers ou à partir d’images.

Le diagramme suivant illustre le contenu d’un fichier JPEG qui comprend des blocs de métadonnées incorporés et des éléments de métadonnées.

![image JPEG avec les métadonnées d’évaluation](graphics/jpeg.png)

Dans cet exemple d’image, les métadonnées sont incorporées dans le fichier image au sein d’une image. Le format JPEG ne prenant pas en charge plusieurs trames d’image, les métadonnées sont attachées de manière conceptuelle à ce frame unique. Les formats qui prennent en charge plusieurs frames, tels que TIFF, peuvent avoir des métadonnées attachées à chaque frame d’image comme le montre ce diagramme. Bien qu’il ne soit pas courant aujourd’hui ni pris en charge par les codecs d’image native, certains formats d’image peuvent également prendre en charge les métadonnées en dehors d’une image. WIC est suffisamment flexible pour gérer les métadonnées de niveau image et les métadonnées en dehors du frame individuel d’une image.

## <a name="reading-image-metadata"></a>Lecture des métadonnées de l’image

Les API WIC fournissent des composants COM qui permettent aux applications de lire et d’écrire facilement des métadonnées d’image.

Le principal moyen de lire les métadonnées consiste à utiliser un lecteur de requêtes de métadonnées ([**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)) pour accéder à des éléments de métadonnées spécifiques. Le composant lecteur de requêtes de métadonnées est implémenté par le codec et est accessible au niveau du décodeur ou via des trames d’image individuelles, qui est la méthode la plus courante. Le code suivant montre comment accéder à un lecteur de requêtes pour un frame individuel à l’aide de la méthode **GetMetadataQueryReader** du lecteur de requête.


```
// Get the query reader
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}
```



Un lecteur de requête fournit des méthodes pour obtenir des informations sur des métadonnées spécifiques et un moyen de spécifier un élément de métadonnées à récupérer. Le code suivant utilise une expression de requête pour demander un élément de métadonnées spécifique dans le bloc répertoire du fichier d’image imbriquée App1 (IFD). Pour ce faire, utilisez la méthode **GetMetadataByName** du lecteur de requête. Le code suivant illustre l’utilisation du lecteur de requête pour obtenir la valeur d’évaluation MicrosoftPhoto.


```
PROPVARIANT value;
PropVariantInit(&value);

LPCWSTR pwzRatingQuery = L"/app1/ifd/{ushort=18249}";

if (SUCCEEDED(hr))
{
    hr = pQueryReader->GetMetadataByName(pwzRatingQuery, &value);
}
```



La variable pwzRatingQuery dans l’exemple précédent est la chaîne de requête pour accéder à l’évaluation de MicrosoftPhoto de l’élément de métadonnées. Cette chaîne est créée à l’aide du langage de requête de métadonnées. Pour créer cette chaîne, il est nécessaire de connaître le format des métadonnées et le langage de requête des métadonnées pour récupérer des éléments de métadonnées individuels. Pour plus d’informations sur le langage de requête de métadonnées, consultez la [vue d’ensemble du langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md).

En arrière-plan, un lecteur de requête utilise un lecteur de métadonnées ([**IWICMetadataReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader)) pour accéder aux métadonnées décrites par l’expression de requête. En plus d’utiliser un lecteur de requêtes, vous pouvez également accéder directement à un lecteur de métadonnées pour lire les métadonnées. Vous pouvez obtenir un lecteur de métadonnées à partir du décodeur ou des frames individuels en interrogeant une interface de lecteur de bloc ([**IWICMetadataBlockReader**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)).

## <a name="writing-image-metadata"></a>Écriture de métadonnées d’image

Le processus d’écriture des métadonnées est similaire à la façon dont il est lu, sauf qu’un enregistreur de requêtes de métadonnées ([**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)) est utilisé. L’interface du writer de requête est implémentée par l’encodeur d’image et, comme dans le lecteur de requête, les métadonnées sont accessibles à la fois sur l’encodeur et sur des frames individuels (en fonction de la prise en charge du format d’image).

Le code suivant montre comment obtenir un enregistreur de requête à partir d’un frame d’encodeur et supprimer la valeur d’évaluation précédemment lue.


```
// Get the frame's query writer
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->GetMetadataQueryWriter(&pFrameQWriter);
}

if (SUCCEEDED(hr))
{
    hr = pFrameQWriter->RemoveMetadataByName(L"/app1/ifd/{ushort=18249}");
}
```



Une autre façon d’écrire des métadonnées consiste à utiliser des mises à jour de métadonnées rapides. L’encodage de métadonnées rapide est un moyen d’écrire des métadonnées d’image sans avoir à recoder un fichier image. Cela s’effectue en écrivant de nouvelles métadonnées dans une zone rembourrée du format de métadonnées. L’encodeur de métadonnées rapide ([**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)) est obtenu à partir de la fabrique de composants, en fonction du décodeur d’image. L’encodeur de métadonnées rapide obtient alors un générateur de requêtes qui est utilisé pour écrire les métadonnées. Enfin, l’encodeur rapide valide la modification.

Le code suivant montre comment obtenir un encodeur de métadonnées rapide et l’utiliser pour écrire la valeur MicrosoftRating.


```
if (SUCCEEDED(hr))
{
    IWICFastMetadataEncoder *pFME = NULL;
    IWICMetadataQueryWriter *pFMEQW = NULL;

    hr = pFactory->CreateFastMetadataEncoderFromFrameDecode(
        pFrameDecode,
        &pFME);

    if (SUCCEEDED(hr))
    {
        hr = pFME->GetMetadataQueryWriter(&pFMEQW);
    }

    if (SUCCEEDED(hr))
    {
        // Add additional metadata
        PROPVARIANT value;

        PropVariantInit(&value);

        value.vt = VT_UI4;
        value.uiVal = 99;
        hr = pFMEQW->SetMetadataByName(L"/app1/ifd/{ushort=18249}", &value);

        PropVariantClear(&value);
    }

    if (SUCCEEDED(hr))
    {
        hr = pFME->Commit();
    }
}
```



Tous les formats de métadonnées ne prennent pas en charge les métadonnées rapides. Pour savoir quels formats pris en charge en mode natif prennent en charge l’encodage de métadonnées rapide, consultez le tableau dans la section [formats de métadonnées pris en charge](#supported-metadata-formats) plus loin dans ce document.

En arrière-plan, un writer de requête utilise un enregistreur de métadonnées ([**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)) pour écrire les métadonnées décrites par l’expression de requête. En plus d’utiliser un lecteur de requêtes, vous pouvez également accéder directement à un enregistreur de métadonnées pour écrire des métadonnées. Vous pouvez obtenir un générateur de métadonnées à partir du décodeur ou des frames individuels à l’aide de l’interrogation d’une interface de writer de bloc ([**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter)).

## <a name="metadata-extensibility"></a>Extensibilité des métadonnées

Comme mentionné précédemment, WIC fournit plusieurs gestionnaires de métadonnées pour lire et écrire des métadonnées pour les formats de métadonnées courants. Toutefois, certains formats de métadonnées ne sont pas pris en charge en mode natif. Par conséquent, WIC fournit des API pour créer des gestionnaires de métadonnées supplémentaires qui peuvent étendre la prise en charge des métadonnées à d’autres formats.

Pour prendre entièrement en charge d’autres formats de métadonnées, deux types de gestionnaires doivent être développés : un lecteur de métadonnées pour lire les métadonnées et un générateur de métadonnées pour écrire des métadonnées. Bien que ces deux gestionnaires soient généralement implémentés par paires pour un format spécifique, ce n’est pas une exigence. Dans certains cas, seule la capacité de lecture ou uniquement la capacité d’écriture est nécessaire.

Pour plus d’informations sur l’extensibilité des métadonnées à l’aide des API WIC, consultez [vue d’ensemble de l’extensibilité des métadonnées](-wic-codec-metadatahandlers.md).

## <a name="supported-metadata-formats"></a>Formats de métadonnées pris en charge

WIC prend en charge plusieurs formats de métadonnées courants. Le tableau suivant répertorie les formats de métadonnées pris en charge, leurs versions, les formats d’image qui prennent en charge le format de métadonnées, et indique si le format de métadonnées prend en charge l’encodage de métadonnées rapide. Pour plus d’informations sur l’encodage des métadonnées rapide, consultez la section [écriture de métadonnées d’image](#writing-image-metadata) plus haut dans ce document.



| Formats de métadonnées pris en charge | Version de la spécification de métadonnées | Prise en charge du format d’image | Prend en charge l’encodage de métadonnées rapide |
|----------------------------|--------------------------------|----------------------|---------------------------------|
| App0                       | JFIF 1,02                      | JPEG                 | Non                              |
| App1                       | JFIF 1,02                      | JPEG, TIFF           | Non                              |
| App13                      | Unknown                        | JPEG, TIFF           | Non                              |
| IFD                        | TIFF 6,0                       | JPEG, TIFF           | Oui                             |
| IRB                        | Unknown                        | JPEG, TIFF           | Non                              |
| Exif                       | EXIF 2,2                       | JPEG, TIFF           | Oui                             |
| XMP                        | XMP 1,0 (septembre 2005)            | JPEG, TIFF           | Oui                             |
| GPS                        | EXIF 2,2                       | JPEG, TIFF           | Oui                             |
| IPTC                       | IPTC 4,0                       | JPEG, TIFF           | Oui                             |
| Financière                       | PNG 1,2                        | PNG                  | Non                              |



 

> [!Note]  
> IPTC prend en charge uniquement FME si la taille des blocs augmente, car IPTC ne prend pas en charge le remplissage.

 

## <a name="metadata-component-summary"></a>Résumé du composant de métadonnées

Le tableau suivant décrit les interfaces WIC qui prennent en charge les métadonnées et leurs composants correspondants. Ces composants fournissent l’accès aux métadonnées d’une image. Pour plus d’informations sur ces composants, consultez [vue d’ensemble du composant de création d’images Windows](-wic-about-windows-imaging-codec.md). 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Composant</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Décodeur bitmap (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder"><strong>IWICBitmapDecoder</strong></a>)</td>
<td><ul>
<li>Lit un flux d’image et produit une source bitmap utilisable. Associé à un format de conteneur tel que TIFF (Tagged Image File Format) ou JPEG (Joint Photographic Experts Group).</li>
<li>Implémente une interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> pour énumérer tous les blocs de métadonnées dans le flux de données du décodeur qui ne se trouvent pas à l’intérieur d’un frame.</li>
<li>Expose un lecteur de requêtes pour lire les métadonnées associées à l’image qui ne se trouve pas à l’intérieur d’un frame.</li>
</ul></td>
</tr>
<tr class="even">
<td>Décodage de cadre bitmap (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode"><strong>IWICBitmapFrameDecode</strong></a>)</td>
<td><ul>
<li>Accède à des frames individuels à partir du flux d’images détenu par le décodeur.</li>
<li>Implémente une interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a> pour énumérer tous les blocs de métadonnées dans le flux de données du frame.</li>
<li>Expose un lecteur de requêtes pour lire les métadonnées associées au frame, à l’aide d’expressions de requête.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Encodeur bitmap (<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder"><strong>IWICBitmapEncoder</strong></a>)</td>
<td><ul>
<li>Écrit une source bitmap dans un flux d’image. Associé à un format de conteneur tel que TIFF ou JPEG.</li>
<li>Implémente une interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> pour générer une liste de blocs de métadonnées à écrire dans le flux de données de l’encodeur.</li>
<li>Expose un générateur de requêtes pour écrire les métadonnées associées à l’image, à l’aide d’expressions de requête.</li>
</ul></td>
</tr>
<tr class="even">
<td>Encodage de trame Bitma (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode"><strong>IWICBitmapFrameEncode</strong></a>)</td>
<td><ul>
<li>Crée un frame qui sera encodé dans le flux détenu par l’encodeur.</li>
<li>Implémente une interface <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a> pour générer une liste de blocs de métadonnées à écrire dans le flux de données du frame.</li>
<li>Expose un générateur de requêtes pour écrire les métadonnées associées au frame, à l’aide d’expressions de requête.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Le tableau suivant décrit les composants de métadonnées WIC. Ces composants vous permettent de lire et d’écrire les métadonnées dans une image exposée par les composants répertoriés dans le tableau précédent. 

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Composant</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lecteur de requêtes de métadonnées (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader"><strong>IWICMetadataQueryReader</strong></a>)</td>
<td><ul>
<li>Prend une chaîne de requête et parcourt la hiérarchie de métadonnées sous-jacente pour obtenir les métadonnées.</li>
</ul></td>
</tr>
<tr class="even">
<td>Générateur de requêtes de métadonnées (<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter"><strong>IWICMetadataQueryWriter</strong></a>)</td>
<td><ul>
<li>Prend une chaîne de requête et parcourt la hiérarchie de métadonnées sous-jacente pour obtenir, définir et supprimer des métadonnées.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lecteur de bloc de métadonnées (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader"><strong>IWICMetadataBlockReader</strong></a>)</td>
<td><ul>
<li>Gère une collection en lecture seule d’objets <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a> en haut de la hiérarchie de métadonnées et permet l’énumération de tous les blocs de métadonnées.</li>
<li>Implémenté par un décodeur bitmap et un frame bitmap décodé.</li>
<li>Implémenté par les développeurs de composants tiers pour les codecs personnalisés.</li>
</ul></td>
</tr>
<tr class="even">
<td>Enregistreur de bloc de métadonnées (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter"><strong>IWICMetadataBlockWriter</strong></a>)</td>
<td><ul>
<li>Gère une collection de lecture et d’écriture d’objets <a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a> en haut de la hiérarchie de métadonnées.</li>
<li>Implémenté par un encodeur bitmap et un encodage de frame bitmap.</li>
<li>Implémenté par les développeurs de composants tiers pour les codecs personnalisés.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Lecteur de métadonnées (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatareader"><strong>IWICMetadataReader</strong></a>)</td>
<td><ul>
<li>Analyse un flux de métadonnées et gère une collection en lecture seule des éléments de métadonnées. Associé à un format de métadonnées tel que EXIF, IFD et XMP.</li>
<li>Agit comme un dictionnaire, en retournant une valeur lorsqu’une paire format-ID est spécifiée.</li>
<li>Implémenté par les développeurs de composants tiers pour les types de métadonnées personnalisés.</li>
</ul></td>
</tr>
<tr class="even">
<td>Enregistreur de métadonnées (<a href="/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter"><strong>IWICMetadataWriter</strong></a>)</td>
<td><ul>
<li>Analyse et sérialise un flux de métadonnées et gère une collection en lecture/écriture d’éléments de métadonnées.</li>
<li>Implémenté par les développeurs de composants tiers pour les types de métadonnées personnalisés.</li>
</ul></td>
</tr>
<tr class="odd">
<td>IWICFastMetadataEncoder rapide de l’encodeur de métadonnées<a href="/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder"><strong></strong></a></td>
<td><ul>
<li>Expose la sémantique pour l’écriture dans une hiérarchie de métadonnées qui met à jour les métadonnées en place sans recoder l’image.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Vue d’ensemble du langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Vue d’ensemble de la lecture et de l’écriture des métadonnées d’image](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Vue d’ensemble de l’extensibilité des métadonnées](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Comment : recoder une image JPEG avec des métadonnées](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



