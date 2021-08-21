---
title: AmbientAttributes.alphaBlendTo
description: La méthode alphaBlendTo ajuste la propriété alphaBlend sur une période donnée.
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- AmbientAttributes. alphaBlendTo Lecteur Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlendTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8e0e29df897d070cd4d337e27a7f5f7f7e3a86c7f44a784afadb5bc203674ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055227"
---
# <a name="ambientattributesalphablendto"></a>AmbientAttributes.alphaBlendTo

La méthode **alphaBlendTo** ajuste la propriété **alphaBlend** sur une période donnée.

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*
</dt> <dd>

**Nombre** (long) spécifiant la nouvelle valeur d’opacité. La plage est comprise entre 0 (aucune opacité) et 255 (opacité complète).

</dd> <dt>

<span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*
</dt> <dd>

**Nombre** (**long**) spécifiant la durée, en millisecondes, nécessaire à l’élément pour modifier l’opacité.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette méthode est utile pour faire apparaître ou disparaître progressivement des éléments.

Quand vous utilisez **alphaBlendTo** avec un élément de **texte** pour lequel le **backgroundColor** n’est pas spécifié, une couleur d’arrière-plan noire est utilisée. Si la couleur de premier plan est également noire (valeur par défaut pour le *texte*).**foregroundColor**), votre texte peut devenir illisible. Pour éviter cela, spécifiez toujours l’attribut **backgroundColor** ou définissez **foregroundColor** sur une couleur autre que Black.

> [!Note]  
> cet attribut n’est pas pris en charge dans Windows 98.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes. alphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**Élément de texte**](text-element.md)
</dt> <dt>

[**TEXT. backgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**TEXT. foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





