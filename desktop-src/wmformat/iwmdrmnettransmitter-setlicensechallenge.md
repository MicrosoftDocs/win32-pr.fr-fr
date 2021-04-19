---
title: Méthode IWMDRMNetTransmitter SetLicenseChallenge (wmdrmsdk. h)
description: La méthode SetLicenseChallenge traite un défi de licence envoyé par un récepteur Windows Media DRM pour les périphériques réseau.
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540358"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a>IWMDRMNetTransmitter :: SetLicenseChallenge, méthode

La méthode **SetLicenseChallenge** traite un défi de licence envoyé par un récepteur Windows Media DRM pour les périphériques réseau.

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

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Si cette méthode est réussie, les appels suivants aux autres méthodes de **IWMDRMNetTransmitter** utiliseront les informations du Challenge traité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





