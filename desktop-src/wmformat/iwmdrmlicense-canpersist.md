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
ms.openlocfilehash: 9e174f0b7d48684e40cc5796d2ae95ec1bcaca99216c493c73609323daf276b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701217"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Aucun.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





