---
title: Listes de tas et parcours du tas
description: Un instantané qui inclut la liste des tas pour un processus spécifié contient des informations d’identification pour chaque segment de mémoire associé au processus spécifié et des informations détaillées sur chaque segment.
ms.assetid: 631096fd-cb2c-4b19-aa71-d47060e2715c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87cc1eaa2093715e3f42fd52cc5191bedf5a0ac137cf93df57daa5ef590e2471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058227"
---
# <a name="heap-lists-and-heap-walking"></a>Listes de tas et parcours du tas

Un instantané qui inclut la liste des tas pour un processus spécifié contient des informations d’identification pour chaque segment de mémoire associé au processus spécifié et des informations détaillées sur chaque segment. Vous pouvez récupérer un identificateur pour le premier tas de la liste de tas à l’aide de la fonction [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) . Après avoir récupéré le premier segment de mémoire de la liste, vous pouvez parcourir la liste des tas pour les tas suivants associés au processus à l’aide de la fonction [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) . **Heap32ListFirst** et **Heap32ListNext** remplissent une structure [**HEAPLIST32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heaplist32) avec l’identificateur de processus, l’identificateur de tas et les indicateurs décrivant le tas.

Vous pouvez récupérer des informations sur le premier bloc d’un segment de mémoire à l’aide de la fonction [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) . Après avoir récupéré le premier bloc d’un segment de mémoire, vous pouvez récupérer des informations sur les blocs suivants du même tas à l’aide de la fonction [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) . **Heap32First** et **Heap32Next** remplissent une structure [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) avec des informations pour le bloc approprié d’un segment de mémoire.

Vous pouvez récupérer un code d’état d’erreur étendu pour [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst), [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext), [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)et [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) à l’aide de la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

> [!Note]  
> L’identificateur de segment de mémoire, qui est spécifié dans le membre **th32HeapID** de la structure [**HEAPENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-heapentry32) , a une signification uniquement pour les fonctions d’aide de l’outil. Ce n’est pas un descripteur et n’est pas utilisable par d’autres fonctions.

 

 

 