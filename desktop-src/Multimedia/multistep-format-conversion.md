---
title: Conversion de format à étapes
description: Conversion de format à étapes
ms.assetid: 21d837e7-d665-461d-9676-68add3829fb0
keywords:
- Gestionnaire de compression audio (ACM), conversion de données
- ACM (gestionnaire de compression audio), conversion de données
- Exemples ACM, conversion de données
- convertir des données
- acmFormatSuggest fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e81ebd5bef17d6a97cb5735e15219c39d3116b
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364052"
---
# <a name="multistep-format-conversion"></a>Conversion de format à étapes

Parfois, l’ACM ne peut pas convertir les données d’un format à un autre en une seule étape. Par exemple, une application peut avoir besoin de convertir des données stéréo 16 bits 44-kHz en ADPCM mono 11-kHz. Si le compresseur ou le décompresseur ne peut pas effectuer cette conversion directement, l’application peut l’essayer en deux étapes. Cela signifie généralement qu’il y a une conversion entre deux formats PCM, puis une autre conversion vers le type de format final.

Pour effectuer une conversion en deux étapes, utilisez la fonction [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) pour rechercher un format PCM qui correspond au format ADPCM. Utilisez ensuite deux flux de conversion pour effectuer la conversion. Par exemple, effectuez une conversion du PCM stéréo 16 bits, 44-kHz vers la valeur mono 16 bits, 11 kHz, puis convertissez-les de 16 bits, de 11 kHz mono à 11-kHz Mono ADPCM.

La conversion en une seule étape se produit également lorsque le format source ou de destination n’est pas PCM. Si le format source n’est pas PCM, vous devez le remplacer par un format PCM avant la conversion. Si le format de destination n’est pas PCM, la source doit être convertie au format PCM intermédiaire, puis convertie au format de destination final.

Les conversions les plus simples se produisent lorsque les formats source et destination sont tous deux des formats PCM. Lorsque le format source ou de destination n’est pas PCM, la conversion peut nécessiter une étape supplémentaire. Si les formats source et de destination ne sont pas PCM, la conversion nécessitera généralement plus d’une étape et, dans certains cas, la conversion peut ne pas être possible.

 

 




