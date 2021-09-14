---
description: Définit le profil d’analyse spécifié comme profil par défaut.
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: 'IScanProfileMgr :: SetDefault, méthode (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.SetDefault
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 3a7c32f246bcafc8ff7ce55e8c6f34ea45553a95
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219988"
---
# <a name="iscanprofilemgrsetdefault-method"></a>IScanProfileMgr :: SetDefault, méthode

Définit le profil d’analyse spécifié comme profil par défaut.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetDefault(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pScanProfile* \[ dans\]
</dt> <dd>

Type : **[ **IScanProfile**](-wia-iscanprofile.md)\***

Pointeur vers le profil.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Utilisez la méthode **IScanProfileMgr :: SetDefault** pour ajouter un `<Default>` élément au profil ou pour supprimer cet élément du profil par défaut précédent de l’appareil.

Utilisez la méthode [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) pour modifier le profil par défaut.

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

 

 




