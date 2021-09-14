---
description: crée un profil de numérisation vide et l’associe à un scanneur ou à un autre élément de l’acquisition d’images Windows (WIA) 2,0.
ms.assetid: daa8cd66-184b-4559-a22a-c3e6d8209a3f
title: 'IScanProfileMgr :: CreateProfile, méthode (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.CreateProfile
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 657cfb339d439452f4a49f048aea50c02ab92ba6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293995"
---
# <a name="iscanprofilemgrcreateprofile-method"></a>IScanProfileMgr :: CreateProfile, méthode

crée un profil de numérisation vide et l’associe à un scanneur ou à un autre élément de l’acquisition d’images Windows (WIA) 2,0.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateProfile(
  [in]  BSTR         bstrDeviceID,
  [in]  BSTR         bstrName,
  [in]  GUID         guidCategory,
  [out] IScanProfile **ppScanProfile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrDeviceID* \[ dans\]
</dt> <dd>

Type : **BSTR**

ID de l’appareil ou de l’élément WIA 2,0.

</dd> <dt>

*bstrName* \[ dans\]
</dt> <dd>

Type : **BSTR**

Nom convivial du nouveau profil.

</dd> <dt>

*guidCategory* \[ dans\]
</dt> <dd>

Type : **GUID**

GUID de la catégorie de l’appareil ou de l’élément WIA 2,0. Il doit s’agir de l’une \_ des \_ constantes de catégorie d’élément WIA de la loi WIA \_ .

</dd> <dt>

*ppScanProfile* \[ à\]
</dt> <dd>

Type : **[ **IScanProfile**](-wia-iscanprofile.md)\*\***

Adresse d’un pointeur vers le nouveau profil.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

**IScanProfileMgr :: CreateProfile** associe le périphérique spécifié au nouveau profil de numérisation.

**IScanProfileMgr :: CreateProfile** génère automatiquement un GUID pour le nouveau profil. Obtient le GUID avec [**GetGuid**](-wia-iscanprofile-getguid.md).

Utilisez la méthode [**IScanProfileMgr :: Refresh**](-wia-iscanprofilemgr-refresh.md) quand plusieurs objets [**IScanProfileMgr**](-wia-iscanprofilemgr.md) peuvent créer ou supprimer des profils en même temps.

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

 

 




