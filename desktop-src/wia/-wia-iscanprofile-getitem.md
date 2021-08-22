---
description: obtient le GUID de la catégorie de l’élément de l’acquisition d’images Windows (WIA) 2,0 auquel le profil est associé.
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: 'IScanProfile :: GetItem, méthode (Scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 5a7f52a2d89bbd35b59febb25528fe493c4b5646afc70251fc19978d6d6265db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451039"
---
# <a name="iscanprofilegetitem-method"></a>IScanProfile :: GetItem, méthode

obtient le GUID de la catégorie de l’élément de l’acquisition d’images Windows (WIA) 2,0 auquel le profil est associé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pguidCategory* \[ à\]
</dt> <dd>

Type : **GUID \***

Pointeur vers le GUID de la catégorie de l’élément WIA 2,0. Il s’agit toujours de l’une \_ des \_ constantes de catégorie d’éléments de la loi WIA \_ .

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

 

 




