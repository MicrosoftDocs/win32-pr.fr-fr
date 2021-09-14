---
title: Méthode IWMDRMDevice2 GetLicenseState
description: La méthode GetLicenseState obtient l’état de licence.
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- Méthode GetLicenseState Gestionnaire de périphériques Windows Media
- Méthode GetLicenseState Gestionnaire de périphériques Windows Media, interface IWMDRMDevice2
- Interface IWMDRMDevice2 Windows Media Gestionnaire de périphériques, méthode GetLicenseState
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetLicenseState
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d075d123ae99b26767621fb1a958cd172bc9e42c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008502"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a>IWMDRMDevice2 :: GetLicenseState, méthode

La méthode **GetLicenseState** obtient l’état de licence.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetLicenseState(
  [in]  BYTE  *pbStateQueryData,
  [in]  DWORD cbStateQueryData,
  [out] DWORD *pdwCategory,
  [out] DWORD *pcRemainingCounts,
  [out] DWORD *pcRemainingHours,
  [out] DWORD *pdwReserved
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pbStateQueryData* \[ dans\]
</dt> <dd>

Pointeur vers les données interrogées de l’état de licence.

</dd> <dt>

*cbStateQueryData* \[ dans\]
</dt> <dd>

Nombre de données interrogées.

</dd> <dt>

*pdwCategory* \[ à\]
</dt> <dd>

Pointeur désignant la catégorie.

</dd> <dt>

*pcRemainingCounts* \[ à\]
</dt> <dd>

Pointeur vers les nombres restants.

</dd> <dt>

*pcRemainingHours* \[ à\]
</dt> <dd>

Pointeur vers les heures restantes.

</dd> <dt>

*pdwReserved* \[ à\]
</dt> <dd>

Réservé pour un usage futur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne un code **HRESULT**. Les valeurs possibles sont notamment celles figurant dans le tableau suivant.



| Code de retour                                                                          | Description                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | La méthode est réussie.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>WMDDRMSP. idl</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>Mssachlp. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IWMDRMDevice2**](iwmdrmdevice2.md)
</dt> </dl>

 

 





