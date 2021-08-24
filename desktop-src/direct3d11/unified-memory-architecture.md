---
title: Architecture de la mémoire unifiée
description: L’interrogation de la prise en charge de l’architecture mémoire unifiée (UMA) peut vous aider à déterminer comment gérer certaines ressources.
ms.assetid: E43892F9-E7CD-4D18-BDDE-3C4F03F8F4EA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09648c69f312f16d1301b6c9b5cad21d544bd456f244950486cf9d6871079c96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119375669"
---
# <a name="unified-memory-architecture"></a>Architecture de la mémoire unifiée

L’interrogation de la prise en charge de l’architecture mémoire unifiée (UMA) peut vous aider à déterminer comment gérer certaines ressources.

Une valeur booléenne, définie par le pilote, peut être lue à partir de la structure de données de la [**\_ fonctionnalité d3d11 \_ \_ d3d11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) pour déterminer si le matériel prend en charge la UMA.

Les applications qui s’exécutent sur une UMA peuvent souhaiter avoir plus de ressources avec un accès processeur activé que si elles ne sont pas disponibles. La UMA permet aux applications de ne pas copier les données des ressources, au lieu de rester efficaces uniquement pour les cartes graphiques non UMA. [Fonctionnalités Direct3D 11,3](direct3d-11-3-features.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnalités Direct3D 11,3](direct3d-11-3-features.md)
</dt> </dl>

 

 




