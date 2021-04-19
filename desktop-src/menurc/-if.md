---
title: " if"
description: La directive \ if contrôle la compilation conditionnelle du fichier de ressources en vérifiant l’expression constante spécifiée.
ms.assetid: 4d0f26a0-1a2d-4fad-b5ce-b9441397d2c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 364d6f5eb818813f61f6428446effb4793b96b2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510609"
---
# <a name="if"></a>\#que

La directive **\# If** contrôle la compilation conditionnelle du fichier de ressources en vérifiant l’expression constante spécifiée. Si l’expression constante est différente de zéro, **\# si** demande au compilateur de poursuivre le traitement des instructions jusqu’à la directive **\# endif**, **\# else** ou **\# Elif** suivante, puis d’ignorer l’instruction après la directive **\# endif** . Si l’expression constante est égale à zéro, **\# si** demande au compilateur d’ignorer la directive **\# endif**, **\# else** ou **\# Elif** suivante.

``` syntax
#if constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*
</dt> <dd>

Expression à vérifier. Cette valeur est un nom défini, une constante entière ou une expression comprenant des noms, des entiers et des opérateurs arithmétiques et relationnels.

</dd> </dl>

## <a name="example"></a>Exemple

Cet exemple compile l’instruction [**bitmap**](bitmap-resource.md) uniquement si la valeur affectée à la valeur est inférieure à 3 :

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Directives de préprocesseur](preprocessor-directives.md)
</dt> </dl>

 

 




