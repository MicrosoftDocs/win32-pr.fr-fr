---
description: cette rubrique fournit des informations sur le codec GIF natif disponible via le composant WIC (Windows Imaging Component).
ms.assetid: CAEC8F92-8971-42B4-BED8-A6A93522D11E
title: Vue d’ensemble du format GIF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 345f3856c01ff94ba51ce16ccc64bd299312d75777b1f269c0cf9a4e67c56a07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709498"
---
# <a name="gif-format-overview"></a>Vue d’ensemble du format GIF

cette rubrique fournit des informations sur le codec GIF natif disponible via le composant WIC (Windows Imaging Component).

## <a name="codec-identity"></a>Identité du codec

Le tableau suivant fournit des informations d’identification du codec.



|  Composant             | Description                           |
|------------------------|---------------------------------------|
| Nom (s) formel (s)         | GIF (Graphics Interchange format 89a) |
| Extension (s) de nom de fichier | GIF                                   |
| type MIME              | image/gif                             |
| Prise en charge des spécifications  | Spécification GIF 89a/89m             |



 

Le tableau suivant répertorie les GUID utilisés pour identifier les composants de codec GIF natifs.



| Composant        | Nom convivial            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Format de conteneur | GUID \_ ContainerFormatGif | 1f8a5601-7d4d-4cbd-9c821bc8d4eeb9a5 |
| Décodeur          | CLSID \_ WICGifDecoder     | 381dda3c-9ce9-4834-a23e1f98f8fc52be |
| Encodeur          | CLSID \_ WICGifEncoder     | 114f5598-0b22-40a0-86a1c83ea495adbd |



 

## <a name="encoding"></a>Encodage

L’API d’encodage WIC est conçue pour être indépendante du codec et l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique. Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Options de l’encodeur

Les codecs compatibles avec WIC diffèrent au niveau de l’option d’encodage. Les options d’encodeur reflètent les fonctionnalités d’un encodeur d’image et chaque codec natif prend en charge un ensemble de ces options d’encodeur. Les options d’encodeur peuvent être des options prises en charge par le WIC de base disponibles pour tous les codes WIC activés (mais pas nécessairement pris en charge) ou les options spécifiques aux codecs conçues par le codec de format d’image. Pour gérer ces options d’encodage pendant le processus d’encodage, WIC utilise l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Pour plus d’informations sur l’utilisation de l’interface **IPropertyBag2** pour l’encodage WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).

L’encodeur GIF ne prend pas en charge les options WIC de base et ne fournit pas d’options d’encodeur personnalisées. Si une option d’encodeur figure dans la liste d’options [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) , elle est ignorée.

## <a name="decoding"></a>Décodage

L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique. Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md). Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).

 

 
