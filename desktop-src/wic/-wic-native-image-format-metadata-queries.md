---
description: Cette rubrique fournit une vue d’ensemble des requêtes de langage de requête de métadonnées pour la lecture et l’écriture de métadonnées prises en charge par les images GIF, PNG, TIFF et JPEG.
ms.assetid: a6ab1708-dd82-4960-b908-f1daef7374ef
title: Requêtes de métadonnées au format d’image natif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 463315a1fb18f0f3dc177635f7e63505589e239257dc9cc25fcfa0773ddb25f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882379"
---
# <a name="native-image-format-metadata-queries"></a>Requêtes de métadonnées au format d’image natif

Cette rubrique fournit une vue d’ensemble des requêtes de [langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md) pour la lecture et l’écriture de métadonnées prises en charge par les images gif, png, TIFF et JPEG. Il comprend des métadonnées spécifiques à chaque format d’image, ainsi que des métadonnées prises en charge par plusieurs formats.

Cette rubrique contient les sections suivantes.

-   [Composants requis](#prerequisites)
-   [Expression de stratégie de métadonnées de photo](#photo-metadata-policy-expression)
-   [Métadonnées spécifiques au format de fichier](#file-format-specific-metadata)
    -   [Métadonnées GIF](#gif-metadata)
    -   [Métadonnées PNG](#png-metadata)
    -   [Métadonnées TIFF](#tiff-metadata)
    -   [Métadonnées JPEG](#jpeg-metadata)
-   [Métadonnées indépendantes du format de fichier](#file-format-independent-metadata)
    -   [Métadonnées IFD](#ifd-metadata)
    -   [Métadonnées EXIF](#exif-metadata)
    -   [Métadonnées GPS](#gps-metadata)
    -   [Métadonnées XMP](#xmp-metadata)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

pour comprendre cette rubrique, vous devez être familiarisé avec le système de métadonnées wic (Windows Imaging Component), comme décrit dans [vue d’ensemble des métadonnées wic](-wic-about-metadata.md). Vous devez également être familiarisé avec le langage de requête utilisé pour lire et écrire des métadonnées, comme décrit dans [vue d’ensemble du langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md).

## <a name="photo-metadata-policy-expression"></a>Expression de stratégie de métadonnées de photo

en plus de prendre en charge le langage de requête de métadonnées, [WIC](-wic-api.md) accepte également les noms de propriété canoniques du [système de propriétés Windows](../properties/windows-properties-system.md). WIC prend en charge un sous-ensemble de l’espace de noms de propriété Windows qui concerne les formats d’image, comme décrit dans [stratégies de métadonnées de photos](photo-metadata-policies.md). une propriété de Windows utilisée en tant que requête de métadonnées WIC est appelée expression de stratégie de métadonnées de photo.

Par exemple, l’expression de stratégie de métadonnées de photo pour l’indicateur d’orientation EXIF est :

-   [System. photo. orientation](-wic-photoprop-system-photo-orientation.md)

en général, les expressions de stratégie sont recommandées par rapport aux requêtes de métadonnées natives pour les éléments de métadonnées d’image courants qui sont couverts par l’espace de noms de propriété Windows. le langage de requête de métadonnées est mieux adapté aux cas où un accès de bas niveau à des éléments de métadonnées d’image spécifiques est nécessaire ou pour des éléments de métadonnées personnalisés ou avancés qui ne sont pas pris en charge par le système de propriétés Windows. Pour plus d’informations, consultez [expressions de stratégie de métadonnées de photos](-wic-codec-metadataquerylanguage.md).

## <a name="file-format-specific-metadata"></a>Métadonnées spécifiques au format de fichier

Les sections suivantes contiennent des tables qui répertorient les requêtes de métadonnées disponibles pour chaque type de fichier image. Chaque table contient les colonnes suivantes :

-   **Path** : chemin d’accès de la requête utilisé pour récupérer l’élément de métadonnées.
-   **Nom** : nom de l’élément de métadonnées.
-   **Type** : type de l’élément de métadonnées récupéré à partir du chemin d’accès de la requête. Les métadonnées récupérées par [WIC](-wic-api.md) sont retournées sous la forme de PROPVARIANT, qui signale le type de données à l’aide de l’énumération VarType. on.

Les chemins d’accès de requête sont utilisés par l’API de métadonnées WIC pour accéder aux métadonnées incorporées d’une image. L’exemple de code suivant illustre l’utilisation d’un [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) pour interroger le bloc de métadonnées IFD d’un JPEG.


```
// Not shown: image decoding 
IWICMetadataQueryReader *pQueryReader = NULL;
IWICMetadataQueryReader *pIFDReader = NULL;

// Get the query reader.
if (SUCCEEDED(hr))
{
    hr = pFrameDecode->GetMetadataQueryReader(&pQueryReader);
}

if (SUCCEEDED(hr))
{
    // Get the nested IFD reader.
    hr = pQueryReader->GetMetadataByName(L"/app1/ifd", &value);
    if (value.vt == VT_UNKNOWN)
    {
        hr = value.punkVal->QueryInterface(IID_IWICMetadataQueryReader, (void **)&pIFDReader);
    }
    PropVariantClear(&value); // Clear value for new query.
}
```



### <a name="gif-metadata"></a>Métadonnées GIF

Le format d’image GIF (Graphics Interchange Format) prend en charge les métadonnées globales et de niveau image. Les deux sections suivantes fournissent les chemins d’accès aux requêtes de métadonnées disponibles pour les métadonnées globales et de niveau de frame de GIF.

> [!Note]  
> Pour obtenir une liste complète des métadonnées GIF et des informations plus détaillées, consultez la [norme gif](https://www.w3.org/Graphics/GIF/spec-gif89a.txt) sur le site Web du W3C.

 

### <a name="global-metadata"></a>Métadonnées globales

Le tableau suivant fournit les chemins d’accès aux requêtes de métadonnées disponibles qui peuvent être utilisés pour accéder aux métadonnées GIF globales.



| Chemin                                               | Nom                       | Type                                |
|----------------------------------------------------|----------------------------|-------------------------------------|
| /commentext ou/ \[ \* \] commentext où \* = 0 à N | Extension de commentaire          | VT \_ inconnu-lecteur/enregistreur de requêtes |
| /commentext/TextEntry                              |                            | VT- \_ LPSTR                           |
| /logscrdesc                                        | Description de l’écran logique | VT \_ inconnu-lecteur/enregistreur de requêtes |
| /logscrdesc/Signature                              |                            | Vecteur VT VT \_ UI1 \| \_               |
| /logscrdesc/Width                                  |                            | \_UI2 VT                             |
| /logscrdesc/Height                                 |                            | \_UI2 VT                             |
| /logscrdesc/GlobalColorTableFlag                   |                            | VT \_ bool                            |
| /logscrdesc/ColorResolution                        |                            | \_UI1 VT                             |
| /logscrdesc/SortFlag                               |                            | VT \_ bool                            |
| /logscrdesc/GlobalColorTableSize                   |                            | \_UI1 VT                             |
| /logscrdesc/BackgroundColorIndex                   |                            | \_UI1 VT                             |
| /logscrdesc/PixelAspectRatio                       |                            | \_UI1 VT                             |
| /appext ou/ \[ \* \] appext où \* = 0 à N         | Extension d’application      | VT \_ inconnu-lecteur/enregistreur de requêtes |
| /appext/Application                                |                            | Vecteur VT VT \_ UI1 \| \_               |
| /appext/Data                                       |                            | Vecteur VT VT \_ UI1 \| \_               |



 

### <a name="frame-metadata"></a>Métadonnées de frame

Le tableau suivant fournit les chemins d’accès aux requêtes de métadonnées disponibles qui peuvent être utilisés pour accéder aux métadonnées GIF au niveau de la trame.



| Chemin                            | Nom                      | Type                              |
|---------------------------------|---------------------------|-----------------------------------|
| /grctlext                       | Extension de contrôle graphique | VT \_ inconnu-lecture/écriture de requêtes |
| /grctlext/Disposal              |                           | \_UI1 VT                           |
| /grctlext/UserInputFlag         |                           | VT \_ bool                          |
| /grctlext/TransparencyFlag      |                           | VT \_ bool                          |
| /grctlext/Delay                 |                           | \_UI2 VT                           |
| /grctlext/TransparentColorIndex |                           | \_UI1 VT                           |
| /imgdesc                        | Descripteur d’image          | VT \_ inconnu-lecture/écriture de requêtes |
| /imgdesc/Left                   |                           | \_UI2 VT                           |
| /imgdesc/Top                    |                           | \_UI2 VT                           |
| /imgdesc/Width                  |                           | \_UI2 VT                           |
| /imgdesc/Height                 |                           | \_UI2 VT                           |
| /imgdesc/LocalColorTableFlag    |                           | VT \_ bool                          |
| /imgdesc/InterlaceFlag          |                           | VT \_ bool                          |
| /imgdesc/SortFlag               |                           | VT \_ bool                          |
| /imgdesc/LocalColorTableSize    |                           | \_UI1 VT                           |



 

### <a name="png-metadata"></a>Métadonnées PNG

Le format d’image PNG (Portable Network Graphics) prend en charge les métadonnées au niveau de la trame.

> [!Note]  
> Pour obtenir une liste complète des métadonnées PNG et des informations plus détaillées, consultez la [norme png](https://www.w3.org/TR/PNG/) sur le site Web du W3C.

 

### <a name="frame-metadata"></a>Métadonnées de frame

Le tableau suivant fournit les chemins d’accès aux requêtes de métadonnées disponibles qui peuvent être utilisés pour accéder aux métadonnées PNG au niveau de la trame.



| Chemin                                                   | Nom             | Type                                      |
|--------------------------------------------------------|------------------|-------------------------------------------|
| /Text ou/ \[ \* \] Text où \* = 0 à N                 | Bloc de texte       | VT \_ /lecteur de requêtes de texte inconnu    |
| /tEXt/{str = \* } où \* = mot clé d’identification du texte |                  | VT- \_ LPSTR                                 |
| /gAMA                                                  | Segment Gama       | VT \_ inconnu-lecteur/enregistreur de requêtes Gama    |
| /gAMA/ImageGamma                                       |                  | VT \_ UI4                                   |
| /iTXt ou/ \[ \* \] iTXt où \* = 0 à N                 | Segment IText      | VT \_ inconnu-lecteur/enregistreur de requêtes iTXt    |
| /iTXt/Keyword                                          |                  | VT- \_ LPSTR                                 |
| /iTXt/CompressionFlag                                  |                  | \_UI1 VT                                   |
| /iTXt/LanguageTag                                      |                  | LPSTR                                     |
| /iTXt/TranslatedKeyword                                |                  | LPWSTR                                    |
| /iTXt/TextEntry                                        |                  | LPWSTR                                    |
| /cHRM                                                  | Segment HRM        | VT \_ inconnu-lecteur/enregistreur de requêtes cHRM    |
| /cHRM/WhitePointX                                      |                  | VT \_ UI4                                   |
| /cHRM/WhitePointY                                      |                  | VT \_ UI4                                   |
| /cHRM/RedX                                             |                  | VT \_ UI4                                   |
| /cHRM/RedY                                             |                  | VT \_ UI4                                   |
| /cHRM/GreenX                                           |                  | VT \_ UI4                                   |
| /cHRM/GreenY                                           |                  | VT \_ UI4                                   |
| /cHRM/BlueX                                            |                  | VT \_ UI4                                   |
| /cHRM/BlueY                                            |                  | VT \_ UI4                                   |
| /sRGB                                                  | Mandrin sRVB       | VT \_ inconnu-lecture/écriture de requêtes sRVB    |
| /sRGB/RenderingIntent                                  |                  | \_UI1 VT                                   |
| /tIME                                                  | Segment de temps       | \_Lecture/écriture de requêtes à temps inconnues VT    |
| /tIME/Year                                             |                  | \_UI2 VT                                   |
| /tIME/Month                                            |                  | \_UI1 VT                                   |
| /tIME/Day                                              |                  | \_UI1 VT                                   |
| /tIME/Hour                                             |                  | \_UI1 VT                                   |
| /tIME/Minute                                           |                  | \_UI1 VT                                   |
| /tIME/Second                                           |                  | \_UI1 VT                                   |
| /bKGD                                                  | Bloc d’arrière-plan | VT \_ inconnu-lecteur/enregistreur de requêtes bKGB    |
| /bKGD/BackgroundColor                                  |                  | VT \_ UI1, VT \_ UI2 ou VT \_ UI2 \| VT \_ Vector |
| /hIST                                                  | Bloc hIST       | VT \_ inconnu-lecteur/enregistreur de requêtes hIST    |
| /hIST/Frequencies                                      |                  | VT \_ UI2 VT Vector \| \_                     |
| /iCCP                                                  | Segment iCCP       | VT \_ inconnu-lecteur/enregistreur de requêtes iCCP    |
| /iCCP/ProfileName                                      |                  | VT- \_ LPSTR                                 |
| /iCCP/ProfileData                                      |                  | VT \_ UI1 VT Vector \| \_                     |



 

### <a name="tiff-metadata"></a>Métadonnées TIFF

Le format d’image TIFF (Tagged Image File Format) prend en charge les métadonnées de niveau trame.

> [!Note]  
> Pour obtenir une liste complète des métadonnées TIFF et des informations plus détaillées, consultez [la norme TIFF](https://www.adobe.io/content/dam/udp/en/open/standards/tiff/TIFF6.pdf).

 

### <a name="frame-metadata"></a>Métadonnées de frame

Le tableau suivant fournit les chemins d’accès aux requêtes de métadonnées disponibles qui peuvent être utilisés pour accéder aux métadonnées TIFF au niveau de la trame.



| Chemin                                          | Nom            | Type                                |
|-----------------------------------------------|-----------------|-------------------------------------|
| /ifd                                          | 0 IFD           | VT \_ inconnu-lecteur/enregistreur de requêtes |
| /IFD/{UShort = \* } où \* = 0 à 65535        | Entrée IFD par ID | Variable                            |
| /IFD/Thumb ou/IFD/{UShort = 330}               | Miniature IFD   | VT \_ inconnu-lecteur/enregistreur de requêtes |
| /IFD/XMP ou/IFD/{UShort = 700}                 | XMP             | VT \_ inconnu-lecteur/enregistreur de requêtes |
| /IFD/EXIF ou/IFD/{UShort = 34665}              | EXIF            | VT \_ inconnu-lecteur/enregistreur de requêtes |
| /IFD/GPS ou/IFD/{UShort = 34853}               | GPS             | VT \_ inconnu-lecteur/enregistreur de requêtes |
| /IFD/EXIF/Interop ou/IFD/EXIF/{UShort = 40965} | Interop         | VT \_ inconnu-lecteur/enregistreur de requêtes |
| /IFD/IPTC ou/IFD/{UShort = 33723}              | IPTC            | VT \_ inconnu-lecteur/enregistreur de requêtes |
| /IFD/IPTC/{Str = \* } where \* = mot clé IPTC    | Entrée IPTC      | Variable                            |
| /ifd/irb/8bimiptc/iptc                        | IPTC            | VT \_ inconnu-lecteur/enregistreur de requêtes |
| /IFD/IRB/8bimiptc/IPTC/{Str = \* }               | Entrée IPTC      | Variable                            |



 

### <a name="jpeg-metadata"></a>Métadonnées JPEG

Le format d’image JPEG prend en charge les métadonnées au niveau du frame.

> [!Note]  
> Pour obtenir la liste complète des métadonnées JPEG et des informations plus détaillées, consultez la [norme EXIF JPEG](http://www.cipa.jp/std/documents/e/DC-008-2010_E.pdf).

 

### <a name="frame-metadata"></a>Métadonnées de frame

Le tableau suivant fournit les chemins d’accès aux requêtes de métadonnées disponibles qui peuvent être utilisés pour accéder aux métadonnées JPEG au niveau de la trame.



| Chemin                                                               | Nom                 | Type                                          |
|--------------------------------------------------------------------|----------------------|-----------------------------------------------|
| /app0                                                              | App0                 | VT \_ inconnu-lecteur/enregistreur de requêtes APP0        |
| /APP0/{UShort = 0}                                                   | Version              | \_UI2 VT                                       |
| /APP0/{UShort = 1}                                                   | Unités                | \_UI1 VT                                       |
| /APP0/{UShort = 2}                                                   | DpiX                 | \_UI2 VT                                       |
| /APP0/{UShort = 3}                                                   | DpiY                 | \_UI2 VT                                       |
| /APP0/{UShort = 4}                                                   | Xthumbnail           | \_UI1 VT                                       |
| /APP0/{UShort = 5}                                                   | Ythumbnail           | \_UI1 VT                                       |
| /APP0/{UShort = 6}                                                   | ThumbnailData        | \_objet BLOB VT                                      |
| /App1                                                              | App1                 | VT \_ inconnu-lecteur/enregistreur de requêtes App1        |
| /App1/IFD ou/App1/{UShort = 0}                                     | 0 IFD                | VT \_ inconnu-lecteur/enregistreur de requêtes IFD         |
| /App1/IFD/EXIF ou/App1/IFD/{UShort = 34665}                         | IFD EXIF             | VT \_ inconnu – lecteur/enregistreur de requêtes EXIF        |
| /App1/Thumb ou/App1/{UShort = 1}                                   | Miniature IFD        | VT \_ inconnu-lecteur/enregistreur de requêtes SubIFD      |
| /app13                                                             | App13                | VT \_ inconnu-lecteur/enregistreur de requêtes APP13       |
| /APP13/IRB ou/APP13/{UShort = 0}                                    | IRB                  | VT \_ inconnu-lecteur/enregistreur de requêtes IRB         |
| /APP13/IRB/{ULONGLONG = \* } où \* = IRB identificateur (voir spécification IRB) | Entrée IRB            | VT \_ inconnu-lecteur/enregistreur de requêtes inconnu     |
| /APP13/IRB/{ULONGLONG = \* }/{}                                       | Contenu de l’entrée IRB   | \_objet BLOB VT                                      |
| /APP13/IRB/8bimiptc ou/APP13/IRB/{ULONGLONG = 61857348781060}       | 8BIMIPTC             | VT \_ inconnu-lecteur/enregistreur de requêtes 8BIMIPTC    |
| /app13/irb/8bimiptc/iptc                                           | IPTC                 | VT \_ inconnu-lecteur/enregistreur de requêtes IPTC        |
| /APP13/IRB/8bimiptc/IPTC/{Str = \* }                                  | Entrée IPTC           | Variable                                      |
| /app13/irb/8bimResInfo ou/APP13/IRB/{ULONGLONG = 61857348781037}    | Informations de résolution de 8BIM | VT \_ inconnu-lecture/écriture de requêtes             |
| /app13/irb/8bimResInfo/PString                                     |                      | VT- \_ LPSTR                                     |
| /app13/irb/8bimResInfo/HResolution                                 |                      | VT \_ UI4                                       |
| /app13/irb/8bimResInfo/VResolution                                 |                      | VT \_ UI4                                       |
| /app13/irb/8bimResInfo/WidthUnit                                   |                      | \_UI2 VT                                       |
| /app13/irb/8bimResInfo/HeightUnit                                  |                      | \_UI2 VT                                       |
| /app13/irb/8bimResInfo/HResolutionUnit                             |                      | \_UI2 VT                                       |
| /app13/irb/8bimResInfo/VResolutionUnit                             |                      | \_UI2 VT                                       |
| /com                                                               | Commentaire JPEG         | VT \_ inconnu-commentaire sur le lecteur/enregistreur de requêtes     |
| /com/TextEntry                                                     |                      | LPSTR                                         |
| /luminance                                                         | Luminance            | VT \_ inconnu-lecteur/enregistreur de requêtes de luminance   |
| /luminance/TableEntry                                              |                      | Vecteur VT VT \_ UI1 \| \_                         |
| /chrominance                                                       | Chrominance          | VT \_ inconnu-lecture/écriture de requête de chrominance |
| /chrominance/TableEntry                                            |                      | Vecteur VT VT \_ UI1 \| \_                         |
| /xmp                                                               | XMP                  | VT \_ inconnu-lecteur/enregistreur de requêtes XMP         |



 

## <a name="file-format-independent-metadata"></a>Métadonnées indépendantes du format de fichier

Les sections suivantes contiennent des informations sur les formats de métadonnées pris en charge par plusieurs formats d’image. Chaque table contient les colonnes suivantes :

-   **Chemin d’accès relatif** : chemin d’accès de la requête utilisé pour récupérer l’élément de métadonnées, relatif au bloc de métadonnées.
-   **Nom** : nom de l’élément de métadonnées.
-   **Type** : type de l’élément de métadonnées récupéré à partir du chemin d’accès de la requête. Les métadonnées récupérées par [WIC](-wic-api.md) sont retournées sous la forme de PROPVARIANT, qui signale le type de données à l’aide de l’énumération VarType.

> [!Note]  
> Les tables ici fournissent uniquement le chemin d’accès relatif pour accéder à un élément de métadonnées dans le format de métadonnées particulier. Pour obtenir la requête de métadonnées complète, ajoutez ce chemin d’accès relatif à la requête de bloc de métadonnées pour le format de métadonnées particulier.

 

Par exemple, pour accéder à l’indicateur d' [orientation](-wic-photoprop-system-photo-orientation.md) dans un fichier JPEG, utilisez l’expression suivante :

-   /App1/IFD/{UShort = 274}

Dans un fichier TIFF, utilisez l’expression suivante :

-   /IFD/{UShort = 274}

Dans cet exemple, Notez que les différents formats d’image peuvent stocker différemment un bloc de métadonnées particulier, de sorte que la requête de métadonnées complète pour accéder à un élément de métadonnées particulier peut être spécifique au format d’image. Consultez le tableau de chaque format pour rechercher la requête de métadonnées appropriée pour accéder à un bloc de métadonnées particulier.

### <a name="ifd-metadata"></a>Métadonnées IFD

Un IFD, ou répertoire de fichiers image, est une structure de données définie dans la norme TIFF qui peut contenir des métadonnées d’image. Il identifie chaque élément de métadonnées à l’aide d’une balise de type UShort. JPEG, TIFF et JPEG-XR prennent en charge les métadonnées IFD. Les formats tiers, tels que certains formats Camera Raw, peuvent également prendre en charge les métadonnées IFD.

Le tableau ci-dessous fournit des chemins d’accès aux requêtes de métadonnées relatives pour accéder à des éléments de métadonnées IFD couramment utilisés. La structure de données IFD autorise l’extensibilité d’un tiers et cette table n’est pas une liste exhaustive. Pour plus d’informations, consultez la norme TIFF.

> [!Note]  
> Bien que JPEG et d’autres formats prennent en charge la structure de données IFD, ils ne peuvent pas utiliser tous les éléments de métadonnées qu’il définit. Pour plus d’informations, reportez-vous à la norme de chaque format.

 

> [!Note]  
> Certains éléments de métadonnées de la table requièrent une interprétation ou des informations supplémentaires pour une utilisation correcte, reportez-vous à la norme TIFF. Par exemple, l’élément de métadonnées [PhotometricInterpretation](-wic-photoprop-system-photo-photometricinterpretation.md) retourne un PROPVARIANT de type VT \_ UI2. Toutefois, conformément à la norme TIFF, elle est interprétée comme une énumération. Pour plus d’informations, consultez la norme TIFF.

 



| Chemin d’accès relatif   | Nom                      | Type                                           |
|-----------------|---------------------------|------------------------------------------------|
| /{UShort = 256}   | ImageWidth                | VT \_ UI2 ou VT \_ UI4                             |
| /{UShort = 257}   | ImageLength               | VT \_ UI2 ou VT \_ UI4                             |
| /{UShort = 258}   | BitsPerSample             | \_UI2 VT                                        |
| /{UShort = 259}   | Compression               | \_UI2 VT                                        |
| /{UShort = 262}   | PhotometricInterpretation | \_UI2 VT                                        |
| /{UShort = 274}   | Orientation               | \_UI2 VT                                        |
| /{UShort = 277}   | SamplesPerPixel           | \_UI2 VT                                        |
| /{UShort = 284}   | PlanarConfiguration       | \_UI2 VT                                        |
| /{UShort = 530}   | YCbCrSubSampling          | VT \_ UI2 VT Vector \| \_                          |
| /{UShort = 531}   | YCbCrPositioning          | \_UI2 VT                                        |
| /{UShort = 282}   | XResolution               | \_UI8 VT                                        |
| /{UShort = 283}   | YResolution               | \_UI8 VT                                        |
| /{UShort = 296}   | ResolutionUnit            | \_UI2 VT                                        |
| /{UShort = 306}   | DateTime                  | VT- \_ LPSTR                                      |
| /{UShort = 270}   | ImageDescription          | VT- \_ LPSTR                                      |
| /{UShort = 271}   | Marque                      | VT- \_ LPSTR                                      |
| /{UShort = 272}   | Modèle                     | VT- \_ LPSTR                                      |
| /{UShort = 305}   | Logiciel                  | VT- \_ LPSTR                                      |
| /{UShort = 315}   | Peinture                    | VT- \_ LPSTR                                      |
| /{UShort = 33432} | copyright                 | VT- \_ LPSTR                                      |
| /{UShort = 338}   | ExtraSamples              | \_UI2 VT                                        |
| /{UShort = 254}   | NewSubfileType            | VT \_ UI4                                        |
| /{UShort = 278}   | RowsPerStrip              | VT \_ UI2 ou VT \_ UI4                             |
| /{UShort = 279}   | StripByteCounts           | VT \_ Vector \| VT \_ UI2 ou VT \_ Vector \| VT \_ UI4 |
| /{UShort = 273}   | StripOffsets              | VT \_ Vector \| VT \_ UI2 ou VT \_ Vector \| VT \_ UI4 |



 

### <a name="exif-metadata"></a>Métadonnées EXIF

Les métadonnées EXIF sont définies dans le cadre de la spécification JPEG EXIF. Les métadonnées EXIF sont basées sur la structure de données IFD telle que définie dans la norme TIFF, et fournissent des attributs supplémentaires, tels que des informations sur les appareils et les attributs photographiques utilisés pour créer l’image. Il identifie chaque élément de métadonnées à l’aide d’une balise de type UShort. JPEG, TIFF et JPEG-XR prennent en charge les métadonnées EXIF. Les formats tiers, tels que certains formats Camera Raw, peuvent également prendre en charge les métadonnées EXIF.

Le tableau suivant fournit des chemins d’accès de requête de métadonnées relatifs pour accéder à des éléments de métadonnées EXIF couramment utilisés. La structure de données EXIF permet une extensibilité tierce et cette table n’est pas une liste exhaustive. Pour plus d’informations, reportez-vous à la norme EXIF.

> [!Note]  
> De nombreux éléments de métadonnées EXIF sont définis dans la norme EXIF comme type « RATIONAL » ou « SRATIONAL ». Un « RATIONAL » se compose d’un numérateur et d’un dénominateur, qui sont tous deux des entiers non signés 32 bits. Le numérateur est contenu dans les 32 bits de poids fort et le dénominateur dans les 32 de poids faible. Dans [WIC](-wic-api.md), ceux-ci sont retournés en tant que PROPVARIANT avec un type VT \_ UI8 ou VT \_ I8, respectivement ; la valeur réelle est stockée en tant qu' \_ entier ULARGE ou \_ entier long, respectivement. Pour accéder au numérateur et au dénominateur, lisez les membres HighPart et LowPart de l’entier ULARGE ou de la valeur de l' \_ \_ entier long.

 

> [!Note]  
> Certains éléments de métadonnées dans le tableau ci-dessous nécessitent une interprétation ou des informations supplémentaires pour utiliser correctement. Par exemple, l’élément de métadonnées [ColorSpace](-wic-photoprop-system-image-colorspace.md) retourne un PROPVARIANT de type VT \_ UI2. Toutefois, selon la norme EXIF, elle est interprétée comme une énumération. Pour plus d’informations, consultez la norme EXIF.

 



| Chemin d’accès relatif   | Nom                      | Type                  |
|-----------------|---------------------------|-----------------------|
| /{UShort = 36864} | ExifVersion               | \_objet BLOB VT              |
| /{UShort = 40960} | FlashpixVersion           | \_objet BLOB VT              |
| /{UShort = 40961} | ColorSpace                | \_UI2 VT               |
| /{UShort = 40962} | PixelXDimension           | VT \_ UI2 ou VT \_ UI4    |
| /{UShort = 40963} | PixelYDimension           | VT \_ UI2 ou VT \_ UI4    |
| /{UShort = 37500} | MakerNote                 | \_objet BLOB VT              |
| /{UShort = 37510} | UserComment               | \_LPWStr VT            |
| /{UShort = 36867} | DateTimeOriginal          | VT- \_ LPSTR             |
| /{UShort = 36868} | DateTimeDigitized         | VT- \_ LPSTR             |
| /{UShort = 42016} | ImageUniqueID             | VT- \_ LPSTR             |
| /{UShort = 42032} | CameraOwnerName           | VT- \_ LPSTR             |
| /{UShort = 42033} | BodySerialNumber          | VT- \_ LPSTR             |
| /{UShort = 42034} | LensSpecification         | VT \_ UI8 VT Vector \| \_ |
| /{UShort = 42035} | LensMake                  | VT- \_ LPSTR             |
| /{UShort = 42036} | LensModel                 | VT- \_ LPSTR             |
| /{UShort = 42037} | LensSerialNumber          | VT- \_ LPSTR             |
| /{UShort = 33434} | ExposureTime              | \_UI8 VT               |
| /{UShort = 33437} | FNumber                   | \_UI8 VT               |
| /{UShort = 34850} | ExposureProgram           | \_UI2 VT               |
| /{UShort = 34852} | SpectralSensitivity       | VT- \_ LPSTR             |
| /{UShort = 34855} | PhotographicSensitivity   | VT \_ UI2 VT Vector \| \_ |
| /{UShort = 34856} | OECF                      | \_objet BLOB VT              |
| /{UShort = 34864} | SensitivityType           | \_UI2 VT               |
| /{UShort = 34865} | StandardOutputSensitivity | VT \_ UI4               |
| /{UShort = 34866} | RecommendedExposureIndex  | VT \_ UI4               |
| /{UShort = 34867} | ISOSpeed                  | VT \_ UI4               |
| /{UShort = 34868} | ISOSpeedLatitudeyyy       | VT \_ UI4               |
| /{UShort = 34869} | ISOSpeedLatitudezzz       | VT \_ UI4               |
| /{UShort = 37377} | ShutterSpeedValue         | Le \_ i8 VT                |
| /{UShort = 37378} | ApertureValue             | \_UI8 VT               |
| /{UShort = 37379} | BrightnessValue           | Le \_ i8 VT                |
| /{UShort = 37380} | ExposureBiasValue         | Le \_ i8 VT                |
| /{UShort = 37381} | MaxApertureValue          | \_UI8 VT               |
| /{UShort = 37382} | SubjectDistance           | \_UI8 VT               |
| /{UShort = 37383} | MeteringMode              | \_UI2 VT               |
| /{UShort = 37384} | LightSource               | \_UI2 VT               |
| /{UShort = 37385} | Clignote                     | \_UI2 VT               |
| /{UShort = 37386} | FocalLength               | \_UI8 VT               |
| /{UShort = 37396} | SubjectArea               | VT \_ UI2 VT Vector \| \_ |
| /{UShort = 41483} | FlashEnergy               | \_UI8 VT               |
| /{UShort = 41484} | SpatialFrequencyResponse  | \_objet BLOB VT              |
| /{UShort = 41486} | FocalPlaneXResolution     | \_UI8 VT               |
| /{UShort = 41487} | FocalPlaneYResolution     | \_UI8 VT               |
| /{UShort = 41488} | FocalPlaneResolutionUnit  | \_UI2 VT               |
| /{UShort = 41492} | SubjectLocation           | VT \_ UI2 VT Vector \| \_ |
| /{UShort = 41493} | ExposureIndex             | \_UI8 VT               |
| /{UShort = 41495} | SensingMethod             | \_UI2 VT               |
| /{UShort = 41728} | FileSource                | \_objet BLOB VT              |
| /{UShort = 41729} | SceneType                 | \_objet BLOB VT              |
| /{UShort = 41730} | CFAPattern                | \_objet BLOB VT              |
| /{UShort = 41985} | CustomRendered            | \_UI2 VT               |
| /{UShort = 41986} | ExposureMode              | \_UI2 VT               |
| /{UShort = 41987} | WhiteBalance              | \_UI2 VT               |
| /{UShort = 41988} | DigitalZoomRatio          | \_UI8 VT               |
| /{UShort = 41989} | FocalLengthIn35mmFilm     | \_UI2 VT               |
| /{UShort = 41990} | SceneCaptureType          | \_UI2 VT               |
| /{UShort = 41991} | GainControl               | \_UI8 VT               |
| /{UShort = 41992} | Comparez                  | \_UI2 VT               |
| /{UShort = 41993} | Saturation                | \_UI2 VT               |
| /{UShort = 41994} | Netteté                 | \_UI2 VT               |
| /{UShort = 41995} | DeviceSettingDescription  | \_objet BLOB VT              |
| /{UShort = 41996} | SubjectDistanceRange      | \_UI2 VT               |



 

### <a name="gps-metadata"></a>Métadonnées GPS

Les métadonnées GPS contiennent des informations de géolocalisation et sont définies dans le cadre de la spécification JPEG EXIF. Il identifie chaque élément de métadonnées à l’aide d’une balise de type UShort. JPEG, TIFF et JPEG-XR prennent en charge les métadonnées GPS ; les formats tiers, tels que certains formats Camera Raw, peuvent également prendre en charge les métadonnées GPS.

Le tableau suivant fournit des chemins d’accès de requête de métadonnées relatifs pour accéder à des éléments de métadonnées GPS couramment utilisés. Ce tableau n’est pas une liste exhaustive. Pour plus d’informations, reportez-vous à la norme EXIF.

> [!Note]  
> De nombreux éléments de métadonnées GPS sont définis dans la norme EXIF comme type « RATIONAL ». Un « RATIONAL » se compose d’un numérateur et d’un dénominateur, qui sont tous deux des entiers non signés 32 bits. Le numérateur est contenu dans les 32 bits de poids fort et le dénominateur dans les 32 de poids faible. Dans [WIC](-wic-api.md), ceux-ci sont retournés en tant que PROPVARIANT avec un type de \_ UI8 VT. La valeur réelle est stockée sous la forme d’un \_ entier ULARGE. Pour accéder au numérateur et au dénominateur, lisez les membres HighPart et LowPart de la \_ valeur entière ULARGE.

 

> [!Note]  
> Certains éléments de métadonnées de la table requièrent des interprétations ou des informations supplémentaires pour utiliser correctement. Par exemple, l’élément de métadonnées GPSLatitudeRef retourne un PROPVARIANT de type VT \_ LPSTR. Selon la norme EXIF, cette chaîne est « N » ou « S », ce qui représente une latitude nord ou sud. Pour plus d’informations, consultez la norme EXIF.

 



| Chemin d’accès relatif | Nom            | Type                                          |
|---------------|-----------------|-----------------------------------------------|
| {UShort = 0}    | GPSVersionID    | VT \_ UI1 VT Vector \| \_                         |
| {UShort = 1}    | GPSLatitudeRef  | VT- \_ LPSTR                                     |
| {UShort = 2}    | GPSLatitude     | VT \_ UI8 VT Vector \| \_                         |
| {UShort = 3}    | GPSLongitudeRef | VT- \_ LPSTR                                     |
| {UShort = 4}    | GPSLongitude    | {UShort = 4} GPSLongitude VT \_ Vector \| VT \_ UI8 |
| {UShort = 5}    | GPSAltitudeRef  | \_UI1 VT                                       |
| {UShort = 6}    | GPSAltitude     | \_UI8 VT                                       |
| {UShort = 7}    | GPSTimeStamp    | VT \_ UI8 VT Vector \| \_                         |
| {UShort = 8}    | GPSSatellites   | VT- \_ LPSTR                                     |
| {UShort = 9}    | GPSStatus       | VT- \_ LPSTR                                     |
| {UShort = 10}   | GPSMeasureMode  | VT- \_ LPSTR                                     |
| {UShort = 11}   | GPSDOP          | \_UI8 VT                                       |
| {UShort = 12}   | GPSSpeedRef     | VT- \_ LPSTR                                     |
| {UShort = 13}   | GPSSpeed        | \_UI8 VT                                       |
| {UShort = 14}   | GPSTrackRef     | VT- \_ LPSTR                                     |
| {UShort = 15}   | GPSTrack        | \_UI8 VT                                       |



 

### <a name="xmp-metadata"></a>Métadonnées XMP

XMP est une norme de métadonnées extensible basée sur XML. Les éléments de métadonnées peuvent être hiérarchiques et contenir des structures de données complexes. JPEG, TIFF et JPEG-XR prennent en charge les métadonnées XMP. Les formats tiers, tels que certains formats Camera Raw, peuvent également prendre en charge les métadonnées XMP.

La norme XMP peut être obtenue à partir de : <https://www.adobe.com/devnet/xmp.html> .

XMP et permet aux entités tierces de publier leurs propres schémas ou espaces de noms, ce qui leur permet de définir de nouveaux éléments de métadonnées sans avoir à modifier la norme XMP. Un schéma XMP est identifié de manière unique par une URL, mais [WIC](-wic-api.md) fournit un ensemble d’identificateurs conviviaux pour les schémas bien connus.

Les éléments de métadonnées XMP sont identifiés par un nom de chaîne, ainsi qu’un identificateur de schéma. En guise de meilleure pratique, chaque requête de métadonnées XMP doit spécifier à la fois le schéma et le nom. Si l’identificateur de schéma est manquant, le format JPEG tente de faire correspondre le nom des métadonnées dans tous les espaces de noms présents dans le paquet de métadonnées XMP.

Par exemple, pour obtenir la propriété Rating telle que définie par le schéma XMP dans une image JPEG, utilisez la requête suivante :

-   /XMP/{WSTR =https://ns.adobe.com/xap/1.0/}:Rating

La première partie, « /XMP », récupère l’enregistreur/lecteur de métadonnées XMP pour l’image. « https://ns.adobe.com/xap/1.0/ » est l’URL du schéma XMP, tel que défini dans la norme XMP. L’URL est placée dans une expression de données pour permettre l’utilisation de caractères tels qu’une barre oblique (/). Enfin, « Rating » est le nom réel de l’élément de métadonnées tel que défini par le schéma XMP et il est séparé de l’identificateur de schéma par un signe deux-points ( :).

Dans cet exemple, WIC fournit un identificateur convivial pour le schéma XMP qui peut être utilisé à la place de l’URL complète. Par conséquent, la requête précédente peut être réécrite comme suit :

-   /XMP/XMP : évaluation

[WIC](-wic-api.md) fournit des préfixes de schéma conviviaux pour les schémas couramment utilisés suivants :



| Préfixe de schéma  | URL du schéma                                        | Lien vers le standard                                         |
|----------------|---------------------------------------------------|----------------------------------------------------------|
| RDF            | https://www.w3.org/1999/02/22-rdf-syntax-ns\#      | <https://www.w3.org/TR/REC-rdf-syntax/>                   |
| dc             | https://purl.org/dc/elements/1.1/                  | <https://www.adobe.com/devnet/xmp.html>                   |
| XMP            | https://ns.adobe.com/xap/1.0/                      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpidq         | https://ns.adobe.com/xmp/Identifier/qual/1.0/      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpRights      | https://ns.adobe.com/xap/1.0/rights/               | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpMM          | https://ns.adobe.com/xap/1.0/mm/                   | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpBJ          | https://ns.adobe.com/xap/1.0/bj/                   | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpTPg         | https://ns.adobe.com/xap/1.0/t/pg/                 | <https://www.adobe.com/devnet/xmp.html>                   |
| pdf            | https://ns.adobe.com/pdf/1.3/                      | <https://www.adobe.com/devnet/xmp.html>                   |
| Photoshop      | https://ns.adobe.com/photoshop/1.0/                | <https://www.adobe.com/devnet/xmp.html>                   |
| tiff           | https://ns.adobe.com/tiff/1.0/                     | <https://www.adobe.com/devnet/xmp.html>                   |
| EXIF           | https://ns.adobe.com/exif/1.0/                     | <https://www.adobe.com/devnet/xmp.html>                   |
| stDim          | https://ns.adobe.com/xap/1.0/sType/Dimensions\#    | <https://www.adobe.com/devnet/xmp.html>                   |
| xapGImg        | https://ns.adobe.com/xap/1.0/g/img/                | <https://www.adobe.com/devnet/xmp.html>                   |
| stEvt          | https://ns.adobe.com/xap/1.0/sType/ResourceEvent\# | <https://www.adobe.com/devnet/xmp.html>                   |
| stRef          | https://ns.adobe.com/xap/1.0/sType/ResourceRef\#   | <https://www.adobe.com/devnet/xmp.html>                   |
| stVer          | https://ns.adobe.com/xap/1.0/sType/Version\#       | <https://www.adobe.com/devnet/xmp.html>                   |
| stJob          | https://ns.adobe.com/xap/1.0/sType/Job\#           | <https://www.adobe.com/devnet/xmp.html>                   |
| Coord            | https://ns.adobe.com/exif/1.0/aux/                 | <https://www.adobe.com/devnet/xmp.html>                   |
| Sir            | https://ns.adobe.com/camera-raw-settings/1.0/      | <https://www.adobe.com/devnet/xmp.html>                   |
| xmpDM          | https://ns.adobe.com/xmp/1.0/DynamicMedia/         | <https://www.adobe.com/devnet/xmp.html>                   |
| Iptc4xmpCore   | https://iptc.org/std/Iptc4xmpCore/1.0/xmlns/       | <https://www.iptc.org/cms/site/index.html?channel=CH0099> |
| MicrosoftPhoto | https://ns.microsoft.com/photo/1.0/                | [Vue d’ensemble du balisage des personnes](-wic-people-tagging.md)       |
| MP             | https://ns.microsoft.com/photo/1.2/                | [Vue d’ensemble du balisage des personnes](-wic-people-tagging.md)       |
| MPRI           | https://ns.microsoft.com/photo/1.2/t/RegionInfo\#  | [Vue d’ensemble du balisage des personnes](-wic-people-tagging.md)       |
| MPReg          | https://ns.microsoft.com/photo/1.2/t/Region\#      | [Vue d’ensemble du balisage des personnes](-wic-people-tagging.md)       |



 

S’il n’existe pas de préfixe de schéma convivial pour un schéma particulier, par exemple si une image contient des métadonnées XMP utilisant un schéma tiers personnalisé, la requête de métadonnées doit utiliser l’URL de schéma complète.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Vue d’ensemble des métadonnées WIC](-wic-about-metadata.md)
</dt> <dt>

[Vue d’ensemble du langage de requête de métadonnées](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Vue d’ensemble de l’extensibilité des métadonnées](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Comment : recoder une image JPEG avec des métadonnées](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 
