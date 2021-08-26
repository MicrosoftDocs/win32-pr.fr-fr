---
title: Fonctions de récupération et de redémarrage de l’application
description: La récupération et le redémarrage de l’application définissent les fonctions suivantes
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df0a2139a24c3e69ae328533d6bf8b1baeee2043bc82b9f8d50f4272a16e2f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024619"
---
# <a name="application-recovery-and-restart-functions"></a>Fonctions de récupération et de redémarrage de l’application

La récupération et le redémarrage de l’application définissent les fonctions suivantes :



| Fonction                                                                               | Description                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**ApplicationRecoveryFinished**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | Indique que l’application appelante a terminé la récupération des données.                    |
| [**ApplicationRecoveryInProgress**](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | Indique que l’application appelante continue à récupérer des données.                      |
| [**GetApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | Récupère un pointeur vers la routine de rappel de récupération inscrite pour le processus spécifié. |
| [**GetApplicationRestartSettings**](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | Récupère les informations de redémarrage inscrites pour le processus spécifié.                    |
| [**RegisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | Inscrit l’instance active d’une application pour la récupération.                              |
| [**RegisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | Inscrit l’instance active d’une application pour le redémarrage.                               |
| [**UnregisterApplicationRecoveryCallback**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | Supprime l’instance active d’une application de la liste de récupération.                      |
| [**UnregisterApplicationRestart**](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | Supprime l’instance active d’une application de la liste de redémarrage.                       |



 

 

 