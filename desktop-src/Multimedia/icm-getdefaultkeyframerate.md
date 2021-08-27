---
title: Message ICM_GETDEFAULTKEYFRAMERATE (VFW. h)
description: le \_ message ICM GETDEFAULTKEYFRAMERATE interroge un pilote de compression vidéo pour son espacement de trame de clé par défaut (ou préféré). Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICGetDefaulteyFrameRate.
ms.assetid: 2ebe37cc-3ec2-4b52-bd8f-71c44b704647
keywords:
- message ICM_GETDEFAULTKEYFRAMERATE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTKEYFRAMERATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff21682f08dfdcda120f5efb5f7f8629a9e93e21faaf27ff4ee9ee59da8c762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038699"
---
# <a name="icm_getdefaultkeyframerate-message"></a>ICM \_ Message GETDEFAULTKEYFRAMERATE

le message **ICM \_ GETDEFAULTKEYFRAMERATE** interroge un pilote de compression vidéo pour son espacement de trame de clé par défaut (ou préféré). Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICGetDefaulteyFrameRate**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultkeyframerate) .


```C++
ICM_GETDEFAULTKEYFRAMERATE 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Adresse qui doit contenir l’espacement de l’image clé préféré.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK si le pilote prend en charge ce message ou ICERR \_ non pris en charge dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de compression vidéo](video-compression-manager.md)
</dt> <dt>

[Messages de compression vidéo](video-compression-messages.md)
</dt> </dl>

 

 





