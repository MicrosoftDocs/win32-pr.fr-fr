---
title: Message ICM_SETSTATE (VFW. h)
description: le ICM le \_ message SETSTATE avertit un pilote de compression vidéo de la définition de l’état du compresseur. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICSetState.
ms.assetid: d1a91847-2893-4c8b-9ca1-02db71ec2c81
keywords:
- message ICM_SETSTATE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_SETSTATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ea6cd7aa0314520a30e293a8f029920c22b8baa58e995eed7ff9e5a96dd1b7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525809"
---
# <a name="icm_setstate-message"></a>ICM \_ Message SETSTATE

le **ICM \_** le message SETSTATE avertit un pilote de compression vidéo de la définition de l’état du compresseur. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICSetState**](/windows/desktop/api/Vfw/nf-vfw-icsetstate) .


```C++
ICM_SETSTATE 
wParam = (DWORD_PTR) (LPVOID) pv; 
lParam = (DWORD_PTR) cb; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*va*
</dt> <dd>

Pointeur vers un bloc de mémoire contenant les données de configuration. Vous pouvez spécifier la **valeur null** pour ce paramètre pour réinitialiser le compresseur à son état par défaut.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*libéré*
</dt> <dd>

Taille, en octets, du bloc de mémoire.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne le nombre d’octets utilisés par le compresseur en cas de réussite ou zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Les informations utilisées par ce message sont privées et spécifiques à un compresseur donné. les applications clientes doivent utiliser ce message uniquement pour restaurer les informations précédemment obtenues avec le message [**ICM \_ GETSTATE**](icm-getstate.md) et doivent utiliser le message [**ICM \_ configurer**](icm-configure.md) pour ajuster la configuration d’un pilote de compression vidéo.

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

 

 





