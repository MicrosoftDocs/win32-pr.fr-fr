---
title: Commutateur/u
description: Le commutateur/U supprime toute définition précédente d’un nom en transmettant le nom au préprocesseur C comme s’il s’agissait d’une directive \ Undefine.
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- MIDL du commutateur/u
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9eab33e5aff861c1afecaafa52e04964ef286c5835e0a6992a3d369210f8927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895769"
---
# <a name="u-switch"></a>Commutateur/u

Le commutateur **/u** supprime toute définition précédente d’un nom en passant le nom au préprocesseur C comme s’il s’agissait d’une directive **\# non définie** .

``` syntax
midl /U name
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*name* 
</dt> <dd>

Spécifie un nom défini à passer au préprocesseur C comme s’il s’agissait d’une directive **\# non définie** . Le nom est prédéfini par le préprocesseur C ou précédemment défini par l’utilisateur.

</dd> </dl>

## <a name="remarks"></a>Remarques

Plusieurs directives **/u** peuvent être utilisées dans une ligne de commande. L’espace blanc entre le commutateur **/u** et le nom non défini est facultatif.

Lorsque le [**commutateur \_ /CPP cmd**](-cpp-cmd.md) est présent et que le commutateur [**/CPP \_ OPT**](-cpp-opt.md) n’est pas, le compilateur MIDL concatène la chaîne spécifiée par le \_ commutateur/CPP cmd avec les options [**/i**](-i.md), [**/d**](-d.md)et **/U** et utilise cette chaîne concaténée pour appeler le préprocesseur C pour chaque fichier source IDL et ACF. Le commutateur du compilateur MIDL **/u** est ignoré lorsque le commutateur du compilateur MIDL **/non \_ CPP** ou **/CPP \_ OPT** est spécifié.

## <a name="examples"></a>Exemples

**MIDL/UUNICODE NomFichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/CPP \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/CPP \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/D**](-d.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[**/non \_ CPP**](-no-cpp-nocpp.md)
</dt> </dl>

 

 




