---
title: Message WM_CAP_GET_SEQUENCE_SETUP (VFW. h)
description: Le \_ \_ \_ \_ message d’installation de la séquence de l’embout du programme WM récupère les paramètres actuels des paramètres de capture de streaming. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capCaptureGetSetup.
ms.assetid: 2220c92a-1994-4f15-9730-1cf01972dda6
keywords:
- Message WM_CAP_GET_SEQUENCE_SETUP Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_GET_SEQUENCE_SETUP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5cd1585b165581f9c9646741b92c5dc841472ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941645"
---
# <a name="wm_cap_get_sequence_setup-message"></a>\_ \_ \_ \_ Message d’installation de la séquence de l’embout WM

Le **message \_ \_ \_ \_ d’installation** de la séquence de l’embout du programme WM récupère les paramètres actuels des paramètres de capture de streaming. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) .


```C++
WM_CAP_GET_SEQUENCE_SETUP 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPCAPTUREPARMS) (s); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Taille, en octets, de la structure référencée par **s**.

</dd> <dt>

<span id="s"></span><span id="S"></span>*x*
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

 

 





