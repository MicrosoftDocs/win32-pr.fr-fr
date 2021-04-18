---
title: Méthode IWMDRMNetReceiver GetLicenseChallenge (wmdrmsdk. h)
description: La méthode GetLicenseChallenge génère un défi de licence Windows Media DRM pour les périphériques réseau qui peut être envoyé à un émetteur lors de la demande de contenu protégé.
ms.assetid: c13b9e9e-b076-411b-a106-b602544faaba
keywords:
- Méthode GetLicenseChallenge format Windows Media
- Méthode GetLicenseChallenge format Windows Media, interface IWMDRMNetReceiver
- Interface IWMDRMNetReceiver Windows Media format, méthode GetLicenseChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f58b85b8dc5edd6c23e809dda8c18bf30137f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540200"
---
# <a name="iwmdrmnetreceivergetlicensechallenge-method"></a>IWMDRMNetReceiver :: GetLicenseChallenge, méthode

La méthode **GetLicenseChallenge** génère un défi de licence Windows Media DRM pour les périphériques réseau qui peut être envoyé à un émetteur lors de la demande de contenu protégé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetLicenseChallenge(
  [in]  BSTR  bstrAction,
  [out] BYTE  **ppbLicenseChallenge,
  [out] DWORD *pcbLicenseChallenge
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrAction* \[ dans\]
</dt> <dd>

Action pour laquelle générer la stimulation.

</dd> <dt>

*ppbLicenseChallenge* \[ à\]
</dt> <dd>

Adresse d’un pointeur défini sur l’adresse de la stimulation générée. Lorsque vous avez terminé ces données, vous devez libérer la mémoire en appelant **CoTaskMemFree**.

</dd> <dt>

*pcbLicenseChallenge* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit la taille de la demande de licence en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



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

[**Interface IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver ::P rocessLicenseResponse**](iwmdrmnetreceiver-processlicenseresponse.md)
</dt> </dl>

 

 





