---
title: EQUALIZERSETTINGS.gainLevels
description: L’attribut gainLevels spécifie ou récupère le niveau de gain de la bande correspondant à l’index fourni.
ms.assetid: fb70e2ef-4cee-457e-a06b-7a1ae6930986
keywords:
- Lecteur Windows Media EQUALIZERSETTINGS. gainLevels
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevels
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d083ac829582f2abc45837cf441b2f0a565ee03a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523938"
---
# <a name="equalizersettingsgainlevels"></a>EQUALIZERSETTINGS.gainLevels

L’attribut **gainLevels** spécifie ou récupère le niveau de gain de la bande correspondant à l’index fourni.

``` syntax
        elementID.gainLevels(theBand)
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**float**) dont la valeur est normalement comprise entre 20 et + 20.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*theBand*
</dt> <dd>

**Nombre**(**long**) entre 1 et 10 indiquant l’index de la bande.

</dd> </dl>

## <a name="remarks"></a>Notes

Cet attribut accepte un paramètre, mais sa valeur est spécifiée dans le code de script de la même façon que les autres valeurs d’attribut. Elle ne peut pas être spécifiée dans l’élément EQUALIZERSETTINGS et ne peut pas être utilisée avec l’attribut Listening **wmpprop** . Au lieu de cela, les attributs de niveau de gain numéroté sont fournis pour ces situations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**Écoute des attributs**](listening-attributes.md)
</dt> </dl>

 

 





