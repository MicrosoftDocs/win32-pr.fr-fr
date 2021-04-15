---
title: Finalisation et annulation d’un travail
description: Pour effectuer une tâche de transfert, appelez la méthode méthode ibackgroundcopyjob Complete.
ms.assetid: 8f96ed59-b038-4047-bea4-c63b9e84c209
keywords:
- BITS du travail de transfert, annulation
- annulation d’un travail BITS
- transférer les BITS du travail, terminer
- achèvement d’un travail BITS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeb5cd6a33cf8cefa8749a1802c922dc80518722
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462075"
---
# <a name="completing-and-canceling-a-job"></a>Finalisation et annulation d’un travail

Pour effectuer une tâche de transfert, appelez la méthode [**méthode ibackgroundcopyjob :: Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) . Pour les travaux de téléchargement, vous pouvez appeler la méthode **Complete** avant que tous les fichiers du travail aient été transférés (avant que l’état du travail soit \_ État du travail BG \_ \_ transféré). Seuls les fichiers qui ont été transférés avec succès vers le client avant l’appel de la méthode **Complete** sont à la disposition de l’utilisateur.

Pour les tâches de chargement, appelez la méthode [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) uniquement si l’état du travail est \_ État du travail BG \_ \_ transféré. Pour déterminer quand l’état du travail est transfert de l’état de la tâche BG \_ \_ \_ , [interrogez](polling-for-the-status-of-the-job.md) la propriété de l’état du travail ou inscrivez-vous pour recevoir la \_ notification d’événements de transfert de travail BG Notify \_ \_ . [](registering-a-com-callback.md)

Pour annuler une tâche de transfert, appelez la méthode [**méthode ibackgroundcopyjob :: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) . La méthode **Cancel** supprime le travail de la file d’attente de transfert et supprime les fichiers temporaires du client. En général, vous appelez cette méthode si vous ne parvenez pas à résoudre une erreur associée au travail.

La méthode [**Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) annule un chargement si le chargement n’est pas terminé. Si le téléchargement est terminé et que le travail est de type réponse du type \_ de travail BG \_ \_ \_ , la méthode annule la réponse.

Si vous n’appelez pas la méthode [**Complete**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-complete) ou la méthode [**méthode ibackgroundcopyjob :: Cancel**](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-cancel) dans un délai de 90 jours (par défaut [paramètre jobinactivitytimeout](group-policies.md) stratégie de groupe), le service annule le travail. Si le service annule le travail, les fichiers téléchargés et le fichier de réponse ne sont pas disponibles pour le client ; l’annulation du travail n’affecte pas les fichiers qui ont été téléchargés avec succès. Vous devez toujours appeler la méthode **Complete** ou **Cancel** et ne pas compter sur la stratégie paramètre jobinactivitytimeout pour nettoyer vos travaux. Les travaux laissés dans la file d’attente peuvent empêcher les utilisateurs de créer d’autres travaux si la limite de stratégie MaxJobsPerUser ou MaxJobsPerMachine est atteinte.

 

 




