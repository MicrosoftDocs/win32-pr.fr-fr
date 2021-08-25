---
title: " elif"
description: La directive \ Elif marque une clause facultative d’un bloc de compilation conditionnelle défini par une directive \ ifdef, \ ifndef ou \ if.
ms.assetid: 432b8543-7e1a-411a-8191-cc0f0e4a2e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e131d40648bcda75025087717798ceb2ad1262d680877512dbb85a451fc86e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720899"
---
# <a name="elif"></a>\#Elif

La directive **\# Elif** marque une clause facultative d’un bloc de compilation conditionnelle définie par une directive **\# ifdef**, **\# ifndef** ou **\# If** . La directive contrôle la compilation conditionnelle du fichier de ressources en vérifiant l’expression constante spécifiée. Si l’expression constante est différente de zéro, **\# Elif** demande au compilateur de poursuivre le traitement des instructions jusqu’à la directive **\# endif**, **\# else** ou **\# Elif** suivante, puis d’ignorer l’instruction après **\# endif**. Si l’expression constante est égale à zéro, **\# Elif** demande au compilateur d’ignorer la directive **\# endif**, **\# else** ou **\# Elif** suivante. Vous pouvez utiliser n’importe quel nombre de directives **\# Elif** dans un bloc conditionnel.

``` syntax
#elif constant-expression
```

<dl> <dt>

<span id="constant-expression"></span><span id="CONSTANT-EXPRESSION"></span>*constant-expression*
</dt> <dd>

Expression à vérifier. Cette valeur est un nom défini, une constante entière ou une expression comprenant des noms, des entiers et des opérateurs arithmétiques et relationnels.

</dd> </dl>

## <a name="example"></a>Exemples

Dans cet exemple, **\# Elif** demande au compilateur de traiter la deuxième instruction [**bitmap**](bitmap-resource.md) uniquement si la valeur assignée à la version de nom est inférieure à 7. La directive **\# Elif** elle-même est traitée uniquement si la version est supérieure ou égale à 3.

``` syntax
#if Version < 3
BITMAP 1 errbox.bmp
#elif Version < 7
BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Directives de préprocesseur](preprocessor-directives.md)
</dt> </dl>

 

 




