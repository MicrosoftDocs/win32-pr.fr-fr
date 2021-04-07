---
title: Fonction named_type_to_local
description: Les stubs appellent le \_ type nommé \_ à la \_ fonction locale pour convertir les données d’un type transmis vers le type qu’ils présentent à l’application.
ms.assetid: c272cc1f-e47b-4d5a-a4e2-cefeaeb8c175
keywords:
- named_type_to_local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 746cbdd01ea657408b1bf355f41b3b9dfba673a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029209"
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

 

 




