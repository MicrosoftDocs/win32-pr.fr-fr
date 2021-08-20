---
title: Méthode IWMDRMDevice SetLicenseResponse
description: La méthode SetLicenseResponse définit la réponse de la licence.
ms.assetid: 1ef3ba9d-d14c-4a20-92d6-0bcb604fd9e2
keywords:
- Méthode SetLicenseResponse Gestionnaire de périphériques Windows Media
- Méthode SetLicenseResponse Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode SetLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetLicenseResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4161732002378449f196fdf83c4b880fcc2c02d345a0b08c6e6a464b81acb1dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055717"
---
# <a name="iwmdrmdevicesetlicenseresponse-method"></a>IWMDRMDevice :: SetLicenseResponse, méthode

La méthode **SetLicenseResponse** définit la réponse de la licence.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetLicenseResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbResponse* \[ dans\]
</dt> <dd>

Spécifie la réponse à définir.

</dd> <dt>

*cbResponse* \[ dans\]
</dt> <dd>

Taille de la réponse, en octets.

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

 

 





