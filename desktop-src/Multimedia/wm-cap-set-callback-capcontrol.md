---
title: Message WM_CAP_SET_CALLBACK_CAPCONTROL (VFW. h)
description: Le \_ message WM Cap \_ Set \_ callback \_ CAPCONTROL définit une fonction de rappel dans l’application, ce qui lui donne un contrôle d’enregistrement précis. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetCallbackOnCapControl.
ms.assetid: 1e93ed7b-8205-45fe-bdcf-efe3f709f728
keywords:
- message WM_CAP_SET_CALLBACK_CAPCONTROL Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_CAPCONTROL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fda38bbc79461b7c5ccaf9b3a32c2c3a0f9e3e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110749"
---
# <a name="wm_cap_set_callback_capcontrol-message"></a>\_ \_ \_ Message CAPCONTROL de rappel Set callback \_ de WM

Le message **WM \_ Cap \_ Set \_ callback \_ CAPCONTROL** définit une fonction de rappel dans l’application, ce qui lui donne un contrôle d’enregistrement précis. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) .


```C++
WM_CAP_SET_CALLBACK_CAPCONTROL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Pointeur vers la fonction de rappel, de type [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback). Spécifiez **null** pour ce paramètre pour désactiver une fonction de rappel précédemment installée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** si une capture de streaming ou une session de capture de trame unique est en cours.

## <a name="remarks"></a>Notes

Une fonction de rappel unique est utilisée pour permettre à l’application de contrôler précisément le moment où la capture de la diffusion en continu commence et se termine. La fenêtre de capture appelle d’abord la procédure avec *nState* défini sur le \_ préroll CONTROLCALLBACK une fois que toutes les mémoires tampons ont été allouées et que toutes les autres préparations de capture sont terminées. Cela donne à l’application la possibilité de Prérouler des sources vidéo, en retournant à partir de la fonction de rappel à l’enregistrement exact du moment. La valeur de retour **true** de la fonction de rappel continue la capture et la valeur de retour **false** abandonne la capture. Une fois la capture commencée, cette fonction de rappel est appelée fréquemment avec *nState* défini sur la \_ capture CONTROLCALLBACK pour permettre à l’application de terminer la capture en renvoyant **false**.

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

 

 





