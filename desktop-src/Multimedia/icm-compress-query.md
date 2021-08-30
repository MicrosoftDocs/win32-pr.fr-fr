---
title: Message ICM_COMPRESS_QUERY (VFW. h)
description: le \_ message de requête ICM compresser \_ interroge un pilote de compression vidéo pour déterminer s’il prend en charge un format d’entrée spécifique ou s’il peut compresser un format d’entrée spécifique dans un format de sortie spécifique.
ms.assetid: 6d0e735e-8252-4507-b8be-1ba87774f637
keywords:
- message ICM_COMPRESS_QUERY Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_COMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75a68bf93a3d3ea96447dd061d859ccbf4483124dc8955fbd6efc39c180d782c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785019"
---
# <a name="icm_compress_query-message"></a>ICM \_ Compresser le \_ message de requête

le message de **\_ \_ requête ICM compresser** interroge un pilote de compression vidéo pour déterminer s’il prend en charge un format d’entrée spécifique ou s’il peut compresser un format d’entrée spécifique dans un format de sortie spécifique. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICCompressQuery**](/windows/desktop/api/Vfw/nf-vfw-iccompressquery) .


```C++
ICM_COMPRESS_QUERY 
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

Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant le format de sortie. Vous pouvez spécifier zéro pour ce paramètre pour indiquer qu’un format de sortie est acceptable.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK si la compression spécifiée est prise en charge ou ICERR BADFORMAT dans le \_ cas contraire.

## <a name="remarks"></a>Remarques

Lorsqu’un pilote reçoit ce message, il doit examiner la structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) associée à *lpbiInput* pour déterminer s’il peut compresser le format d’entrée.

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

 

