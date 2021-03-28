---
title: " undef (directive)"
description: Directive de préprocesseur qui supprime la définition actuelle d’une constante ou d’une macro précédemment définie à l’aide de la directive \ define.
ms.assetid: ba6bbe6b-ecfa-40cb-887f-e42b6e22c7bd
keywords:
- Directive undef (HLSL)
topic_type:
- apiref
api_name:
- undef Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7358dc60d002e784394f64773934a18f7413e493
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312553"
---
# <a name="undef-directive"></a>\#undef (directive)

Directive de préprocesseur qui supprime la définition actuelle d’une constante ou d’une macro précédemment définie à l’aide de la directive [ \# define](dx-graphics-hlsl-appendix-pre-define.md) .



| \#*identificateur* undef |
|----------------------|



 

## <a name="parameters"></a>Paramètres



| Élément                                                                              | Description                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*identificateur*<br/> | Identificateur de la constante ou de la macro dont la définition doit être supprimée. Si vous ne définissez pas une macro, fournissez uniquement l’identificateur, et non la liste de paramètres. <br/> |



 

## <a name="remarks"></a>Notes

Vous pouvez appliquer la \# directive undef à un identificateur qui n’a pas de définition précédente. cela garantit que l’identificateur n’est pas défini. Le remplacement de macro n’est pas effectué dans les \# instructions undef.

La \# directive undef est généralement associée à une directive [ \# define](dx-graphics-hlsl-appendix-pre-define.md) pour créer une région dans un programme source dans lequel un identificateur a une signification particulière. Par exemple, une fonction spécifique du programme source peut utiliser des constantes manifestes pour définir les valeurs spécifiques à l'environnement qui n'affectent pas le reste du programme. La \# directive undef fonctionne également avec la directive [) pour contrôler la compilation conditionnelle du programme source.

Les constantes et les macros peuvent être non définies à partir de la ligne de commande à l’aide de l’option/U, suivie des identificateurs à non définir. Cela équivaut à ajouter une séquence de \# directives undef au début du fichier source.

## <a name="examples"></a>Exemples

L’exemple suivant montre comment utiliser la \# directive undef pour supprimer les définitions d’une constante symbolique et une macro.


```
#define WIDTH           80
#define ADD( X, Y )     (X) + (Y)

#undef WIDTH
#undef ADD
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Directives de préprocesseur (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#define, directive (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#Si,)](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





