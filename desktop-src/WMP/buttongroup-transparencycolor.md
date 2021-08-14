---
title: BUTTONGROUP. transparencyColor
description: L’attribut transparencyColor spécifie ou récupère la couleur transparente des images BUTTONGROUP.
ms.assetid: 604c5b29-50b9-4df6-9e48-488bf4fb7227
keywords:
- BUTTONGROUP. transparencyColor Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTONGROUP.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf97a25081e3f5c5729721bd675d9c59be1a4d52adc86acf6b9b75a0ee86dbac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342662"
---
# <a name="buttongrouptransparencycolor"></a>BUTTONGROUP. transparencyColor

L’attribut **transparencyColor** spécifie ou récupère la couleur transparente des images **BUTTONGROUP** .

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture sans valeur par défaut, contenant l’une des valeurs suivantes.



| Valeur                                       | Description                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------|
| Auto                                        | Le pixel à l’emplacement 0, 0 dans l’image devient la couleur transparente.                              |
| toute valeur de couleur Microsoft Internet Explorer | Une valeur de couleur d’Internet Explorer devient la couleur transparente (par exemple, « rouge » ou « \# FF0000 »). |
| Aucun                                        | Par défaut. Aucune transparence.                                                                          |



 

## <a name="remarks"></a>Remarques

Une couleur transparente dans une image permet à tout ce qui se trouve derrière l’image de s’afficher dans les zones de transparence. La région transparente est cliquable, sauf si elle est découpée par la balise **clippingImage** .

La couleur peut être n’importe quelle valeur de couleur Microsoft Internet Explorer. Si la valeur est auto, la couleur du pixel à l’emplacement 0, 0 dans l’image est utilisée.

Si la couleur spécifiée ne fait pas partie des couleurs Internet Explorer valides, un avertissement est renvoyé et la valeur précédente est conservée.

Étant donné que les JPGs sont perdus et, par conséquent, soumis à une modification de couleur inattendue, ils ne sont pas recommandés lorsque **transparencyColor** est utilisé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément BUTTONGROUP**](buttongroup-element.md)
</dt> <dt>

[**Référence de couleur**](color-reference.md)
</dt> </dl>

 

 





