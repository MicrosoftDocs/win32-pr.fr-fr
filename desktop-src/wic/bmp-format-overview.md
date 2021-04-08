---
description: Cette rubrique fournit des informations sur le codec BMP natif disponible via le composant WIC (Windows Imaging Component).
ms.assetid: 85AC5A30-A915-439E-A10F-B2833DDA995C
title: Vue d’ensemble du format BMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3492189f80b43915bab94a7ea8359f2e5950f7c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756910"
---
# <a name="bmp-format-overview"></a>Vue d’ensemble du format BMP

Cette rubrique fournit des informations sur le codec BMP natif disponible via le composant WIC (Windows Imaging Component).

## <a name="codec-identity"></a>Identité du codec

Le tableau suivant fournit des informations d’identification du codec.



|                        |                       |
|------------------------|-----------------------|
| Nom (s) formel (s)         | Format bitmap Windows |
| Extension (s) de nom de fichier | BMP, DIB              |
| type MIME              | image/bmp             |
| Prise en charge des spécifications  | BMP spécification v5  |



 

Le tableau suivant répertorie les GUID utilisés pour identifier les composants du codec BMP natifs.



| Composant        | Nom convivial            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Format de conteneur | GUID \_ ContainerFormatBmp | 0af1d87e-fcfe-4188-bdeba7906471cbe3 |
| Décodeur          | CLSID \_ WICBmpDecoder     | 6b462062-7cbf-400d-9fdb813dd10f2778 |
| Encodeur          | CLSID \_ WICBmpEncoder     | 69be8bb4-d66d-47c8-865aed1589433782 |



 

## <a name="encoding"></a>Encodage

L’API d’encodage WIC est conçue pour être indépendante du codec et, par conséquent, l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique. Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Options de l’encodeur

Les codecs compatibles avec WIC diffèrent au niveau de l’option d’encodage. Les options d’encodeur reflètent les fonctionnalités d’un encodeur d’image et chaque codec natif prend en charge un ensemble de ces options d’encodeur. Les options d’encodeur peuvent être des options prises en charge par le WIC de base disponibles pour tous les codes WIC activés (mais pas nécessairement pris en charge) ou les options spécifiques aux codecs conçues par le codec de format d’image. Pour gérer ces options d’encodage pendant le processus d’encodage, WIC utilise l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Pour plus d’informations sur l’utilisation de l’interface **IPropertyBag2** pour l’encodage WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).

Le tableau suivant répertorie les options de codeur WIC prises en charge par le codec BMP natif.



| Nom de la propriété               | VARTYPE      | Plage de valeurs                      | Valeur par défaut      |
|-----------------------------|--------------|----------------------------------|--------------------|
| **EnableV5Header32bppBGRA** | **VT \_ bool** | **VARIANTE \_ vrai/variante \_ faux** | **VARIANTE \_ false** |



 

### <a name="enablev5header32bppbgra"></a>EnableV5Header32bppBGRA

Spécifie s’il faut autoriser l’encodage des données au \_ format de pixel GUID WICPixelFormat32bppBGRA. Si cette option a la valeur **Variant \_ true**, le BMP est écrit avec un en-tête BITMAPV5HEADER.

La valeur par défaut **est \_ false**.

Si une option d’encodeur est présente dans la liste d’options IPropertyBag2 que le codec ne prend pas en charge, elle est ignorée.

Remarque pour les fichiers Windows BMP 16 bits et 32 bits, le codec BMP ignore tout canal alpha, car de nombreux fichiers image hérités contiennent des données non valides dans ce canal supplémentaire. À compter de Windows 8, les fichiers Windows BMP 32 bits écrits à l’aide de **BITMAPV5HEADER** avec un contenu de canal alpha valide sont lus en tant que WICPixelFormat32bppBGRA

## <a name="decoding"></a>Décodage

L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique. Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md). Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).

 

 
