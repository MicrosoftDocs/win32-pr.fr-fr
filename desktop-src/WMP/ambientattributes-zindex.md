---
title: AmbientAttributes. zIndex
description: L’attribut zIndex spécifie ou récupère l’ordre dans lequel le contrôle est rendu.
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- AmbientAttributes. zIndex Lecteur Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0ebccb050d80371b5865316dd341c8e371d3bfd399d14545b312cf8d265bac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124039"
---
# <a name="ambientattributeszindex"></a>AmbientAttributes. zIndex

L’attribut **ZIndex** spécifie ou récupère l’ordre dans lequel le contrôle est rendu.

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**long**) avec une valeur par défaut de zéro. La plage est celle d’un entier long signé.

## <a name="remarks"></a>Remarques

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

 

 





