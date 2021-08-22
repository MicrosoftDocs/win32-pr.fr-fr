---
description: Le code suivant décharge un module de symboles référencé par l’adresse du module BaseOfDll à l’aide de SymUnloadModule64.
ms.assetid: f185ae64-1de9-4139-acd5-7c3a108e1eba
title: Déchargement d’un module de symboles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0da437fe0ce188e3559280d2bc347f3b976aba52adbf8e4a0306e4e469747435
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929279"
---
# <a name="unloading-a-symbol-module"></a>Déchargement d’un module de symboles

Le code suivant décharge un module de symboles référencé par l’adresse du module BaseOfDll à l’aide de [**SymUnloadModule64**](/windows/desktop/api/Dbghelp/nf-dbghelp-symunloadmodule).


```C++
if (SymUnloadModule64(hProcess, BaseOfDll))
{
    // SymUnloadModule64 returned success
}
else
{
    // SymUnloadModule64 failed
    DWORD error = GetLastError();
    printf("SymUnloadModule64 returned error : %d\n", error);
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Chargement d’un module de symboles](loading-a-symbol-module.md)
</dt> </dl>

 

 



