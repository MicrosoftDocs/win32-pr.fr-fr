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
ms.openlocfilehash: d6efa129182da256a6ce62b3754ea422df908248f7b0ecc30d3b690c29ffaf9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419659"
---
# <a name="process-walking"></a>Parcours du processus

Un instantané qui inclut la liste des processus contient des informations sur chaque processus en cours d’exécution. Vous pouvez récupérer des informations pour le premier processus de la liste à l’aide de la fonction [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) . Après avoir récupéré le premier processus de la liste, vous pouvez parcourir la liste des processus pour d’autres entrées à l’aide de la fonction [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) . **Process32First** et **Process32Next** remplissent une structure [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) avec les informations relatives à un processus de l’instantané. Pour obtenir un exemple, consultez la page création [d’un instantané et affichage des processus](taking-a-snapshot-and-viewing-processes.md).

Vous pouvez récupérer un code d’état d’erreur étendu pour [**Process32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first) et [**Process32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next) à l’aide de la fonction [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Vous pouvez lire la mémoire d’un processus spécifique dans une mémoire tampon à l’aide de la fonction [**Toolhelp32ReadProcessMemory**](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) (ou de la fonction [**VirtualQueryEx**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualqueryex) ).

> [!Note]  
> Le contenu des membres **th32ProcessID** et **th32ParentProcessID** de [**PROCESSENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-processentry32) sont des identificateurs de processus et peut être utilisé par toutes les fonctions qui requièrent un identificateur de processus.

 

 

 