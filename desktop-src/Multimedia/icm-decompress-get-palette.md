---
title: Message ICM_DECOMPRESS_GET_PALETTE (VFW. h)
description: Le \_ \_ message d’extraction de la palette ICM décompresse les \_ demandes que le pilote de décompression vidéo fournisse la table des couleurs de la structure BITMAPINFOHEADER de sortie. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDecompressGetPalette.
ms.assetid: f9fae9ab-9f69-44b6-bedb-f56f43845229
keywords:
- Message ICM_DECOMPRESS_GET_PALETTE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6255ea99b9177819dee6d227c45d2229deab57f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510560"
---
# <a name="icm_decompress_get_palette-message"></a>Message d’extraction de la \_ \_ \_ palette ICM

Le message d’extraction de la **\_ \_ \_ palette ICM décompresse** les demandes que le pilote de décompression vidéo fournisse la table des couleurs de la structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) de sortie. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .


```C++
ICM_DECOMPRESS_GET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = (DWORD_PTR) (LPVOID) lpbiOutput; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Pointeur vers une structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) contenant le format d’entrée.

</dd> <dt>

<span id="lpbiOutput"></span><span id="lpbioutput"></span><span id="LPBIOUTPUT"></span>*lpbiOutput*
</dt> <dd>

Pointeur vers une structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) pour contenir la table de couleurs. L’espace réservé pour la table de couleurs est toujours au moins de 256 couleurs. Vous pouvez spécifier zéro pour ce paramètre pour retourner uniquement la taille de la table des couleurs.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Notes

Si *lpbiOutput* est différent de zéro, le pilote définit le membre **biClrUsed** de [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) sur le nombre de couleurs dans la table des couleurs. Le pilote remplit le membre **bmiColors** de [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) avec les couleurs réelles.

Le pilote ne doit prendre en charge ce message que s’il utilise une palette différente de celle spécifiée dans le format d’entrée.

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

 

