---
description: Obtient tous les ID de propriété disponibles dans un profil.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: 'IScanProfile :: GetAllPropIDs, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 7fd54e3e1cd45c3631df9b069ddf3c2e897037efb2870d00946f0a002e12f145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965778"
---
# <a name="iscanprofilegetallpropids-method"></a>IScanProfile :: GetAllPropIDs, méthode

Obtient tous les ID de propriété disponibles dans un profil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*nombre* \[ in, out\]
</dt> <dd>

Type : **ULong \***

Nombre d’ID de propriété demandés ou retournés.

</dd> <dt>

*PPID* \[ à\]
</dt> <dd>

Type : **propid \***

Pointeur vers un tableau d’ID de propriété.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| MIDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IScanProfile**](-wia-iscanprofile.md)
</dt> <dt>

[Analyser le schéma de profil](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




