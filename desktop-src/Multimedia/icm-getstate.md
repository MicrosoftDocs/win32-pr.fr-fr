---
title: Message ICM_GETSTATE (VFW. h)
description: le \_ message ICM GETSTATE interroge un pilote de compression vidéo pour retourner sa configuration actuelle dans un bloc de mémoire ou pour déterminer la quantité de mémoire nécessaire pour récupérer les informations de configuration.
ms.assetid: 4b77e294-f3aa-45f9-a4f4-f103b83eae8d
keywords:
- message ICM_GETSTATE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9bf21d808752b8a3ac3ba71a8593cd6dc577b3af4f34f421682d126c73b3578
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119784949"
---
# <a name="icm_getstate-message"></a>ICM \_ Message GETSTATE

le message **ICM \_ GETSTATE** interroge un pilote de compression vidéo pour retourner sa configuration actuelle dans un bloc de mémoire ou pour déterminer la quantité de mémoire nécessaire pour récupérer les informations de configuration. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICGetState**](/windows/desktop/api/Vfw/nf-vfw-icgetstate) .


```C++
ICM_GETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*va*
</dt> <dd>

Pointeur vers un bloc de mémoire destiné à contenir les informations de configuration actuelles. Vous pouvez spécifier la **valeur null** pour ce paramètre afin de déterminer la quantité de mémoire requise pour les informations de configuration, comme dans [**ICGetStateSize**](/windows/desktop/api/Vfw/nf-vfw-icgetstatesize).

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*libéré*
</dt> <dd>

Taille, en octets, du bloc de mémoire.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si *PV* est **null**, retourne la quantité de mémoire, en octets, requise pour les informations de configuration.

Si *PV* n’est pas **null**, retourne ICERR \_ OK en cas de réussite ou une erreur dans le cas contraire.

## <a name="remarks"></a>Remarques

La structure utilisée pour représenter les informations de configuration est spécifique au pilote et est définie par le pilote.

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

 

 





