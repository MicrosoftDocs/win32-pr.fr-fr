---
title: Fonction named_type_free_inst
description: Les stubs appellent le \_ type nommé \_ Free \_ inst fonction pour libérer de la mémoire associée au type transmis.
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2d3b5103572eb58e4311c65b0e1cff02e91f66f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672261"
---
# <a name="the-named_type_free_inst-function"></a>Le \_ type nommé \_ Free \_ inst, fonction

Les stubs appellent **le \_ type nommé \_ Free \_ inst** fonction pour libérer de la mémoire associée au type transmis. La fonction est définie comme suit :

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

Le paramètre pointe vers l’instance du type transmis. Cet objet ne doit pas être libéré. Pour plus d’informations sur l’appel de la fonction, consultez [l' \_ attribut « représenter comme](the-represent-as-attribute.md)».

 

 




