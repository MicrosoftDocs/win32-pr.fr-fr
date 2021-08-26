---
title: Message ICM_GET (VFW. h)
description: le ICM \_ obtenir le message récupère une valeur DWORD définie par l’application à partir d’un pilote de compression vidéo.
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- message ICM_GET Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_GET
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8885faf7b0605378ace3004165004384a582c9d49a0a8ce047122c108b6cb8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038729"
---
# <a name="icm_get-message"></a>ICM \_ RECEVOIR un message

le **ICM \_ obtenir** le message récupère une valeur **DWORD** définie par l’application à partir d’un pilote de compression vidéo.


```C++
ICM_GET 
wParam = (DWORD) (LPVOID) pv; 
lParam = (DWORD) cb; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="pv"></span><span id="PV"></span>*va*
</dt> <dd>

Pointeur vers un bloc de mémoire à remplir avec l’état actuel. Vous pouvez également spécifier la **valeur null** pour déterminer la quantité de mémoire requise par les informations d’État.

</dd> <dt>

<span id="cb"></span><span id="CB"></span>*libéré*
</dt> <dd>

Taille, en octets, du bloc de mémoire.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la quantité de mémoire, en octets, requise pour stocker les informations d’État.

## <a name="remarks"></a>Remarques

La structure utilisée pour représenter les informations d’État est spécifique au pilote et est définie par le pilote.

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

 

 





