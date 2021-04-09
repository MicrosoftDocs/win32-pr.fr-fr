---
title: Message ICM_DECOMPRESSEX (VFW. h)
description: Le \_ message DECOMPRESSEX ICM indique à un pilote de compression vidéo de décompresser un frame de données directement à l’écran, d’effectuer une décompression vers un DIB inversé ou de décompresser des images décrites dans des rectangles source et de destination.
ms.assetid: ed253280-c246-4e86-91f1-ad1e1132d732
keywords:
- Message ICM_DECOMPRESSEX Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESSEX
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d33451547bc598250a97e73682712e157aa13a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033129"
---
# <a name="icm_decompressex-message"></a>\_Message DECOMPRESSEX ICM

Le **message \_ DECOMPRESSEX ICM** indique à un pilote de compression vidéo de décompresser un frame de données directement à l’écran, d’effectuer une décompression vers un DIB inversé ou de décompresser des images décrites dans des rectangles source et de destination.


```C++
ICM_DECOMPRESSEX 
wParam = (DWORD_PTR) (LPVOID) &icdex; 
lParam = sizeof(ICDECOMPRESSEX); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="icdex"></span><span id="ICDEX"></span>*icdex*
</dt> <dd>

Pointeur vers une structure [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Taille, en octets, de [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Notes

Ce message est similaire à [**la \_ décompression ICM**](icm-decompress.md) , sauf qu’elle utilise la structure [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) pour définir ses informations de décompression.

Si vous souhaitez que le pilote décompresse les données directement à l’écran, envoyez le message [**ICM \_ Draw**](icm-draw.md) .

Le pilote retourne une erreur si ce message est reçu avant le message de [**\_ \_ début de DECOMPRESSEX ICM**](icm-decompressex-begin.md) .

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

 

 





