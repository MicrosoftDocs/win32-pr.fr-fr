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
ms.openlocfilehash: 230e0aaf3752016efd276d7d55624ee2abb4f8e0
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364152"
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

 

 





