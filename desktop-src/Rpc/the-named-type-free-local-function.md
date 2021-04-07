---
title: Fonction named_type_free_local
description: Les stubs appellent la \_ \_ fonction locale Free de type pour libérer la mémoire allouée par un appel au \_ type nommé à la \_ \_ routine locale.
ms.assetid: 8e8c6a46-20c1-483b-b804-0772391e9918
keywords:
- named_type_free_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f2796f33e9dc60364b6afda244d8dae47eef0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672258"
---
# <a name="the-named_type_free_local-function"></a>\_ \_ Fonction locale Free de type nommé \_

Les stubs appellent la fonction **\_ \_ locale Free de type** pour libérer la mémoire allouée par un appel au [type nommé à la routine \_ \_ \_ locale](the-named-type-to-local-function.md) . Elle ne libère pas la mémoire allouée par le stub. Le prototype de fonction est défini comme suit :

``` syntax
void __RPC_USER <local_type>_free_local(<named_type> __RPC_FAR *);
```

Le paramètre est un pointeur vers la mémoire allouée par le **\_ type nommé \_ à \_ local**.

 

 




