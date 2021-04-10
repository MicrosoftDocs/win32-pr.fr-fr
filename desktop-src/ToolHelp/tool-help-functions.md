---
title: Fonctions d’aide de l’outil
description: Répertorie les fonctions de la bibliothèque d’aide de l’outil.
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f9d95598f9b48343ea9731e1a826fb147a73a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029715"
---
# <a name="tool-help-functions"></a><span data-ttu-id="73267-103">Fonctions d’aide de l’outil</span><span class="sxs-lookup"><span data-stu-id="73267-103">Tool Help Functions</span></span>

<span data-ttu-id="73267-104">Les fonctions suivantes font partie de la bibliothèque d’aide d’outils.</span><span class="sxs-lookup"><span data-stu-id="73267-104">The following functions are part of the tool help library.</span></span>



| <span data-ttu-id="73267-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="73267-105">Function</span></span>                                                           | <span data-ttu-id="73267-106">Description</span><span class="sxs-lookup"><span data-stu-id="73267-106">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="73267-107">**CreateToolhelp32Snapshot**</span><span class="sxs-lookup"><span data-stu-id="73267-107">**CreateToolhelp32Snapshot**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | <span data-ttu-id="73267-108">Prend un instantané des processus spécifiés, ainsi que les tas, les modules et les threads utilisés par ces processus.</span><span class="sxs-lookup"><span data-stu-id="73267-108">Takes a snapshot of the specified processes, as well as the heaps, modules, and threads used by these processes.</span></span> |
| [<span data-ttu-id="73267-109">**Heap32First**</span><span class="sxs-lookup"><span data-stu-id="73267-109">**Heap32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | <span data-ttu-id="73267-110">Récupère des informations sur le premier bloc d’un segment de mémoire qui a été alloué par un processus.</span><span class="sxs-lookup"><span data-stu-id="73267-110">Retrieves information about the first block of a heap that has been allocated by a process.</span></span>                      |
| [<span data-ttu-id="73267-111">**Heap32ListFirst**</span><span class="sxs-lookup"><span data-stu-id="73267-111">**Heap32ListFirst**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | <span data-ttu-id="73267-112">Récupère des informations sur le premier segment de mémoire qui a été alloué par un processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="73267-112">Retrieves information about the first heap that has been allocated by a specified process.</span></span>                       |
| [<span data-ttu-id="73267-113">**Heap32ListNext**</span><span class="sxs-lookup"><span data-stu-id="73267-113">**Heap32ListNext**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | <span data-ttu-id="73267-114">Récupère des informations sur le segment de mémoire suivant qui a été alloué par un processus.</span><span class="sxs-lookup"><span data-stu-id="73267-114">Retrieves information about the next heap that has been allocated by a process.</span></span>                                  |
| [<span data-ttu-id="73267-115">**Heap32Next**</span><span class="sxs-lookup"><span data-stu-id="73267-115">**Heap32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | <span data-ttu-id="73267-116">Récupère des informations sur le bloc suivant d’un segment de mémoire qui a été alloué par un processus.</span><span class="sxs-lookup"><span data-stu-id="73267-116">Retrieves information about the next block of a heap that has been allocated by a process.</span></span>                       |
| [<span data-ttu-id="73267-117">**Module32First**</span><span class="sxs-lookup"><span data-stu-id="73267-117">**Module32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | <span data-ttu-id="73267-118">Récupère des informations sur le premier module associé à un processus.</span><span class="sxs-lookup"><span data-stu-id="73267-118">Retrieves information about the first module associated with a process.</span></span>                                          |
| [<span data-ttu-id="73267-119">**Module32Next**</span><span class="sxs-lookup"><span data-stu-id="73267-119">**Module32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | <span data-ttu-id="73267-120">Récupère des informations sur le module suivant associé à un processus ou à un thread.</span><span class="sxs-lookup"><span data-stu-id="73267-120">Retrieves information about the next module associated with a process or thread.</span></span>                                 |
| [<span data-ttu-id="73267-121">**Process32First**</span><span class="sxs-lookup"><span data-stu-id="73267-121">**Process32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | <span data-ttu-id="73267-122">Récupère des informations sur le premier processus rencontré dans un instantané système.</span><span class="sxs-lookup"><span data-stu-id="73267-122">Retrieves information about the first process encountered in a system snapshot.</span></span>                                  |
| [<span data-ttu-id="73267-123">**Process32Next**</span><span class="sxs-lookup"><span data-stu-id="73267-123">**Process32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | <span data-ttu-id="73267-124">Récupère des informations sur le processus suivant enregistré dans un instantané système.</span><span class="sxs-lookup"><span data-stu-id="73267-124">Retrieves information about the next process recorded in a system snapshot.</span></span>                                      |
| [<span data-ttu-id="73267-125">**Thread32First**</span><span class="sxs-lookup"><span data-stu-id="73267-125">**Thread32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | <span data-ttu-id="73267-126">Récupère des informations sur le premier thread d’un processus rencontré dans un instantané système.</span><span class="sxs-lookup"><span data-stu-id="73267-126">Retrieves information about the first thread of any process encountered in a system snapshot.</span></span>                    |
| [<span data-ttu-id="73267-127">**Thread32Next**</span><span class="sxs-lookup"><span data-stu-id="73267-127">**Thread32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | <span data-ttu-id="73267-128">Récupère des informations sur le thread suivant d’un processus rencontré dans l’instantané de la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="73267-128">Retrieves information about the next thread of any process encountered in the system memory snapshot.</span></span>            |
| [<span data-ttu-id="73267-129">**Toolhelp32ReadProcessMemory**</span><span class="sxs-lookup"><span data-stu-id="73267-129">**Toolhelp32ReadProcessMemory**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | <span data-ttu-id="73267-130">Copie la mémoire allouée à un autre processus dans une mémoire tampon fournie par l’application.</span><span class="sxs-lookup"><span data-stu-id="73267-130">Copies memory allocated to another process into an application-supplied buffer.</span></span>                                  |



 

 

 




