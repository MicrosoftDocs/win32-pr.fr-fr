---
title: Message ICM_COMPRESS_BEGIN (VFW. h)
description: le message de début de compression ICM \_ \_ notifie un pilote de compression vidéo pour préparer la compression des données. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICCompressBegin.
ms.assetid: dd1d3a66-c625-4f55-b65a-8545c1c16301
keywords:
- message ICM_COMPRESS_BEGIN Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e358aa3ab589af0be1e4e490c141ed41baeb5874
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364100"
---
# <a name="icm_compress_begin-message"></a>ICM \_ Compresser le \_ message de début

le message de **\_ \_ début** de compression ICM notifie un pilote de compression vidéo pour préparer la compression des données. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICCompressBegin**](/windows/desktop/api/Vfw/nf-vfw-iccompressbegin) .


```C++
ICM_COMPRESS_BEGIN 
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

Retourne ICERR \_ OK si le pilote prend en charge le BADFORMAT de compression ou de ICERR spécifié \_ si le format d’entrée ou de sortie n’est pas pris en charge.

## <a name="remarks"></a>Remarques

le pilote doit allouer et initialiser les tables ou la mémoire dont il a besoin pour compresser les formats de données lorsqu’il reçoit le message [**ICM \_ compresser**](icm-compress.md) .

VCM enregistre les paramètres du message de **début de \_ compression \_ ICM** le plus récent. les messages de [**\_ \_ fin**](icm-compress-end.md) compresser les **ICM de \_ compression \_ BEGIN** et ICM ne sont pas imbriqués. si votre pilote reçoit **ICM la compression \_ \_ commencent** avant l’arrêt de la compression avec **ICM \_ \_ fin** de compression, il doit redémarrer la compression avec les nouveaux paramètres.

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

 

