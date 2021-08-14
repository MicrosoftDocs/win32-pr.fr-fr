---
description: Supprime tous les profils d’analyse disponibles pour l’utilisateur dans le système sous lequel votre application s’exécute.
ms.assetid: 1a79fd0e-1309-4fc4-863f-6dfb20594d91
title: IScanProfileMgr ::D méthode eleteAllProfilesForUser (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfilesForUser
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 967a2ca3e2ed313c024f52cec6d8064c702c6caedc122ce7bd4409f3408ec995
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209099"
---
# <a name="iscanprofilemgrdeleteallprofilesforuser-method"></a>IScanProfileMgr ::D méthode eleteAllProfilesForUser

Supprime tous les profils d’analyse disponibles pour l’utilisateur dans le système sous lequel votre application s’exécute.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeleteAllProfilesForUser();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

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

 

 




