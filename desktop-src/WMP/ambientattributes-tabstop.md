---
title: AmbientAttributes. tabStop
description: L’attribut tabStop spécifie ou récupère une valeur indiquant si le contrôle est dans l’ordre de tabulation. Vous définissez l’ordre de tabulation en plaçant le contrôle dans le script global avant ou après d’autres balises de contrôle.
ms.assetid: 3d4b7fe4-1032-44e1-bae5-f253d00881bf
keywords:
- AmbientAttributes. tabStop Lecteur Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.tabStop
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4005fc26a2bc5f928cde0f5ed67ec2098cf3e6bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416276"
---
# <a name="ambientattributestabstop"></a>AmbientAttributes. tabStop

L’attribut **tabStop** spécifie ou récupère une valeur indiquant si le contrôle est dans l’ordre de tabulation. Vous définissez l’ordre de tabulation en plaçant le contrôle dans le script global avant ou après d’autres balises de contrôle.

``` syntax
        elementID.tabStop
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | Le contrôle se trouve dans l’ordre de tabulation (le contrôle aura un taquet de tabulation : exigence d’accessibilité). |
| false | Le contrôle n’est pas dans l’ordre de tabulation.                                                       |



 

## <a name="remarks"></a>Notes

L’attribut **tabStop** n’est pas applicable à l’élément **Effects** .

La valeur par défaut de cet attribut est true pour tous les éléments, à l’exception du **menu** automatique et du **texte**, dont la valeur par défaut est false.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> </dl>

 

 





