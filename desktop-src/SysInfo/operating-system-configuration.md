---
description: le répertoire Windows est le répertoire qui contient des applications basées sur des Windows, des fichiers d’initialisation et des fichiers d’aide. La fonction GetWindowsDirectory récupère le chemin d’accès à ce répertoire.
ms.assetid: c07c6337-2c92-42c5-8283-c95637fcb85a
title: Configuration du système d’exploitation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 747a881568f9814152a230880d38891590d33ffc67cfa5e8178adfa66c1a01fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885286"
---
# <a name="operating-system-configuration"></a>Configuration du système d’exploitation

le *répertoire Windows* est le répertoire qui contient des applications basées sur des Windows, des fichiers d’initialisation et des fichiers d’aide. La fonction [**GetWindowsDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) récupère le chemin d’accès à ce répertoire.

Le *répertoire système* est le répertoire qui contient les bibliothèques de liens dynamiques, les pilotes et les fichiers de police. La fonction [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) récupère le chemin d’accès à ce répertoire.

La fonction [**getUserName**](/windows/desktop/api/Winbase/nf-winbase-getusernamea) récupère le nom de l’utilisateur actuellement connecté au système. Le nom d’utilisateur est soit le nom d’ouverture de session, soit le nom complet de l’utilisateur, si ce dernier est inclus dans le registre.

Une *variable d’environnement* est une variable symbolique qui représente un élément du système, tel qu’un chemin d’accès, un nom de fichier ou d’autres données littérales. Par exemple, le chemin d’accès de la variable d’environnement représente les répertoires dans lesquels rechercher les fichiers exécutables. Lorsqu’un utilisateur ouvre une session, le système initialise les variables d’environnement en fonction de la section environnement du Registre. La fonction [**ExpandEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-expandenvironmentstringsa) récupère les valeurs des variables d’environnement spécifiées.

Des informations supplémentaires sont fournies par l’interface [**IADsADSystemInfo**](/windows/desktop/api/iads/nn-iads-iadsadsysteminfo) .

 

 
