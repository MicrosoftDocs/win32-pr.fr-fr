---
title: Méthode IWMDRMDevice SetSecureClockResponse
description: La méthode SetSecureClockResponse définit la réponse de l’horloge sécurisée.
ms.assetid: 3f0a1487-d8c4-478d-bfb0-8d09931fd4b6
keywords:
- Méthode SetSecureClockResponse Gestionnaire de périphériques Windows Media
- Méthode SetSecureClockResponse Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode SetSecureClockResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetSecureClockResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821aceda734aceb7a80774db05465f31213eec47
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008504"
---
# <a name="iwmdrmdevicesetsecureclockresponse-method"></a>IWMDRMDevice :: SetSecureClockResponse, méthode

La méthode **SetSecureClockResponse** définit la réponse de l’horloge sécurisée.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetSecureClockResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbResponse* \[ dans\]
</dt> <dd>

Réponse d’horloge sécurisée à définir.

</dd> <dt>

*cbResponse* \[ dans\]
</dt> <dd>

Taille spécifiée de la réponse d’horloge sécurisée, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

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

 

 





