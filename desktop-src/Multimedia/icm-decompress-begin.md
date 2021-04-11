---
title: Message ICM_DECOMPRESS_BEGIN (VFW. h)
description: Le message de début de décompression ICM \_ \_ envoie une notification à un pilote de décompression vidéo pour préparer la décompression des données. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDecompressBegin.
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- Message ICM_DECOMPRESS_BEGIN Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59b8f55ebb5543c73e0d7a9c9ee800fabfc483d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105436"
---
# <a name="icm_decompress_begin-message"></a>Message de début de la \_ décompression ICM \_

Le message de **\_ \_ début** de décompression ICM envoie une notification à un pilote de décompression vidéo pour préparer la décompression des données. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) .


```C++
ICM_DECOMPRESS_BEGIN 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant le format d’entrée.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant le format de sortie.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK si la décompression spécifiée est prise en charge ou ICERR BADFORMAT dans le \_ cas contraire.

## <a name="remarks"></a>Notes

Lorsque le pilote reçoit ce message, il doit allouer des tampons et effectuer toutes les opérations qui prennent du temps afin qu’il puisse traiter les messages de [**\_ décompression ICM**](icm-decompress.md) de manière efficace.

Si vous souhaitez que le pilote décompresse les données directement à l’écran, envoyez le message [**ICM \_ Draw**](icm-draw.md) .

Les messages de [**\_ \_ fin**](icm-decompress-end.md) de décompression **ICM \_ \_ Begin** et ICM ne sont pas imbriqués. Si le pilote reçoit la décompression ICM avant que la décompression ne soit arrêtée avec la **\_ \_ fin** de la décompression ICM, il doit redémarrer la décompression avec les nouveaux paramètres. **\_ \_**

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

 

