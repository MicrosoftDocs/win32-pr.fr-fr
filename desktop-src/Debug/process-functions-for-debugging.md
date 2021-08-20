---
description: La fonction CreateProcess permet à un débogueur de démarrer un processus et de le déboguer.
ms.assetid: 7056e181-9bc5-4530-a7b8-d5ff1e345eef
title: Traiter les fonctions pour le débogage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6dec70de05e9b77cd3ff0b2ee8cd01c90ded2987f7ba1cacc3530f040344915
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162630"
---
# <a name="process-functions-for-debugging"></a>Traiter les fonctions pour le débogage

La fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) permet à un débogueur de démarrer un processus et de le déboguer. Le paramètre *fdwCreate* de **CreateProcess** est utilisé pour spécifier le type d’opération de débogage. Si l' \_ indicateur de processus de débogage est spécifié pour le paramètre, un débogueur débogue le nouveau processus et tous les descendants du processus, à condition que les descendants soient créés sans l’indicateur de processus de débogage \_ .

Si le processus de débogage \_ et DÉboguer \_ uniquement \_ ces \_ indicateurs de processus sont spécifiés pour *fdwCreate*, un débogueur débogue le nouveau processus, mais aucun de ses descendants.

Un débogueur peut déboguer un autre en créant un processus avec l’indicateur de processus de débogage \_ . Le nouveau processus (le débogueur en cours de débogage) doit ensuite créer un processus avec l’indicateur de processus de débogage \_ .

La fonction [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) permet à un débogueur d’obtenir l’identificateur d’un processus existant. (La fonction [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) utilise cet identificateur pour attacher le débogueur au processus.) En règle générale, les débogueurs ouvrent un processus avec les \_ \_ indicateurs de lecture et de traitement des ordinateurs \_ virtuels \_ . L’utilisation de ces indicateurs permet au débogueur de lire et d’écrire dans la mémoire virtuelle du processus à l’aide des fonctions [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) et [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) . Pour plus d’informations, consultez [**processus et threads**](../procthread/processes-and-threads.md).

 

 
