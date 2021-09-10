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
ms.openlocfilehash: f9508972c173c9e189bdc092a63d849adf3be739
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124367927"
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

 

