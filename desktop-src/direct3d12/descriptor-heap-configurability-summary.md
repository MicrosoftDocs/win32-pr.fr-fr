---
title: Résumé de la configuration du tas de descripteurs
description: Le tableau suivant récapitule les informations sur la prise en charge des tas et des tas visibles non-nuanceur.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cfef479e88e5c77df0732113597a4742ecb909c
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335566"
---
# <a name="descriptor-heap-configurability-summary"></a>Résumé de la configuration du tas de descripteurs

Le tableau suivant récapitule les informations sur la prise en charge des tas et des tas visibles non-nuanceur.



|                               | Tas du descripteur visible du nuanceur                                                 | Tas du descripteur visible non-nuanceur                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Types de tas pris en charge**          | CBV \_ SRV \_ UAV, échantillonneur                                                         | Tous                                                                                                                                                                                                                                                                                                                                                                 |
| **Propriétés de la page UC prises en charge** | NON \_ disponible, combinaison d’écriture \_                                                 | ÉCRITURE \_ différée                                                                                                                                                                                                                                                                                                                                                         |
| **Gestion de la résidence par application**   | Oui, l’application est responsable                                                           | Non applicable (pas de GPU visible).                                                                                                                                                                                                                                                                                                                                   |
| **Prise en charge des modifications de descripteur**       | Destination de copie uniquement, via la mise à jour de la liste de commandes et/ou la copie de l’UC si l’UC est visible. | Lecture et écriture de l’UC uniquement. Aucun accès direct au GPU. Peut être utilisé pour la copie de l’UC immédiate (en tant que source et destination). Peut être utilisé en tant que source de mise à jour dans une liste de commandes : copie les descripteurs dans le stockage de la liste de commandes lors de l’enregistrement de la liste de commandes. Lors de l’exécution, la copie stockée est copiée vers la destination, qui doit être un tas visible par le nuanceur. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tas de descripteurs](descriptor-heaps.md)
</dt> </dl>

 

 




