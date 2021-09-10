---
title: Message ICM_DECOMPRESS_GET_FORMAT (VFW. h)
description: le \_ \_ message de format d’extraction de la ICM décompresser \_ demande le format de sortie des données décompressées à partir d’un pilote de décompression vidéo. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDecompressGetFormat.
ms.assetid: 51753f47-758b-4d3e-9a53-9db284da2473
keywords:
- message ICM_DECOMPRESS_GET_FORMAT Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_FORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc7eefa655646deae8e67fa16a87bfdb81a8b936
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364176"
---
# <a name="icm_decompress_get_format-message"></a>ICM \_ Message de \_ format d’extraction de DÉcompression \_

le message de format d’extraction de la **ICM \_ \_ \_ décompresser** demande le format de sortie des données décompressées à partir d’un pilote de décompression vidéo. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDecompressGetFormat**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformat) .


```C++
ICM_DECOMPRESS_GET_FORMAT 
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

Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) pour contenir le format de sortie. Vous pouvez spécifier zéro pour demander uniquement la taille du format de sortie, comme dans la macro [**ICDecompressGetFormatSize**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetformatsize) .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si *lpbiOutput* est égal à zéro, retourne la taille de la structure.

Si *lpbiOutput* est différent de zéro, retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

Si *lpbiOutput* est différent de zéro, le pilote doit remplir la structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) avec le format de sortie par défaut correspondant au format d’entrée spécifié pour *lpbiInput*. Si le compresseur peut produire plusieurs formats, le format par défaut doit être celui qui conserve la plus grande quantité d’informations.

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

 

