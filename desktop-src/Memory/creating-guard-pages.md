---
description: Une page de garde fournit une alarme pour l’accès à la page mémoire.
ms.assetid: 763bc763-e178-481e-a81a-c15715e56901
title: Création de pages de garde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10768da75090a28ffecd5302d88dbc142ae9c147
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543457"
---
# <a name="creating-guard-pages"></a><span data-ttu-id="caf94-103">Création de pages de garde</span><span class="sxs-lookup"><span data-stu-id="caf94-103">Creating Guard Pages</span></span>

<span data-ttu-id="caf94-104">Une page de garde fournit une alarme pour l’accès à la page mémoire.</span><span class="sxs-lookup"><span data-stu-id="caf94-104">A guard page provides a one-shot alarm for memory page access.</span></span> <span data-ttu-id="caf94-105">Cela peut être utile pour une application qui doit surveiller la croissance de grandes structures de données dynamiques.</span><span class="sxs-lookup"><span data-stu-id="caf94-105">This can be useful for an application that needs to monitor the growth of large dynamic data structures.</span></span> <span data-ttu-id="caf94-106">Par exemple, certains systèmes d’exploitation utilisent des pages de garde pour implémenter la vérification de pile automatique.</span><span class="sxs-lookup"><span data-stu-id="caf94-106">For example, there are operating systems that use guard pages to implement automatic stack checking.</span></span>

<span data-ttu-id="caf94-107">Pour créer une page de garde, définissez le modificateur de protection de page **page \_ Guard** pour la page.</span><span class="sxs-lookup"><span data-stu-id="caf94-107">To create a guard page, set the **PAGE\_GUARD** page protection modifier for the page.</span></span> <span data-ttu-id="caf94-108">Cette valeur peut être spécifiée, ainsi que d’autres modificateurs de protection de page, dans les fonctions [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex), [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)et [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) .</span><span class="sxs-lookup"><span data-stu-id="caf94-108">This value can be specified, along with other page protection modifiers, in the [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex), [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect), and [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) functions.</span></span> <span data-ttu-id="caf94-109">Le modificateur **page \_ Guard** peut être utilisé avec d’autres modificateurs de protection de page, à l’exception de la **page \_ NoAccess**.</span><span class="sxs-lookup"><span data-stu-id="caf94-109">The **PAGE\_GUARD** modifier can be used with any other page protection modifiers, except **PAGE\_NOACCESS**.</span></span>

<span data-ttu-id="caf94-110">Si un programme tente d’accéder à une adresse au sein d’une page de garde, le système déclenche une exception de **\_ \_ \_ violation de page d’État** (0x80000001).</span><span class="sxs-lookup"><span data-stu-id="caf94-110">If a program attempts to access an address within a guard page, the system raises a **STATUS\_GUARD\_PAGE\_VIOLATION** (0x80000001) exception.</span></span> <span data-ttu-id="caf94-111">Le système efface également le modificateur de **\_ garde de page** , en supprimant l’état de la page de garde de la page mémoire.</span><span class="sxs-lookup"><span data-stu-id="caf94-111">The system also clears the **PAGE\_GUARD** modifier, removing the memory page's guard page status.</span></span> <span data-ttu-id="caf94-112">Le système n’arrêtera pas la prochaine tentative d’accès à la page de mémoire avec une exception de **\_ violation de \_ page \_ Status Guard** .</span><span class="sxs-lookup"><span data-stu-id="caf94-112">The system will not stop the next attempt to access the memory page with a **STATUS\_GUARD\_PAGE\_VIOLATION** exception.</span></span>

<span data-ttu-id="caf94-113">Si une exception de page de garde se produit pendant un service système, le service échoue et retourne généralement un indicateur d’état d’échec.</span><span class="sxs-lookup"><span data-stu-id="caf94-113">If a guard page exception occurs during a system service, the service fails and typically returns some failure status indicator.</span></span> <span data-ttu-id="caf94-114">Étant donné que le système supprime également l’état de la page de garde de la page de mémoire appropriée, l’appel suivant du même service système n’échoue pas en raison d’une exception de **\_ violation de \_ page \_ Status Guard** (sauf si, bien sûr, quelqu’un rétablit la page de garde).</span><span class="sxs-lookup"><span data-stu-id="caf94-114">Since the system also removes the relevant memory page's guard page status, the next invocation of the same system service won't fail due to a **STATUS\_GUARD\_PAGE\_VIOLATION** exception (unless, of course, someone reestablishes the guard page).</span></span>

<span data-ttu-id="caf94-115">Le petit programme suivant illustre le comportement de la protection de la page Guard.</span><span class="sxs-lookup"><span data-stu-id="caf94-115">The following short program illustrates the behavior of guard page protection.</span></span>


```C++
/* A program to demonstrate the use of guard pages of memory. Allocate
   a page of memory as a guard page, then try to access the page. That
   will fail, but doing so releases the lock on the guard page, so the
   next access works correctly.

   The output will look like this. The actual address may vary.

   This computer has a page size of 4096.
   Committed 4096 bytes at address 0x00520000
   Cannot lock at 00520000, error = 0x80000001
   2nd Lock Achieved at 00520000

   This sample does not show how to use the guard page fault to
   "grow" a dynamic array, such as a stack. */

#include <windows.h>
#include <stdio.h>
#include <stdlib.h>
#include <tchar.h>

int main()
{
  LPVOID lpvAddr;               // address of the test memory
  DWORD dwPageSize;             // amount of memory to allocate.
  BOOL bLocked;                 // address of the guarded memory
  SYSTEM_INFO sSysInfo;         // useful information about the system

  GetSystemInfo(&sSysInfo);     // initialize the structure

  _tprintf(TEXT("This computer has page size %d.\n"), sSysInfo.dwPageSize);

  dwPageSize = sSysInfo.dwPageSize;

  // Try to allocate the memory.

  lpvAddr = VirtualAlloc(NULL, dwPageSize,
                         MEM_RESERVE | MEM_COMMIT,
                         PAGE_READONLY | PAGE_GUARD);

  if(lpvAddr == NULL) {
    _tprintf(TEXT("VirtualAlloc failed. Error: %ld\n"),
             GetLastError());
    return 1;

  } else {
    _ftprintf(stderr, TEXT("Committed %lu bytes at address 0x%lp\n"),
              dwPageSize, lpvAddr);
  }

  // Try to lock the committed memory. This fails the first time 
  // because of the guard page.

  bLocked = VirtualLock(lpvAddr, dwPageSize);
  if (!bLocked) {
    _ftprintf(stderr, TEXT("Cannot lock at %lp, error = 0x%lx\n"),
              lpvAddr, GetLastError());
  } else {
    _ftprintf(stderr, TEXT("Lock Achieved at %lp\n"), lpvAddr);
  }

  // Try to lock the committed memory again. This succeeds the second
  // time because the guard page status was removed by the first 
  // access attempt.

  bLocked = VirtualLock(lpvAddr, dwPageSize);

  if (!bLocked) {
    _ftprintf(stderr, TEXT("Cannot get 2nd lock at %lp, error = %lx\n"),
              lpvAddr, GetLastError());
  } else {
    _ftprintf(stderr, TEXT("2nd Lock Achieved at %lp\n"), lpvAddr);
  }

  return 0;
}
```



<span data-ttu-id="caf94-116">La première tentative de verrouillage du bloc de mémoire échoue, déclenchant une exception de **\_ violation de \_ page \_ Status Guard** .</span><span class="sxs-lookup"><span data-stu-id="caf94-116">The first attempt to lock the memory block fails, raising a **STATUS\_GUARD\_PAGE\_VIOLATION** exception.</span></span> <span data-ttu-id="caf94-117">La deuxième tentative réussit, car la protection de la page de garde du bloc de mémoire a été désactivée à la première tentative.</span><span class="sxs-lookup"><span data-stu-id="caf94-117">The second attempt succeeds, because the memory block's guard page protection has been toggled off by the first attempt.</span></span>

 

 
