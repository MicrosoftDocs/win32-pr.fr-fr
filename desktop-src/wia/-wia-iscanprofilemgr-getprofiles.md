---
description: Obtient tous les profils d’analyse disponibles pour l’utilisateur dans le système sous lequel votre application s’exécute.
ms.assetid: 9787079e-283c-4f6d-b97c-cfc1349ada30
title: 'IScanProfileMgr :: GetProfiles, méthode (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 13949fe08dd547ecb5319e18ecc84139ccd310bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404522"
---
# <a name="iscanprofilemgrgetprofiles-method"></a>IScanProfileMgr :: GetProfiles, méthode

Obtient tous les profils d’analyse disponibles pour l’utilisateur dans le système sous lequel votre application s’exécute.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetProfiles(
  [in, out] ULONG        *pulNumProfiles,
  [out]     IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pulNumProfiles* \[ in, out\]
</dt> <dd>

Type : **ULong \***

En cas de réussite, pointeur vers le nombre maximal de profils à retourner. En cas de retour, pointeur vers le nombre de profils retournés.

</dd> <dt>

*ppScanProfile* \[ à\]
</dt> <dd>

Type : **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Adresse d’un tableau de pointeurs vers des profils.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Si le nombre total de profils disponibles pour l’utilisateur est inférieur à la valeur transmise à *pulNumProfiles*, *pulNumProfiles* retourne ce total. Sinon, elle retourne la même valeur que celle qui lui a été passée.

## <a name="requirements"></a>Spécifications



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

 

 




