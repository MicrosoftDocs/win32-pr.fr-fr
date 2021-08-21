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
ms.openlocfilehash: 211f8de60cddb153e157af64ee300a4bbaf327d70a1564fbd9e622008c055cb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027567"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Remarques

Si cette méthode est réussie, les appels suivants aux autres méthodes de **IWMDRMNetTransmitter** utiliseront les informations du Challenge traité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





