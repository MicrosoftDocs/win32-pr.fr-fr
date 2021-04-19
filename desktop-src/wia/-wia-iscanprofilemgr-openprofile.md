---
description: Ouvre un profil de numérisation enregistré sur le disque sous la forme d’un fichier XML.
ms.assetid: 2b45280e-a1b6-4db9-af8c-09faff34b067
title: 'IScanProfileMgr :: OpenProfile, méthode (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.OpenProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 40d380a2b0405445cba72a0aac73c4b529114fcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524665"
---
# <a name="iscanprofilemgropenprofile-method"></a>IScanProfileMgr :: OpenProfile, méthode

Ouvre un profil de numérisation enregistré sur le disque sous la forme d’un fichier XML.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT OpenProfile(
  [in]  GUID         guid,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*GUID* \[ dans\]
</dt> <dd>

Type : **GUID**

GUID du profil.

</dd> <dt>

*ppScanProfile* \[ à\]
</dt> <dd>

Type : **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Adresse d’un pointeur vers le profil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Si un profil de numérisation est enregistré à l’aide de la méthode [**Save**](-wia-iscanprofile-save.md) , il est stocké sous la forme d’un fichier XML dans% UserProfile% \\ Application Data \\ Microsoft \\ document Center \\ UserScanProfiles.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Scanprofilemgr. h</dt> </dl> |
| MIDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IScanProfileMgr**](-wia-iscanprofilemgr.md)
</dt> <dt>

[Analyser le schéma de profil](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




