---
title: Message ICM_DRAW_QUERY (VFW. h)
description: Le \_ message de requête ICM Draw \_ interroge un pilote de rendu pour déterminer s’il peut restituer des données dans un format spécifique. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDrawQuery.
ms.assetid: b829a04b-c1be-47c6-96e9-a6dc6f802811
keywords:
- Message ICM_DRAW_QUERY Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_QUERY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27266484cffa503583df32b60c6e8a0c04f344f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465667"
---
# <a name="icm_draw_query-message"></a>Message de requête ICM de \_ dessin \_

Le message de **\_ \_ requête ICM Draw** interroge un pilote de rendu pour déterminer s’il peut restituer des données dans un format spécifique. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) .


```C++
ICM_DRAW_QUERY 
wParam = (DWORD_PTR) (LPVOID) lpbiInput; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpbiInput"></span><span id="lpbiinput"></span><span id="LPBIINPUT"></span>*lpbiInput*
</dt> <dd>

Pointeur vers une structure [**BITMAPINFO,**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) contenant le format d’entrée.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK si le pilote peut restituer des données au format spécifié ou ICERR BADFORMAT dans le \_ cas contraire.

## <a name="remarks"></a>Notes

Ce message diffère du message [**ICM \_ Draw \_ Begin**](icm-draw-begin.md) dans le sens où il interroge le pilote de manière générale. **ICM \_ DESSINER \_ commencer** détermine si le pilote peut dessiner les données à l’aide du format spécifié dans des conditions spécifiques, telles que l’étirement de l’image.

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

 

