---
description: Suggestions de conception pour le développement d’un CRM COM+
ms.assetid: dde1b978-6d35-4a75-91fd-69dfcc6c43d2
title: Suggestions de conception pour le développement d’un CRM COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dcdb59f0ea23fb6879300d0bacec7df12970d81
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200982"
---
# <a name="design-suggestions-for-developing-a-com-crm"></a>Suggestions de conception pour le développement d’un CRM COM+

Voici les étapes suggérées pour le développement d’un CRM COM+ :

1.  Avant de commencer le développement, définissez le délai d’expiration de la transaction sur zéro (à l’aide de l’outil d’administration Services de composants). Définissez l’indicateur de Registre VTRACE1 (consultez [paramètres de Registre CRM com+](com--crm-registry-settings.md)) pour afficher les messages d’avertissement et d’erreur CRM sur la trace de débogage.
2.  Déterminez l’ensemble d’interfaces que vous devez utiliser, structuré (variantes) ou non structuré. (Voir [interfaces CRM com+](com--crm-interfaces.md).) Cela dépend du langage que vous utilisez pour développer votre CRM, par exemple, Microsoft Visual C++ ou Microsoft Visual Basic.
3.  Commencez par développer le travail CRM. Déterminez les informations requises dans les enregistrements de journal. Définissez les types d’enregistrements de journal requis et leur format.
4.  Un compensateur CRM de débogage est fourni dans le cadre des exemples CRM (dans le SDK Windows). Cela peut être utilisé temporairement lors du débogage du processus de travail CRM à la place du compensateur CRM réel.
5.  Lorsque le processus de travail CRM fonctionne correctement, développez le compensateur CRM réel et remplacez le compensateur CRM de débogage par le compensateur CRM réel.
6.  Il peut être souhaitable de ne pas tester initialement le cas de récupération. Si c’est le cas, supprimez le fichier journal CRM de l’application CRM Server chaque fois avant de démarrer l’application CRM Server.

## <a name="considerations"></a>Considérations

1.  **Écrivez à l’avance.** Le composant de travail CRM doit écrire à l’avance ; autrement dit, il doit écrire un enregistrement de journal indiquant qu’il va exécuter une action avant d’effectuer cette action. En outre, cet enregistrement de journal doit être forcé sur le disque après l’écriture et avant l’exécution de l’action.
2.  **Isolation.** Le CRM n’applique pas l’isolation. La conception CRM doit assurer l’isolation entre plusieurs clients sur des transactions distinctes et doit également prendre en compte le cas avant la récupération.
3.  **Récupération en cours.** Le processus de travail CRM doit gérer le code d’erreur « récupération en cours ». Pour plus d’informations sur ce code d’erreur, consultez [résolution des problèmes liés à com+ CRM](troubleshooting-the-com--crm.md) .
4.  **Gestion des erreurs.** Le processus de travail CRM doit faire face au cas où la transaction est abandonnée plus tôt que prévu. Consultez la section [gestion des erreurs dans le CRM com+](error-handling-in-the-com--crm.md).
5.  **Temps de récupération.** Le compensateur CRM doit être conçu pour effectuer une récupération rapide afin de ne pas avoir à attendre le nouveau travail de l’application CRM Server.
6.  **L’idempotence.** Il est possible qu’un compensateur CRM reçoive à nouveau le même enregistrement de journal, pour annuler ou rétablir une action qui a déjà été annulée ou rétablie. Les actions que le compensateur CRM peut effectuer doivent être idempotent, ce qui signifie souvent que les codes d’erreur retournés par ces actions doivent être ignorés.
7.  **Lancement de la récupération.** La récupération d’une application CRM Server est effectuée au démarrage de l’application CRM Server. Toutefois, il n’existe pas de démarrage automatique d’une application CRM Server. Le développeur de l’application doit prendre en compte la façon dont le démarrage et la récupération doivent être initiés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de Gestionnaire des ressources de compensation COM+](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



