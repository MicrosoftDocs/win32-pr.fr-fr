---
title: Méthode IWMDRMNonSilentLicenseAquisition GetChallenge (wmdrmsdk. h)
description: La méthode GetChallenge récupère la demande de licence qui doit être publiée sur le serveur de licences.
ms.assetid: f2ff8484-8fe2-4c74-82c1-9bc14f8197e0
keywords:
- Méthode GetChallenge format Windows Media
- Méthode GetChallenge format Windows Media, interface IWMDRMNonSilentLicenseAquisition
- Interface IWMDRMNonSilentLicenseAquisition Windows Media format, méthode GetChallenge
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetChallenge
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa0dc63c63e5d7a62c06cbe791d9a5e5e8d09c5d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195944"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongetchallenge-method"></a>IWMDRMNonSilentLicenseAquisition :: GetChallenge, méthode

La méthode **GetChallenge** récupère la demande de licence qui doit être publiée sur le serveur de licences.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetChallenge(
  [out] BSTR *pbstrChallenge
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbstrChallenge* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit la demande de licence.

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
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Wmdrmsdk. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>Wmdrmsdk. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md)
</dt> </dl>

 

 





