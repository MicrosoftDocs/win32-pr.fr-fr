---
title: " else"
description: La directive \ else marque une clause facultative d’un bloc de compilation conditionnelle défini par une directive \ ifdef, \ ifndef ou \ if. La directive \ else doit être la dernière directive avant la directive \ endif.
ms.assetid: 982466d9-ae77-4e1c-89f3-511335165da7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aade46f8d2af211d4ed09e596ec3a42fa57d141d3d533bdbe34be09d9e9988c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060199"
---
# <a name="else"></a>\#else

La directive **\# else** marque une clause facultative d’un bloc de compilation conditionnelle définie par une directive **\# ifdef**, **\# ifndef** ou **\# If** . La directive **\# else** doit être la dernière directive avant la directive **\# endif** .

``` syntax
#else
```

Cette directive n’a aucun paramètre.

## <a name="example"></a>Exemple

Cet exemple compile la deuxième instruction [**bitmap**](bitmap-resource.md) uniquement si debug n’est pas défini :

``` syntax
#ifdef DEBUG
    BITMAP 1 errbox.bmp
#else
    BITMAP 1 userbox.bmp
#endif
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Directives de préprocesseur](preprocessor-directives.md)
</dt> </dl>

 

 




