---
description: Supprime le profil de numérisation spécifié.
ms.assetid: 31020528-3a96-492f-a3a1-e9075d4ffd14
title: IScanProfileMgr ::D méthode eleteProfile (Scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: f45dfa3ef96fee194348192c2898a44df5f34be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103952070"
---
# <a name="iscanprofilemgrdeleteprofile-method"></a>IScanProfileMgr ::D méthode eleteProfile

Supprime le profil de numérisation spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DeleteProfile(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pScanProfile* \[ dans\]
</dt> <dd>

Tapez : **[**IScanProfile**](-wia-iscanprofile.md) \** _

Pointeur vers le profil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

**IScanProfileMgr ::D eleteprofile** supprime le profil du disque et détruit l’objet de profil en mémoire.

Utilisez la méthode [**IScanProfileMgr :: Refresh**](-wia-iscanprofilemgr-refresh.md) quand plusieurs objets [**IScanProfileMgr**](-wia-iscanprofilemgr.md) peuvent créer ou supprimer des profils en même temps.

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

 

 




