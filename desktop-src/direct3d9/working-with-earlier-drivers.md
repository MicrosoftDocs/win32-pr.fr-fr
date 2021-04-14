---
description: Cette section répertorie les problèmes qui peuvent se produire lors de l’utilisation de Direct3D 9 sur des pilotes écrits pour des versions de Direct3D antérieures à Direct3D 9.
ms.assetid: 891198e8-6c45-4f03-99bb-e24a4082b0d8
title: Utilisation des pilotes antérieurs (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76567bc4778924835e20a476b03dc94ea77739fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392412"
---
# <a name="working-with-earlier-drivers-direct3d-9"></a>Utilisation des pilotes antérieurs (Direct3D 9)

Cette section répertorie les problèmes qui peuvent se produire lors de l’utilisation de Direct3D 9 sur des pilotes écrits pour des versions de Direct3D antérieures à Direct3D 9.

-   Lors de l’utilisation d’un périphérique HAL T&L, l’intensité du brouillard est calculée, mais l’opération de valeur absolue n’est pas appliquée à cette valeur. Au lieu de cela, la valeur est laissée négative si c’est ce qui est calculé. La meilleure façon d’éviter cette situation consiste à configurer les transformations de manière appropriée. Une méthode moins recommandée consiste à faire en sorte que les valeurs de début de brouillard et de fin de brouillard soient négatives.

Pour rechercher un pilote Direct3D 9, recherchez une valeur différente de zéro pour D3DDEVCAPS2 \_ STREAMOFFSET dans le membre DevCaps2 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conseils de programmation](programming-tips.md)
</dt> </dl>

 

 



