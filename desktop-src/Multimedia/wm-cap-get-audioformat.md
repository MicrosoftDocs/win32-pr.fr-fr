---
title: Message WM_CAP_GET_AUDIOFORMAT (VFW. h)
description: Le \_ message WM \_ Cap \_ AUDIOFORMAT obtient le format audio ou la taille du format audio. Vous pouvez envoyer ce message explicitement ou à l’aide des macros capGetAudioFormat et capGetAudioFormatSize.
ms.assetid: 25e58863-2b1e-4ed8-9f34-c39617a15bc1
keywords:
- message WM_CAP_GET_AUDIOFORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d247c035f251b387537f8e6c360adf79e6ed479d8d40e4f8fe8180e059dab3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940737"
---
# <a name="wm_cap_get_audioformat-message"></a>Message WM d' \_ \_ extraction de \_ AUDIOFORMAT

Le **message \_ WM \_ Cap \_ AUDIOFORMAT** obtient le format audio ou la taille du format audio. Vous pouvez envoyer ce message explicitement ou à l’aide des macros [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) et [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) .


```C++
WM_CAP_GET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Taille, en octets, de la structure référencée par **s**.

</dd> <dt>

<span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*
</dt> <dd>

Pointeur vers une structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) , ou **null**. Si la valeur est **null**, la taille, en octets, nécessaire pour contenir la structure est retournée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la taille, en octets, du format audio.

## <a name="remarks"></a>Remarques

Étant donné que les formats audio compressés varient en fonction de la taille requise, les applications doivent d’abord récupérer la taille, puis allouer de la mémoire et enfin demander les données de format audio.

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

 

