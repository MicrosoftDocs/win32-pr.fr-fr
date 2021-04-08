---
description: Envoyé à une fenêtre que l’utilisateur redimensionne. En traitant ce message, une application peut surveiller la taille et la position du rectangle de glissement et, si nécessaire, modifier sa taille ou sa position.
ms.assetid: 8cf56194-8a10-48e1-b0eb-aa3d66896599
title: Message WM_SIZING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ab865994352eba28cdebaff3faab72a484ce0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756633"
---
# <a name="wm_sizing-message"></a>\_Message de dimensionnement WM

Envoyé à une fenêtre que l’utilisateur redimensionne. En traitant ce message, une application peut surveiller la taille et la position du rectangle de glissement et, si nécessaire, modifier sa taille ou sa position.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_SIZING                       0x0214
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Bord de la fenêtre en cours de dimensionnement. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                         | Signification                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| <span id="WMSZ_BOTTOM"></span><span id="wmsz_bottom"></span><dl> <dt>**WMSZ \_**</dt> <dt>6</dt> derniers </dl>                | Bord inférieur<br/>         |
| <span id="WMSZ_BOTTOMLEFT"></span><span id="wmsz_bottomleft"></span><dl> <dt>**WMSZ \_ BOTTOMLEFT**</dt> <dt>7</dt> </dl>    | Angle inférieur gauche<br/>  |
| <span id="WMSZ_BOTTOMRIGHT"></span><span id="wmsz_bottomright"></span><dl> <dt>**WMSZ \_ BOTTOMRIGHT**</dt> <dt>8</dt> </dl> | Coin inférieur droit<br/> |
| <span id="WMSZ_LEFT"></span><span id="wmsz_left"></span><dl> <dt>**WMSZ \_ GAUCHE**</dt> <dt>1</dt> </dl>                      | Bord gauche<br/>           |
| <span id="WMSZ_RIGHT"></span><span id="wmsz_right"></span><dl> <dt>**WMSZ \_ DROIT**</dt> <dt>2</dt> </dl>                   | Bord droit<br/>          |
| <span id="WMSZ_TOP"></span><span id="wmsz_top"></span><dl> <dt>**WMSZ \_**</dt> <dt>3</dt> premiers </dl>                         | Bord supérieur<br/>            |
| <span id="WMSZ_TOPLEFT"></span><span id="wmsz_topleft"></span><dl> <dt>**WMSZ \_ GAUCHE**</dt> <dt>4</dt> </dl>             | Coin supérieur gauche<br/>     |
| <span id="WMSZ_TOPRIGHT"></span><span id="wmsz_topright"></span><dl> <dt>**WMSZ \_ À droite**</dt> <dt>5</dt> </dl>          | Coin supérieur droit<br/>    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) avec les coordonnées d’écran du rectangle de glissement. Pour modifier la taille ou la position du rectangle de glissement, une application doit modifier les membres de cette structure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Une application doit retourner la **valeur true** si elle traite ce message.

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

[**dédéplacement de WM \_**](wm-moving.md)
</dt> <dt>

[**taille du WM \_**](wm-size.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**RECTANGULAIRE**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

 
