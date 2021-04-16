---
title: Parcours du processus
description: Un instantané qui inclut la liste des processus contient des informations sur chaque processus en cours d’exécution.
ms.assetid: 4fb55763-2206-48ad-8b1f-ed2c33b6f56b
keywords:
- énumérer
- énumération, processus
- processus
- processus, énumération des processus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc95f0de4021ce3c355286376decbdecef2c883
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463362"
---
# <a name="process-walking"></a><span data-ttu-id="2de3a-107">Parcours du processus</span><span class="sxs-lookup"><span data-stu-id="2de3a-107">Process Walking</span></span>

<span data-ttu-id="2de3a-108">Un instantané qui inclut la liste des processus contient des informations sur chaque processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2de3a-108">A snapshot that includes the process list contains information about each currently executing process.</span></span> <span data-ttu-id="2de3a-109">Vous pouvez récupérer des informations pour le premier processus de la liste à l’aide de la fonction [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) .</span><span class="sxs-lookup"><span data-stu-id="2de3a-109">You can retrieve information for the first process in the list by using the [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) function.</span></span> <span data-ttu-id="2de3a-110">Après avoir récupéré le premier processus de la liste, vous pouvez parcourir la liste des processus pour d’autres entrées à l’aide de la fonction [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) .</span><span class="sxs-lookup"><span data-stu-id="2de3a-110">After retrieving the first process in the list, you can traverse the process list for subsequent entries by using the [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) function.</span></span> <span data-ttu-id="2de3a-111">**Process32First** et **Process32Next** remplissent une structure [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) avec les informations relatives à un processus de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="2de3a-111">**Process32First** and **Process32Next** fill a [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) structure with information about a process in the snapshot.</span></span> <span data-ttu-id="2de3a-112">Pour obtenir un exemple, consultez la page création [d’un instantané et affichage des processus](taking-a-snapshot-and-viewing-processes.md).</span><span class="sxs-lookup"><span data-stu-id="2de3a-112">For an example, see [Taking a Snapshot and Viewing Processes](taking-a-snapshot-and-viewing-processes.md).</span></span>

<span data-ttu-id="2de3a-113">Vous pouvez récupérer un code d’état d’erreur étendu pour [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) et [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) à l’aide de la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="2de3a-113">You can retrieve an extended error status code for [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) and [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="2de3a-114">Vous pouvez lire la mémoire d’un processus spécifique dans une mémoire tampon à l’aide de la fonction [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) (ou de la fonction [**VirtualQueryEx**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) ).</span><span class="sxs-lookup"><span data-stu-id="2de3a-114">You can read the memory in a specific process into a buffer by using the [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) function (or the [**VirtualQueryEx**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) function).</span></span>

> [!Note]  
> <span data-ttu-id="2de3a-115">Le contenu des membres **th32ProcessID** et **th32ParentProcessID** de [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) sont des identificateurs de processus et peut être utilisé par toutes les fonctions qui requièrent un identificateur de processus.</span><span class="sxs-lookup"><span data-stu-id="2de3a-115">The contents of the **th32ProcessID** and **th32ParentProcessID** members of [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) are process identifiers and can be used by any functions that require a process identifier.</span></span>

 

 

 