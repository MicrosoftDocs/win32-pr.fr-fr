---
title: Message ICM_DRAW_SETTIME (VFW. h)
description: La \_ commande ICM Draw \_ setTime fournit des informations de synchronisation à un pilote de rendu qui gère le minutage des frames de dessin.
ms.assetid: 211e8ecc-ef36-4598-aa1d-cb0a06e64f14
keywords:
- Message ICM_DRAW_SETTIME Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_SETTIME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce1e37709477ba6080219e5225b3fde02dfed75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843405"
---
# <a name="icm_draw_settime-message"></a>\_Message de dessin de ICM ICM \_

La commande **ICM \_ Draw \_ setTime** fournit des informations de synchronisation à un pilote de rendu qui gère le minutage des frames de dessin. Les informations de synchronisation sont le numéro d’exemple du cadre à dessiner. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) .


```C++
ICM_DRAW_SETTIME 
wParam = (DWORD_PTR) lpTime; 
lParam = 0; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lpTime"></span><span id="lptime"></span><span id="LPTIME"></span>*lpTime*
</dt> <dd>

Exemple de numéro de l’image à afficher.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Notes

En général, le pilote compare la valeur spécifiée avec le numéro de frame associé à l’heure de son horloge interne et tente de synchroniser les deux si la différence est importante.

Utilisez ce message lorsque le matériel effectue sa propre décompression, synchronisation et dessin asynchrones, et que le matériel s’appuie sur un signal de synchronisation externe (le matériel n’est pas utilisé en tant que maître de synchronisation).

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

 

 





