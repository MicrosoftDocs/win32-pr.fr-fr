---
description: Définit le nom convivial du profil.
ms.assetid: a0a2de8b-ab7b-49a8-b513-32af0052975f
title: 'IScanProfile :: SetName, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 0023353f298d5b6690345d559517c3840d33da6eb836c983b85924b5c4ac4260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441474"
---
# <a name="iscanprofilesetname-method"></a>IScanProfile :: SetName, méthode

Définit le nom convivial du profil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetName(
  [in] BSTR bstrName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrName* \[ dans\]
</dt> <dd>

Type : **BSTR**

Nom convivial du profil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

Cette méthode est requise car le GUID d’un profil ne peut pas être utilisé pour afficher le profil de numérisation à un utilisateur.

Un utilisateur peut modifier le nom convivial d’un profil à l’aide de la méthode [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

Les modifications apportées à un profil ne sont pas enregistrées sur le disque tant que l’application n’a pas appelé la méthode [**IScanProfile :: Save**](-wia-iscanprofile-save.md) .

Si deux applications créent des objets de profil d’analyse à partir du même fichier XML, et que chaque application écrit des modifications dans son objet, seules les modifications apportées par l’application qui appelle [**IScanProfile :: Save**](-wia-iscanprofile-save.md) Last sont enregistrées sur le disque.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                        |
| En-tête<br/>                   | <dl> <dt>Scanprofile. h</dt> </dl>    |
| MIDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



 

 




