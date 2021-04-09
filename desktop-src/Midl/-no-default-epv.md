---
title: commutateur/no_default_epv
description: Le \_ commutateur EPV par défaut de/non \_ indique au compilateur MIDL qu’il ne doit pas générer de vecteur de point d’entrée par défaut (EPV). L’utilisation de cet attribut n’est pas recommandée.
ms.assetid: 160b5fd3-cd9c-4f51-8c35-6cddab120021
keywords:
- /commutateur no_default_epv MIDL
topic_type:
- apiref
api_name:
- /no_default_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0a6e39319c5f03c1cd41959a009307b07bef66f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940879"
---
# <a name="no_default_epv-switch"></a>\_ \_ commutateur EPV par défaut

Le **commutateur \_ \_ EPV par défaut de/non** indique au compilateur MIDL qu’il ne doit pas générer de vecteur de point d’entrée par défaut (EPV). L’utilisation de cet attribut n’est pas recommandée.

``` syntax
midl /no_default_epv
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

Dans ce cas, l’application doit inscrire un EPV avec l’appel [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) . Comparez ce commutateur avec le commutateur [**/Utilisez \_ EPV**](-use-epv.md) .

## <a name="examples"></a>Exemples

**MIDL/non \_ par défaut \_ EPV nom_fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/Utilisez \_ EPV**](-use-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 