---
description: Envoyé à une application pour fournir des commandes et demander des informations. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: c5e9f256-eed2-46cb-bb33-0e640a975f1f
title: Message WM_IME_REQUEST (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d0cea120d088fe1423b1d7dcb822307886675b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514190"
---
# <a name="wm_ime_request-message"></a>Message WM_IME_REQUEST

Envoyé à une application pour fournir des commandes et demander des informations. Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,       
  WM_IME_REQUEST,  
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

Commande. Ce paramètre peut prendre l'une des valeurs suivantes :

<dl> 
<dd><a href="imr-candidatewindow.md">IMR_CANDIDATEWINDOW</a></dd> 
<dd><a href="imr-compositionfont.md">IMR_COMPOSITIONFONT</a></dd> 
<dd><a href="imr-compositionwindow.md">IMR_COMPOSITIONWINDOW</a></dd> 
<dd><a href="imr-confirmreconvertstring.md">IMR_CONFIRMRECONVERTSTRING</a></dd> 
<dd><a href="imr-documentfeed.md">IMR_DOCUMENTFEED</a></dd> 
<dd><a href="imr-querycharposition.md">IMR_QUERYCHARPOSITION</a></dd> 
<dd><a href="imr-reconvertstring.md">IMR_RECONVERTSTRING</a></dd> 
</dl> 
</dd> 
<dt>

*lParam* 
</dt> <dd>

Données spécifiques à la commande. Pour plus d’informations, consultez la description de chaque commande.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur spécifique à une commande.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                                                      |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h); </dt> <dt>IMM. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de méthode d’entrée](input-method-manager.md)
</dt> <dt>

[Messages du gestionnaire de méthode d’entrée](input-method-manager-messages.md)
</dt> <dt>

[IMR_CANDIDATEWINDOW](imr-candidatewindow.md)
</dt> <dt>

[IMR_COMPOSITIONFONT](imr-compositionfont.md)
</dt> <dt>

[IMR_COMPOSITIONWINDOW](imr-compositionwindow.md)
</dt> <dt>

[IMR_CONFIRMRECONVERTSTRING](imr-confirmreconvertstring.md)
</dt> <dt>

[IMR_DOCUMENTFEED](imr-documentfeed.md)
</dt> <dt>

[IMR_QUERYCHARPOSITION](imr-querycharposition.md)
</dt> <dt>

[IMR_RECONVERTSTRING](imr-reconvertstring.md)
</dt> </dl>

 

 
