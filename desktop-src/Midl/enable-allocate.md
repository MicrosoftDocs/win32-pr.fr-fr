---
title: attribut enable_allocate
description: L’attribut \ Enable \_ allocate \ ACF spécifie que le code stub du serveur doit activer l’environnement de gestion de la mémoire stub.
ms.assetid: 3a232a82-f114-4d8c-8b71-cf8860c77db3
keywords:
- enable_allocate MIDL de l’attribut
topic_type:
- apiref
api_name:
- enable_allocate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43e8c10592fcf99ea294327c400c579ce45bf6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093638"
---
# <a name="enable_allocate-attribute"></a>activer l' \_ attribut d’allocation

L’attribut **\[ Enable ACF \_ allocate \]** spécifie que le code stub du serveur doit activer l’environnement de gestion de la mémoire stub.

> [!Note]  
> L’attribut **\[ Enable \_ allocate \]** est obsolète et n’est plus pris en charge.

 

``` syntax
[
    enable_allocate
  [ , optional-attribute-list]
]
interface interface-name
{
    . . .
};
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Optional-attribute-List* 
</dt> <dd>

Spécifie une liste de zéro ou plusieurs attributs MIDL supplémentaires.

</dd> <dt>

*nom de l’interface* 
</dt> <dd>

Nom de l’interface à laquelle l’attribut **\[ Enable \_ allcoate \]** sera appliqué.

</dd> </dl>

## <a name="remarks"></a>Notes

En mode par défaut, le stub serveur Active l’environnement de mémoire uniquement lorsque l’attribut **\[ Enable \_ allocate \]** est utilisé. L’environnement de gestion de la mémoire doit être activé pour que la mémoire puisse être allouée à l’aide de [**RpcSmAllocate**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmallocate). En mode **OSF** (lorsque vous compilez à l’aide du commutateur [**/OSF**](-osf.md) ), le stub active automatiquement cet environnement, ou à la demande lorsque l’attribut **\[ Enable \_ allocate \]** est utilisé.

Le stub côté client peut être sensible à l’environnement de gestion de mémoire **RPCSS** . Si un stub client sensible est exécuté lorsque le package **RPCSS** est désactivé, l’allocateur/annulateurs d’utilisateur par défaut est appelé (par exemple, l’utilisateur [MIDL \_ \_ alloue](/windows/desktop/Rpc/the-midl-user-allocate-function)l' /  [ \_ utilisateur MIDL \_ gratuitement](/windows/desktop/Rpc/the-midl-user-free-function)). Lorsqu’il est activé, le package **RPCSS** utilise la paire Allocator/annulateur du package. Dans le mode par défaut, le client est sensible uniquement lorsque l’attribut **\[ Enable \_ allocate \]** est utilisé. En règle générale, le stub côté client s’exécute dans l’environnement désactivé. En mode **OSF** (lorsque vous compilez à l’aide du commutateur [**/OSF**](-osf.md) ), le client est toujours sensible à l’environnement de gestion de mémoire **RPCSS** et, par conséquent, l’attribut **\[ Enable \_ allocate \]** n’affecte pas les stubs du client.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fichier de configuration de l’application (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[allouer un \_ utilisateur MIDL \_](/windows/desktop/Rpc/the-midl-user-allocate-function)
</dt> <dt>

[\_utilisateur \_ gratuit MIDL](/windows/desktop/Rpc/the-midl-user-free-function)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[RpcSmDisableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmdisableallocate)
</dt> <dt>

[RpcSmEnableAllocate](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmenableallocate)
</dt> <dt>

[RpcSmFree](/windows/desktop/api/rpcndr/nf-rpcndr-rpcsmfree)
</dt> </dl>

 

 