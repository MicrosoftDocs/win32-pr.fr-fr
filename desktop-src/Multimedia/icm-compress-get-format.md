---
title: Message ICM_COMPRESS_GET_FORMAT (VFW. h)
description: le \_ message ICM compresser \_ obtenir \_ le format demande le format de sortie des données compressées à partir d’un pilote de compression vidéo. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICCompressGetFormat.
ms.assetid: ac12d415-bad5-4838-b206-09c8097d3fd9
keywords:
- message ICM_COMPRESS_GET_FORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ac1bf9b3c9a3ae0535da008786bf8baef19c8b51e27446b84e4b95805a1c4a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785029"
---
# <a name="icm_compress_get_format-message"></a>ICM \_ \_Message de mise en forme de la compression \_

le message **ICM \_ compresser \_ obtenir le \_ format** demande le format de sortie des données compressées à partir d’un pilote de compression vidéo. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICCompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformat) .


```C++
ICM_COMPRESS_GET_FORMAT 
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

Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) pour contenir le format de sortie. Vous pouvez spécifier zéro pour ce paramètre pour demander uniquement la taille du format de sortie, comme dans la macro [**ICCompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-iccompressgetformatsize) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si *lpbiOutput* est égal à zéro, retourne la taille de la structure.

Si *lpbiOutput* est différent de zéro, retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

Si *lpbiOutput* est différent de zéro, le pilote doit remplir la structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) avec le format de sortie par défaut correspondant au format d’entrée spécifié pour *lpbiInput*. Si le compresseur peut produire plusieurs formats, le format par défaut doit être celui qui conserve la plus grande quantité d’informations.

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

 

