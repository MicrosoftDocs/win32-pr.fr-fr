---
title: Fonction named_type_free_local
description: Les stubs appellent la \_ \_ fonction locale Free de type pour libérer la mémoire allouée par un appel au \_ type nommé à la \_ \_ routine locale.
ms.assetid: 8e8c6a46-20c1-483b-b804-0772391e9918
keywords:
- named_type_free_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 123e0eb12a187ee6a5b7665ec126ba98153638e9d766015a0c9e7b1c7aec7dee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924079"
---
# <a name="the-named_type_free_local-function"></a>\_ \_ Fonction locale Free de type nommé \_

Les stubs appellent la fonction **\_ \_ locale Free de type** pour libérer la mémoire allouée par un appel au [type nommé à la routine \_ \_ \_ locale](the-named-type-to-local-function.md) . Elle ne libère pas la mémoire allouée par le stub. Le prototype de fonction est défini comme suit :

``` syntax
void __RPC_USER <local_type>_free_local(<named_type> __RPC_FAR *);
```

Le paramètre est un pointeur vers la mémoire allouée par le **\_ type nommé \_ à \_ local**.

 

 




