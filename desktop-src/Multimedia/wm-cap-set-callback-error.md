---
title: Message WM_CAP_SET_CALLBACK_ERROR (VFW. h)
description: Le \_ \_ \_ message d’erreur WM Cap Set callback \_ définit une fonction de rappel d’erreur dans l’application cliente. AVICap appelle cette procédure lorsque des erreurs se produisent. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capSetCallbackOnError.
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- Message WM_CAP_SET_CALLBACK_ERROR Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_ERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f50d62112d71f78196a17b958dc7d3d10702e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465662"
---
# <a name="wm_cap_set_callback_error-message"></a>Message d’erreur de rappel de l' \_ \_ ensemble de connexions WM \_ \_

Le message d' **\_ erreur WM Cap \_ Set \_ callback \_** définit une fonction de rappel d’erreur dans l’application cliente. AVICap appelle cette procédure lorsque des erreurs se produisent. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) .


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*
</dt> <dd>

Pointeur vers la fonction de rappel d’erreur, de type [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka). Spécifiez **null** pour ce paramètre pour désactiver une fonction de rappel d’erreur précédemment installée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** si la capture en continu ou une session de capture de trame unique est en cours.

## <a name="remarks"></a>Notes

Les applications peuvent éventuellement définir une fonction de rappel d’erreur. Si cette valeur est définie, AVICap appelle la procédure d’erreur dans les situations suivantes :

-   Le disque est plein.
-   Une fenêtre de capture ne peut pas être connectée à un pilote de capture.
-   Impossible d’ouvrir un appareil Waveform-Audio.
-   Le nombre de trames supprimées pendant la capture dépasse le pourcentage spécifié.
-   Les trames ne peuvent pas être capturées en raison de problèmes d’interruption de synchronisation verticale.

## <a name="requirements"></a>Configuration requise



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

 

 





