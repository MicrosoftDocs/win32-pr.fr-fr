---
title: Message ICM_DECOMPRESS_QUERY (VFW. h)
description: Le message de requête de décompression ICM \_ \_ interroge un pilote de décompression vidéo pour déterminer s’il prend en charge un format d’entrée spécifique ou s’il peut décompresser un format d’entrée spécifique dans un format de sortie spécifique.
ms.assetid: 622dd1de-3f7a-4841-913c-282c2ad766f4
keywords:
- Message ICM_DECOMPRESS_QUERY Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 838c946a38f9c2fda0c9178a36107af73f539a03
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511585"
---
# <a name="icm_decompress_query-message"></a>\_Message de requête de décompression ICM \_

Le message de **\_ \_ requête** de décompression ICM interroge un pilote de décompression vidéo pour déterminer s’il prend en charge un format d’entrée spécifique ou s’il peut décompresser un format d’entrée spécifique dans un format de sortie spécifique. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDecompressQuery**](/windows/desktop/api/Vfw/nf-vfw-icdecompressquery) .


```C++
ICM_DECOMPRESS_QUERY 
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

Retourne ICERR \_ OK si la décompression spécifiée est prise en charge ou ICERR BADFORMAT dans le \_ cas contraire.

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

 

