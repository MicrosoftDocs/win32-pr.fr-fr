---
title: IDeliveryOptimizationFile GetStats, méthode (Deliveryoptimization. h)
description: Retourne les statistiques de téléchargement et de téléchargement pour un fichier spécifique.
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- GetStats (méthode)
- GetStats, méthode, interface IDeliveryOptimizationFile
- Interface IDeliveryOptimizationFile, GetStats, méthode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile.GetStats
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08c5cff0672130049c325a00cb63c8dbc5c2e8ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915656"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a>IDeliveryOptimizationFile :: GetStats, méthode

Retourne les statistiques de téléchargement et de téléchargement pour un fichier spécifique.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*swarmStats* \[ à\]
</dt> <dd>

Retourne les statistiques de téléchargement et de téléchargement pour un fichier spécifique. Pour plus d’informations, consultez la structure [**DOSwarmStats**](doswarmstats.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode doit retourner **S_OK**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationFile est défini en tant que B76B9699-E99E-4101-803F-A20E325D93E2<br/>        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IDeliveryOptimizationFile**](ideliveryoptimizationfile.md)
</dt> </dl>

 

 





