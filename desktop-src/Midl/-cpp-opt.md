---
title: commutateur/cpp_opt
description: Le \_ commutateur/CPP opt spécifie les options à transmettre au préprocesseur C/C++.
ms.assetid: f0059caa-aff3-4e96-95f8-a0014d6a6556
keywords:
- /commutateur cpp_opt MIDL
topic_type:
- apiref
api_name:
- /cpp_opt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00e352a89ddadfc0a92e33e964afb5f0d9e9df6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093954"
---
# <a name="cpp_opt-switch"></a>\_commutateur/CPP opt

Le commutateur **/CPP \_ OPT** spécifie les options à transmettre au préprocesseur C/C++.

``` syntax
midl /cpp_opt "C_preprocessor_option" file.idl
```

## <a name="switch-options"></a>Options de commutateur

<dl> <dt>

*\_Option de préprocesseur \_ C* 
</dt> <dd>

Spécifie l’option de ligne de commande associée au préprocesseur appelé. 

**Remarque**: pour les préprocesseurs Microsoft C/C++, vous devez fournir le `/E` commutateur dans le cadre de la chaîne d' *\_ \_ option de préprocesseur c* . 

Des guillemets sont requis lorsque plusieurs options sont utilisées, et pour les espaces.

</dd> </dl>

## <a name="remarks"></a>Notes

N’utilisez pas ce commutateur à moins qu’il y ait une raison spécifique. Pour obtenir des informations importantes sur le prétraitement, consultez la [Configuration requise pour le préprocesseur C pour MIDL](c-preprocessor-requirements-for-midl.md) .

Le commutateur **/CPP \_ OPT** peut être utilisé avec ou sans le commutateur [**/CPP \_ cmd**](-cpp-cmd.md) . Consultez **/CPP \_ cmd** pour plus d’informations sur la construction de la ligne de commande du préprocesseur dans les deux cas.

Le commutateur **/CPP \_ OPT** , s’il est spécifié, doit toujours être inclus `/E` pour fonctionner correctement.

## <a name="examples"></a>Exemples

**MIDL/CPP \_ cmd d : \\ NT \\ Tools \\ ia64 \\cl.exe/DFLAG = true/IC : \\ Inc filename. idl**

**MIDL/CPP \_ cmd "mycpp"/DFLAG = true/IC : \\ Inc filename. idl**

**MIDL/CPP \_ OPT "/E/DFLAG = true/IC : \\ Inc" nom_fichier. idl**

**MIDL/CPP \_ cmd "cl"/CPP \_ OPT "/e/DFLAG = true/IC : \\ Inc" nom_fichier. idl**

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**/savePP**](-savepp.md)
</dt> <dt>

[**/CPP \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/non \_ CPP**](-no-cpp-nocpp.md)
</dt> <dt>

[C-Configuration requise pour le préprocesseur pour MIDL](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




