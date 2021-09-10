---
title: Message ICM_DECOMPRESS_GET_PALETTE (VFW. h)
description: la ICM \_ décompresser les \_ \_ messages de la PALETTE demandent que le pilote de décompression vidéo fournisse la table des couleurs de la structure BITMAPINFOHEADER de sortie. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDecompressGetPalette.
ms.assetid: f9fae9ab-9f69-44b6-bedb-f56f43845229
keywords:
- message ICM_DECOMPRESS_GET_PALETTE Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364179"
---
# <a name="icm_decompress_get_palette-message"></a>ICM \_ Décompresser le \_ message d’extraction de \_ palette

la **ICM \_ décompresser \_ \_** les messages de la PALETTE demandent que le pilote de décompression vidéo fournisse la table des couleurs de la structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) de sortie. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDecompressGetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompressgetpalette) .


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

## <a name="remarks"></a>Remarques

Si *lpbiOutput* est différent de zéro, le pilote définit le membre **biClrUsed** de [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) sur le nombre de couleurs dans la table des couleurs. Le pilote remplit le membre **bmiColors** de [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) avec les couleurs réelles.

Le pilote ne doit prendre en charge ce message que s’il utilise une palette différente de celle spécifiée dans le format d’entrée.

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

 

