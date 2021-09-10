---
title: Message ICM_DECOMPRESSEX (VFW. h)
description: le \_ message ICM DECOMPRESSEX indique à un pilote de compression vidéo de décompresser un frame de données directement à l’écran, de décompresser un DIB inversé ou de décompresser les images décrites avec les rectangles source et de destination.
ms.assetid: ed253280-c246-4e86-91f1-ad1e1132d732
keywords:
- message ICM_DECOMPRESSEX Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364164"
---
# <a name="icm_decompressex-message"></a>ICM \_ Message DECOMPRESSEX

le message **ICM \_ DECOMPRESSEX** indique à un pilote de compression vidéo de décompresser un frame de données directement à l’écran, de décompresser un DIB inversé ou de décompresser les images décrites avec les rectangles source et de destination.


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

## <a name="remarks"></a>Remarques

ce message est similaire à [**ICM \_ décompresser**](icm-decompress.md) , à ceci près qu’il utilise la structure [**ICDECOMPRESSEX**](/windows/desktop/api/Vfw/ns-vfw-icdecompressex) pour définir ses informations de décompression.

si vous souhaitez que le pilote décompresse les données directement à l’écran, envoyez le [**ICM \_ dessiner**](icm-draw.md) le message.

le pilote renvoie une erreur si ce message est reçu avant le message [**ICM \_ DECOMPRESSEX \_ BEGIN**](icm-decompressex-begin.md) .

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

 

 





