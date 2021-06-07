---
description: Cette rubrique fournit des informations sur le codec TIFF natif disponible via WIC (Windows Imaging Component).
ms.assetid: 021AAF33-A89E-4336-AEB1-1A0D79A14C75
title: Vue d’ensemble du format TIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b28dfcc85dac21e95e6c76118d2db57cb74a08
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444420"
---
# <a name="tiff-format-overview"></a>Vue d’ensemble du format TIFF

Cette rubrique fournit des informations sur le codec TIFF natif disponible via WIC (Windows Imaging Component).

-   [Identité du codec](#codec-identity)
-   [Encodage](#encoding)
    -   [Options de l’encodeur](#encoder-options)
-   [Décodage](#decoding)

## <a name="codec-identity"></a>Identité du codec

Le tableau suivant fournit des informations d’identification du codec.



|   Composant            |   Description                   |
|------------------------|---------------------------------|
| Nom (s) formel (s)         | format TIFF (Tagged Image File Format) |
| Extension (s) de nom de fichier | TIFF, TIF                       |
| Type (s) MIME           | image/TIFF, image/TIF           |
| Prise en charge des spécifications  | Spécification TIFF 6,0          |



 

Le tableau suivant répertorie les GUID utilisés pour identifier les composants natifs du codec TIFF.



| Composant        | Nom convivial             | GUID                                 |
|------------------|---------------------------|--------------------------------------|
| Format de conteneur | GUID \_ ContainerFormatTiff | 163bcc30-e2e9-4f0b-961da3e9fdb788a3  |
| Décodeur          | CLSID \_ WICTiffDecoder     | b54e85d9-fe23-499f-8b886acea7137502b |
| Encodeur          | CLSID \_ WICTiffEncoder     | 0131be10-2001-4c5f-a9b0cc88fab64ce8  |



 

## <a name="encoding"></a>Encodage

L’API d’encodage WIC est conçue pour être indépendante du codec et l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique. Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Options de l’encodeur

Les codecs compatibles avec WIC diffèrent au niveau de l’option d’encodage. Les options d’encodeur reflètent les fonctionnalités d’un encodeur d’image et chaque codec natif prend en charge un ensemble de ces options d’encodeur. Les options d’encodeur peuvent être des options prises en charge par le WIC de base disponibles pour tous les codes WIC activés (mais pas nécessairement pris en charge) ou les options spécifiques aux codecs conçues par le codec de format d’image. Pour gérer ces options d’encodage pendant le processus d’encodage, WIC utilise l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Pour plus d’informations sur l’utilisation de l’interface **IPropertyBag2** pour l’encodage WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).

Le codec TIFF utilise les options de base du WIC. Le tableau suivant répertorie les options de codeur WIC prises en charge par le codec TIFF natif.

| Nom de la propriété         | VARTYPE | Plage de valeurs | Valeur par défaut    |
|-----------------------|---------|-------------|------------------|
| CompressionQuality    | VT \_ R4  | 0-1,0     | 0                |
| TiffCompressionMethod | \_UI1 VT | [**WICTiffCompressionOption**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) | [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption) |

Si une option d’encodeur est présente dans la liste d’options [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que le codec ne prend pas en charge, elle est ignorée.

### <a name="compressionquality-option"></a>Option CompressionQuality

Spécifie la qualité de compression souhaitée. 0,0 indique le schéma de compression le moins efficace disponible. En règle générale, ce schéma entraîne un encodage plus rapide mais une sortie plus grande. La valeur 1,0 spécifie le schéma de compression le plus efficace disponible. En règle générale, ce schéma entraîne un encodage plus long, mais produit une sortie plus petite.

La valeur par défaut est 0.

### <a name="tiffcompressionmethod-option"></a>Option TiffCompressionMethod

Spécifie la méthode de compression TIFF.

La valeur par défaut est [**WICTiffCompressionDontCare**](/windows/desktop/api/Wincodec/ne-wincodec-wictiffcompressionoption).

## <a name="decoding"></a>Décodage

Les API de décodage WIC sont conçues pour être indépendantes du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique. Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md). Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).

 

 
