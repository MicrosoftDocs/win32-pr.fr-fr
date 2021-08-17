---
description: Obtient le nombre de profils de numérisation pour l’appareil.
ms.assetid: fb1f8884-28ef-460e-a8c4-b9608cc89dc6
title: 'IScanProfileMgr :: GetNumProfilesforDeviceID, méthode (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: c2af1e4bc73afee090d947e6bcca0060521cb15cf2faff06be8c9a893534ea4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119264389"
---
# <a name="iscanprofilemgrgetnumprofilesfordeviceid-method"></a>IScanProfileMgr :: GetNumProfilesforDeviceID, méthode

Obtient le nombre de profils de numérisation pour l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNumProfilesforDeviceID(
  [in]  BSTR  bstrDeviceID,
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrDeviceID* \[ dans\]
</dt> <dd>

Type : **BSTR**

ID de l’appareil.

</dd> <dt>

*pulNumProfiles* \[ à\]
</dt> <dd>

Type : **ULong \***

Pointeur vers le nombre de profils disponibles pour l’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| MIDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Analyser le schéma de profil](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




