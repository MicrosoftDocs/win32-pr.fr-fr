---
title: Message ICM_DECOMPRESS (VFW. h)
description: le \_ message ICM décompresser indique à un pilote de décompression vidéo de décompresser une trame de données dans une mémoire tampon définie par l’application.
ms.assetid: 666f2ebf-80a5-4846-861d-c79c3001c5a0
keywords:
- message ICM_DECOMPRESS Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c890a8ca15202f57fdaa02922e364af75f7b952
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364156"
---
# <a name="icm_decompress-message"></a>ICM \_ Décompresser le message

le message **ICM \_ décompresser** indique à un pilote de décompression vidéo de décompresser une trame de données dans une mémoire tampon définie par l’application.


```C++
ICM_DECOMPRESS 
wParam = (DWORD) (LPVOID) &icd; 
lParam = sizeof(ICDECOMPRESS); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="icd"></span><span id="ICD"></span>*ICD*
</dt> <dd>

Pointeur vers une structure [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress) .

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Taille, en octets, de [**ICDECOMPRESS**](/windows/desktop/api/Vfw/ns-vfw-icdecompress).

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

si vous souhaitez que le pilote décompresse les données directement à l’écran, envoyez le [**ICM \_ dessiner**](icm-draw.md) le message.

le pilote renvoie une erreur si ce message est reçu avant le message de début de la [**ICM de \_ décompression \_**](icm-decompress-begin.md) .

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

 

 





