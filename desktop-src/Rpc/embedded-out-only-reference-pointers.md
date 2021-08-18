---
title: Pointeurs de référence Out-Only incorporés
description: Pointeurs de référence Out-Only incorporés
ms.assetid: b0fcba9e-b285-4d29-9ffc-c8d6d7818824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d36fc6229c0b155e3fa9a7f66e6cd1fbd742d7ec876264a8706ce81c4150d6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930519"
---
# <a name="embedded-out-only-reference-pointers"></a>Pointeurs de référence Out-Only incorporés

Lorsque vous utilisez des \[ [](/windows/desktop/Midl/out-idl) \] pointeurs de référence en sortie seule dans Microsoft RPC, les stubs de serveur générés allouent uniquement le premier niveau des pointeurs accessibles à partir du pointeur de référence. Les pointeurs à des niveaux plus profonds ne sont pas alloués par les stubs, mais doivent être alloués par la couche d’application serveur. Par exemple, supposons qu’une interface spécifie un \[  \] tableau en dehors des pointeurs de référence :

``` syntax
/* IDL file (fragment) */
typedef [ref] short * PREF;

Proc1([out] PREF array[10]);
```

Dans cet exemple, le stub serveur alloue de la mémoire pour 10 pointeurs et définit la valeur de chaque pointeur sur null. L’application serveur doit allouer la mémoire pour les 10 entiers [**courts**](/windows/desktop/Midl/short) référencés par les pointeurs, puis définir les 10 pointeurs pour qu’ils pointent vers les entiers.

Lorsque la \[ [](/windows/desktop/Midl/out-idl) \] structure de données en sortie seule comprend des pointeurs de référence imbriqués, les stubs de serveur allouent uniquement le premier pointeur accessible à partir du pointeur de référence. Par exemple :

``` syntax
/* IDL file (fragment) */
typedef struct 
{
    [ref] small * psValue;
} STRUCT1_TYPE;

typedef struct 
{
    [ref] STRUCT1_TYPE * ps1;
} STRUCT_TOP_TYPE;

Proc2([out, ref] STRUCT_TOP_TYPE * psTop);
```

Dans l’exemple précédent, les stubs de serveur allouent le pointeur *psTop* et le **\_ \_ type struct** de structure. Le point de référence *ps1* dans le type de la **\_ partie \_ supérieure** de la structure a la valeur null. Le stub serveur n’alloue pas tous les niveaux de la structure de données, ni n’alloue le **\_ type STRUCT1** ou son pointeur incorporé, *psValue*.

 

 