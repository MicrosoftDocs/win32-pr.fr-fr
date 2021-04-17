---
title: Message WM_CAP_SET_SEQUENCE_SETUP (VFW. h)
description: Le \_ \_ message d’installation de la séquence WM Cap Set \_ \_ définit les paramètres de configuration utilisés avec la capture de streaming. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capCaptureSetSetup.
ms.assetid: ba9adb26-6627-469b-a836-f4f277ddb7c4
keywords:
- Message WM_CAP_SET_SEQUENCE_SETUP Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_SET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54a2129021f31694d9e601ecd97503e2a5f5c925
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509358"
---
# <a name="wm_cap_set_sequence_setup-message"></a>\_ \_ \_ \_ Message d’installation de la séquence de définition de l’embout WM

Le **message \_ \_ \_ \_ d’installation de la séquence WM Cap Set** définit les paramètres de configuration utilisés avec la capture de streaming. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) .


```C++
WM_CAP_SET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (psCapParms); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Taille, en octets, de la structure référencée par **s**.

</dd> <dt>

<span id="psCapParms"></span><span id="pscapparms"></span><span id="PSCAPPARMS"></span>*psCapParms*
</dt> <dd>

Pointeur vers une structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Pour plus d’informations sur les paramètres utilisés pour contrôler la capture de la diffusion en continu, consultez la structure [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .

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

 

 





