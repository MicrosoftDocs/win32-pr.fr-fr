---
title: attribut midl_user_free
description: La \_ fonction gratuite de l’utilisateur MIDL \_ est fournie par les applications client et serveur pour libérer de la mémoire allouée dynamiquement.
ms.assetid: b5d8f133-ddd9-4b92-8540-611a03835be0
keywords:
- midl_user_free MIDL de l’attribut
topic_type:
- apiref
api_name:
- midl_user_free
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 686850418079b86b4bd083a4ea8c25ce6a0dd876f6f613647e389e3670d699f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991165"
---
# <a name="midl_user_free-attribute"></a>\_ \_ attribut gratuit de l’utilisateur MIDL

La **fonction \_ \_ gratuite de l’utilisateur MIDL** est fournie par les applications client et serveur pour libérer de la mémoire allouée dynamiquement.

``` syntax
void __RPC_API midl_user_free(void __RPC_FAR * p);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*p* 
</dt> <dd>

Pointeur vers le bloc de mémoire à libérer.

</dd> </dl>

## <a name="remarks"></a>Remarques

L’application cliente et l’application serveur doivent implémenter la fonction **\_ \_ gratuite utilisateur MIDL** , sauf si vous compilez en mode de compatibilité OSF ([**/OSF**](-osf.md)). La **fonction \_ \_ gratuite de l’utilisateur MIDL** doit pouvoir libérer tout le stockage alloué par l’allocation de l' [**\_ utilisateur \_ MIDL**](/windows/desktop/Rpc/the-midl-user-allocate-function).

Les applications et les stubs appellent **MIDL \_ \_ sans utilisateur** lors de la gestion d’objets référencés par des pointeurs :

-   L’application serveur doit appeler **l' \_ utilisateur MIDL \_ gratuit** pour libérer de la mémoire allouée par le application, par exemple, lors de la suppression d’un nœud spécifié.
-   Le stub serveur appelle **l' \_ utilisateur MIDL \_ gratuit** pour libérer de la mémoire sur le serveur après avoir marshalé tous les **\[** arguments [**out**](out-idl.md) **\]** , les arguments out, les **\[** arguments **out \]** et la valeur de retour. [](in.md)

## <a name="examples"></a>Exemples


```C++
#include <windows.h>

void __RPC_API midl_user_free(void __RPC_FAR * p) 
{ 
    free(p); 
}
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**tableaux**](arrays-1.md)
</dt> <dt>

[Tableaux et pointeurs](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Attributs de tableau et de Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**dans**](in.md)
</dt> <dt>

[**allouer un \_ utilisateur MIDL \_**](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**unique**](unique.md)
</dt> </dl>

 

 