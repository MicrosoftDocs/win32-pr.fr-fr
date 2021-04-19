---
description: Le composant WIC (Windows Imaging Component) fournit une API COM (Component Object Model) à utiliser en C et C++.
ms.assetid: 74b14b5e-70e9-410f-a6e6-d8873a5f4fa4
title: Vue d’ensemble de l’API WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f86e5a876010e52489adac9baa7ce57fdfdf80f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536681"
---
# <a name="wic-api-overview"></a>Vue d’ensemble de l’API WIC

Le composant WIC (Windows Imaging Component) fournit une API COM (Component Object Model) à utiliser en C et C++. L’API WIC expose une variété de fonctionnalités liées aux images, notamment :

-   Codecs intégrés pour les formats d’image Web standard.
-   Prise en charge intégrée des formats de métadonnées standard.
-   Large éventail de prise en charge du format de pixel.
-   Prise en charge des couleurs élevées ; y compris les formats de pixels étendus 30 bits, haute précision 30 bits et haute précision 48 bits et à large gamme.
-   Framework extensible pour les codecs d’image, les formats de pixel et les formats de métadonnées.

Cette rubrique contient les rubriques suivantes.

-   [Fichiers d’en-tête WIC](#wic-header-files)
-   [Fichiers de bibliothèque](#library-files)
-   [Fabriques de classes](#class-factories)
-   [Composants de création d’images](#imaging-components)
-   [Voir aussi](#see-also)

## <a name="wic-header-files"></a>Fichiers d’en-tête WIC

Les API WIC sont définies dans les fichiers d’en-tête et IDL (Interface Definition Language) suivants :



| Fichier              | Description                                          |
|-------------------|------------------------------------------------------|
| wincodec. h        | Définit les versions C et C++ des API WIC principales.  |
| wincodec. idl      | Définit les interfaces WIC principales.                  |
| wincodecsdk. h     | Définit les versions C et C++ des API WIC de métadonnées. |
| wincodecsdk. idl   | Définit les interfaces de métadonnées WIC.                 |
| wincodec \_ proxy. h | Définit les exportations du proxy WIC.                       |



 

Pour utiliser le WIC, vos applications doivent inclure wincodec. h et/ou wincodecsdk. h, en fonction de l’API dont votre application a besoin.

## <a name="library-files"></a>Fichiers de bibliothèque

Fichiers de bibliothèque WIC :



| Fichier              | Description                                                            |
|-------------------|------------------------------------------------------------------------|
| windowscodecs. lib | Bibliothèque d’importation fournie par le kit de développement logiciel (SDK) Windows. |
| windowscodecs.dll | Bibliothèque d’implémentation stock fournie par le système d’exploitation.         |



 

Pour créer un lien vers des API WIC, votre application doit inclure windowscodec. lib comme dépendance supplémentaire de l’éditeur de liens.

## <a name="class-factories"></a>Fabriques de classes

Le tableau suivant décrit les deux fabriques de classes COM fournies par les API WIC pour la création de composants WIC.



| Interface de fabrique                                               | Description                                                                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)     | Fabrique de classe principale pour le développement d’applications à l’aide de composants WIC. Cette fabrique crée des composants tels que les décodeurs d’images, les encodeurs et les flux.   |
| [**IWICComponentFactory**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) | Fabrique de classe ciblée pour les développeurs de composants WIC. Les composants créés à partir de cette fabrique sont principalement utilisés dans le codec et le développement du gestionnaire de métadonnées. |



 

Pour créer une fabrique de classes, utilisez la fonction com [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) . L’exemple suivant illustre la création de la fabrique d’images WIC.


```C++
// Initialize COM
CoInitialize(NULL);

// The factory pointer
IWICImagingFactory *pFactory = NULL;

// Create the COM imaging factory
HRESULT hr = CoCreateInstance(
    CLSID_WICImagingFactory,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_PPV_ARGS(&pFactory)
);
```



## <a name="imaging-components"></a>Composants de création d’images

Les API WIC fournissent plusieurs types de composants d’image. Le tableau suivant décrit certains des composants de WIC courants. Pour obtenir la liste complète des composants disponibles, consultez [interfaces WIC](-wic-codec-ifaces.md).



| Type de composant                                                      | Description                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**Bitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)                             | Représente une représentation en mémoire accessible en écriture d’un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource). |
| [**Décodeur**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)                     | Utilisé pour décoder les données d’image d’un flux dans un format utile pour le traitement d’image.                    |
| [**Codeur**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)                     | Écrit des données d’image dans un flux.                                                                                |
| [**Stream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)                             | Utilisé pour lire et écrire des données à partir d’un fichier, d’une ressource réseau, d’un bloc de mémoire, etc.                      |
| [**Convertisseur de format**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)          | Utilisé pour convertir d’un format de pixel à un autre.                                                             |
| [**Lecteur de requêtes de métadonnées**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) | Utilisé pour lire les métadonnées d’une image ou d’un frame d’image.                                                             |
| [**Générateur de requêtes de métadonnées**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) | Utilisé pour écrire des métadonnées dans une image ou un frame d’image.                                                            |



 

## <a name="see-also"></a>Voir aussi

[Informations de référence](-wic-codec-reference.md)


[Exemples et exemples de code](-wic-samples.md)


 

 
