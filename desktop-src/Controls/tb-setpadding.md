---
title: Message TB_SETPADDING (commctrl. h)
description: Définit la marge intérieure d’un contrôle de barre d’outils.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- TB_SETPADDING les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_SETPADDING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65fae53f7e7702528915af7631bd675f11188b71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105751"
---
# <a name="tb_setpadding-message"></a>TO \_ SETPADDING message

Définit la marge intérieure d’un contrôle de barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la marge intérieure horizontale, en pixels. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le remplissage vertical, en pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **DWORD** qui contient le remplissage horizontal précédent dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) et le remplissage vertical précédent dans le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), en pixels.

## <a name="remarks"></a>Notes

Les valeurs de remplissage sont utilisées pour créer une zone vide entre le bord du bouton et l’image et/ou le texte du bouton. L’emplacement et la quantité de remplissage réellement appliqués dépendent du type du bouton et de la présence ou non d’une image. Le remplissage horizontal est appliqué à droite et à gauche du bouton, et le remplissage vertical est appliqué à la fois au haut et au bas du bouton. Le remplissage est appliqué uniquement aux boutons qui ont le style de [**\_ redimensionnement automatique TBSTYLE**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TO \_ GETPADDING**](tb-getpadding.md)
</dt> </dl>

 

