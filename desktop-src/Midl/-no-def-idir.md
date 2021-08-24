---
title: commutateur/no_def_idir
description: Lorsque les répertoires sont spécifiés avec le commutateur/I, le \_ commutateur/non Def \_ idir demande au compilateur MIDL de rechercher uniquement les répertoires spécifiés à l’aide du commutateur/i.
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /commutateur no_def_idir MIDL
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c93d61bff28ad0aa4306047755c88419d0b925431f9b3ea476ec957dcd62b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811299"
---
# <a name="no_def_idir-switch"></a>\_commutateur/non Def \_ idir

Lorsque les répertoires sont spécifiés avec le commutateur [**/i**](-i.md) , le commutateur **/non \_ Def \_ idir** demande au compilateur MIDL de rechercher uniquement les répertoires spécifiés à l’aide du commutateur **/i** , en ignorant le répertoire actif, ainsi que les répertoires spécifiés par la variable d’environnement include.

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a>Options de commutateur

Ce commutateur n’a aucun paramètre.

## <a name="remarks"></a>Remarques

Quand aucun répertoire n’est spécifié avec le commutateur [**/i**](-i.md) , le commutateur **/non \_ Def \_ idir** demande au compilateur MIDL de rechercher uniquement le répertoire actif.

## <a name="examples"></a>Exemples

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Syntaxe générale de la ligne de commande MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**/I**](-i.md)
</dt> </dl>

 

 




