---
description: Utilisé par les applications pour afficher une boîte de dialogue d’appareil à l’utilisateur.
ms.assetid: 3b486220-32ab-4d6c-872c-684f9d1ee660
title: DeviceDialog, fonction (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceDialog
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: de8a3d36472d51c24a2c007ad7be0be371a0b5d8bb39e75f457e204250e8f53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441677"
---
# <a name="devicedialog-function"></a>DeviceDialog fonction)

Utilisé par les applications pour afficher une boîte de dialogue d’appareil à l’utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT WINAPI DeviceDialog(
  _In_ PDEVICEDIALOGDATA pDeviceDialogData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDeviceDialogData* \[ dans\]
</dt> <dd>

Type : **PDEVICEDIALOGDATA**

[**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) à utiliser pour créer la boîte de dialogue de l’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl>   |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DEVICEDIALOGDATA**](-wia-devicedialogdata.md)
</dt> </dl>

 

 




