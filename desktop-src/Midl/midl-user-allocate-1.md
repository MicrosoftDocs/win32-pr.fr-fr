---
title: attribut midl_user_allocate
description: La \_ \_ fonction d’allocation utilisateur MIDL est une fonction que les applications client et serveur fournissent pour allouer de la mémoire.
ms.assetid: 0eaf6df5-791d-4f6d-8f49-cc1ce64e7ab4
keywords:
- midl_user_allocate MIDL de l’attribut
topic_type:
- apiref
api_name:
- midl_user_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4be10c5e1c7073afb3abf359c3ec2fb79a4335b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093398"
---
# <a name="midl_user_allocate-attribute"></a>attribut d’allocation de l' \_ utilisateur MIDL \_

La fonction d' **\_ \_ allocation utilisateur MIDL** est une fonction que les applications client et serveur fournissent pour allouer de la mémoire.

``` syntax
void __RPC_FAR * __RPC_API midl_user_allocate (size_t cBytes);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*cBytes* 
</dt> <dd>

Spécifie le nombre d’octets à allouer.

</dd> </dl>

## <a name="remarks"></a>Notes

Les applications clientes et les applications serveur doivent implémenter la fonction d' **\_ \_ allocation utilisateur MIDL** , sauf si vous compilez en mode de compatibilité OSF ([**/OSF**](-osf.md)). Les applications et les stubs générés appellent **MIDL \_ User \_ allocate** lors du traitement d’objets référencés par des pointeurs :

-   L’application serveur doit appeler **MIDL \_ User \_ allocate** pour allouer de la mémoire pour le application, par exemple, lors de la création d’un nouveau nœud.
-   Le stub serveur appelle **l' \_ \_ allocation d’utilisateur MIDL** lors du démarshaling de données pointant vers l’espace d’adressage du serveur.
-   Le stub client appelle **l' \_ \_ allocation d’utilisateur MIDL** lors du démarshaling de données à partir du serveur qui est référencé par un pointeur de [**sortie**](out-idl.md) . Notez que pour les **\[** [](in.md) **\]** pointeurs in, **\[ \] out** et **\[** [**unique**](unique.md) **\]** , le stub client appelle l’allocation de l' **\_ utilisateur \_ MIDL** uniquement si la valeur de pointeur **\[ unique \]** était **null** en entrée et que les modifications apportées à une valeur non **null** au cours de l’appel. Si le pointeur **\[ \] unique** n’était pas **null** en entrée, le stub client écrit les données associées dans la mémoire existante.

Si **l' \_ \_ allocation d’utilisateur MIDL** échoue pour allouer de la mémoire, elle doit retourner un pointeur **null** .

Il est recommandé que **l' \_ \_ allocation d’utilisateur MIDL** retourne un pointeur de 8 octets alignés.

## <a name="examples"></a>Exemples


```C++
#include <windows.h>

void __RPC_FAR * __RPC_API midl_user_allocate(size_t cBytes) 
{ 
    return(malloc(cBytes)); 
}
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**lui**](allocate.md)
</dt> <dt>

[**tableaux**](arrays-1.md)
</dt> <dt>

[Tableaux et pointeurs](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[Attributs de tableau et de Sized-Pointer](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**dans**](in.md)
</dt> <dt>

[**\_utilisateur \_ gratuit MIDL**](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**à**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**unique**](unique.md)
</dt> </dl>

 

 