---
description: Tâches des transactions COM+
ms.assetid: fe4374f1-2452-4316-be57-b866c438404d
title: Tâches des transactions COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 102b0ec6ae54430be5499c67b5041ee26035eb077e27b1b860377cd728e3e42d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118307589"
---
# <a name="com-transactions-tasks"></a>Tâches des transactions COM+

Bien que le traitement automatique des transactions dans COM+ vous permette de consacrer un temps de développement plus productif à la création et à la configuration d’objets que vous souhaitez faire participer aux transactions automatiques, vous pouvez effectuer certaines tâches de programmation pour adapter le comportement des transactions aux besoins de votre application.

Les rubriques suivantes présentent des options de programmation spécifiques liées au traitement des transactions.



| Rubrique                                                                                             | Description                                                                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Définition de l’attribut de transaction](setting-the-transaction-attribute.md)<br/>             | Décrit comment définir des valeurs d’attribut de transaction pour vos objets de transaction.<br/>         |
| [Définition du niveau d’isolation des transactions](setting-the-transaction-isolation-level.md)<br/> | Décrit comment définir les niveaux d’isolation des transactions pour vos objets de transaction.<br/>     |
| [Définition du délai d’expiration de la transaction](setting-the-transaction-time-out.md)<br/>               | Décrit comment définir des intervalles de délai d’attente pour vos transactions.<br/>                          |
| [Définition des indicateurs cohérents et terminés](setting-the-consistent-and-done-flags.md)<br/>     | Montre comment utiliser les indicateurs cohérents et terminés pour contrôler le résultat d’une transaction.<br/> |
| [Création d’objets BYOT](creating-byot-objects.md)<br/>                                     | Décrit comment créer des objets pour que vous puissiez apporter votre propre transaction (BYOT).<br/>           |



 

> [!Note]  
> En règle générale, tout composant qui met à jour l’état persistant doit prendre en charge les transactions. Les composants qui combinent les opérations d’au moins deux objets en une seule tâche doivent utiliser des transactions pour simplifier la récupération des erreurs. En outre, pour libérer des ressources, telles que des connexions de base de données, les transactions dans COM+ doivent être aussi courtes que possible.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts des transactions COM+](com--transactions-concepts.md)
</dt> </dl>

 

 




