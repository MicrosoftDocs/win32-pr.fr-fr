---
title: AmbientAttributes. zIndex
description: L’attribut zIndex spécifie ou récupère l’ordre dans lequel le contrôle est rendu.
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- Lecteur Windows Media AmbientAttributes. zIndex
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52480cc387c0a9e5e45c4b8e8fd2dae4199dbd16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528956"
---
# <a name="ambientattributeszindex"></a>AmbientAttributes. zIndex

L’attribut **ZIndex** spécifie ou récupère l’ordre dans lequel le contrôle est rendu.

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**long**) avec une valeur par défaut de zéro. La plage est celle d’un entier long signé.

## <a name="remarks"></a>Notes

L’image bitmap d’arrière-plan d’une **vue** ou d’un sous- **affichage** a un index z fixe égal à zéro. Si vous souhaitez qu’un contrôle soit derrière l’arrière-plan, **ZIndex** doit être défini sur un nombre négatif.

L’index z d’une **vue** ou d’une sous- **vue** est un index absolu, tandis que l’index z d’un contrôle est relatif à l’index z de la **vue** ou de la sous- **vue** qui le contient.

L’attribut **ZIndex** n’est pas pris en charge par les éléments **Browser** et **playlist** . Elle ne fonctionnera pas avec l’élément **vidéo** si vous utilisez la *vidéo*. **sans fenêtre** est défini sur false, ni avec l’élément **Effects** si **Effects**. **Windowed** a la valeur true.

Les éléments **BUTTONELEMENT** utilisent le **ZIndex** de leur **BUTTONGROUP**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> </dl>

 

 





