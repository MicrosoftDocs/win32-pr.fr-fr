---
description: 'En savoir plus sur : considérations relatives à la programmation pour l’écriture de gestionnaires de ressources'
ms.assetid: 7f1e61e8-15e1-4a25-b864-eeadcac61108
title: Considérations relatives à la programmation pour l’écriture de gestionnaires de ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a20d84695a5bc0f378c8b93519a35b9a1d95bcc58d718520478e519707553b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388908"
---
# <a name="programming-considerations-for-writing-resource-managers"></a>Considérations relatives à la programmation pour l’écriture de gestionnaires de ressources

Lorsque vous utilisez l’API du gestionnaire de transactions du noyau pour ajouter la prise en charge des transactions à vos applications, prenez en compte les éléments suivants :

-   Lorsque vous écrivez votre propre gestionnaire de ressources, vous devez disposer d’une bonne connaissance pratique des techniques et des protocoles de gestion des transactions.
-   Si vous n’écrivez pas correctement les gestionnaires de ressources, vous pouvez corrompre vos propres données avec des opérations de récupération correctement gérées. Vous pouvez également épingler la fin du journal des transactions et remplir votre système de fichiers à l’aide des journaux de transactions.
-   Si votre stratégie de taille de journal n’est pas définie pour empêcher la taille du journal, votre gestionnaire de ressources n’arrête pas les transactions. Votre gestionnaire de ressources doit arrêter la mise à jour du système afin qu’il ne sature pas les ressources du système de fichiers.
-   Les gestionnaires de ressources doivent utiliser des listes de contrôle d’accès (ACL) pour contrôler l’accès aux fichiers journaux. dans le cas contraire, les attaques par déni de service sont possibles.
-   Tout gestionnaire de ressources ou participant de transaction qui met en cache des données doit s’inscrire pour les notifications de prépréparation. Lors de la réception d’une notification de prépréparation, vous devez vider toutes vos données, de sorte que tous les gestionnaires de ressources en aval puissent s’inscrire avant la phase de préparation. Tout travail supplémentaire dans cette transaction ne doit pas être mis en cache.
-   Ne fermez pas un handle d’inscription tant que la transaction est toujours active ; Cela entraîne la restauration de la transaction.

 

 



