---
title: Message TB_SETPADDING (commctrl. h)
description: Définit la marge intérieure d’un contrôle de barre d’outils.
ms.assetid: a18c4efb-1140-4149-8dce-dfc1f03bb61a
keywords:
- TB_SETPADDING les contrôles de Windows de message
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
ms.openlocfilehash: da488c7aab3a6856fd1bd8db6911336eb52881da396e287937678600158d9655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078163"
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

## <a name="remarks"></a>Remarques

Les valeurs de remplissage sont utilisées pour créer une zone vide entre le bord du bouton et l’image et/ou le texte du bouton. L’emplacement et la quantité de remplissage réellement appliqués dépendent du type du bouton et de la présence ou non d’une image. Le remplissage horizontal est appliqué à droite et à gauche du bouton, et le remplissage vertical est appliqué à la fois au haut et au bas du bouton. Le remplissage est appliqué uniquement aux boutons qui ont le style de [**\_ redimensionnement automatique TBSTYLE**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TO \_ GETPADDING**](tb-getpadding.md)
</dt> </dl>

 

