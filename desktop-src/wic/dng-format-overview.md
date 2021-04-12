---
description: Cette rubrique fournit des informations sur le codec DNG natif disponible par le biais du composant WIC (Windows Imaging Component).
ms.assetid: 6F87A47D-E54A-42D9-92DC-2411803278AA
title: Vue d’ensemble du format DNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63f766356f7c13d7b2bb25adab5411ae55c2735f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319302"
---
# <a name="dng-format-overview"></a>Vue d’ensemble du format DNG

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Cette rubrique fournit des informations sur le codec DNG natif disponible par le biais du composant WIC (Windows Imaging Component).

-   [Identité du codec](#codec-identity)
-   [Décodage](#decoding)

## <a name="codec-identity"></a>Identité du codec

Le tableau suivant fournit des informations d’identification du codec.



|                        |                                                      |
|------------------------|------------------------------------------------------|
| Nom (s) formel (s)         | Négatif numérique (DNG)                               |
| Extension (s) de nom de fichier | .dng                                                 |
| Type (s) MIME           | image/DNG                                            |
| Prise en charge des spécifications  | Version de spécification Digital Negative (DNG) 1.4.0.0 |



 

Le tableau suivant répertorie les GUID utilisés pour identifier les composants de codec DNG natifs.



| Composant        | Nom convivial             | GUID                                |
|------------------|---------------------------|-------------------------------------|
| Format de conteneur | GUID \_ ContainerFormatAdng | f3ff6d0d-38c0-41c4-b1fe1f3824f17b84 |
| Décodeur          | CLSID \_ WICAdngDecoder     | 981d9411-909e-42a7-8f5da747ff052edb |



 

## <a name="decoding"></a>Décodage

L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique. Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md). Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).

Le décodeur ne prend pas en charge le décodage des données de capteur brutes et ne prend en charge que les fichiers avec une représentation d’image non brute incorporée dans un IFD avec NewSubFileType égal à 1.

 

 



