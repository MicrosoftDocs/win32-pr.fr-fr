---
title: EFFECTs. effectType
description: La méthode effectType récupère le nom du registre de la visualisation avec l’index de Registre spécifié. Ce nom est un ID unique défini par l’auteur de la visualisation.
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- effects. effectType Lecteur Windows Media
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a452f9218c7004d1078ae6b9e878421a7cad301f3ee913ef6296aaa1c681b736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749231"
---
# <a name="effectseffecttype"></a>EFFECTs. effectType

La méthode **effectType** récupère le nom du registre de la visualisation avec l’index de Registre spécifié. Ce nom est un ID unique défini par l’auteur de la visualisation.

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*évaluer*
</dt> <dd>

**Nombre** (**long**) contenant l’index du registre d’une visualisation.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne une **chaîne**.

## <a name="remarks"></a>Remarques

Cette méthode est utile pour basculer entre les visualisations dans le script. Une interface utilisateur peut afficher le jeu de titres, mais lorsque l’utilisateur en sélectionne un, le script doit utiliser **currentEffectType** pour basculer les visualisations.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément EFFECTs**](effects-element.md)
</dt> <dt>

[**EFFECTs. currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





