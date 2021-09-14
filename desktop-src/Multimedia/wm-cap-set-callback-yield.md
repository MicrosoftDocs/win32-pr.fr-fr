---
title: Message WM_CAP_SET_CALLBACK_YIELD (VFW. h)
description: Le \_ message WM Cap \_ Set \_ callback \_ yield définit une fonction de rappel dans l’application. AVICap appelle cette procédure lorsque la fenêtre de capture est obtenue pendant la capture en continu. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetCallbackOnYield.
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- message WM_CAP_SET_CALLBACK_YIELD Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_YIELD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95c9ba0be7a0abeb99c0590e255adb0bd442343
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110737"
---
# <a name="wm_cap_set_callback_yield-message"></a>\_Message de \_ \_ \_ régénérer le rappel de la définition de l’embout WM

Le message **WM \_ Cap \_ Set \_ callback \_ yield** définit une fonction de rappel dans l’application. AVICap appelle cette procédure lorsque la fenêtre de capture est obtenue pendant la capture en continu. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) .


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Pointeur vers la fonction de rappel yield, de type [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback). Spécifiez **null** pour ce paramètre pour désactiver une fonction de rappel yield précédemment installée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** si la capture en continu ou une session de capture de trame unique est en cours.

## <a name="remarks"></a>Notes

Les applications peuvent éventuellement définir une fonction de rappel yield. La fonction de rappel Yield est appelée au moins une fois pour chaque image vidéo capturée pendant la capture en continu. Si une fonction de rappel Yield est installée, elle est appelée indépendamment de l’état du membre **fYield** de la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .

Si la fonction de rappel Yield est utilisée, elle doit être installée avant le démarrage de la session de capture et elle doit rester activée pendant toute la durée de la session. Elle peut être désactivée après la fin de la capture de streaming.

Les applications exécutent généralement un certain type de traitement des messages dans la fonction de rappel composée d’une boucle [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) , comme dans la boucle de message d’une fonction [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) . La fonction de rappel yield doit également filtrer et supprimer les messages qui peuvent provoquer des problèmes de réentrance.

Une application retourne généralement la **valeur true** dans la procédure yield pour continuer la capture de la diffusion en continu. Si une fonction de rappel yield retourne la **valeur false**, la fenêtre de capture arrête le processus de capture.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Capture vidéo](video-capture.md)
</dt> <dt>

[Messages de capture vidéo](video-capture-messages.md)
</dt> </dl>

 

