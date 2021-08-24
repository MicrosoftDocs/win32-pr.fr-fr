---
description: Envoyé par une application pour indiquer à la fenêtre IME d’exécuter la commande demandée.
ms.assetid: 5d3b7f8a-57c9-41e3-8022-9a3f515fc32e
title: Message WM_IME_CONTROL (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104ef8eb2a90c7c55eb0d4bca2fcdb1744dd9433f131b753e962fcfec571f43d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822469"
---
# <a name="wm_ime_control-message"></a>Message WM_IME_CONTROL

Envoyé par une application pour indiquer à la fenêtre IME d’exécuter la commande demandée. L’application utilise ce message pour contrôler la fenêtre IME qu’elle a créée. Pour envoyer ce message, l’application appelle la fonction [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) avec les paramètres suivants.


```C++
SendMessage(
  HWND   hwnd,
  WM_IME_CONTROL, 
  WPARAM wParam,
  LPARAM lParam             
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle vers la fenêtre.

</dd> <dt>

*wParam* 
</dt> <dd>

Commande. Ce paramètre peut prendre l'une des valeurs suivantes :

<dl>
<dd><a href="imc-closestatuswindow.md">IMC_CLOSESTATUSWINDOW</a></dd> 
<dd><a href="imc-getcandidatepos.md">IMC_GETCANDIDATEPOS</a></dd> 
<dd><a href="imc-getcompositionfont.md">IMC_GETCOMPOSITIONFONT</a></dd> 
<dd><a href="imc-getcompositionwindow.md">IMC_GETCOMPOSITIONWINDOW</a></dd> 
<dd><a href="imc-getstatuswindowpos.md">IMC_GETSTATUSWINDOWPOS</a></dd> 
<dd><a href="imc-openstatuswindow.md">IMC_OPENSTATUSWINDOW</a></dd> 
<dd><a href="imc-setcandidatepos.md">IMC_SETCANDIDATEPOS</a></dd> 
<dd><a href="imc-setcompositionfont.md">IMC_SETCOMPOSITIONFONT</a>></dd> 
<dd><a href="imc-setcompositionwindow.md">IMC_SETCOMPOSITIONWINDOW</a></dd> 
<dd><a href="imc-setstatuswindowpos.md">IMC_SETSTATUSWINDOWPOS</a></dd> 
</dl>
</dd>

<dt>

*lParam* 
</dt> <dd>

Données spécifiques à la commande, avec un format dépendant de la valeur du paramètre *wParam* . Pour plus d’informations, reportez-vous à la documentation de chaque commande.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Le message retourne une valeur spécifique à la commande.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                                                      |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h);</dt> <dt>Imm. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de méthode d’entrée](input-method-manager.md)
</dt> <dt>

[Messages du gestionnaire de méthode d’entrée](input-method-manager-messages.md)
</dt> <dt>

[IMC_CLOSESTATUSWINDOW](imc-closestatuswindow.md)
</dt> <dt>

[IMC_GETCANDIDATEPOS](imc-getcandidatepos.md)
</dt> <dt>

[IMC_GETCOMPOSITIONFONT](imc-getcompositionfont.md)
</dt> <dt>

[IMC_GETCOMPOSITIONWINDOW](imc-getcompositionwindow.md)
</dt> <dt>

[IMC_GETSTATUSWINDOWPOS](imc-getstatuswindowpos.md)
</dt> <dt>

[IMC_OPENSTATUSWINDOW](imc-openstatuswindow.md)
</dt> <dt>

[IMC_SETCANDIDATEPOS](imc-setcandidatepos.md)
</dt> <dt>

[IMC_SETCOMPOSITIONFONT](imc-setcompositionfont.md)
</dt> <dt>

[IMC_SETCOMPOSITIONWINDOW](imc-setcompositionwindow.md)
</dt> <dt>

[IMC_SETSTATUSWINDOWPOS](imc-setstatuswindowpos.md)
</dt> </dl>

 

 
