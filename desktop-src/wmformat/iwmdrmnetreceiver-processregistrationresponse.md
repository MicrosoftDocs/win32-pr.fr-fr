---
title: Méthode IWMDRMNetReceiver ProcessRegistrationResponse (wmdrmsdk. h)
description: La méthode ProcessRegistrationResponse traite une réponse d’inscription envoyée par l’émetteur en réponse à une demande d’inscription.
ms.assetid: d0260e93-0a5e-494b-a723-bb62206ed55b
keywords:
- Méthode ProcessRegistrationResponse format Windows Media
- Méthode ProcessRegistrationResponse format Windows Media, interface IWMDRMNetReceiver
- Interface IWMDRMNetReceiver Windows Media format, méthode ProcessRegistrationResponse
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessRegistrationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a0461bc19aa1f3de2751516aedc8e76a0201417fe017881fb0fbd8da8156b39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930809"
---
# <a name="iwmdrmnetreceiverprocessregistrationresponse-method"></a>IWMDRMNetReceiver ::P méthode rocessRegistrationResponse

La méthode **ProcessRegistrationResponse** traite une réponse d’inscription envoyée par l’émetteur en réponse à une demande d’inscription.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ProcessRegistrationResponse(
  [in]  BYTE     *pbRegistrationResponse,
  [in]  DWORD    cbRegistrationResponse,
  [out] IUnknown **ppunkCancellationCookie
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbRegistrationResponse* \[ dans\]
</dt> <dd>

Réponse d’inscription reçue de l’émetteur.

</dd> <dt>

*cbRegistrationResponse* \[ dans\]
</dt> <dd>

Taille de la réponse d’inscription en octets.

</dd> <dt>

*ppunkCancellationCookie* \[ à\]
</dt> <dd>

Pointeur qui reçoit un pointeur vers l’interface **IUnknown** d’un objet qui identifie cet appel asynchrone. Ce pointeur d’interface peut être utilisé pour annuler l’appel asynchrone en appelant la méthode [**IWMDRMEventGenerator :: CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Remarques

Cette méthode s’exécute de façon asynchrone ; une fois le traitement terminé, l’événement MEProximityCompleted est envoyé à l’interface **IMFMediaEventGenerator** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> <dt>

[**IWMDRMNetReceiver::GetRegistrationChallenge**](iwmdrmnetreceiver-getregistrationchallenge.md)
</dt> </dl>

 

 





