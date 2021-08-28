---
title: Message MCIWNDM_PUT_SOURCE (VFW. h)
description: Le \_ \_ message source MCIWNDM place redéfinit les coordonnées du rectangle source utilisé pour le rognage des images d’un fichier AVI lors de la lecture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndPutSource.
ms.assetid: cff95139-0302-4db3-bf2e-559e75257e85
keywords:
- message MCIWNDM_PUT_SOURCE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c21e11142a1b47a8984712de664151b686cfa3c3cb9bf153dcbc2a23fa459c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807779"
---
# <a name="mciwndm_put_source-message"></a>MCIWNDM \_ Placer le \_ message source

Le **message \_ \_ source MCIWNDM place** redéfinit les coordonnées du rectangle source utilisé pour le rognage des images d’un fichier AVI lors de la lecture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) .


```C++
MCIWNDM_PUT_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*République*
</dt> <dd>

Pointeur vers une structure [Rect](/previous-versions//ms536136(v=vs.85)) contenant les coordonnées du rectangle source.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne zéro en cas de réussite ou une erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



 

