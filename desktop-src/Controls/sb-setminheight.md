---
title: Message SB_SETMINHEIGHT (commctrl. h)
description: Définit la hauteur minimale de la zone de dessin d’une fenêtre d’État.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- SB_SETMINHEIGHT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- SB_SETMINHEIGHT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bcad3bf0cb4d11567e82aae4ef46a95fefe3890
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117066"
---
# <a name="sb_setminheight-message"></a>\_Message SB SETMINHEIGHT

Définit la hauteur minimale de la zone de dessin d’une fenêtre d’État.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Hauteur minimale, en pixels, de la fenêtre.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

La hauteur minimale est la somme de *wParam* et du double de la largeur, en pixels, de la bordure verticale de la fenêtre d’État. Une application doit envoyer le message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) à la fenêtre d’État pour redessiner la fenêtre. Les paramètres *wParam* et *lParam* du message **de \_ taille WM** doivent être définis sur zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

