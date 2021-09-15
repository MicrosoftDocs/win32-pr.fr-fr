---
title: Message WM_CAP_DRIVER_GET_NAME (VFW. h)
description: Le \_ message WM Cap \_ Driver \_ obtenir \_ le nom renvoie le nom du pilote de capture connecté à la fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro capDriverGetName.
ms.assetid: 84cecaf1-e0ff-424f-8c10-8bfe5cc2e7ea
keywords:
- message WM_CAP_DRIVER_GET_NAME Windows Multimedia
topic_type:
- apiref
api_name:
- WM_CAP_DRIVER_GET_NAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256b5f7913c83ddd278f3f3a05552b3d81070c73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413851"
---
# <a name="wm_cap_driver_get_name-message"></a>\_Message d' \_ extraction du pilote WM Cap \_ \_

Le message **WM \_ Cap \_ Driver obtenir le \_ \_ nom** renvoie le nom du pilote de capture connecté à la fenêtre de capture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**capDriverGetName**](/windows/desktop/api/Vfw/nf-vfw-capdrivergetname) .


```C++
WM_CAP_DRIVER_GET_NAME 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Taille, en octets, de la mémoire tampon référencée par **szName**.

</dd> <dt>

<span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*
</dt> <dd>

Pointeur vers une mémoire tampon définie par l’application utilisée pour retourner le nom de l’appareil sous la forme d’une chaîne terminée par le caractère null.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** en cas de réussite ou **false** si la fenêtre de capture n’est pas connectée à un pilote de capture.

## <a name="remarks"></a>Notes

Le nom est une chaîne de texte Récupérée à partir de la zone de ressources du pilote. Les applications doivent allouer environ 80 octets pour cette chaîne. Si le pilote ne contient pas de ressource de nom, le nom de chemin d’accès complet du pilote figurant dans le registre ou dans le fichier SYSTEM.INI est retourné.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                       |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Capture vidéo](video-capture.md)
</dt> <dt>

[Messages de capture vidéo](video-capture-messages.md)
</dt> </dl>

 

 





