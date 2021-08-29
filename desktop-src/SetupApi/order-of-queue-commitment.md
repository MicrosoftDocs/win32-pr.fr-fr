---
description: 'Lorsque la fonction SetupCommitFileQueue valide la file d’attente de fichiers, elle traite les opérations de fichiers dans l’ordre suivant : opérations de suppression de fichiers, opérations de changement de nom de fichier et enfin, opérations de copie de fichiers.'
ms.assetid: 23aae815-ff1a-435d-b14d-3c62a3355a1b
title: Ordre de validation des files d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a7ff3cc211b2a2d253dd307ca83113b536a3d9eaf21b7b2cec5bc977f585026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665538"
---
# <a name="order-of-queue-commitment"></a>Ordre de validation des files d’attente

Lorsque la fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) valide la file d’attente de fichiers, elle traite les opérations de fichiers dans l’ordre suivant : opérations de suppression de fichiers, opérations de changement de nom de fichier et enfin, opérations de copie de fichiers. Le schéma suivant illustre le cycle de vie du processus d’engagement d’une file d’attente.

 

-   Démarrer la sous-file d’attente de suppression
    -   démarrer une opération de suppression de fichier <--répéter pour chaque
    -   terminer une opération de suppression de fichier <--suppression de fichier en file d’attente
-   terminer la suppression de la sous-file d’attente

<!-- -->

-   Démarrer la sous-file d’attente de renommage
    -   démarrer une opération de changement de nom de fichier <--répéter pour chaque
    -   terminer une opération de suppression de fichier <--renommage de fichier en file d’attente
-   terminer la sous-file d’attente de renommage

<!-- -->

-   Démarrer la copie subque
    -   démarrer une opération de copie de fichiers <--répéter pour chaque
    -   terminer une opération de copie de fichiers <--copie de fichiers en file d’attente
    -   terminer la sous-file d’attente de copie
-   terminer la file d’attente

 

À chaque étape, ou si une erreur se produit, la fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) envoie une notification à la routine de rappel. La routine de rappel peut utiliser les informations envoyées par la file d’attente pour suivre la progression de l’installation et, si nécessaire, interagir avec l’utilisateur.

Par exemple, si une opération de copie de fichiers a besoin d’un fichier source qui n’était pas disponible dans le chemin d’accès actuel, [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) enverra une \_ notification NEEDMEDIA SPFILENOTIFY à la routine de rappel, ainsi que des informations sur le fichier et le support requis. La routine de rappel peut utiliser ces informations pour générer une boîte de dialogue qui invite l’utilisateur à insérer le disque suivant en appelant [ **SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)

Une routine de rappel de file d’attente par défaut, [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka), est incluse avec l’API d’installation. Cette routine gère les notifications de file d’attente et génère des boîtes de dialogue d’erreur et des barres de progression pour l’installation. Vous pouvez utiliser la routine de rappel de file d’attente par défaut, ou écrire une routine de rappel de filtre pour gérer un sous-ensemble des notifications et passer les autres à la routine de rappel de file d’attente par défaut.

Si aucune des fonctionnalités de la routine de rappel ne répond à vos besoins, vous pouvez écrire une routine de rappel personnalisé autonome qui n’appelle pas la routine de rappel de file d’attente par défaut.

Pour plus d’informations sur les routines de rappel de file d’attente, consultez [routine de rappel de file d’attente par défaut](default-queue-callback-routine.md)et [création d’une routine de rappel de file d’attente personnalisée](creating-a-custom-queue-callback-routine.md).

 

 



