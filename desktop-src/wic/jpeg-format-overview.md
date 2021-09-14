---
description: cette rubrique fournit des informations sur le codec JPEG natif disponible via le composant WIC (Windows Imaging Component).
ms.assetid: 9DCBCE9B-965B-4C18-992C-EFFFF32FCE5E
title: Vue d’ensemble du format JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2acc7fcd71fc962d3321112d342f675b878188
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219916"
---
# <a name="jpeg-format-overview"></a>Vue d’ensemble du format JPEG

cette rubrique fournit des informations sur le codec JPEG natif disponible via le composant WIC (Windows Imaging Component).

## <a name="codec-identity"></a>Identité du codec

Le tableau suivant fournit des informations d’identification du codec.



|   Composant            | Description                             |
|------------------------|-----------------------------------------|
| Nom (s) formel (s)         | Joint Photographic Experts Group (JPEG) |
| Extension (s) de nom de fichier | JPE, JPEG, jpg                          |
| type MIME              | image/JPEG, image/JPE, image/jpg        |
| Prise en charge des spécifications  | Spécification JFIF 1,02                 |



 

Le tableau suivant répertorie les GUID utilisés pour identifier les composants de codec JPEG natifs.



| Composant        | Nom convivial             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Format de conteneur | GUID \_ ContainerFormatJpeg | 19e4a5aa-5662-4fc5-a0c01758028e1057 |
| Décodeur          | CLSID \_ WICJpegDecoder     | 9456a480-e88b-43ea-9e730b2d9b71b1ca |
| Encodeur          | CLSID \_ WICJpegEncoder     | 1a34f5c1-4a5a-46dc-b6441f4567e7a676 |



 

## <a name="encoding"></a>Encodage

L’API d’encodage WIC est conçue pour être indépendante du codec et l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique. Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Options de l’encodeur

Les codecs compatibles avec WIC diffèrent au niveau de l’option d’encodage. Les options d’encodeur reflètent les fonctionnalités d’un encodeur d’image et chaque codec natif prend en charge un ensemble de ces options d’encodeur. Les options d’encodeur peuvent être des options prises en charge par le WIC de base disponibles pour tous les codes WIC activés (mais pas nécessairement pris en charge) ou les options spécifiques aux codecs conçues par le codec de format d’image. Pour gérer ces options d’encodage pendant le processus d’encodage, WIC utilise l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Pour plus d’informations sur l’utilisation de l’interface **IPropertyBag2** pour l’encodage WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).

Le codec JPEG utilise les options de base du WIC. Le tableau suivant répertorie les options de codeur WIC prises en charge par le codec JPEG natif.



| Nom de la propriété                                        | VARTYPE           | Plage de valeurs                                                                       | Valeur par défaut                                                                  |
|------------------------------------------------------|-------------------|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [ImageQuality](#imagequality-option)                 | VT \_ R4            | 0-1,0                                                                           | 0.9                                                                            |
| [BitmapTransform](#bitmaptransform-option)           | \_UI1 VT           | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)         | [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions)      |
| [Luminance](#luminance-option)                       | \_Groupe VT UI4/VT \_ | 64 entrées (DCT)                                                                  | Table de luminance par défaut.                                                       |
| [Chrominance](#chrominance-option)                   | \_Groupe VT UI4/VT \_ | 64 entrées (DCT)                                                                  | Table de chrominance par défaut.                                                     |
| [JpegYCrCbSubsampling](#jpegycrcbsubsampling-option) | \_UI1 VT           | [**WICJpegYCrCbSubsamplingOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) | [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption) |
| [SuppressApp0](/windows)                       | VT \_ bool          | **True** / **Valeur false**                                                                | **FALSE**                                                                      |



 

Si une option d’encodeur est présente dans la liste d’options [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que le codec ne prend pas en charge, elle est ignorée.

### <a name="imagequality-option"></a>Option ImageQuality

Spécifie la fidélité de l’image souhaitée. 0,0 indique la fidélité la plus faible possible et 1,0 spécifie la fidélité la plus élevée.

La valeur par défaut est 0,9.

### <a name="bitmaptransform-option"></a>Option BitmapTransform

Spécifie comment l’image doit être transformée lors du décodage de l’image. Cette option doit être définie sur l’une des valeurs d’énumération [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .

La valeur par défaut est [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).

### <a name="luminance-option"></a>Option de luminance

Spécifie la table de niveau de luminosité en nuances de gris à utiliser pour l’encodage.

### <a name="chrominance-option"></a>Chrominance (option)

Spécifie la table de chrominance à utiliser pour l’encodage.

### <a name="jpegycrcbsubsampling-option"></a>Option JpegYCrCbSubsampling

Spécifie le ratio d’échantillonnage à utiliser pour l’encodage YCrCb.

La valeur par défaut est [**WICJpegYCrCbSubsampling420**](/windows/desktop/api/Wincodec/ne-wincodec-wicjpegycrcbsubsamplingoption).

### <a name="suppressapp0-option"></a>Option SuppressApp0

Spécifie s’il faut supprimer l’écriture des métadonnées APP0 lors de l’encodage des données d’image.

La valeur par défaut est **FALSE**.

## <a name="decoding"></a>Décodage

L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique. Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md). Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).

Le codec JPEG natif prend également en charge l' [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) sur le décodage de trame qui ajoute des options avancée pour décoder un flux d’image. Pour plus d’informations sur ces options avancées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).

 

 
