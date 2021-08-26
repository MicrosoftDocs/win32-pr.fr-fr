---
description: Il existe diverses fonctions permettant d’obtenir des informations sur les processus.
ms.assetid: f9ec6aa5-15ad-47e6-b5f8-8ac4daaf178f
title: Obtention d’informations supplémentaires sur le processus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98b4ed87fca02dfcee4cbcd36621fffb9920a3f320cfeac771507748a151cf33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032119"
---
# <a name="obtaining-additional-process-information"></a>Obtention d’informations supplémentaires sur le processus

Il existe diverses fonctions permettant d’obtenir des informations sur les processus. Certaines de ces fonctions peuvent être utilisées uniquement pour le processus appelant, car elles ne prennent pas de handle de processus en tant que paramètre. Vous pouvez utiliser des fonctions qui prennent un handle de processus pour obtenir des informations sur d’autres processus.

-   Pour obtenir la chaîne de ligne de commande pour le processus en cours, utilisez la fonction [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) .
-   Pour récupérer la structure [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) spécifiée lors de la création du processus en cours, utilisez la fonction [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) .
-   Pour obtenir les informations de version à partir de l’en-tête de l’exécutable, utilisez la fonction [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) .
-   Pour obtenir le chemin d’accès complet et le nom de fichier du fichier exécutable contenant le code de processus, utilisez la fonction [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .
-   Pour obtenir le nombre de descripteurs des objets de l’interface graphique utilisateur (GUI) en cours d’utilisation, utilisez la fonction [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) .
-   Pour déterminer si un processus est en cours de débogage, utilisez la fonction [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .
-   Pour récupérer des informations de gestion de comptes pour toutes les opérations d’e/s effectuées par le processus, utilisez la fonction [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) .

 

 
