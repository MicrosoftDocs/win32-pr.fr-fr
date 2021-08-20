---
title: Message ICM_COMPRESS_FRAMES_INFO (VFW. h)
description: le \_ message d’informations ICM compresser les \_ frames \_ indique à un pilote de compression de définir les paramètres de la compression en attente.
ms.assetid: d2f6f3b7-dff6-4fef-a642-cb77b00119af
keywords:
- message ICM_COMPRESS_FRAMES_INFO Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_FRAMES_INFO
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2382a930b0ce12e212adf78ddaf3c7e1b3300e47597b4671d0eae223cb536f73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140910"
---
# <a name="icm_compress_frames_info-message"></a>ICM \_ Message d’informations de compression des \_ frames \_

le message d' **\_ informations ICM compresser les \_ frames \_** indique à un pilote de compression de définir les paramètres de la compression en attente.


```C++
ICM_COMPRESS_FRAMES_INFO 
wParam = (DWORD) (LPVOID) &icf; 
lParam = sizeof(ICCOMPRESSFRAMES); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="icf"></span><span id="ICF"></span>*ICF*
</dt> <dd>

Pointeur vers une structure [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes) . Les membres **GetData** et **PutData** de cette structure ne sont pas utilisés avec ce message.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Taille, en octets, de [**ICCOMPRESSFRAMES**](/windows/desktop/api/Vfw/ns-vfw-iccompressframes).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

Un compresseur peut utiliser ce message pour déterminer la quantité d’espace à allouer pour chaque image pendant la compression.

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

 

 





