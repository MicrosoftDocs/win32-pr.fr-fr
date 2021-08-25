---
title: Message TTM_SETMARGIN (commctrl. h)
description: Définit les marges supérieure, gauche, inférieure et droite d’une fenêtre d’info-bulle. Une marge est la distance, en pixels, entre la bordure de la fenêtre d’info-bulle et le texte contenu dans la fenêtre d’info-bulle.
ms.assetid: f1663861-c217-42dd-8249-7647b1651910
keywords:
- TTM_SETMARGIN les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TTM_SETMARGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e5792b33f7f9f5a997759ba390c1b8a713308f95c4ba3f7b5cd0460747ff62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914059"
---
# <a name="ttm_setmargin-message"></a>\_Message atténuation SETMARGIN

Définit les marges supérieure, gauche, inférieure et droite d’une fenêtre d’info-bulle. Une marge est la distance, en pixels, entre la bordure de la fenêtre d’info-bulle et le texte contenu dans la fenêtre d’info-bulle.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui contient les informations sur les marges à définir. Les membres de la structure **Rect** ne définissent pas de rectangle englobant. Dans le cadre de ce message, les membres de la structure sont interprétés comme suit :



| Valeur                                                                                                                                   | Signification                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="top"></span><span id="TOP"></span><dl> <dt>**top**</dt> </dl>          | Distance entre la bordure supérieure et le texte de l’info-bulle, en pixels.<br/>         |
| <span id="left"></span><span id="LEFT"></span><dl> <dt>**gauche**</dt> </dl>       | Distance entre la bordure gauche et l’extrémité gauche du texte d’info-bulle, en pixels.<br/>   |
| <span id="bottom"></span><span id="BOTTOM"></span><dl> <dt>**ballon**</dt> </dl> | Distance entre la bordure inférieure et le bas du texte de l’info-bulle, en pixels.<br/>   |
| <span id="right"></span><span id="RIGHT"></span><dl> <dt>**Oui**</dt> </dl>    | Distance entre la bordure droite et l’extrémité droite du texte d’info-bulle, en pixels.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="remarks"></a>Remarques

ce message n’a aucun effet lorsque l’application s’exécute sur Windows Vista et que les styles visuels sont activés pour l’info-bulle. Vous pouvez désactiver les styles visuels pour l’info-bulle à l’aide de [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ATTÉNUATION \_ GETMARGIN**](ttm-getmargin.md)
</dt> </dl>

 

