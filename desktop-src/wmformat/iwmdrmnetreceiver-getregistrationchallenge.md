---
title: Méthode IWMDRMNetReceiver GetRegistrationChallenge (wmdrmsdk. h)
description: La méthode GetRegistrationChallenge génère un message de stimulation d’inscription Windows Media DRM pour les périphériques réseau.
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- Méthode GetRegistrationChallenge format Windows Media
- Méthode GetRegistrationChallenge format Windows Media, interface IWMDRMNetReceiver
- Interface IWMDRMNetReceiver Windows Media format, méthode GetRegistrationChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetRegistrationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a292749e95ca6ba2dabc8f3829eae827dbdd8325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521691"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a>IWMDRMNetReceiver :: GetRegistrationChallenge, méthode

La méthode **GetRegistrationChallenge** génère un message de stimulation d’inscription Windows Media DRM pour les périphériques réseau.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppbRegistrationChallenge* \[ à\]
</dt> <dd>

Adresse d’un pointeur qui reçoit l’adresse de la stimulation générée. Lorsque vous avez terminé ces données, vous devez libérer la mémoire en appelant **CoTaskMemFree**.

</dd> <dt>

*pcbRegistrationChallenge* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit la taille de la demande d’inscription en octets.

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

[**IWMDRMNetReceiver ::P rocessRegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





