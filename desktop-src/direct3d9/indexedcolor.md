---
description: Se compose d’un paramètre d’index et d’une couleur RVBA et est utilisé pour définir des couleurs de vertex de maillage. L’index définit le vertex auquel la couleur est appliquée.
ms.assetid: 63909c54-c2de-4065-9882-58fca2b4e893
title: IndexedColor
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c895cf56efedfa7214bcfa6acafd32ab9324bbe8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524921"
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

 

 



