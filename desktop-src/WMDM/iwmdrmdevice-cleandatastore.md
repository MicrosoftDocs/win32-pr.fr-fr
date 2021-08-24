---
title: Méthode IWMDRMDevice CleanDataStore
description: La méthode CleanDataStore démarre le processus de nettoyage de la Banque de données DRM sur l’appareil.
ms.assetid: aad99137-6d2b-4612-8014-9783035af929
keywords:
- Méthode CleanDataStore Gestionnaire de périphériques Windows Media
- Méthode CleanDataStore Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode CleanDataStore
topic_type:
- apiref
api_name:
- IWMDRMDevice.CleanDataStore
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9decc999d1ecb6c97359d1c4c169b84e7f67da88f5fa25bfe2cb17b2c31f9fd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766639"
---
# <a name="iwmdrmdevicecleandatastore-method"></a>IWMDRMDevice :: CleanDataStore, méthode

La méthode **CleanDataStore** démarre le processus de nettoyage de la Banque de données DRM sur l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CleanDataStore(
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Indicateurs pour les critères de nettoyage des magasins.

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

 

 





