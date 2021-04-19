---
description: Envoyé à une application lorsque le système d’exploitation est sur le ou la modification de l’éditeur IME actuel. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 5559b3ab-8d81-4f33-b0af-d05489371328
title: Message WM_IME_SELECT (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 940858e12c616b1d6281c23633b2f0f5e9657a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515865"
---
# <a name="wm_ime_select-message"></a>Message de sélection de l' \_ IME WM \_

Envoyé à une application lorsque le système d’exploitation est sur le ou la modification de l’éditeur IME actuel. Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,       
 WM_IME_SELECT,   
 WPARAM wParam,   
 LPARAM lParam    
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de fenêtre.

</dd> <dt>

*wParam* 
</dt> <dd>

Indicateur de sélection. Ce paramètre spécifie la **valeur true** si l’IME indiqué est sélectionné. Le paramètre a la valeur **false** si l’IME spécifié n’est plus sélectionné.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificateur de paramètres régionaux d’entrée associé à l’IME.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message n’a pas de valeur de retour.

## <a name="remarks"></a>Notes

Une application qui a créé une fenêtre IME doit transmettre ce message à cette fenêtre afin qu’il puisse récupérer le handle de la disposition du clavier vers l’IME nouvellement sélectionné.

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  traite ce message en transmettant les informations à la fenêtre IME par défaut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de méthode d’entrée](input-method-manager.md)
</dt> <dt>

[Messages du gestionnaire de méthode d’entrée](input-method-manager-messages.md)
</dt> </dl>

 

 
