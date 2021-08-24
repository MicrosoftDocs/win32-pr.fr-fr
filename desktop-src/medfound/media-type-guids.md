---
description: Types de médias principaux
ms.assetid: 1cca3539-a920-4938-93b9-ae41e1c0a287
title: Types de médias principaux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec660dcb86cfd1da5a80bef106ee8ddd17cf1e89899fea6b824fba5ab9be04e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715299"
---
# <a name="major-media-types"></a>Types de médias principaux

Dans un type de média, le *type principal* décrit la catégorie globale des données, telles que l’audio ou la vidéo. Le sous- *type*, s’il est présent, affine davantage le type principal. Par exemple, si le type principal est vidéo, le sous-type peut être une vidéo RGB de 32 bits. Les sous-types distinguent également les formats encodés, tels que la vidéo H. 264, des formats non compressés.

Le type et le sous-type principaux sont identifiés par des GUID et stockés dans les attributs suivants :



| Attribut                                             | Description |
|-------------------------------------------------------|-------------|
| [\_type de \_ majeurese MF MT \_](mf-mt-major-type-attribute.md) | Type principal. |
| [\_sous- \_ type MF MT](mf-mt-subtype-attribute.md)        | Sous-type.    |



 

Les types principaux suivants sont définis.



| Type principal                    | Description                                                                                                                                                | Sous-types                                             |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| **MFMediaType \_ audio**        | HD.                                                                                                                                                     | [GUID de sous-type audio](audio-subtype-guids.md).      |
| **\_Binaire MFMediaType**       | Flux binaire.                                                                                                                                             | Aucun.                                                |
| **MFMediaType \_ filetransfer** | Flux qui contient des fichiers de données.                                                                                                                         | Aucun.                                                |
| **\_HTML MFMediaType**         | Flux HTML.                                                                                                                                               | Aucun.                                                |
| **\_Image MFMediaType**        | Flux d’images fixes.                                                                                                                                        | [GUID et CLSID WIC](../wic/-wic-guids-clsids.md).       |
| **\_Métadonnées MFMediaType**        | Flux de métadonnées.                                                                                                                                        | Aucun.       |
| **MFMediaType \_ protégé**    | Média protégé.                                                                                                                                           | Le sous-type spécifie le schéma de protection de contenu. |
| **MFMediaType \_ perception**   | Flux à partir d’un capteur d’appareil photo ou d’une unité de traitement qui a des raisons et comprennent des données vidéo brutes et qui permet de comprendre l’environnement ou les êtres humains. | Aucun.                                                |
| **\_Sami MFMediaType**         | Les sous-titres SAMI (Synchronized Accessible Media Interchange).                                                                                                 | Aucun.                                                |
| **\_Script MFMediaType**       | Flux de script.                                                                                                                                             | Aucun.                                                |
| **\_Flux MFMediaType**       | Flux multiplexé ou flux élémentaire.                                                                                                                   | [GUID de sous-type de flux](stream-subtype-guids.md)     |
| **\_Vidéo MFMediaType**        | Vidéo.                                                                                                                                                     | [GUID de sous-type de vidéo](video-subtype-guids.md).      |



 

Les composants tiers peuvent définir de nouveaux types principaux et de nouveaux sous-types.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Types de médias](media-types.md)
</dt> </dl>

 

 
