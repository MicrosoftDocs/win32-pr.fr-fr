---
title: Méthode IWMDRMLicense PersistLicense (wmdrmsdk. h)
description: La méthode PersistLicense enregistre la licence actuelle du magasin temporaire dans le magasin de licences local permanent.
ms.assetid: 80a0f932-2800-416b-9dfe-97654a76c19b
keywords:
- Méthode PersistLicense format Windows Media
- Méthode PersistLicense format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode PersistLicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.PersistLicense
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f41b61cdf448d757d13917ca22af0c3d9d9d390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534981"
---
# <a name="iwmdrmlicensepersistlicense-method"></a>IWMDRMLicense ::P méthode ersistLicense

La méthode **PersistLicense** enregistre la licence actuelle du magasin temporaire dans le magasin de licences local permanent.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT PersistLicense();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Si la licence actuelle ne se trouve pas dans le magasin temporaire, cette méthode échoue.

Vous pouvez appeler [**CanPersist**](iwmdrmlicense-canpersist.md) pour demander si la licence est autorisée à être persistante.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMLicense**](iwmdrmlicense.md)
</dt> </dl>

 

 





