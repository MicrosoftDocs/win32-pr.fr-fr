---
title: BUTTON. transparencyColor
description: L’attribut transparencyColor spécifie ou récupère la couleur qui sera transparente dans les images de bouton.
ms.assetid: c22f9965-3118-4c96-8ff5-7fbaa28cbb57
keywords:
- BUTTON. transparencyColor Lecteur Windows Media
topic_type:
- apiref
api_name:
- BUTTON.transparencyColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771249ddb070c596dc126b9b0c8c7d04a4b4268f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855729"
---
# <a name="buttontransparencycolor"></a>BUTTON. transparencyColor

L’attribut **transparencyColor** spécifie ou récupère la couleur qui sera transparente dans les images de **bouton** .

``` syntax
        elementID.transparencyColor
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture sans valeur par défaut contenant l’une des valeurs suivantes.



| Valeur                                    | Description                                                                                               |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Auto                                     | La couleur du pixel à l’emplacement 0, 0 dans l’image devient la couleur transparente.                        |
| Toute valeur de format de couleur Internet Explorer | Une valeur de format de couleur d’Internet Explorer devient la couleur transparente (par exemple, « rouge » ou « \# FF0000 »). |
| None                                     | Aucune transparence.                                                                                          |



 

## <a name="remarks"></a>Notes

Une couleur transparente dans une image permet à tout ce qui se trouve derrière l’image de s’afficher dans les zones transparentes. Le **bouton** continuera de recevoir des clics sur la zone transparente.

La couleur transparente peut être n’importe quelle valeur de couleur Internet Explorer. Si la valeur de l’attribut **transparencyColor** est définie sur « auto », la couleur du pixel à l’emplacement 0, 0 dans l’image est utilisée.

Si la couleur spécifiée ne fait pas partie des couleurs IE valides, la valeur précédente est conservée.

Étant donné que les JPGs sont perdus et, par conséquent, soumis à une modification de couleur inattendue, ils ne sont pas recommandés lorsque **transparencyColor** est utilisé.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BUTTON, élément**](button-element.md)
</dt> <dt>

[**BOUTON. image**](button-image.md)
</dt> <dt>

[**Référence de couleur**](color-reference.md)
</dt> </dl>

 

 





