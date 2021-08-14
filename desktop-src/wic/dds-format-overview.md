---
description: fournit des informations sur le codec DDS natif disponible via le composant WIC (Windows Imaging Component).
ms.assetid: 6CFDD674-C8AE-4F29-B2E5-C9C9431CB85A
title: Vue d’ensemble du format DDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a9fd00f17d17b7bb227a04e56bbc9369de86eb03f9c953a73267400d4a6df9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118204476"
---
# <a name="dds-format-overview"></a>Vue d’ensemble du format DDS

cette rubrique fournit des informations sur le codec DDS natif disponible via le composant WIC (Windows Imaging Component).

## <a name="codec-identity"></a>Identité du codec

Le tableau suivant fournit des informations d’identification du codec.



| Composant              | Description        |
|------------------------|--------------------|
| Nom (s) formel (s)         | Surface DirectDraw |
| Extension (s) de nom de fichier | DDS                |
| type MIME              | image/VND-ms. DDS   |



 

Le tableau suivant répertorie les GUID utilisés pour identifier les composants de codec DDS natifs.



| Composant        | Nom convivial            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Format de conteneur | GUID \_ ContainerFormatDds | 9967cb95-2e85-4ac8-8ca283d7ccd425c9 |
| Décodeur          | CLSID \_ WICDdsDecoder     | 9053699f-a341-429d-9e90ee437cf80c73 |
| Encodeur          | CLSID \_ WICDdsEncoder     | a61dde94-66ce-4ac1-881b71680588895e |



 

## <a name="pixel-format-support"></a>Prise en charge du format pixel

Notez que le format DDS prend en charge toute valeur de [**\_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) valide. Toutefois, le codec WIC DDS prend uniquement en charge le décodage et l’encodage des fichiers contenant les formats suivants :

-   DXGI \_ format \_ BC1 \_ UNORM
-   DXGI \_ format \_ BC2 \_ UNORM
-   DXGI \_ format \_ BC3 \_ UNORM

## <a name="encoding"></a>Encodage

Les API de codage WIC sont conçues pour être indépendantes du codec et, par conséquent, l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique. Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).

Le format de fichier DDS a des exigences uniques qui résultent de sa prise en charge des concepts tels que les des mipmaps et les tableaux de texture. Pour exercer un contrôle complet sur l’encodage d’image DDS, vous devez utiliser l’interface [**IWICDdsEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsencoder) pour définir des paramètres d’encodage spécifiques à DDS.

## <a name="decoding"></a>Décodage

Les API de décodage WIC sont conçues pour être indépendantes du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique. Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md). Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).

## <a name="block-compressed-data-access"></a>Bloquer l’accès aux données compressées

En plus de prendre en charge les interfaces de codec WIC standard, le décodeur DDS fournit un accès direct aux données compressées en bloc natives à l’aide des interfaces spécifiques à DDS, [**IWICDdsDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsdecoder) et [**IWICDdsFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicddsframedecode). Pour utiliser ces interfaces, appelez QueryInterface sur [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) et [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), respectivement.

 

 
