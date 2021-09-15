---
title: Méthode IWMDRMLicense CanPersist (wmdrmsdk. h)
description: La méthode CanPersist interroge si la licence peut être rendue persistante dans un magasin de licences local.
ms.assetid: 040b30d8-4e47-44a3-8b09-e81cc30e8a53
keywords:
- Méthode CanPersist format Windows Media
- Méthode CanPersist format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode CanPersist
topic_type:
- apiref
api_name:
- IWMDRMLicense.CanPersist
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7772dac73b99443626b1eeec6f5e90851f92c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404471"
---
# <a name="iwmdrmlicensecanpersist-method"></a>IWMDRMLicense :: CanPersist, méthode

La méthode **CanPersist** interroge si la licence peut être rendue persistante dans un magasin de licences local.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CanPersist(
  [out] BOOL *pfCanPersist
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pfCanPersist* \[ à\]
</dt> <dd>

La valeur TRUE indique que la licence peut être persistante.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





