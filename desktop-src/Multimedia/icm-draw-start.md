---
title: Message ICM_DRAW_START (VFW. h)
description: le \_ message ICM DRAW \_ START indique à un pilote de rendu de démarrer son horloge interne pour le minutage des frames de dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawStart.
ms.assetid: d49e0d97-5a29-46f7-82d7-e3d4b4f7666f
keywords:
- message ICM_DRAW_START Windows Multimedia
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
ms.openlocfilehash: 720d8c2f919d2b00955892a42ba8fca95b2b426c3cbb396aa4ac71a5cf912307
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690949"
---
# <a name="icm_draw_start-message"></a>ICM \_ DESSINER le \_ message de début

le message **ICM \_ DRAW \_ START** indique à un pilote de rendu de démarrer son horloge interne pour le minutage des frames de dessin. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) .


```C++
ICM_DRAW_START 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Ce message est utilisé par le matériel qui effectue sa propre décompression, son minutage et son dessin asynchrones.

lorsque le pilote reçoit ce message, il doit commencer à afficher les données à la fréquence spécifiée avec le message [**ICM \_ DRAW \_ BEGIN**](icm-draw-begin.md) .

le **ICM \_ dessiner \_ démarrer** et [**ICM \_ dessiner \_**](icm-draw-stop.md) les messages d’arrêt ne sont pas imbriques. si votre pilote reçoit **ICM \_ dessin \_ démarrer** avant l’arrêt du rendu avec **ICM \_ trace \_ STOP**, il doit redémarrer le rendu avec de nouveaux paramètres.

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

 

 





