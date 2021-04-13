---
title: Message WM_HSCROLLCLIPBOARD (winuser. h)
description: Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers.
ms.assetid: 73558de6-a822-40f7-9eb2-47ea5afd4e6e
keywords:
- WM_HSCROLLCLIPBOARD l’échange de données de message
topic_type:
- apiref
api_name:
- WM_HSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34ee33709601b483258ae0aec4873c47fa69a00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466366"
---
# <a name="wm_hscrollclipboard-message"></a>\_Message WM HSCROLLCLIPBOARD

Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers. Cela se produit lorsque le presse-papiers contient des données au format [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) et qu’un événement se produit dans la barre de défilement horizontale de la visionneuse du presse-papiers. Le propriétaire doit faire défiler l’image du presse-papiers et mettre à jour les valeurs de la barre de défilement.


```C++
#define WM_HSCROLLCLIPBOARD             0x030E
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre de la visionneuse du presse-papiers.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible de *lParam* spécifie un événement de barre de défilement. Ce paramètre peut prendre les valeurs suivantes. Le mot de poids fort de *lParam* spécifie la position actuelle de la case de défilement si le mot de poids faible de *lParam* est **SB \_ THUMBPOSITION**; sinon, le mot de poids fort n’est pas utilisé.



| Valeur                                                                                                                                                                                                                         | Signification                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ENDSCROLL**</dt> <dt>8</dt> </dl>             | Fin du défilement.<br/>                                                                            |
| <span id="SB_LEFT"></span><span id="sb_left"></span><dl> <dt>**SB \_**</dt> <dt>6</dt> à gauche </dl>                            | Faites défiler vers le haut à gauche.<br/>                                                                  |
| <span id="SB_RIGHT"></span><span id="sb_right"></span><dl> <dt>**SB \_**</dt> <dt>7</dt> droits </dl>                         | Faites défiler vers la droite.<br/>                                                                 |
| <span id="SB_LINELEFT"></span><span id="sb_lineleft"></span><dl> <dt>**SB \_ LINELEFT**</dt> <dt>0</dt> </dl>                | Fait défiler d’une unité vers la gauche.<br/>                                                              |
| <span id="SB_LINERIGHT"></span><span id="sb_lineright"></span><dl> <dt>**SB \_ LINERIGHT**</dt> <dt>1</dt> </dl>             | Fait défiler vers la droite d’une unité.<br/>                                                             |
| <span id="SB_PAGELEFT"></span><span id="sb_pageleft"></span><dl> <dt>**SB \_ PAGELEFT**</dt> <dt>2</dt> </dl>                | Fait défiler vers la gauche de la largeur de la fenêtre.<br/>                                               |
| <span id="SB_PAGERIGHT"></span><span id="sb_pageright"></span><dl> <dt>**SB \_ ÉPINGLÉE**</dt> <dt>3</dt> </dl>             | Fait défiler la largeur de la fenêtre vers la droite.<br/>                                              |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt> </dl> | Faites défiler jusqu’à position absolue. La position actuelle est spécifiée par le mot de poids fort.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Le propriétaire du presse-papiers peut utiliser la fonction [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) pour faire défiler l’image dans la fenêtre de la visionneuse du presse-papiers et invalider la région appropriée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Presse-papiers](clipboard.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)
</dt> </dl>

 

