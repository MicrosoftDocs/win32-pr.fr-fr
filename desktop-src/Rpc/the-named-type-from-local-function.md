---
title: Fonction named_type_from_local
description: Les stubs appellent le \_ type nommé \_ à partir de la \_ fonction locale.
ms.assetid: ba35e2fb-957e-4e62-b0d4-ae76e30fa343
keywords:
- named_type_from_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94606a197f3763770db8e0d455a9d0b09f5dab0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309602"
---
# <a name="the-named_type_from_local-function"></a>Type nommé \_ \_ à partir de la \_ fonction locale

Les stubs appellent le \_ type nommé \_ à partir de la \_ fonction locale. Il convertit le type que l’application utilise dans le type transmis par les stubs sur le réseau. La fonction est définie comme suit :

``` syntax
void __RPC_USER <named_type>_from_local ( 
    <local_type> __RPC_FAR *, <named_type> __RPC_FAR * __RPC_FAR *);
```

Le premier paramètre est un pointeur vers les données d’application. Le deuxième paramètre est un pointeur vers un pointeur. La fonction pointe vers les données transmises. La fonction doit allouer de la mémoire pour le type transmis.

 

 




