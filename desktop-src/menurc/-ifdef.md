---
title: " ifdef"
description: La directive \ ifdef contrôle la compilation conditionnelle du fichier de ressources en vérifiant le nom spécifié.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38170fb2140f8405a86529c0899c1e4d4e93c026
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379976"
---
# <a name="ifdef"></a>\#ifdef

La directive **\# ifdef** contrôle la compilation conditionnelle du fichier de ressources en vérifiant le nom spécifié. Si le nom a été défini à l’aide d’une directive de **\# définition** ou à l’aide de l’option de ligne de commande **/d** avec le compilateur de ressources, **\# ifdef** demande au compilateur de continuer avec l’instruction qui suit immédiatement la directive **\# ifdef** . Si le nom n’a pas été défini, **\# ifdef** demande au compilateur d’ignorer toutes les instructions jusqu’à la directive **\# endif** suivante.

``` syntax
#ifdef name
```

<dl> <dt>

<span id="name"></span><span id="NAME"></span>*nomme*
</dt> <dd>

Nom à vérifier par la directive.

</dd> </dl>

## <a name="example"></a>Exemple

Cet exemple compile l’instruction [**bitmap**](bitmap-resource.md) uniquement si debug est défini :

``` syntax
#ifdef Debug
BITMAP 1 errbox.bmp
#endif
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Directives de préprocesseur](preprocessor-directives.md)
</dt> </dl>

 

 




