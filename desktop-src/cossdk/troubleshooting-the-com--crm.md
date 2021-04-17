---
description: Résolution des problèmes liés à COM+ CRM
ms.assetid: 4d2d9372-b540-4e08-9b57-8687802610b6
title: Résolution des problèmes liés à COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b04e37d183dbf3df8d017e780917f955e14a033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523863"
---
# <a name="troubleshooting-the-com-crm"></a>Résolution des problèmes liés à COM+ CRM

Voici les problèmes les plus courants rencontrés lors du développement et de l’utilisation du CRM COM+ :

-   **Messages du journal des événements.** Si l’application serveur CRM rencontre une erreur interne grave, elle échoue (met fin au processus de l’application CRM Server) et écrit un message dans le journal des événements Windows. Reportez-vous au journal des événements si des problèmes surviennent.

-   **Exceptions du compensateur CRM.** L’infrastructure CRM crée le compensateur CRM et lui transmet les notifications de résultat de la transaction et les enregistrements de journal écrits par le processus de travail CRM. Si le compensateur CRM retourne une erreur ou lève une exception, il est intercepté par l’infrastructure CRM et provoque un FailFast. Un message dans le journal des événements indique qu’une exception a été reçue du compensateur CRM. Il est possible de forcer l’ignorance de ces exceptions. (Voir [paramètres du Registre CRM com+](com--crm-registry-settings.md).) Les exceptions du compensateur CRM signifient probablement un problème dans le composant CRM Compensator spécifique et non dans l’infrastructure CRM elle-même.

-   **Trace de récupération.** Le suivi de récupération peut être très utile pour déterminer les problèmes lors de la récupération. Pour plus d’informations sur l’activation de la trace de récupération, consultez [paramètres de Registre CRM com+](com--crm-registry-settings.md).

-   **La tentative d’exécution avec le CRM n’est pas activée.** Il n’est pas suffisant simplement de placer les composants de travail CRM et du compensateur CRM dans l’application serveur COM+. La prise en charge de CRM doit être activée spécifiquement pour l’application serveur COM+ spécifique à l’aide de l’option **activer les gestionnaires de ressources de compensation** sous l’onglet **avancé** des pages de propriétés de l’application com+. (Pour plus d’informations, consultez [Configuration des composants CRM de com+](configuring-com--crm-components.md) .) En cas de tentative d’utilisation d’un CRM à l’intérieur d’une application serveur pour laquelle le CRM n’est pas activé, un code d’erreur est renvoyé au traitement CRM.

-   **Tentative d’exécution de CRM dans les processus client.** Les CRM ne s’exécutent pas dans les processus clients ; ils doivent s’exécuter dans un processus d’application serveur COM+. Les composants CRM peuvent être placés dans un package de bibliothèque pour être utilisés par plusieurs applications serveur COM+, mais ils ne sont pas disponibles pour une utilisation dans les processus clients. Toute tentative d’utilisation des interfaces CRM à l’intérieur d’un processus client retourne un code d’erreur au travail CRM.

-   **Récupération en cours.** La récupération démarre au démarrage d’une application de serveur CRM. Toutefois, la récupération se produit en arrière-plan pendant le traitement normal de l’application CRM Server. Le processus de travail CRM peut être créé avant la fin de la récupération. Les CRM ne peuvent pas être utilisés dans un processus d’application CRM Server tant que la récupération n’a pas abouti. Dans ce cas, le processus de travail CRM reçoit un code d’erreur « récupération en cours » lorsqu’il tente d’inscrire le compensateur CRM. Le processus de travail CRM doit interroger ou différer jusqu’à ce que la récupération soit terminée. Le temps de récupération est spécifique à un type particulier de CRM et doit être pris en compte lors de la conception du CRM. Les récupérations de longue durée ne sont pas souhaitables.

-   **Sécurité dans le fichier journal CRM.** Si l’accès au fichier journal CRM est refusé, consultez Considérations sur la [sécurité de com+ CRM](com--crm-security-considerations.md) pour obtenir une description de la façon dont la sécurité est définie sur le fichier journal CRM.

-   **Transactions incertaines.** Dans de rares cas, une transaction DTC peut passer à l’état incertain ; autrement dit, le DTC ne peut pas déterminer le résultat de la transaction. Dans ce cas, pendant la récupération, le CRM conserve les enregistrements de journal pour cette transaction dans le fichier journal CRM. Lorsque la transaction incertaine a été résolue par le DTC, une autre récupération de CRM termine la transaction.

-   **Création et publication du compensateur CRM.** La première fois qu’un compensateur CRM est inscrit par un travail CRM, il est créé par l’infrastructure CRM et interrogé pour déterminer quelles interfaces du compensateur CRM prennent en charge. Il est ensuite immédiatement libéré. Les compensateurs CRM doivent prendre en charge la possibilité d’être créés et libérés sans qu’aucun appel de méthode n’ait été effectué. Si le compensateur CRM ne peut pas être créé correctement, peut-être en raison d’une inscription COM incorrecte, ou s’il ne prend pas en charge au moins l’une des interfaces CRM Compensator appropriées, un code d’erreur est renvoyé au traitement CRM.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de Gestionnaire des ressources de compensation COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



