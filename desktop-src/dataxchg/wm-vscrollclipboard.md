---
title: Message WM_VSCROLLCLIPBOARD (winuser. h)
description: Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers lorsque le presse-papiers contient des données au \_ format CF OWNERDISPLAY et qu’un événement se produit dans la barre de défilement verticale de la visionneuse du presse-papiers.
ms.assetid: 17bd32c4-1b07-42b7-b269-f517e3ec13f3
keywords:
- WM_VSCROLLCLIPBOARD des données de message Exchange
topic_type:
- apiref
api_name:
- WM_VSCROLLCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87a9e80aa342065ee88c8e1d7aa44c1fd598e411
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126852352"
---
# <a name="wm_vscrollclipboard-message"></a>\_Message WM VSCROLLCLIPBOARD

Envoyé au propriétaire du presse-papiers par une fenêtre de la visionneuse du presse-papiers lorsque le presse-papiers contient des données au format [**CF \_ OWNERDISPLAY**](standard-clipboard-formats.md) et qu’un événement se produit dans la barre de défilement verticale de la visionneuse du presse-papiers. Le propriétaire doit faire défiler l’image du presse-papiers et mettre à jour les valeurs de la barre de défilement.


```C++
#define WM_VSCROLLCLIPBOARD             0x030A
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre de la visionneuse du presse-papiers.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible de *lParam* spécifie un événement de barre de défilement. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                         | Signification                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="SB_BOTTOM"></span><span id="sb_bottom"></span><dl> <dt>**SB \_**</dt> <dt>7</dt> en bas </dl>                      | Faites défiler vers la droite.<br/>                                                                 |
| <span id="SB_ENDSCROLL"></span><span id="sb_endscroll"></span><dl> <dt>**SB \_ ENDSCROLL**</dt> <dt>8</dt> </dl>             | Fin du défilement.<br/>                                                                            |
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> <dt>1</dt> </dl>                | Faire défiler d’une ligne vers le dessous.<br/>                                                                  |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**SB \_ GAMME**</dt> <dt>0</dt> </dl>                      | Faire défiler d’une ligne vers le haut.<br/>                                                                    |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PG SUIV**</dt> <dt>3</dt> </dl>                | Faire défiler d’une page vers le dessous.<br/>                                                                  |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PG PRÉC**</dt> <dt>2</dt> </dl>                      | Faire défiler d’une page vers le haut.<br/>                                                                    |
| <span id="SB_THUMBPOSITION"></span><span id="sb_thumbposition"></span><dl> <dt>**SB \_ THUMBPOSITION**</dt> <dt>4</dt> </dl> | Faites défiler jusqu’à position absolue. La position actuelle est spécifiée par le mot de poids fort.<br/> |
| <span id="SB_TOP"></span><span id="sb_top"></span><dl> <dt>**SB \_**</dt> <dt>6</dt> premiers </dl>                               | Faites défiler vers le haut à gauche.<br/>                                                                  |



 

Le mot de poids fort de *lParam* spécifie la position actuelle de la case de défilement si le mot de poids faible de *lParam* est **SB \_ THUMBPOSITION**; dans le cas contraire, le mot de poids fort de *lParam* n’est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Le propriétaire du presse-papiers peut utiliser la fonction [**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx) pour faire défiler l’image dans la fenêtre de la visionneuse du presse-papiers et invalider la région appropriée.

## <a name="requirements"></a>Spécifications



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

**Conceptuel**
</dt> <dt>

[Presse-papiers](clipboard.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**ScrollWindow**](https://msdn.microsoft.com/library/Cc410994(v=MSDN.10).aspx)
</dt> </dl>

 

