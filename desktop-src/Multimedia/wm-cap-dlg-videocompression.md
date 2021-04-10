---
title: Message WM_CAP_DLG_VIDEOCOMPRESSION (VFW. h)
description: Le \_ message WM Cap \_ DLG \_ VIDEOCOMPRESSION affiche une boîte de dialogue dans laquelle l’utilisateur peut sélectionner un compresseur à utiliser pendant le processus de capture.
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- Message WM_CAP_DLG_VIDEOCOMPRESSION Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOCOMPRESSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d851f73df7adbc205585eb7c69ad9d4d969aba66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032829"
---
# <a name="wm_cap_dlg_videocompression-message"></a>\_Message WM Cap \_ DLG \_ VIDEOCOMPRESSION

Le message **WM \_ Cap \_ DLG \_ VIDEOCOMPRESSION** affiche une boîte de dialogue dans laquelle l’utilisateur peut sélectionner un compresseur à utiliser pendant le processus de capture. La liste des compresseurs disponibles peut varier en fonction du format vidéo sélectionné dans la boîte de dialogue Format vidéo du pilote de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) .


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Utilisez ce message avec des pilotes de capture qui fournissent des frames uniquement au \_ format RGB de bi. Ce message est particulièrement utile dans l’opération de capture d’étape pour combiner la capture et la compression en une seule opération. La compression des frames avec un compresseur logiciel dans le cadre d’une opération de capture en temps réel est probablement trop longue.

La compression n’affecte pas les frames copiés dans le presse-papiers.

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

 

 





