---
title: Message ICM_DRAW_BEGIN (VFW. h)
description: le \_ message ICM DRAW \_ BEGIN notifie un pilote de rendu pour préparer le dessin de données.
ms.assetid: e5ecd7dd-376b-422c-bbb8-4e7c41e3cac8
keywords:
- message ICM_DRAW_BEGIN Windows Multimedia
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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364171"
---
# <a name="icm_draw_begin-message"></a>ICM \_ DESSINER le \_ message de début

le message **ICM \_ DRAW \_ BEGIN** notifie un pilote de rendu pour préparer le dessin de données.


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



 

## <a name="remarks"></a>Remarques

si vous souhaitez que le pilote décompresse les données dans une mémoire tampon, envoyez le message de début de la [**ICM de \_ décompression \_**](icm-decompress-begin.md) .

le **ICM \_ dessiner \_ commencer** et [**ICM \_ dessiner \_**](icm-draw-end.md) les messages de fin ne sont pas imbriqués. si votre pilote reçoit **ICM \_ \_ commencer** avant que la décompression ne s’arrête avec **ICM \_ dessiner \_**, il doit redémarrer la décompression avec les nouveaux paramètres.

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

 

 





