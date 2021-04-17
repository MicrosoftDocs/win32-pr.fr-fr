---
description: Retourne le GUID du profil.
ms.assetid: 184456dd-515d-4744-91f3-0ef8b4d2114d
title: 'IScanProfile :: GetGUID, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetGUID
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: e3c39815e1bc88830f64f632689028c4c527a710
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318581"
---
# <a name="iscanprofilegetguid-method"></a>IScanProfile :: GetGUID, méthode

Retourne le GUID du profil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetGUID(
  [out] GUID *retVal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*retVal* \[ à\]
</dt> <dd>

Type : **GUID \** _

Pointeur vers le GUID du profil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Le GUID d’un profil est généré automatiquement lors de la création du profil avec [**CreateProfile**](-wia-iscanprofilemgr-createprofile.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| MIDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Analyser le schéma de profil](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




