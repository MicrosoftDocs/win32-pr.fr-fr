---
description: Contrôle des graphiques de filtre à l’aide de C
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: Contrôle des graphiques de filtre à l’aide de C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e234413f7642d7349c2bf378d1aded97b399e252117b0793f90335de8643912e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073753"
---
# <a name="controlling-filter-graphs-using-c"></a>Contrôle des graphiques de filtre à l’aide de C

si vous écrivez une application DirectShow en C (plutôt que C++), vous devez utiliser un pointeur vtable pour appeler des méthodes. L’exemple suivant illustre l’appel de la méthode **IUnknown :: QueryInterface** à partir d’une application écrite en C :


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



L’exemple suivant illustre l’appel équivalent en C++ :


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



En C, les interfaces COM sont définies en tant que structures. Le membre **lpVtbl** est un pointeur vers une table de méthodes d’interface (vtable). Toutes les méthodes prennent un paramètre supplémentaire, qui est un pointeur vers l’interface.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Annexes](appendixes.md)
</dt> </dl>

 

 



