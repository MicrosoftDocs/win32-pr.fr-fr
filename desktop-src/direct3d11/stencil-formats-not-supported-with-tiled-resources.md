---
title: Formats de stencil non pris en charge avec les ressources en mosaïque
description: Les formats qui contiennent le stencil ne sont pas pris en charge avec les ressources en mosaïque.
ms.assetid: 1B675245-F21F-47B5-B3B4-C8307DAC575B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce07b64e54808a2b4b730f6ed9c5321956f6bf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028489"
---
# <a name="stencil-formats-not-supported-with-tiled-resources"></a>Formats de stencil non pris en charge avec les ressources en mosaïque

Les formats qui contiennent le stencil ne sont pas pris en charge avec les ressources en mosaïque.

Les formats qui contiennent le stencil incluent DXGI \_ format \_ D24 \_ UNORM \_ S8 \_ uint (et les formats associés dans la famille R24G8) et dxgi \_ format d32 \_ \_ float \_ S8X24 \_ uint (et les formats associés dans la famille R32G8X24).

Certaines implémentations stockent la profondeur et le stencil dans des allocations distinctes, tandis que d’autres les stockent ensemble. La gestion des vignettes pour les deux schémas devrait être différente et aucune API ne peut abstraire ou rationaliser les différences. Nous vous recommandons d’utiliser du matériel pour prendre en charge des surfaces de stencil et de profondeur indépendantes, chacune étant présentée indépendamment. la profondeur de 32 bits comporterait des vignettes 128 x 128 et le stencil de 8 bits aurait des vignettes 256x256. Par conséquent, les applications doivent être en ligne avec un mauvais alignement de forme de vignette entre la profondeur et le gabarit. Mais le même problème existe déjà avec des formats de surface cible de rendu différents.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Partage de ressources en mosaïque et partage d’appareils](tiled-resource-cross-process-and-device-sharing.md)
</dt> </dl>

 

 




