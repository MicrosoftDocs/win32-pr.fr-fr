---
title: EFFECTs. AutoriserTout
description: L’attribut AutoriserTout spécifie ou récupère une valeur indiquant s’il faut inclure toutes les visualisations qui se trouvent dans le registre.
ms.assetid: 8552cc06-05b2-4049-ba7d-f6bd770449e0
keywords:
- effects. autorisertout Lecteur Windows Media
topic_type:
- apiref
api_name:
- EFFECTS.allowAll
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7a87aa8336e3961b31716c8d6bbfaa6aee71374a0f3c6e17b644a47136df550
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996842"
---
# <a name="effectsallowall"></a>EFFECTs. AutoriserTout

L’attribut **AutoriserTout** spécifie ou récupère une valeur indiquant s’il faut inclure toutes les visualisations qui se trouvent dans le registre.

``` syntax
        elementID.allowAll
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                                         |
|-------|---------------------------------------------------------------------|
| true  | Par défaut. Autorise le cycle de toutes les visualisations sur le système de l’utilisateur. |
| false | Limite le cycle aux visualisations apparaissant dans les balises d' **effets** . |



 

## <a name="remarks"></a>Remarques

Si cet attribut est défini sur false, seules les visualisations apparaissant dans les balises d' **effets** peuvent être recycles à l’aide du précédent/suivant. Si la valeur est true, toutes les visualisations inscrites sur le système de l’utilisateur peuvent être recyclees. Si la valeur est true et que vous spécifiez des visualisations dans les balises d' **effets** , les attributs spécifiés dans ces balises sont appliqués à toutes les visualisations sur le système de l’utilisateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EFFECTs**](effects-element.md)
</dt> </dl>

 

 





