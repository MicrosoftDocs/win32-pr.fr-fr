---
title: À propos du service BITS
description: Utilisez Service de transfert intelligent en arrière-plan (BITS) pour transférer des fichiers de façon asynchrone entre un client et un serveur.
ms.assetid: 056007f4-6a71-4f8e-bf7d-17ed87088edf
keywords:
- Service de transfert intelligent en arrière-plan, Description
- BITS de file d’attente de transfert
- BITS de file d’attente de transfert, limitation
ms.topic: article
ms.date: 7/12/2019
ms.openlocfilehash: 53693b7087d647e8d6e89a8c81e09895dc3866b964642475466bbf8f52ddbae5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529279"
---
# <a name="about-bits"></a>À propos du service BITS

Utilisez Service de transfert intelligent en arrière-plan (BITS) pour télécharger des fichiers à partir de ou télécharger des fichiers vers des serveurs Web HTTP ou des serveurs de fichiers SMB. 

Le service BITS continue de transférer des fichiers après la fermeture d’une application tant que l’utilisateur qui a initié le transfert reste connecté et qu’une connexion réseau est conservée. Le service BITS ne force pas une connexion réseau. Le service BITS reprend les transferts après qu’une connexion réseau qui a été perdue est rétablie ou après qu’un utilisateur a fermé la session. Pour plus d’informations, consultez [utilisateurs et connexions réseau](users-and-network-connections.md).

Le service BITS est conscient du coût actuel du réseau et de la congestion afin qu’une tâche en arrière-plan interfère le moins possible avec l’expérience de premier plan de l’utilisateur. BITS utilise la [bande passante réseau](network-bandwidth.md) inactive pour transférer les fichiers et augmente ou diminue la vitesse de transfert des fichiers en fonction de la quantité de bande passante réseau inactive disponible. Si une application réseau commence à utiliser davantage de bande passante, le service BITS diminue son taux de transfert pour préserver l’expérience interactive de l’utilisateur. BITS utilise des stratégies de [transfert](how-to-block-a-bits-job-from-downloading-over-an-expensive-connection.md) spécifiées par l’application pour empêcher le transfert de fichiers sur des connexions réseau coûteuses.

Le service BITS est également conscient de l’utilisation de l’alimentation. à partir de la Mise à jour de mai 2019 de Windows 10, BITS transfère les fichiers lorsque l’ordinateur est en mode [veille moderne](/windows-hardware/design/device-experiences/modern-standby) et que l’ordinateur est branché.

L’application BITS peut utiliser les différents [niveaux de priorité](/windows/desktop/api/Bits/ne-bits-bg_job_priority) bits pour permettre aux bits de choisir les tâches de transfert à exécuter de manière intelligente. Les tâches ayant la priorité la plus élevée devancent celles avec la priorité la plus faible. Les tâches au même niveau de priorité partagent le temps de transfert, ce qui empêche une tâche volumineuse de bloquer les petites tâches dans la file d’attente de transfert. Les tâches avec la priorité la plus faible ne reçoivent pas de temps de transfert tant que toutes les tâches ayant la priorité la plus élevée ne sont pas terminées ou dans un état d’erreur.

BITS utilise Windows BranchCache pour la mise en cache d’homologue. Pour plus d’informations, consultez la [vue d’ensemble de BranchCache](/previous-versions/windows/it-pro/windows-7/dd755969(v=ws.10)).

les développeurs plateforme Windows universelle (UWP) doivent utiliser le [Windows. L’API Networking. BackgroundTransfer](/uwp/api/Windows.Networking.BackgroundTransfer) et non l’API bits.

Il existe trois types de [**tâches de transfert**](/windows/desktop/api/Bits/ne-bits-bg_job_type). Un travail de téléchargement télécharge des fichiers sur le client, un travail de chargement charge un fichier sur le serveur et un travail de chargement-réponse charge un fichier sur le serveur et reçoit un fichier de réponse de l’application serveur.

Les rubriques suivantes fournissent des informations plus détaillées sur BITS :

-   [Authentification](authentication.md)
-   [Cycle de vie d’une tâche BITS](life-cycle-of-a-bits-job.md)
-   [Utilisateurs et connexions réseau](users-and-network-connections.md)
-   [Bande passante réseau](network-bandwidth.md)
-   [Stratégies de groupe](group-policies.md)
-   [Comptes de service et BITS](service-accounts-and-bits.md)
-   [Jetons d’assistance pour les tâches de transfert BITS](helper-tokens-for-bits-transfer-jobs.md)
-   [Cohérence du transfert de fichiers](file-transfer-consistency.md)
-   [Configuration HTTP requise pour les téléchargements BITS](http-requirements-for-bits-downloads.md)
-   [Configuration requise pour IIS pour les téléchargements BITS](iis-requirements-for-bits-uploads.md)
-   [Nettoyage de répertoire virtuel](virtual-directory-cleanup.md)
-   [BITS et restauration du système](bits-and-system-restore.md)
-   [Type de démarrage BITS](bits-startup-type.md)
-   [Partage de connexion Internet](internet-connection-sharing.md)
-   [Mise en cache d’homologue](peer-caching.md)
-   [Sécurité BITS, jetons et comptes d’administrateur](user-account-control-and-bits.md)
-   [BITS Compact Server](bits-compact-server.md)

Utilisez les [interfaces](bits-interfaces.md) bits pour écrire des applications qui créent et surveillent les tâches de transfert. Pour plus d’informations sur l’utilisation des interfaces BITS, consultez [utilisation de bits](using-bits.md).