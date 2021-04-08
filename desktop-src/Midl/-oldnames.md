---
title: commutateur/oldnames
description: Le commutateur/oldnames indique au compilateur MIDL de générer des noms d’interface qui n’incluent pas le numéro de version.
ms.assetid: 3a79c399-e115-46fd-9559-681b85cd872d
keywords:
- MIDL du commutateur/oldnames
topic_type:
- apiref
api_name:
- /oldnames
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44cf861d2bf4f4123d7a1ee103e6966e5d404946
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725445"
---
# <a name="oldnames-switch"></a>commutateur/oldnames

Le commutateur **/oldnames** indique au compilateur MIDL de générer des noms d’interface qui n’incluent pas le numéro de version.

``` syntax
midl /oldnames
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Notes

Le compilateur MIDL incorpore le numéro de version de l’interface dans le nom de l’interface qui est généré dans le stub (par exemple, iface \_ v1 \_ 0 \_ ServerIfHandle). Ce format de nommage est cohérent avec le format utilisé par le compilateur de l’IDL DCE OSF. Toutefois, il diffère du format d’affectation de noms utilisé par le compilateur MIDL 1,0. Le compilateur MIDL 1,0 n’incluait pas de numéros de version dans les noms d’interface (par exemple, iface \_ ServerIfHandle). Le commutateur **/oldnames** vous permet d’ordonner au compilateur MIDL de générer des noms d’interface qui n’incluent pas le numéro de version. De cette façon, le format est cohérent avec les noms générés par le compilateur MIDL 1,0.

Si vous avez un code d’application serveur qui a été écrit pour une utilisation avec un stub généré par le compilateur MIDL 1,0 et qu’il fait référence au nom d’interface généré par MIDL (par exemple, dans un appel à [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif)), vous devez le modifier pour référencer le style du nom d’interface pris en charge par la version 2,0 ou ultérieure du compilateur MIDL. Vous pouvez également utiliser le commutateur **/oldnames** lors de l’appel du compilateur MIDL.

## <a name="examples"></a>Exemples

**MIDL/oldnames NomFichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[Fichier de définition d’interface (IDL)](interface-definition-idl-file.md)
</dt> </dl>

 

 