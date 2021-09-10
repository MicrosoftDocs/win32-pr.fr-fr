---
title: Message ICM_DECOMPRESS_BEGIN (VFW. h)
description: le \_ message ICM décompresser \_ BEGIN envoie une notification au pilote de décompression vidéo pour préparer la décompression des données. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDecompressBegin.
ms.assetid: 24cd5220-d473-4968-8678-b00670eecf8f
keywords:
- message ICM_DECOMPRESS_BEGIN Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364160"
---
# <a name="icm_decompress_begin-message"></a>ICM \_ Message de début de la décompression \_

le message **ICM \_ décompresser \_ BEGIN** envoie une notification au pilote de décompression vidéo pour préparer la décompression des données. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDecompressBegin**](/windows/desktop/api/Vfw/nf-vfw-icdecompressbegin) .


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

## <a name="remarks"></a>Remarques

lorsque le pilote reçoit ce message, il doit allouer des tampons et effectuer des opérations qui prennent du temps pour qu’il puisse traiter [**ICM \_ décompresser**](icm-decompress.md) les messages efficacement.

si vous souhaitez que le pilote décompresse les données directement à l’écran, envoyez le [**ICM \_ dessiner**](icm-draw.md) le message.

les messages de fin de **\_ décompression ICM de \_ début** et de [**\_ \_ fin de ICM**](icm-decompress-end.md) ne sont pas imbriqués. si votre pilote reçoit **ICM \_ décompresser \_ BEGIN** avant que la décompression ne s’arrête avec **ICM \_ \_ fin** de décompression, il doit redémarrer la décompression avec les nouveaux paramètres.

## <a name="requirements"></a>Spécifications



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

 

