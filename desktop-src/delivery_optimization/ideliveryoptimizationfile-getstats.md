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
ms.openlocfilehash: f4e2f0a3b680e682944740cb570bfb4889b22ba8e7ec56d3aefc9e34fcdd6a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635759"
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

## <a name="return-value"></a>Valeur retournée

Cette méthode doit retourner **S_OK**.

## <a name="requirements"></a>Configuration requise



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

 

 





