---
title: " ifdef"
description: La directive \ ifdef contrôle la compilation conditionnelle du fichier de ressources en vérifiant le nom spécifié.
ms.assetid: 877c6b58-d8a1-4e68-8b69-29fe106d6cbd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e834dc84d54e1d6f7725008b8bcf28f4ed49fc3fe45f36fb291ddc397d30eb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034477"
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

## <a name="example"></a>Exemples

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

 

 




