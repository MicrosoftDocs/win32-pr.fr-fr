---
title: Méthode IWMDRMDevice SetMeterResponse
description: La méthode SetMeterResponse définit la réponse de contrôle.
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- Méthode SetMeterResponse Gestionnaire de périphériques Windows Media
- Méthode SetMeterResponse Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode SetMeterResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed70b158215eb831296ad083af8cd2c001cb38f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126919484"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a>IWMDRMDevice :: SetMeterResponse, méthode

La méthode **SetMeterResponse** définit la réponse de contrôle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetMeterResponse(
  [in]  BYTE  *pbMeterResponse,
  [in]  DWORD cbMeterResponse,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbMeterResponse* \[ dans\]
</dt> <dd>

Réponse de contrôle à définir.

</dd> <dt>

*cbMeterResponse* \[ dans\]
</dt> <dd>

Taille de la réponse de contrôle, en octets.

</dd> <dt>

*pdwFlags* \[ à\]
</dt> <dd>

Indicateurs de réponse. Cette valeur doit être l’un des indicateurs suivants.



| Indicateur                            | Description              |
|---------------------------------|--------------------------|
| \_réponse du compteur WMDRM \_ \_ All     | Toutes les réponses de compteur.     |
| réponse de compteur de WMDRM \_ \_ \_ partielle | Réponses à des compteurs partiels. |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





