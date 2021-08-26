---
title: Fonction named_type_free_inst
description: Les stubs appellent le \_ type nommé \_ Free \_ inst fonction pour libérer de la mémoire associée au type transmis.
ms.assetid: 4b9e10cb-25bb-4f00-86a0-5436e5ac71d9
keywords:
- named_type_free_inst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aa55e896b89fccc513795a62634e805c2ad6e21b7bdecdd99a0b9cfe2d71cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120016888"
---
# <a name="the-named_type_free_inst-function"></a>Le \_ type nommé \_ Free \_ inst, fonction

Les stubs appellent **le \_ type nommé \_ Free \_ inst** fonction pour libérer de la mémoire associée au type transmis. La fonction est définie comme suit :

``` syntax
void __RPC_USER <named_type>_free_inst(<type> __RPC_FAR *)
```

Le paramètre pointe vers l’instance du type transmis. Cet objet ne doit pas être libéré. Pour plus d’informations sur l’appel de la fonction, consultez [l' \_ attribut « représenter comme](the-represent-as-attribute.md)».

 

 




