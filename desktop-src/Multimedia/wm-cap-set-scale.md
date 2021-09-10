---
title: Message WM_CAP_SET_SCALE (VFW. h)
description: Le \_ message WM embout \_ Set \_ Scale active ou désactive la mise à l’échelle des images vidéo en préversion.
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- message WM_CAP_SET_SCALE Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCALE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd3bfc5dc463d84c935f994519060c33f89b8c0a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368036"
---
# <a name="wm_cap_set_scale-message"></a>Message de mise à l’échelle du jeu de \_ connexions WM \_ \_

Le message **WM \_ embout \_ Set \_ Scale** active ou désactive la mise à l’échelle des images vidéo en préversion. Si la mise à l’échelle est activée, l’image vidéo capturée est étirée sur les dimensions de la fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) .


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="f"></span><span id="F"></span>*FA*
</dt> <dd>

Indicateur de mise à l’échelle de l’aperçu. Spécifiez **true** pour que ce paramètre étire les images d’aperçu à la taille de la fenêtre de capture ou **false** pour les afficher à leur taille naturelle.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

La mise à l’échelle des images d’aperçu contrôle la présentation immédiate des frames capturés dans la fenêtre de capture. Elle n’a aucun effet sur la taille des frames enregistrés dans le fichier.

La mise à l’échelle n’a aucun effet lors de l’utilisation de la superposition pour afficher la vidéo dans la mémoire tampon de trame.

## <a name="requirements"></a>Spécifications



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

 

 





