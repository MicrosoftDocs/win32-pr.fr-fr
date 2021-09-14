---
title: IWMDRMNonSilentLicenseAquisition GetURL, méthode (wmdrmsdk. h)
description: La méthode GetURL récupère l’URL vers laquelle la demande de licence doit être publiée.
ms.assetid: f65f1984-74bc-4cd0-957e-930aa6a6f6a5
keywords:
- GetURL, méthode Windows Media format
- GetURL, méthode Windows Media format, interface IWMDRMNonSilentLicenseAquisition
- Interface IWMDRMNonSilentLicenseAquisition Windows Media format, GetURL, méthode
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition.GetURL
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79212d19d7dbf4a66e2b72dcbdeba9262a9aeddd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195943"
---
# <a name="iwmdrmnonsilentlicenseaquisitiongeturl-method"></a>IWMDRMNonSilentLicenseAquisition :: GetURL, méthode

La méthode **getURL** récupère l’URL vers laquelle la demande de licence doit être publiée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetURL(
  [out] BSTR *pbstrURL
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbstrURL* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit l’URL.

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

 

 





