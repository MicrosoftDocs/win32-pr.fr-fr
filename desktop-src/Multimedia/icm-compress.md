---
title: Message ICM_COMPRESS (VFW. h)
description: le \_ message ICM compresser indique à un pilote de compression vidéo de compresser une trame de données dans une mémoire tampon définie par l’application.
ms.assetid: d95b943f-458d-4a5e-bab1-e3648d323395
keywords:
- message ICM_COMPRESS Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1230f429eb49596dd8a450b8a384e0a69856b69c51141834458c09fa41ca54d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678469"
---
# <a name="icm_compress-message"></a>ICM \_ Compresser le message

le message **ICM \_ compresser** indique à un pilote de compression vidéo de compresser une trame de données dans une mémoire tampon définie par l’application.


```C++
ICM_COMPRESS 
wParam = (DWORD) (LPVOID) &icc; 
lParam = sizeof(ICCOMPRESS); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="icc"></span><span id="ICC"></span>*rencontres*
</dt> <dd>

Pointeur vers une structure [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress) . Les membres suivants de cette structure spécifient les paramètres de compression suivants : **lpbiInput**, **lpInput**, **lpbiOutput**, **lpOutput**, **lpbiPrev**, **lpPrev**, **lpckid**, **lpdwFlags**, **dwFrameSize** et **dwQuality**. Le pilote doit également utiliser le membre **biSizeImage** de la structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) associée à **lpbiOutput** de **ICCOMPRESS** pour retourner la taille du frame compressé.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Taille, en octets, de [**ICCOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-iccompress).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

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

 

