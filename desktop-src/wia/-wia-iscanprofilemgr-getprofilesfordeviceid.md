---
description: Obtient tous les profils d’analyse associés à un appareil.
ms.assetid: 2e509f01-9c5e-4d17-8888-b08b6b4b9fa9
title: 'IScanProfileMgr :: GetProfilesforDeviceID, méthode (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfilesforDeviceID
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 8ca150d02aff2f84becf8b36aca87e2da24b2b83c9ccd85c0cf5a1c5ced0d664
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209055"
---
# <a name="iscanprofilemgrgetprofilesfordeviceid-method"></a>IScanProfileMgr :: GetProfilesforDeviceID, méthode

Obtient tous les profils d’analyse associés à un appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetProfilesforDeviceID(
  [in]      BSTR         bstrDeviceID,
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrDeviceID* \[ dans\]
</dt> <dd>

Type : **BSTR**

ID de l’appareil.

</dd> <dt>

*pulNumProfiles* \[ in, out\]
</dt> <dd>

Type : **ULong \***

En cas de réussite, pointeur vers le nombre maximal de profils à retourner. En cas de retour, pointeur vers le nombre de profils retournés.

</dd> <dt>

*ppScanProfile* \[ à\]
</dt> <dd>

Type : **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Adresse d’un pointeur vers un tableau de profils.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Si le nombre total de profils associés à l’appareil est inférieur à la valeur transmise à *pulNumProfiles*, *pulNumProfiles* retourne ce total. Sinon, elle retourne la même valeur que celle qui lui a été passée.

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

 

 




