---
title: Message ICM_GETBUFFERSWANTED (VFW. h)
description: le \_ message ICM GETBUFFERSWANTED interroge un pilote sur le nombre de mémoires tampons à allouer. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICGetBuffersWanted.
ms.assetid: 109e8627-7ed4-4f17-bf7f-e77f42dfc8c7
keywords:
- message ICM_GETBUFFERSWANTED Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETBUFFERSWANTED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06de8cc3bcfe463d0318651c8e2d51b269504769
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364215"
---
# <a name="icm_getbufferswanted-message"></a>ICM \_ Message GETBUFFERSWANTED

le message **ICM \_ GETBUFFERSWANTED** interroge un pilote sur le nombre de mémoires tampons à allouer. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) .


```C++
ICM_GETBUFFERSWANTED 
wParam = (DWORD_PTR) (LPVOID) lpdwBuffers; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpdwBuffers"></span><span id="lpdwbuffers"></span><span id="LPDWBUFFERS"></span>*lpdwBuffers*
</dt> <dd>

Adresse qui contient le nombre d’échantillons dont le pilote a besoin pour restituer efficacement les données.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou ICERR \_ non pris en charge dans le cas contraire.

## <a name="remarks"></a>Remarques

Ce message est utilisé par les pilotes qui utilisent le matériel pour afficher les données et qui souhaitent garantir un délai minimal en raison de l’arrivée d’une mémoire tampon. Par exemple, si un pilote contrôle une carte de décompression vidéo qui peut contenir 10 images vidéo, il peut renvoyer 10 pour ce message. Cela indique aux applications d’essayer de conserver 10 frames à l’avance du frame dont il a besoin.

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

 

 





