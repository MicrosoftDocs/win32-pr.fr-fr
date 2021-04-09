---
title: Fonctions de récupération et de redémarrage de l’application
description: La récupération et le redémarrage de l’application définissent les fonctions suivantes
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f9f5fb41f2ef694b4d99044a8756ff0bb66c3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102036"
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



 

 

 