---
description: cette rubrique fournit des informations sur le codec ICO natif disponible via le composant WIC (Windows Imaging Component).
ms.assetid: EF28956E-7156-4BAE-8805-C64B8C8ADE50
title: Vue d’ensemble du format ICO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 329a53a3b5d386c5e5386141162c608dc9db1ec0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411163"
---
# <a name="ico-format-overview"></a>Vue d’ensemble du format ICO

cette rubrique fournit des informations sur le codec ICO natif disponible via le composant WIC (Windows Imaging Component).

## <a name="codec-identity"></a>Identité du codec

Le tableau suivant fournit des informations d’identification du codec.



|   Composant            | Description       |
|------------------------|-------------------|
| Nom (s) formel (s)         | Format d’icône (ICO) |
| Extension (s) de nom de fichier | ICO               |
| type MIME              | image/ico         |
| Prise en charge des spécifications  |                   |



 

Le tableau suivant répertorie les GUID utilisés pour identifier les composants du codec ICO natifs.



| Composant        | Nom convivial            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Format de conteneur | GUID \_ ContainerFormatIco | a3a860c4-338f-4c17-919afba4b5628f21 |
| Décodeur          | CLSID \_ WICIcoDecoder     | c61bfcdf-2e0f-4aad-a8d7e06bafebcdfe |
| Encodeur          | NON DISPONIBLE            | NON DISPONIBLE                       |



 

## <a name="encoding"></a>Encodage

WIC ne fournit pas d’encodeur d’image ICO natif.

## <a name="decoding"></a>Décodage

L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique. Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md). Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).

 

 



