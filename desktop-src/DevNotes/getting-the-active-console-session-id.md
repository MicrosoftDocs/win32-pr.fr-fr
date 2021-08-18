---
description: La définition winternl. h suivante est l’adresse mémoire statique de l’ID de session active des services Terminal Server. cet ID de session de la console active n’est pas défini dans les versions du système d’exploitation Microsoft Windows antérieures à Windows XP.
ms.assetid: f3022ab8-60ea-490b-a87d-cc1afc99d26f
title: Obtention de l’ID de session de la console active
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f7b23669240f0cd109a48f454ee6f6329f6839221a1677e81b75712430cb42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002299"
---
# <a name="getting-the-active-console-session-id"></a>Obtention de l’ID de session de la console active

La définition winternl. h suivante est l’adresse mémoire statique de l’ID de session active des services Terminal Server. cet ID de session de la console active n’est pas défini dans les versions du système d’exploitation Microsoft Windows antérieures à Windows XP.

> [!Note]  
> Cette définition peut changer dans les versions ultérieures de Windows. Pour vous assurer que votre application continuera à s’exécuter correctement à l’avenir, votre application doit appeler [**WTSGetActiveConsoleSessionId**](/windows/win32/api/winbase/nf-winbase-wtsgetactiveconsolesessionid).

 

``` syntax
#define INTERNAL_TS_ACTIVE_CONSOLE_ID    
        (*((volatile ULONG*)(0x7ffe02d8)))
```

 

 
