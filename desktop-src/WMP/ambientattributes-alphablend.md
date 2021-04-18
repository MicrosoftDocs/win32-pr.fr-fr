---
title: AmbientAttributes. alphaBlend
description: L’attribut alphaBlend spécifie ou récupère une valeur pour la fusion alpha d’une vue, d’une sous-vue ou d’un widget d’interface utilisateur.
ms.assetid: a6c47d32-a497-4bfa-8fa3-ef94e267d94b
keywords:
- Lecteur Windows Media AmbientAttributes. alphaBlend
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlend
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8c0f0cb9d885f643b39acfbc5148403a5c8b788
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533178"
---
# <a name="ambientattributesalphablend"></a>AmbientAttributes. alphaBlend

L’attribut **alphaBlend** spécifie ou récupère une valeur pour la fusion alpha d’une **vue**, d’une sous- **vue** ou d’un widget d’interface utilisateur.

``` syntax
        elementID.alphaBlend
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est un **nombre** en lecture/écriture (**long**) dont la valeur est comprise entre 0 (aucune opacité) et 255 (opacité complète) et une valeur par défaut de 255.

## <a name="remarks"></a>Notes

Cet attribut permet à un élément d’apparaître comme translucide, en fonction de la quantité d’opacité définie. Moins l’opacité est faible, plus l’élément est transparent. Chaque élément de l’apparence peut avoir une valeur d’opacité distincte, à l’exception des éléments de bouton dans un contrôle **BUTTONGROUP** . Quand **alphaBlend** est défini dans la **vue**, l’opacité de la totalité de l’apparence est définie. Alpha Blend ne fonctionne pas pour les contrôles avec fenêtres, y compris les **sélections**, les **effets**, la zone de liste, les **menus contextuels** **, les** **zones** d’édition et les **vidéos** (si l’absence de **fenêtre** est définie sur false). Quand **alphaBlend** est défini sur **View**, la totalité de la peau devient transparente. Les attributs **transparencyColor** utilisés par plusieurs éléments ne sont pas pris en charge par **alphaBlend**.

Lorsque vous utilisez **alphaBlend** avec un élément de **texte** pour lequel le **backgroundColor** n’est pas spécifié, une couleur d’arrière-plan noire est utilisée. Si la couleur de premier plan est également noire (valeur par défaut pour le *texte*).**foregroundColor**), votre texte peut devenir illisible. Pour éviter cela, spécifiez toujours l’attribut **backgroundColor** ou définissez **foregroundColor** sur une couleur autre que Black.

> [!Note]  
> Cet attribut n’est pas pris en charge dans Windows 98.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.alphaBlendTo**](ambientattributes-alphablendto.md)
</dt> <dt>

[**Élément de texte**](text-element.md)
</dt> <dt>

[**TEXT. backgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**TEXT. foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





