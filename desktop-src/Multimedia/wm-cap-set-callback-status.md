---
title: Message WM_CAP_SET_CALLBACK_STATUS (VFW. h)
description: Le \_ message WM Cap \_ Set \_ callback \_ Status définit une fonction de rappel d’État dans l’application. AVICap appelle cette procédure à chaque modification de l’état de la fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetCallbackOnStatus.
ms.assetid: 451ba9f9-7bfb-4c57-af6c-d5f691f39618
keywords:
- message WM_CAP_SET_CALLBACK_STATUS Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 493893a51d51b1ce61d43ff54461bb71c08a9f6a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110745"
---
# <a name="wm_cap_set_callback_status-message"></a>\_Message d' \_ \_ État de rappel \_ de la définition de l’embout WM

Le message **WM \_ Cap \_ Set \_ callback \_ Status** définit une fonction de rappel d’État dans l’application. AVICap appelle cette procédure à chaque modification de l’état de la fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) .


```C++
WM_CAP_SET_CALLBACK_STATUS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Pointeur vers la fonction de rappel d’État, de type [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka). Spécifiez **null** pour ce paramètre pour désactiver une fonction de rappel d’état précédemment installée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** si la capture en continu ou une session de capture de trame unique est en cours.

## <a name="remarks"></a>Notes

Les applications peuvent éventuellement définir une fonction de rappel d’État. Si cette valeur est définie, AVICap appelle cette procédure dans les cas suivants :

-   Une session de capture est terminée.
-   Un pilote de capture s’est correctement connecté à une fenêtre de capture.
-   Une palette optimale est créée.
-   Le nombre de frames capturés est signalé.

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

 

 





