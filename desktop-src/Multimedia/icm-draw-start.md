---
title: Message ICM_DRAW_START (VFW. h)
description: Le \_ message de début de dessin ICM \_ indique à un pilote de rendu de démarrer son horloge interne pour le minutage des frames de dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawStart.
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- Message ICM_DRAW_START Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_START
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538659eb9878be819ee6ec1506403fcce314eb0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384483"
---
# <a name="icm_draw_start-message"></a>Message de début de \_ dessin ICM \_

Le message de **\_ \_ début de dessin ICM** indique à un pilote de rendu de démarrer son horloge interne pour le minutage des frames de dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) .


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Ce message est utilisé par le matériel qui effectue sa propre décompression, son minutage et son dessin asynchrones.

Lorsque le pilote reçoit ce message, il doit commencer à afficher les données à la fréquence spécifiée avec le message de [**\_ \_ début**](icm-draw-begin.md) de l’ICM.

Les messages d' [**\_ \_ arrêt**](icm-draw-stop.md) de dessin **ICM \_ \_** et ICM ne sont pas imbriqués. Si votre pilote reçoit **le \_ dessin \_ ICM, démarrer** avant l’arrêt du rendu avec **ICM \_ Draw \_ Stop**, il doit redémarrer le rendu avec de nouveaux paramètres.

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

 

 





