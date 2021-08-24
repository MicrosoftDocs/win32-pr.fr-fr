---
description: Se compose d’un paramètre d’index et d’une couleur RVBA et est utilisé pour définir des couleurs de vertex de maillage. L’index définit le vertex auquel la couleur est appliquée.
ms.assetid: 63909c54-c2de-4065-9882-58fca2b4e893
title: IndexedColor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b0dcaf850786a18e5fc317276939436b93c3a49765d520aa40f88cd53707d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563729"
---
# <a name="indexedcolor"></a>IndexedColor

Se compose d’un paramètre d’index et d’une couleur RVBA et est utilisé pour définir des couleurs de vertex de maillage. L’index définit le vertex auquel la couleur est appliquée.

``` syntax
template IndexedColor
{
    < 1630B820-7842-11cf-8F52-0040333594A3 >
    DWORD index;
    ColorRGBA indexColor;
} 
```

Où :

-   index : DWORD. Consultez la Description ci-dessus.
-   indexColor : modèle ColorRGBA. Consultez [**ColorRGBA**](colorrgba.md).

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



