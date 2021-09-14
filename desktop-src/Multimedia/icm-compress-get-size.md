---
title: Message ICM_COMPRESS_GET_SIZE (VFW. h)
description: le \_ message ICM compresser la taille de l' \_ extraction \_ demande que le pilote de compression vidéo fournisse la taille maximale d’une trame de données lorsqu’elle est compressée dans le format de sortie spécifié. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICCompressGetSize.
ms.assetid: 6910e588-e60f-43b1-8fa6-113c2ec32a53
keywords:
- message ICM_COMPRESS_GET_SIZE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_SIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b0b61c78cc684de27d1e9a2747498e30eb3fe9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195352"
---
# <a name="icm_compress_get_size-message"></a>ICM \_ \_Message d’extraction de taille de compression \_

le message **ICM \_ compresser la \_ \_ taille** de l’extraction demande que le pilote de compression vidéo fournisse la taille maximale d’une trame de données lorsqu’elle est compressée dans le format de sortie spécifié. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICCompressGetSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetsize) .


```C++
ICM_COMPRESS_GET_SIZE 
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

Retourne le nombre maximal d’octets qu’un seul Frame compressé peut occuper.

## <a name="remarks"></a>Notes

En règle générale, les applications envoient ce message pour déterminer la taille d’une mémoire tampon à allouer pour le frame compressé.

Le pilote doit calculer la taille du plus grand Frame possible en fonction des formats d’entrée et de sortie.

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

 

