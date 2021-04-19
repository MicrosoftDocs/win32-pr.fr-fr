---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: Création d’un document PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ccb1adf4626254ba9f71c706ad7d4556a23aeb6
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106535751"
---
# <a name="creating-a-printcapabilities-document"></a>Création d’un document PrintCapabilities

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

Une fois qu’un PrintTicket est validé, il peut être utilisé pour créer un instantané du PrintCapabilities. Le fournisseur doit avoir une représentation interne pour toute propriété dont la valeur dépend de la configuration de l’appareil. Par exemple, si SpotDiameter est une propriété qui dépend à la fois des fonctionnalités de résolution et de MediaType, une représentation interne de SpotDiameter telle qu’elle est liée aux différentes valeurs pour la résolution et le MediaType peut apparaître comme dans le tableau suivant :



| Résolution      | MediaType         | SpotDiameter   |
|-----------------|-------------------|----------------|
| 300<br/>  | Liés<br/>   | 520<br/> |
| 300<br/>  | Brillance<br/> | 350<br/> |
| 600<br/>  | Liés<br/>   | 330<br/> |
| 600<br/>  | Brillance<br/> | 180<br/> |
| 1200<br/> | Liés<br/>   | 250<br/> |
| 1200<br/> | Brillance<br/> | 100<br/> |



 

Pour cet exemple, le fournisseur PrintCapabilities doit utiliser le PrintTicket fourni pour sélectionner l’entrée appropriée dans la table interne et signaler comme valeur pour la propriété SpotDiameter. Ce processus est répété pour chaque propriété à valeurs multiples (pour chaque propriété dont la valeur dépend de la configuration). La section [schéma PrintCapabilities et construction de document](printcapabilities-schema-and-document-construction.md) décrit les autres étapes impliquées dans la création d’un instantané du PrintCapabilities.

Pour créer un instantané du document PrintCapabilities par défaut, fournissez un PrintTicket par défaut (plutôt qu’un PrintTicket arbitraire) à la méthode qui crée des documents PrintCapabilities.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




