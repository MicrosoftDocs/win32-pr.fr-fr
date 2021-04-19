---
title: Parcours du thread
description: Un instantané qui inclut la liste des threads contient des informations sur chaque thread de chaque processus en cours d’exécution.
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- énumérer
- énumération, threads
- threads
- threads, énumération des threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32eff584aedaa3f6124cc358a4ee9d2a94962843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510481"
---
# <a name="thread-walking"></a><span data-ttu-id="f9bec-107">Parcours du thread</span><span class="sxs-lookup"><span data-stu-id="f9bec-107">Thread Walking</span></span>

<span data-ttu-id="f9bec-108">Un instantané qui inclut la liste des threads contient des informations sur chaque thread de chaque processus en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f9bec-108">A snapshot that includes the thread list contains information about each thread of each currently executing process.</span></span> <span data-ttu-id="f9bec-109">Vous pouvez récupérer des informations pour le premier thread de la liste à l’aide de la fonction [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) .</span><span class="sxs-lookup"><span data-stu-id="f9bec-109">You can retrieve information for the first thread in the list by using the [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) function.</span></span> <span data-ttu-id="f9bec-110">Après avoir récupéré le premier thread de la liste, vous pouvez récupérer des informations pour les threads suivants à l’aide de la fonction [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) .</span><span class="sxs-lookup"><span data-stu-id="f9bec-110">After retrieving the first thread in the list, you can retrieve information for subsequent threads by using the [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) function.</span></span> <span data-ttu-id="f9bec-111">**Thread32First** et **Thread32Next** remplissent une structure [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) avec des informations sur les threads individuels de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="f9bec-111">**Thread32First** and **Thread32Next** fill a [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) structure with information about individual threads in the snapshot.</span></span>

<span data-ttu-id="f9bec-112">Vous pouvez énumérer les threads d’un processus spécifique en prenant un instantané qui comprend les threads, puis en parcourant la liste des threads, en conservant les informations sur les threads qui ont le même identificateur de processus que le processus spécifié.</span><span class="sxs-lookup"><span data-stu-id="f9bec-112">You can enumerate the threads of a specific process by taking a snapshot that includes the threads and then by traversing the thread list, keeping information about the threads that have the same process identifier as the specified process.</span></span>

<span data-ttu-id="f9bec-113">Vous pouvez récupérer un code d’état d’erreur étendu pour [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) et [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) à l’aide de la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="f9bec-113">You can retrieve an extended error status code for [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) and [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

> [!Note]  
> <span data-ttu-id="f9bec-114">Le contenu du membre **th32ThreadID** de [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) est un identificateur de thread et peut être utilisé par toutes les fonctions qui requièrent un identificateur de thread.</span><span class="sxs-lookup"><span data-stu-id="f9bec-114">The contents of the **th32ThreadID** member of [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) is a thread identifier and can be used by any functions that require a thread identifier.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f9bec-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f9bec-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9bec-116">Parcours de la liste des threads</span><span class="sxs-lookup"><span data-stu-id="f9bec-116">Traversing the Thread List</span></span>](traversing-the-thread-list.md)
</dt> </dl>

 

 