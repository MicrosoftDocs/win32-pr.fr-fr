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
ms.openlocfilehash: b05941619d30ea067dc594e05b7b427ec5d825ef3e0c3c441cdfb3c723e94d4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619569"
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

[**Interface IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





