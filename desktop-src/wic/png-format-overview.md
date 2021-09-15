---
description: cette rubrique fournit des informations sur le codec PNG natif disponible via le composant WIC (Windows Imaging Component).
ms.assetid: 703217EA-70C8-4F86-B8DF-95468C78C8DA
title: Vue d’ensemble du format PNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bb00b7530a22fcdbcce112053431ace5e553383
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404231"
---
# <a name="png-format-overview"></a>Vue d’ensemble du format PNG

cette rubrique fournit des informations sur le codec PNG natif disponible via le composant WIC (Windows Imaging Component).

## <a name="codec-identity"></a>Identité du codec

Le tableau suivant fournit des informations d’identification du codec.



|     Composant          | Description                     |
|------------------------|---------------------------------|
| Nom (s) formel (s)         | format PNG (Portable Network Graphics) |
| Extension (s) de nom de fichier | png                             |
| type MIME              | image/png                       |
| Prise en charge des spécifications  | Spécification PNG 1,2           |



 

Le tableau suivant répertorie les GUID utilisés pour identifier les composants de codec PNG natifs.



| Composant        | Nom convivial            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Format de conteneur | GUID \_ ContainerFormatPng | 1b7cfaf4-713f-473c-bbcd6137425faeaf |
| Décodeur          | CLSID \_ WICPngDecoder     | 389ea17b-5078-4cde-b6ef25c15175c751 |
| Encodeur          | CLSID \_ WICPngEncoder     | 27949969-876a-41d7-9447568f6a35a4dc |



 

### <a name="windows-8-and-later"></a>Windows 8 et versions ultérieures

à compter de Windows 8 WIC fournit un décodeur PNG supplémentaire

## <a name="encoding"></a>Encodage

L’API d’encodage WIC est conçue pour être indépendante du codec et l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique. Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Options de l’encodeur

Les codecs compatibles avec WIC diffèrent au niveau de l’option d’encodage. Les options d’encodeur reflètent les fonctionnalités d’un encodeur d’image et chaque codec natif prend en charge un ensemble de ces options d’encodeur. Les options d’encodeur peuvent être des options prises en charge par le WIC de base disponibles pour tous les codes WIC activés (mais pas nécessairement pris en charge) ou les options spécifiques aux codecs conçues par le codec de format d’image. Pour gérer ces options d’encodage pendant le processus d’encodage, WIC utilise l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Pour plus d’informations sur l’utilisation de l’interface **IPropertyBag2** pour l’encodage WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).

Le codec PNG utilise les options de l’encodeur WIC de base. Le tableau suivant répertorie les options de codeur WIC prises en charge par le codec PNG natif.



| Nom de la propriété   | VARTYPE  | Plage de valeurs                                                 | Valeur par défaut                                                    |
|-----------------|----------|-------------------------------------------------------------|------------------------------------------------------------------|
| InterlaceOption | VT \_ bool | **True** / **Valeur false**                                          | **FALSE**                                                        |
| FilterOption    | \_UI1 VT  | [**WICPngFilterOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) | [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption) |



 

Si une option d’encodeur est présente dans la liste d’options [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que le codec ne prend pas en charge, elle est ignorée.

### <a name="interlaceoption"></a>InterlaceOption

Spécifie s’il faut encoder les données d’image comme entrelacées.

La valeur par défaut est **FALSE**.

### <a name="filteroption"></a>FilterOption

Spécifie l’option de filtre à utiliser pour la compression d’image.

La valeur par défaut est [**WICPngFilterUnspecified**](/windows/desktop/api/Wincodec/ne-wincodec-wicpngfilteroption).

## <a name="decoding"></a>Décodage

L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique. Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md). Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).

Le codec PNG natif prend également en charge le [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) sur le décodage de trame qui ajoute des options avancées pour le décodage d’un flux d’image. Pour plus d’informations sur ces options avancées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).

 

 
