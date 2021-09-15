---
description: Obtient le nombre de profils d’analyse créés pour l’utilisateur dans le système sous lequel votre application s’exécute.
ms.assetid: 0667a885-d61f-4c44-b988-a42242c2678e
title: 'IScanProfileMgr :: GetNumProfiles, méthode (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: a8c3167bd428054054a32d7823ce57e562501533
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404524"
---
# <a name="iscanprofilemgrgetnumprofiles-method"></a>IScanProfileMgr :: GetNumProfiles, méthode

Obtient le nombre de profils d’analyse créés pour l’utilisateur dans le système sous lequel votre application s’exécute.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetNumProfiles(
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pulNumProfiles* \[ à\]
</dt> <dd>

Type : **ULong \***

Pointeur vers le nombre de profils créés pour l’utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

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

 

 




