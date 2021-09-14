---
title: Méthode IWMDRMNetTransmitter SetLicenseChallenge (wmdrmsdk. h)
description: la méthode SetLicenseChallenge traite un défi de licence envoyé par une Windows Media DRM pour les périphériques réseau.
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- Méthode SetLicenseChallenge format Windows Media
- Méthode SetLicenseChallenge format Windows Media, interface IWMDRMNetTransmitter
- Interface IWMDRMNetTransmitter Windows Media format, méthode SetLicenseChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.SetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94b83ca615896039a592d147fe8c14d15493cec0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127195955"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a>IWMDRMNetTransmitter :: SetLicenseChallenge, méthode

la méthode **SetLicenseChallenge** traite un défi de licence envoyé par une Windows Media DRM pour les périphériques réseau.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbLicenseChallenge* \[ dans\]
</dt> <dd>

Pointeur vers les données de demande de licence qui ont été envoyées par un récepteur.

</dd> <dt>

*cbLicenseChallenge* \[ dans\]
</dt> <dd>

Taille de la demande de licence en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Si cette méthode est réussie, les appels suivants aux autres méthodes de **IWMDRMNetTransmitter** utiliseront les informations du Challenge traité.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





