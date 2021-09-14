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
ms.openlocfilehash: c5d723379bb542346e3612f70c19a1629d325ebe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293991"
---
# <a name="iscanprofilemgrdeleteallprofilesforuser-method"></a>IScanProfileMgr ::D méthode eleteAllProfilesForUser

Supprime tous les profils d’analyse disponibles pour l’utilisateur dans le système sous lequel votre application s’exécute.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeleteAllProfilesForUser();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

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

 

 




