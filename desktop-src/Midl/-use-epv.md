---
title: commutateur/use_epv
description: Le \_ commutateur/utilisez EPV indique au compilateur MIDL de générer le code stub du serveur qui appelle la routine de l’application serveur via un vecteur de point d’entrée (EPV), plutôt que par un appel statique. L’utilisation de cet attribut n’est pas recommandée.
ms.assetid: 2853d836-ded3-412a-916b-1143968123a2
keywords:
- /commutateur use_epv MIDL
topic_type:
- apiref
api_name:
- /use_epv
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec73b5cb9833c15a77c96a784e1ded88d266f9a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "106512094"
---
# <a name="use_epv-switch"></a>\_commutateur/utilisez EPV

Le commutateur **/Utilisez \_ EPV** indique au compilateur MIDL de générer le code stub du serveur qui appelle la routine de l’application serveur via un vecteur de point d’entrée (EPV), plutôt que par un appel statique. L’utilisation de cet attribut n’est pas recommandée.

``` syntax
midl /use_epv
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

En règle générale, les applications requièrent une liaison statique à la routine d’application serveur. Le compilateur MIDL génère ce type d’appel par défaut. Toutefois, si une application requiert que le stub serveur appelle la routine d’application serveur à l’aide de EPV, le commutateur **/Utilisez \_ EPV** doit être spécifié. Quand le commutateur **/Utilisez \_ EPV** est spécifié, le compilateur MIDL génère un EPV par défaut. Ce EPV par défaut est ensuite utilisé si l’application n’enregistre pas un autre EPV via l’appel [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) .

## <a name="examples"></a>Exemples

**MIDL/utilisez \_ EPV** *nom de fichier * * *. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**/non \_ par défaut \_ EPV**](-no-default-epv.md)
</dt> <dt>

[**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)
</dt> </dl>

 

 