---
title: Méthode IWMDRMDevice GetMeterChallenge
description: La méthode GetMeterChallenge récupère le défi de contrôle.
ms.assetid: 4c122886-46bd-4e63-8e7d-5e6132363662
keywords:
- Méthode GetMeterChallenge Gestionnaire de périphériques Windows Media
- Méthode GetMeterChallenge Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode GetMeterChallenge
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a916afa90d1db310041f9b92be94d3af9154df4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532488"
---
# <a name="iwmdrmdevicegetmeterchallenge-method"></a>IWMDRMDevice :: GetMeterChallenge, méthode

La méthode **GetMeterChallenge** récupère le défi de contrôle.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetMeterChallenge(
  [in]  BSTR  bstrMeterCert,
  [out] BYTE  **ppbMeterChallenge,
  [out] DWORD *pcbMeterChallenge
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrMeterCert* \[ dans\]
</dt> <dd>

Certificat de contrôle que le propriétaire du contenu envoie à l’ordinateur hôte pour la collecte des données de contrôle associées sur l’appareil

</dd> <dt>

*ppbMeterChallenge* \[ à\]
</dt> <dd>

Résultat du test de contrôle récupéré.

</dd> <dt>

*pcbMeterChallenge* \[ à\]
</dt> <dd>

Taille du test de contrôle, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La méthode retourne un **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | S_OK<br/> |



 

## <a name="remarks"></a>Notes

Les données de contrôle sont collectées et stockées dans le magasin de données DRM sur l’appareil pour le contenu avec contrôle activé. Les actions telles que la lecture seront enregistrées. Lorsque cette fonction est appelée, l’appareil recueille les données de contrôle dans le magasin de données DRM sous la forme d’un document XML et l’envoie au hostcomputer. Si les données sont trop nombreuses, elles sont envoyées en plusieurs phases.

Lorsque l’ordinateur hôte reçoit les données de contrôle, il envoie les données via Internet à l’URL spécifiée dans le certificat de contrôle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMDevice**](iwmdrmdevice.md)
</dt> </dl>

 

 





