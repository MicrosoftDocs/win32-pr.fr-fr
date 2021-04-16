---
description: Il existe diverses fonctions permettant d’obtenir des informations sur les processus.
ms.assetid: f9ec6aa5-15ad-47e6-b5f8-8ac4daaf178f
title: Obtention d’informations supplémentaires sur le processus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b90f7c68a89e2989c33c5f57a4e4fb5cead86a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529091"
---
# <a name="obtaining-additional-process-information"></a><span data-ttu-id="c0306-103">Obtention d’informations supplémentaires sur le processus</span><span class="sxs-lookup"><span data-stu-id="c0306-103">Obtaining Additional Process Information</span></span>

<span data-ttu-id="c0306-104">Il existe diverses fonctions permettant d’obtenir des informations sur les processus.</span><span class="sxs-lookup"><span data-stu-id="c0306-104">There are a variety of functions for obtaining information about processes.</span></span> <span data-ttu-id="c0306-105">Certaines de ces fonctions peuvent être utilisées uniquement pour le processus appelant, car elles ne prennent pas de handle de processus en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="c0306-105">Some of these functions can be used only for the calling process, because they do not take a process handle as a parameter.</span></span> <span data-ttu-id="c0306-106">Vous pouvez utiliser des fonctions qui prennent un handle de processus pour obtenir des informations sur d’autres processus.</span><span class="sxs-lookup"><span data-stu-id="c0306-106">You can use functions that take a process handle to obtain information about other processes.</span></span>

-   <span data-ttu-id="c0306-107">Pour obtenir la chaîne de ligne de commande pour le processus en cours, utilisez la fonction [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) .</span><span class="sxs-lookup"><span data-stu-id="c0306-107">To obtain the command-line string for the current process, use the [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) function.</span></span>
-   <span data-ttu-id="c0306-108">Pour récupérer la structure [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) spécifiée lors de la création du processus en cours, utilisez la fonction [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) .</span><span class="sxs-lookup"><span data-stu-id="c0306-108">To retrieve the [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure specified when the current process was created, use the [**GetStartupInfo**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getstartupinfow) function.</span></span>
-   <span data-ttu-id="c0306-109">Pour obtenir les informations de version à partir de l’en-tête de l’exécutable, utilisez la fonction [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) .</span><span class="sxs-lookup"><span data-stu-id="c0306-109">To obtain the version information from the executable header, use the [**GetProcessVersion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessversion) function.</span></span>
-   <span data-ttu-id="c0306-110">Pour obtenir le chemin d’accès complet et le nom de fichier du fichier exécutable contenant le code de processus, utilisez la fonction [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .</span><span class="sxs-lookup"><span data-stu-id="c0306-110">To obtain the full path and file name for the executable file containing the process code, use the [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function.</span></span>
-   <span data-ttu-id="c0306-111">Pour obtenir le nombre de descripteurs des objets de l’interface graphique utilisateur (GUI) en cours d’utilisation, utilisez la fonction [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) .</span><span class="sxs-lookup"><span data-stu-id="c0306-111">To obtain the count of handles to graphical user interface (GUI) objects in use, use the [**GetGuiResources**](/windows/desktop/api/Winuser/nf-winuser-getguiresources) function.</span></span>
-   <span data-ttu-id="c0306-112">Pour déterminer si un processus est en cours de débogage, utilisez la fonction [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) .</span><span class="sxs-lookup"><span data-stu-id="c0306-112">To determine whether a process is being debugged, use the [**IsDebuggerPresent**](/windows/win32/api/debugapi/nf-debugapi-isdebuggerpresent) function.</span></span>
-   <span data-ttu-id="c0306-113">Pour récupérer des informations de gestion de comptes pour toutes les opérations d’e/s effectuées par le processus, utilisez la fonction [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) .</span><span class="sxs-lookup"><span data-stu-id="c0306-113">To retrieve accounting information for all I/O operations performed by the process, use the [**GetProcessIoCounters**](/windows/desktop/api/WinBase/nf-winbase-getprocessiocounters) function.</span></span>

 

 
