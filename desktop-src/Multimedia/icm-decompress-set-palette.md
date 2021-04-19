---
title: Message ICM_DECOMPRESS_SET_PALETTE (VFW. h)
description: Le \_ message de palette DÉcompresser les DÉcompresses \_ \_ spécifie une palette pour un pilote de décompression vidéo à utiliser s’il est décompressé dans un format qui utilise une palette. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDecompressSetPalette.
ms.assetid: 269d01f9-b7c8-40e4-abdb-24dd0c9cc18d
keywords:
- Message ICM_DECOMPRESS_SET_PALETTE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_SET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2bbbf1b09b8c5954a2149edd16cb213a08fb3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511584"
---
# <a name="icm_decompress_set_palette-message"></a>\_ \_ Message de palette de DÉcompression ICM \_

Le message de **\_ \_ \_ palette décompresser les décompresses** spécifie une palette pour un pilote de décompression vidéo à utiliser s’il est décompressé dans un format qui utilise une palette. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) .


```C++
ICM_DECOMPRESS_SET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiPalette; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*
</dt> <dd>

Pointeur vers une structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) dont la table des couleurs contient les couleurs à utiliser si possible. Vous pouvez spécifier zéro pour utiliser l’ensemble de couleurs de sortie par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK si le pilote de décompression peut décompresser des images de manière précise dans la palette suggérée à l’aide de l’ensemble de couleurs à mesure qu’elles sont organisées dans la palette. Retourne ICERR \_ non pris en charge dans le cas contraire.

## <a name="remarks"></a>Notes

Ce message ne doit pas affecter la décompression déjà en cours ; au lieu de cela, les couleurs transmises à l’aide de ce message doivent être retournées en réponse à l’avenir de la [**\_ décompression \_ \_ ICM**](icm-decompress-get-format.md) , de l’extraction des messages de la [**\_ \_ \_ palette**](icm-decompress-get-palette.md) . Les couleurs sont renvoyées au pilote de décompression dans un prochain message de [**\_ \_ début**](icm-decompress-begin.md) de décompression ICM.

Ce message est principalement utilisé lorsqu’un pilote décompresse des images à l’écran et qu’une autre application qui utilise une palette est au premier plan, forçant le pilote de décompression à s’adapter à un ensemble de couleurs étranger.

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

 

