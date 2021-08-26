---
title: Fonction named_type_from_local
description: Les stubs appellent le \_ type nommé \_ à partir de la \_ fonction locale.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c294398913a3bf6fe8b88eed5c42ceec84abf6b23ed994c85ff0fae8f21f2e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127619"
---
# <a name="the-named_type_from_local-function"></a>Type nommé \_ \_ à partir de la \_ fonction locale

Les stubs appellent le \_ type nommé \_ à partir de la \_ fonction locale. Il convertit le type que l’application utilise dans le type transmis par les stubs sur le réseau. La fonction est définie comme suit :

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

Le premier paramètre est un pointeur vers les données d’application. Le deuxième paramètre est un pointeur vers un pointeur. La fonction pointe vers les données transmises. La fonction doit allouer de la mémoire pour le type transmis.

 

 




