---
title: Message ICM_DRAW_WINDOW (VFW. h)
description: le \_ message ICM dessiner \_ une fenêtre notifie un pilote de rendu que la fenêtre spécifiée pour le \_ message de début de dessin ICM \_ doit être redessinée.
ms.assetid: 4df1b9a7-8d61-4e79-8f43-1e7ee266375c
keywords:
- message ICM_DRAW_WINDOW Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a1f66ca5beefa3d7eb774174bccc9d9482aebddd4a82341e9c83bb265d7788e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690920"
---
# <a name="icm_draw_window-message"></a>ICM \_ DESSINER un \_ message de fenêtre

le message **ICM \_ dessiner une \_ fenêtre** notifie un pilote de rendu que la fenêtre spécifiée pour le message de [**\_ \_ début de dessin ICM**](icm-draw-begin.md) doit être redessinée. La fenêtre a été déplacée ou devenue temporairement masquée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) .


```C++
ICM_DRAW_WINDOW 
wParam = (DWORD_PTR) (LPVOID) prc; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="prc"></span><span id="PRC"></span>*République*
</dt> <dd>

Pointeur vers le rectangle de destination en coordonnées d’écran. Si ce paramètre pointe vers un rectangle vide, le dessin doit être désactivé.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

Ce message est pris en charge par le matériel qui effectue sa propre décompression, son minutage et son dessin asynchrones.

Les pilotes vidéo-superposition utilisent ce message pour dessiner lorsque la fenêtre est masquée ou déplacée. quand une fenêtre spécifiée pour [**ICM \_ DRAW \_ BEGIN**](icm-draw-begin.md) est complètement masquée par d’autres fenêtres, le rectangle de destination est vide. Les pilotes doivent désactiver le matériel de superposition vidéo lorsque cette condition se produit.

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

 

 





