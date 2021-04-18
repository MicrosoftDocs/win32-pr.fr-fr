---
description: Obtient le GUID de la catégorie de l’élément WIA (Windows Image Acquisition) 2,0 auquel le profil est associé.
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
ms.openlocfilehash: 888a3bb5bcb6e6c4fc2fefff2d976eb7fc1c7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519763"
---
# <a name="iscanprofilegetitem-method"></a>IScanProfile :: GetItem, méthode

Obtient le GUID de la catégorie de l’élément WIA (Windows Image Acquisition) 2,0 auquel le profil est associé.

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

Type : **GUID \** _

Pointeur vers le GUID de la catégorie de l’élément WIA 2,0. Il s’agit toujours de l’une \_ des \_ constantes de catégorie d’éléments de la loi WIA \_ .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : _ *HRESULT**

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

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

 

 




