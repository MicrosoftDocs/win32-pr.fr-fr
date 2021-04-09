---
description: Le gestionnaire de symboles est conçu pour effectuer le suivi de différents jeux de fichiers de symboles.
ms.assetid: 1bd7ac25-e46d-442b-b365-52edcd8bf922
title: Initialisation du gestionnaire de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146af0e1118e85a3478ca45be7a86c4b1d8dfe83
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110202"
---
# <a name="symbol-handler-initialization"></a>Initialisation du gestionnaire de symboles

Le gestionnaire de symboles est conçu pour effectuer le suivi de différents jeux de fichiers de symboles.

Pour initialiser le gestionnaire de symboles, appelez la fonction [**syminitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) . Le paramètre *hProcess* peut être un nombre arbitraire unique, une valeur retournée par la fonction [**GetCurrentProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getcurrentprocess) ou l’identificateur de tout processus en cours d’exécution. Le paramètre *fInvadeProcess* indique si le gestionnaire de symboles doit énumérer les modules chargés par le processus et charger des symboles pour chacun de ses modules. Si *fInvadeProcess* a la valeur **true**, le paramètre *hProcess* doit être la valeur retournée par **GetCurrentProcess** ou l’identificateur d’un processus existant. Pour actualiser cette liste, utilisez la fonction [**SymRefreshModuleList**](/windows/desktop/api/Dbghelp/nf-dbghelp-symrefreshmodulelist) .

L’utilisation de *fInvadeProcess* est un moyen simple de charger tous les fichiers de symboles d’un processus. Toutefois, le gestionnaire de symboles ne tente pas de charger les symboles pour les modules qui sont ensuite chargés par la fonction [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) . Dans ce cas, vous devez utiliser la fonction [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) .

 

 
