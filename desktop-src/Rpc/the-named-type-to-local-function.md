---
title: Fonction named_type_to_local
description: Les stubs appellent le \_ type nommé \_ à la \_ fonction locale pour convertir les données d’un type transmis vers le type qu’ils présentent à l’application.
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59fc1d45545c920ef19eb4c230045e62322833d3ef38e765357c29b20a48589c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924059"
---
# <a name="the-named_type_to_local-function"></a>Le \_ type nommé \_ vers la \_ fonction locale

Les stubs appellent **le \_ type nommé \_ à \_** la fonction locale pour convertir les données d’un type transmis vers le type qu’ils présentent à l’application. La fonction est définie comme suit :

``` syntax
void __RPC_USER <named_type>_to_local( 
    <named_type> __RPC_FAR * _RPC_FAR * , 
    <local_type> __RPC_FAR * );
```

Le premier paramètre pointe vers les données transmises. La fonction définit le deuxième paramètre pour qu’il pointe vers les données présentées.

Le **\_ type nommé \_ à \_** la fonction locale doit gérer la mémoire pour le type présenté. La fonction doit allouer de la mémoire pour l’ensemble de la structure de données qui commence à l’adresse indiquée par le deuxième paramètre, à l’exception du paramètre lui-même (le stub alloue de la mémoire pour le nœud racine et le transmet à la fonction). La valeur du deuxième paramètre ne peut pas changer pendant l’appel. La fonction peut modifier le contenu à cette adresse.

 

 




