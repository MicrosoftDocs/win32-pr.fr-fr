---
description: Envoyé à une fenêtre lorsque la fenêtre va être masquée ou affichée.
ms.assetid: dea7c9aa-eba7-4b93-a4c5-9b2d36999780
title: Message WM_SHOWWINDOW (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbca6cbb4c73ff1cad31754b1b581e0c892970e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319205"
---
# <a name="wm_showwindow-message"></a>\_Message ShowWindow WM

Envoyé à une fenêtre lorsque la fenêtre va être masquée ou affichée.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_SHOWWINDOW                   0x0018
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Indique si une fenêtre est affichée. Si *wParam* a la **valeur true**, la fenêtre est affichée. Si *wParam* a la **valeur false**, la fenêtre est masquée.

</dd> <dt>

*lParam* 
</dt> <dd>

État de la fenêtre affichée. Si *lParam* est égal à zéro, le message a été envoyé en raison d’un appel à la fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) ; dans le cas contraire, *lParam* est l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                         | Signification                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="SW_OTHERUNZOOM"></span><span id="sw_otherunzoom"></span><dl> <dt>**Logiciels \_ OTHERUNZOOM**</dt> <dt>4</dt> </dl>       | La fenêtre est en cours de récupération, car une fenêtre agrandie a été restaurée ou réduite.<br/> |
| <span id="SW_OTHERZOOM"></span><span id="sw_otherzoom"></span><dl> <dt>**Logiciels \_ OTHERZOOM**</dt> <dt>2</dt> </dl>             | La fenêtre est couverte par une autre fenêtre qui a été agrandie.<br/>             |
| <span id="SW_PARENTCLOSING"></span><span id="sw_parentclosing"></span><dl> <dt>**Logiciels \_ PARENTCLOSING**</dt> <dt>1</dt> </dl> | La fenêtre propriétaire de la fenêtre est réduite.<br/>                                      |
| <span id="SW_PARENTOPENING"></span><span id="sw_parentopening"></span><dl> <dt>**Logiciels \_ PARENTOPENING**</dt> <dt>3</dt> </dl> | La fenêtre propriétaire de la fenêtre est en cours de restauration.<br/>                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) masque ou affiche la fenêtre, comme spécifié par le message. Si une fenêtre a le style [**WS \_ visible**](window-styles.md) lors de sa création, la fenêtre reçoit ce message après sa création, mais avant son affichage. Une fenêtre reçoit également ce message lorsque son état de visibilité est modifié par la fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) ou [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) .

Le message **WM \_ ShowWindow** n’est pas envoyé dans les circonstances suivantes :

-   Quand une fenêtre de niveau supérieur, avec chevauchement est créée avec le style [**WS \_ Maximize**](window-styles.md) ou **WS \_ Minimize** .
-   Lorsque l’indicateur **SW \_ SHOWNORMAL** est spécifié dans l’appel à la fonction [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) .

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups)
</dt> <dt>

[**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
