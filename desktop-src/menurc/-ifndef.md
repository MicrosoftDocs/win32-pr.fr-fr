---
title: " ifndef"
description: La directive \ ifndef contrôle la compilation conditionnelle du fichier de ressources en vérifiant le nom spécifié.
ms.assetid: b83d7b0e-1a37-47a8-b495-0eab05ed3a9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23728acabc0ca0179c544a66657a2d1b8343d5eae24556018e0e65025420bfba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472985"
---
# <a name="ifndef"></a>\#ifndef

La directive **\# ifndef** contrôle la compilation conditionnelle du fichier de ressources en vérifiant le nom spécifié. Si le nom n’a pas été défini ou si sa définition a été supprimée à l’aide de la directive **\# undef** , **\# ifndef** indique au compilateur de poursuivre le traitement des instructions jusqu’à la directive **\# endif**, **\# else** ou **\# Elif** suivante, puis d’ignorer l’instruction après la directive **\# endif** . Si le nom est défini, **\# ifndef** indique au compilateur d’ignorer la directive **\# endif**, **\# else** ou **\# Elif** suivante.

``` syntax
#ifndef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*nomme*
</dt> <dd>

Nom à vérifier par la directive.

</dd> </dl>

## <a name="example"></a> Exemple

Cet exemple compile l’instruction [**bitmap**](bitmap-resource.md) uniquement si l’optimisation n’est pas définie :

``` syntax
#ifndef Optimize
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Directives de préprocesseur](preprocessor-directives.md)
</dt> </dl>

 

 




