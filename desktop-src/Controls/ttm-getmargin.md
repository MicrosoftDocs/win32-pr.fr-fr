---
title: Message TTM_GETMARGIN (commctrl. h)
description: Récupère les marges supérieure, gauche, inférieure et droite définies pour une fenêtre d’info-bulle. Une marge est la distance, en pixels, entre la bordure de la fenêtre d’info-bulle et le texte contenu dans la fenêtre d’info-bulle.
ms.assetid: c33ee1de-5fbd-4c7e-a703-576c2ffd3052
keywords:
- TTM_GETMARGIN les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TTM_GETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3e795d8eac14522f0994a342c7f781b7112ce
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115873"
---
# <a name="ttm_getmargin-message"></a>\_Message atténuation GETMARGIN

Récupère les marges supérieure, gauche, inférieure et droite définies pour une fenêtre d’info-bulle. Une marge est la distance, en pixels, entre la bordure de la fenêtre d’info-bulle et le texte contenu dans la fenêtre d’info-bulle.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui recevra les informations de marge. Les membres de la structure **Rect** ne définissent pas de rectangle englobant. Dans le cadre de ce message, les membres de la structure sont interprétés comme suit :



| Valeur                                                                                                                                   | Signification                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**top**</dt> </dl>          | Distance entre la bordure supérieure et le texte de l’info-bulle, en pixels.<br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**gauche**</dt> </dl>       | Distance entre la bordure gauche et l’extrémité gauche du texte d’info-bulle, en pixels.<br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <dt>**ballon**</dt> </dl> | Distance entre la bordure inférieure et le bas du texte de l’info-bulle, en pixels.<br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <dt>**Oui**</dt> </dl>    | Distance entre la bordure droite et l’extrémité droite du texte d’info-bulle, en pixels.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour de ce message n’est pas utilisée.

## <a name="remarks"></a>Notes

Par défaut, les quatre marges sont égales à zéro lorsque vous créez le contrôle ToolTip.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ATTÉNUATION \_ SETMARGIN**](ttm-setmargin.md)
</dt> </dl>

 

