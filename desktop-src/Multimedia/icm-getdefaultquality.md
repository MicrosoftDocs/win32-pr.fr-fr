---
title: Message ICM_GETDEFAULTQUALITY (VFW. h)
description: le \_ message ICM GETDEFAULTQUALITY interroge un pilote de compression vidéo pour fournir son paramètre de qualité par défaut. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICGetDefaultQuality.
ms.assetid: bba7f451-52c2-4684-a7c9-e4b05cb946c5
keywords:
- message ICM_GETDEFAULTQUALITY Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETDEFAULTQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4350539851ca720e3538d297f955a56fedfc4a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195272"
---
# <a name="icm_getdefaultquality-message"></a>ICM \_ Message GETDEFAULTQUALITY

le message **ICM \_ GETDEFAULTQUALITY** interroge un pilote de compression vidéo pour fournir son paramètre de qualité par défaut. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICGetDefaultQuality**](/windows/desktop/api/Vfw/nf-vfw-icgetdefaultquality) .


```C++
ICM_GETDEFAULTQUALITY 
wParam = (DWORD_PTR) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Adresse qui doit contenir la valeur de qualité par défaut. Les valeurs de qualité sont comprises entre 0 et 10 000.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK si le pilote prend en charge ce message ou ICERR \_ non pris en charge dans le cas contraire.

## <a name="requirements"></a>Spécifications



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

 

 





