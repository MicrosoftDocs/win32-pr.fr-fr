---
description: Une page de garde fournit une alarme pour l’accès à la page mémoire.
ms.assetid: 763bc763-e178-481e-a81a-c15715e56901
title: Création de pages de garde
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee4d4a44a6e64d6af81e4b847347f357c3590edbd7e6b806e8f32653e1f869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963289"
---
# <a name="creating-guard-pages"></a>Création de pages de garde

Une page de garde fournit une alarme pour l’accès à la page mémoire. Cela peut être utile pour une application qui doit surveiller la croissance de grandes structures de données dynamiques. Par exemple, certains systèmes d’exploitation utilisent des pages de garde pour implémenter la vérification de pile automatique.

Pour créer une page de garde, définissez le modificateur de protection de page **page \_ Guard** pour la page. Cette valeur peut être spécifiée, ainsi que d’autres modificateurs de protection de page, dans les fonctions [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc), [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex), [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect)et [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) . Le modificateur **page \_ Guard** peut être utilisé avec d’autres modificateurs de protection de page, à l’exception de la **page \_ NoAccess**.

Si un programme tente d’accéder à une adresse au sein d’une page de garde, le système déclenche une exception de **\_ \_ \_ violation de page d’État** (0x80000001). Le système efface également le modificateur de **\_ garde de page** , en supprimant l’état de la page de garde de la page mémoire. Le système n’arrêtera pas la prochaine tentative d’accès à la page de mémoire avec une exception de **\_ violation de \_ page \_ Status Guard** .

Si une exception de page de garde se produit pendant un service système, le service échoue et retourne généralement un indicateur d’état d’échec. Étant donné que le système supprime également l’état de la page de garde de la page de mémoire appropriée, l’appel suivant du même service système n’échoue pas en raison d’une exception de **\_ violation de \_ page \_ Status Guard** (sauf si, bien sûr, quelqu’un rétablit la page de garde).

Le petit programme suivant illustre le comportement de la protection de la page Guard.


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



La première tentative de verrouillage du bloc de mémoire échoue, déclenchant une exception de **\_ violation de \_ page \_ Status Guard** . La deuxième tentative réussit, car la protection de la page de garde du bloc de mémoire a été désactivée à la première tentative.

 

 
