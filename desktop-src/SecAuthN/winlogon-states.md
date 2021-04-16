---
description: Winlogon conserve l’état de station de travail utilisé par le GINA pour déterminer les actions d’authentification requises.
ms.assetid: e04175c4-bb43-4f76-8ceb-50282a1ebed0
title: États Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d2e4ec690d6bdda15fb8e350969b36e01d5c68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558234"
---
# <a name="winlogon-states"></a>États Winlogon

[*Winlogon*](../secgloss/w-gly.md) conserve l’état de station de travail utilisé par le [*Gina*](../secgloss/g-gly.md) pour déterminer les actions d’authentification requises.

À tout moment, Winlogon est dans l’un des trois États suivants :

-   [État de la déconnexion](#logged-off-state)
-   [État de connexion](#logged-on-state)
-   [État verrouillé de la station de travail](#workstation-locked-state)

Ces trois États sont présentés dans l’illustration suivante.

![États Winlogon](images/winlogonst.png)

## <a name="logged-off-state"></a>État de l' Logged-Off

Lorsque Winlogon est à l’état déconnecté, les utilisateurs sont invités à s’identifier et à fournir des informations d’authentification. Si un utilisateur fournit des informations de compte d’utilisateur correctes et qu’aucune restriction ne l’empêche, l’utilisateur est connecté et un programme d’interpréteur de commandes (tel que l’Explorateur Windows) est exécuté sur le Bureau de l’application. Winlogon passe à l’état connecté.

## <a name="logged-on-state"></a>État de l' Logged-On

Lorsque Winlogon est dans l’état connecté, les utilisateurs peuvent interagir avec l’interpréteur de commandes, activer des applications supplémentaires et effectuer leur travail. À partir de l’état de connexion, les utilisateurs peuvent arrêter tout le travail et se déconnecter, ou verrouiller leurs stations de travail (en laissant tout le travail en place). Si l’utilisateur décide de se déconnecter, Winlogon met fin à tous les processus associés à cette [*session de connexion*](../secgloss/l-gly.md) et la station de travail est disponible pour un autre utilisateur. Si, à la place, l’utilisateur décide de verrouiller la station de travail, Winlogon passe à l’état verrouillé de la station de travail.

## <a name="workstation-locked-state"></a>État de l' Workstation-Locked

Lorsque Winlogon est dans l’état verrouillé de la station de travail, un Bureau sécurisé s’affiche jusqu’à ce que l’utilisateur déverrouille la station de travail en fournissant les mêmes informations d’identification et d’authentification que l’utilisateur qui s’est connecté à l’origine, ou jusqu’à ce qu’un administrateur force une fermeture de session. Si la station de travail est déverrouillée, le Bureau de l’application est affiché et le travail peut reprendre. Toutefois, si un administrateur déverrouille la station de travail (en fournissant les informations d’identification et d’authentification d’un compte d’administrateur), les processus de l’utilisateur connecté sont interrompus et Winlogon passe à l’état déconnecté.

Plusieurs actions différentes peuvent être effectuées dans chacun des États Winlogon. Une DLL GINA peut implémenter des actions qui ne font pas partie du système d’exploitation Windows standard. Par exemple, un système de sécurité élevé peut verrouiller automatiquement une station de travail toutes les 10 minutes et forcer les utilisateurs à se réauthentifier.

Pour plus d’informations sur la création de postes de travail et l’inscription d’une [*séquence de touches sécurisées*](../secgloss/s-gly.md) , consultez [initialisation de Winlogon](initializing-winlogon.md). Pour plus d’informations sur les opérations de délai d’attente, consultez [opérations de temps de service de boîte de dialogue prises en charge](supported-dialog-box-service-time-out-operations.md). Pour plus d’informations sur l’envoi de messages au GINA lors de l’affichage d’une boîte de dialogue, consultez [envoi de messages au Gina](sending-messages-to-the-gina.md). Pour plus d’informations sur les fonctions de prise en charge, consultez [Winlogon Support Functions](authentication-functions.md).

 

 
