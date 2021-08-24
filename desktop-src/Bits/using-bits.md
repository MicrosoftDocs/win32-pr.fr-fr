---
title: Utilisation de BITS
description: Utilisation de BITS
ms.assetid: 65b69ccb-b413-4690-ac0d-774d88608bdf
keywords:
- Service de transfert intelligent en arrière-plan (BITS)
- Service de transfert intelligent en arrière-plan, tâches
- BITS de transfert de fichiers
- Utilisation de bits bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b301c1d96956bca924d99ef41ade3032f58dc4e194b420069cbae1071c916b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801159"
---
# <a name="using-bits"></a>Utilisation de BITS

Les étapes suivantes montrent comment effectuer un transfert de fichiers à l’aide des  [interfaces](bits-interfaces.md)service de transfert intelligent en arrière-plan (bits).

**Pour effectuer un transfert de fichiers**

1.  [Connecter au service BITS](connecting-to-the-bits-service.md)
2.  [Créer une tâche de transfert](creating-a-job.md)
3.  [Ajouter des fichiers au travail](adding-files-to-a-job.md)
4.  [Démarrage du travail](/windows/desktop/api/Bits/nf-bits-ibackgroundcopyjob-resume)
5.  [Déterminer si BITS a transféré les fichiers avec succès](determining-the-status-of-a-job.md)
6.  [Terminer la tâche](completing-and-canceling-a-job.md)

Les étapes précédentes montrent comment transférer des fichiers à l’aide des valeurs de propriété par défaut pour un travail. Vous pouvez modifier le comportement par défaut en modifiant une ou plusieurs des valeurs de propriété du travail. Par exemple, vous pouvez modifier la priorité de traitement du travail par rapport à d’autres travaux de la file d’attente, spécifier votre propre paramètre de proxy et vous inscrire pour recevoir une notification d’événement lorsque le service BITS a transféré les fichiers. Pour plus d’informations, consultez [définition et récupération des propriétés d’un travail](setting-and-retrieving-the-properties-of-a-job.md).

Windows PowerShell fournit un mécanisme simple pour gérer de nombreuses tâches BITS. cette section contient les rubriques suivantes qui montrent comment utiliser Windows PowerShell applets de commande avec BITS :

-   [Utilisation de Windows PowerShell pour créer des tâches de transfert BITS](using-windows-powershell-to-create-bits-transfer-jobs.md)
-   [Utilisation des applets de commande Windows PowerShell WinRM pour gérer les tâches de transfert BITS](using-winrm-windows-powershell-cmdlets-to-manage-bits-transfer-jobs.md)
-   [utilisation des applets de commande WMI Windows PowerShell pour gérer BITS Compact Server](using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server.md)

> [!Note]
>
> à partir de Windows 10, la version 1607, vous pouvez également exécuter des applets de commande powershell et utiliser BITSAdmin ou d’autres applications qui utilisent les [interfaces](bits-interfaces.md) BITS à partir d’une ligne de commande à distance powershell connectée à un autre ordinateur (physique ou virtuel). Cette fonctionnalité n’est pas disponible lors de l’utilisation d’une ligne de commande [PowerShell direct](/virtualization/hyper-v-on-windows/user_guide/vmsession) sur un ordinateur virtuel sur la même machine physique, et elle n’est pas disponible lors de l’utilisation des applets de commande WinRM.
>
> Un travail BITS créé à partir d’une session PowerShell distante s’exécute dans le contexte du compte d’utilisateur de cette session et ne progresse que lorsqu’il y a au moins une session de connexion locale active ou une session PowerShell distante associée à ce compte d’utilisateur. Pour plus d’informations, consultez [pour gérer les sessions à distance PowerShell](using-windows-powershell-to-create-bits-transfer-jobs.md).

 

Cette section contient également les rubriques suivantes :

-   [Meilleures pratiques lors de l’utilisation de BITS](best-practices-when-using-bits.md)
-   [Énumération des travaux dans la file d’attente de transfert](enumerating-jobs-in-the-transfer-queue.md)
-   [Énumération de fichiers dans un travail](enumerating-files-in-a-job.md)
-   [Gestion des erreurs](handling-errors.md)
-   [Récupérer la réponse d’une tâche de chargement-réponse](retrieving-the-reply-from-an-upload-reply-job.md)

Pour obtenir un exemple de code qui utilise les interfaces BITS, consultez [exemples et outils bits](bits-samples-and-tools.md).

 

 