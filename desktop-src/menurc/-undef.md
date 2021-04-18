---
title: " undef"
description: La directive \ undef supprime la définition actuelle du nom spécifié. Toutes les occurrences ultérieures du nom sont traitées sans remplacement.
ms.assetid: c9a0b538-3030-4d39-bfc2-d158061967b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a04b14eeea18a05795cd8ebbb94d81d0aead6a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512664"
---
# <a name="undef"></a>\#undef

La directive **\# undef** supprime la définition actuelle du nom spécifié. Toutes les occurrences ultérieures du nom sont traitées sans remplacement.

``` syntax
#undef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*nomme*
</dt> <dd>

Nom à supprimer. Cette valeur correspond à toute combinaison de lettres, de chiffres et de signes de ponctuation valide pour le préprocesseur C/C++.

</dd> </dl>

## <a name="example"></a>Exemple

Cet exemple supprime les définitions pour les noms non nuls et USERCLASS :

``` syntax
#undef     nonzero
#undef     USERCLASS
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Directives de préprocesseur](preprocessor-directives.md)
</dt> </dl>

 

 




