---
title: Méthode IWMDRMDevice GetSecureClockChallenge
description: La méthode GetSecureClockChallenge récupère le résultat du Challenge d’horloge sécurisé.
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- Méthode GetSecureClockChallenge Gestionnaire de périphériques Windows Media
- Méthode GetSecureClockChallenge Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode GetSecureClockChallenge
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClockChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaed21ddffb9c2001c3b57d32d34ac9106ede7cecaff723cb95d8cee1c428fb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957249"
---
# <a name="iwmdrmdevicegetsecureclockchallenge-method"></a>IWMDRMDevice :: GetSecureClockChallenge, méthode

La méthode **GetSecureClockChallenge** récupère le résultat du Challenge d’horloge sécurisé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSecureClockChallenge(
  [out] BYTE  **ppbChallenge,
  [out] DWORD *pcbChallenge
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppbChallenge* \[ à\]
</dt> <dd>

Résultat de la stimulation récupéré.

</dd> <dt>

*pcbChallenge* \[ à\]
</dt> <dd>

Taille du résultat de la vérification, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetSecureClock**](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[**Interface IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





