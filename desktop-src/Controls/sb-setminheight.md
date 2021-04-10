---
title: Message SB_SETMINHEIGHT (commctrl. h)
description: Définit la hauteur minimale de la zone de dessin d’une fenêtre d’État.
ms.assetid: 346fe654-f808-4191-9c3d-f9a4def08df1
keywords:
- SB_SETMINHEIGHT les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942545"
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

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

La hauteur minimale est la somme de *wParam* et du double de la largeur, en pixels, de la bordure verticale de la fenêtre d’État. Une application doit envoyer le message de [**\_ taille WM**](/windows/desktop/winmsg/wm-size) à la fenêtre d’État pour redessiner la fenêtre. Les paramètres *wParam* et *lParam* du message **de \_ taille WM** doivent être définis sur zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

