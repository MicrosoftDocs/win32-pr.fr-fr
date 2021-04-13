---
description: Obtient le nom convivial du profil.
ms.assetid: db2f8229-ce43-4608-af3f-a06011b4fac0
title: 'IScanProfile :: GetName, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 81d1a0293802ea137f4e23b4571d32fd3d54ee44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201670"
---
# <a name="iscanprofilegetname-method"></a>IScanProfile :: GetName, méthode

Obtient le nom convivial du profil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbstrName* \[ à\]
</dt> <dd>

Type : **BSTR \** _

Nom convivial du profil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Cette méthode est requise car le GUID d’un profil ne peut pas être utilisé pour afficher le profil de numérisation à un utilisateur.

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

 

 




