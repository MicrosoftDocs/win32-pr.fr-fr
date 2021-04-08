---
title: Message ICM_GET (VFW. h)
description: Le \_ message d’extraction ICM récupère une valeur DWORD définie par l’application à partir d’un pilote de compression vidéo.
ms.assetid: 288c0053-16a1-4547-b748-da218a0b588c
keywords:
- Message ICM_GET Windows Multimedia
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
ms.openlocfilehash: e23cd994546be41b5f938331b2dc632897635c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740493"
---
# <a name="icm_get-message"></a>\_Message d’extraction ICM

Le message d' **\_ extraction ICM** récupère une valeur **DWORD** définie par l’application à partir d’un pilote de compression vidéo.


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

## <a name="remarks"></a>Notes

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

 

 





