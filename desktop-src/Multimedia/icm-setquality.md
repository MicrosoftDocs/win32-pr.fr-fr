---
title: Message ICM_SETQUALITY (VFW. h)
description: le \_ message ICM SETQUALITY fournit un pilote de compression vidéo avec un niveau de qualité à utiliser pendant la compression.
ms.assetid: 487ff1de-7178-440a-b38d-0b82a30d7297
keywords:
- message ICM_SETQUALITY Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_SETQUALITY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adb840b3dc283d0cd81b4662322e0571b8e687bbdd4b6e7009a6fa1786e95920
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784909"
---
# <a name="icm_setquality-message"></a>ICM \_ Message SETQUALITY

le message **ICM \_ SETQUALITY** fournit un pilote de compression vidéo avec un niveau de qualité à utiliser pendant la compression.


```C++
ICM_SETQUALITY 
wParam = (DWORD) (LPVOID) &dwICValue; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="dwICValue"></span><span id="dwicvalue"></span><span id="DWICVALUE"></span>*dwICValue*
</dt> <dd>

Nouvelle valeur de qualité. Les valeurs de qualité sont comprises entre 0 et 10 000.

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

 

 





