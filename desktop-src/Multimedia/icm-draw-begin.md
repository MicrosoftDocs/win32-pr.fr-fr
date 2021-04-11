---
title: Message ICM_DRAW_BEGIN (VFW. h)
description: Le \_ message ICM Draw \_ Begin notifie un pilote de rendu pour préparer le dessin de données.
ms.assetid: e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8
keywords:
- Message ICM_DRAW_BEGIN Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_BEGIN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db7b9e20a0b0621038e1c7e092a871a6727566cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942631"
---
# <a name="icm_draw_begin-message"></a>Message de début du \_ dessin ICM \_

Le message **ICM \_ Draw \_ Begin** notifie un pilote de rendu pour préparer le dessin de données.


```C++
ICM_DRAW_BEGIN 
wParam = (DWORD) (LPVOID) &icdrwBgn; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="icdrwBgn"></span><span id="icdrwbgn"></span><span id="ICDRWBGN"></span>*icdrwBgn*
</dt> <dd>

Pointeur vers une structure [**ICDRAWBEGIN**](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin) contenant le format d’entrée.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Taille, en octets, de **ICDRAWBEGIN**.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne ICERR \_ OK si le pilote prend en charge le dessin des données à l’écran de la manière spécifiée et le format, ou un code d’erreur dans le cas contraire. Les valeurs d’erreur possibles sont les suivantes.



| Valeur               | Signification                                                                       |
|---------------------|-------------------------------------------------------------------------------|
| ICERR \_ BADFORMAT    | Le format d’entrée ou de sortie n’est pas pris en charge.                                      |
| ICERR \_ NOTSUPPORTED | Le pilote ne dessine pas directement sur l’écran ou ne prend pas en charge ce message. |



 

## <a name="remarks"></a>Notes

Si vous souhaitez que le pilote décompresse les données dans une mémoire tampon, envoyez le message de début de la [**\_ \_ décompression ICM**](icm-decompress-begin.md) .

Les messages de [**\_ \_ fin**](icm-draw-end.md) de dessin **ICM \_ \_** et ICM ne sont pas imbriqués. Si votre pilote reçoit **le \_ dessin \_ ICM, commencez** la décompression avec **les nouveaux paramètres \_ \_** pour arrêter la décompression.

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

 

 





