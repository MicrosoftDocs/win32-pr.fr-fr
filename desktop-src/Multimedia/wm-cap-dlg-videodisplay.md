---
title: Message WM_CAP_DLG_VIDEODISPLAY (VFW. h)
description: Le \_ message WM Cap \_ DLG \_ VIDEODISPLAY affiche une boîte de dialogue dans laquelle l’utilisateur peut définir ou ajuster la sortie vidéo.
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- message WM_CAP_DLG_VIDEODISPLAY Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEODISPLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16afffbf1d3450670b99d26303627771aa4bd3399a252cd16a68bc690012f541
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803869"
---
# <a name="wm_cap_dlg_videodisplay-message"></a>\_Message WM Cap \_ DLG \_ VIDEODISPLAY

Le message **WM \_ Cap \_ DLG \_ VIDEODISPLAY** affiche une boîte de dialogue dans laquelle l’utilisateur peut définir ou ajuster la sortie vidéo. Cette boîte de dialogue peut contenir des contrôles qui affectent la teinte, le contraste et la luminosité de l’image affichée, ainsi que l’alignement des couleurs des touches. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) .


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Les contrôles de cette boîte de dialogue n’affectent pas les données vidéo numérisées ; elles affectent uniquement la sortie ou le réaffichage du signal vidéo.

La boîte de dialogue affichage vidéo est unique pour chaque pilote de capture. Certains pilotes de capture peuvent ne pas prendre en charge une boîte de dialogue d’affichage vidéo. Les applications peuvent déterminer si le pilote de capture prend en charge ce message en vérifiant le membre **fHasDlgVideoDisplay** de la structure [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Capture vidéo](video-capture.md)
</dt> <dt>

[Messages de capture vidéo](video-capture-messages.md)
</dt> </dl>

 

 





