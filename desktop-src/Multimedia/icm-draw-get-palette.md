---
title: Message ICM_DRAW_GET_PALETTE (VFW. h)
description: le \_ message ICM dessiner \_ obtenir \_ la palette demande à un pilote de rendu de retourner une palette.
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- message ICM_DRAW_GET_PALETTE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ef07085bef92d6191cea69429a5b544d5d2f706e1771baa404741aa98a5812b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117987389"
---
# <a name="icm_draw_get_palette-message"></a>ICM \_ DESSINER un \_ message d’extraction de \_ palette

le message **ICM \_ dessiner obtenir la \_ \_ palette** demande à un pilote de rendu de retourner une palette.


```C++
ICM_DRAW_GET_PALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valeur renvoyée

Le pilote doit retourner l’un des éléments suivants : un descripteur de la palette utilisée, **null** s’il n’a pas de handle à retourner, ou ICERR non \_ pris en charge s’il ne prend pas en charge les palettes.

## <a name="requirements"></a>Conditions requises



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

 

 





