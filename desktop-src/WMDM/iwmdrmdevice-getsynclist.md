---
title: Méthode IWMDRMDevice GetSyncList
description: La méthode GetSyncList récupère la liste de synchronisation de licences sur l’appareil. La synchronisation des licences permet à l’ordinateur hôte de transférer des licences mises à jour sur un appareil en fonction des critères spécifiés.
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- Méthode GetSyncList Gestionnaire de périphériques Windows Media
- Méthode GetSyncList Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode GetSyncList
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6424daa720f9987228175a7698a29f7056e5d4b4d174d1d635bbcd1ed7f8382
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119619579"
---
# <a name="iwmdrmdevicegetsynclist-method"></a>IWMDRMDevice :: GetSyncList, méthode

La méthode **GetSyncList** récupère la liste de synchronisation de licences sur l’appareil. La synchronisation des licences permet à l’ordinateur hôte de transférer des licences mises à jour sur un appareil en fonction des critères spécifiés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cMinCountThreshold* \[ dans\]
</dt> <dd>

Seuil de nombre minimal.

</dd> <dt>

*cMinHoursThreshold* \[ dans\]
</dt> <dd>

Seuil d’heures minimum.

</dd> <dt>

*ppbSyncList* \[ à\]
</dt> <dd>

Liste de synchronisation de la licence récupérée.

</dd> <dt>

*pcbSyncList* \[ à\]
</dt> <dd>

Taille de la liste de synchronisation de licence, en octets.

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

 

 





