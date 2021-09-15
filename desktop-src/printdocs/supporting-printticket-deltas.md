---
description: En savoir plus sur la prise en charge des deltas PrintTicket. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 80fdc8f1-4fda-4102-9b27-16d9acb4d077
title: Prise en charge des deltas PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7f72f82875d0207ed232f4db897c78295ce2ee0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403705"
---
# <a name="supporting-printticket-deltas"></a>Prise en charge des deltas PrintTicket

Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

L’interface du fournisseur PrintTicket a des méthodes qui peuvent être utilisées pour apporter des modifications incrémentielles à un PrintTicket existant. Les modifications Incremental PrintTicket peuvent être spécifiées dans un PrintTicket partiel appelé « un Delta PrintTicket ». Un PrintTicket révisé est créé en fusionnant un Delta PrintTicket avec un PrintTicket existant. Pour plus d’informations sur les méthodes impliquant des deltas PrintTicket, consultez le document de l’interface de fournisseur PrintTicket à venir.

Lors du traitement d’un Delta PrintTicket, les étapes suivantes doivent être effectuées.

1.  Identifiez les instances de fonctionnalité ou de ParameterInit qui sont communes à la fois à l’instance PrintTicket existante (le PrintTicket cible) et à l’écart PrintTicket.

    -   Pour chaque fonctionnalité commune à la fois à la cible PrintTicket et au Delta PrintTicket, remplacez la fonctionnalité dans le PrintTicket cible par la fonctionnalité correspondante dans le delta PrintTicket.

    -   Pour chaque ParameterInit commun à la fois à la cible PrintTicket et à l’écart PrintTicket, remplacez le ParameterInit dans le PrintTicket cible par le ParameterInit correspondant dans le delta PrintTicket.

2.  Copiez toutes les instances de fonctionnalité et ParameterInit restantes dans le delta PrintTicket dans le PrintTicket cible.

3.  Si votre algorithme de résolution des conflits permet de spécifier des priorités dans le PrintTicket lui-même, vous pouvez choisir d’élever les priorités de la fonctionnalité et les instances ParameterInit nommées dans le delta PrintTicket.

4.  Exécutez la validation PrintTicket comme décrit dans la liste de contrôle de [validation PrintTicket](printticket-validation-checklist.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



