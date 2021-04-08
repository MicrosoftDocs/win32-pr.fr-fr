---
description: Répertorie et explique les responsabilités du GINA.
ms.assetid: 5cffe4a6-6475-441e-bf81-f3cbcf1fee3f
title: Responsabilités du GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3481aea9f5a92a485c42fb00b43d7062012d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034472"
---
# <a name="responsibilities-of-the-gina"></a>Responsabilités du GINA

> [!Note]  
> Les DLL GINA sont ignorées dans Windows Vista.

 

Une dll [*Gina*](../secgloss/g-gly.md) a les responsabilités suivantes :

-   Analyse SAS

    La GINA est chargée de reconnaître une [*séquence de sécurité sécurisée*](../secgloss/s-gly.md) (SAS), de surveiller les événements SAS et de notifier Winlogon quand une SAP s’est produite. Notez qu’il peut y avoir plus d’une SAP définie et que l’ensemble de SASs défini peut changer au fil du temps. Par exemple, il peut y avoir un jeu de SASs lorsque [*Winlogon*](../secgloss/w-gly.md) est dans l’état de déconnexion et un autre ensemble lorsqu’il se trouve à l’état connecté.

    Winlogon fournit des services pour assister le GINA dans à l’aide de la combinaison de touches CTRL + ALT + DEL SAS.

-   Traitement SAS

    L’une des raisons qui justifient le remplacement de GINA est de fournir d’autres mécanismes d’identification et d’authentification. Pour ce faire, GINA doit présenter toutes les interfaces utilisateur résultant de la reconnaissance d’une signature d’accès partagé. Quand aucun utilisateur n’est connecté, GINA est responsable de la présentation des options d’identification et d’authentification, ainsi que de toutes les autres options autorisées qui ne sont pas authentifiées. Lorsqu’un utilisateur a ouvert une session, GINA est responsable de la présentation des options pertinentes à l’utilisateur, ainsi que de la réalisation des actions jugées appropriées. Par exemple, dans un système qui comprend une [*carte à puce*](../secgloss/s-gly.md), il peut être approprié de verrouiller automatiquement la station de travail si l’utilisateur supprime la carte à puce.

-   Activation du shell

    Lorsqu’un utilisateur ouvre une session, GINA est responsable de la création d’un ou plusieurs processus initiaux pour cet utilisateur. (Dans cette documentation, on suppose que ces processus initiaux présentent une interface à l’utilisateur. Toutefois, les processus peuvent être des processus et n’ont pas nécessairement besoin d’interagir avec l’utilisateur.) Ces processus sont appelés Shell de l' *utilisateur* ou simplement l' *interpréteur* de commandes. Dans le cadre de l’activation de l’interpréteur de commandes, le GINA doit affecter le jeton de l’utilisateur qui vient d’être connecté aux processus. Winlogon fournit un service pour aider la GINA à assigner le jeton.

 

 
