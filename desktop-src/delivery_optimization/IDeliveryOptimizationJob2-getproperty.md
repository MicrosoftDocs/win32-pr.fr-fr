---
title: 'IDeliveryOptimizationJob2 :: GetProperty, méthode'
description: Retourne une seule propriété de la tâche d’optimisation de la remise.
keywords:
- GetProperty, méthode
- Méthode GetProperty, interface IDeliveryOptimizationJob2
- Interface IDeliveryOptimizationJob2, méthode GetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2b849d4d9871a730e420f95b52f26b73b8e7b7a7
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520636"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a>IDeliveryOptimizationJob2 :: GetProperty, méthode

Cette méthode retourne une seule propriété de la tâche d’optimisation de la remise.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT GetProperty(
  [in]  DOJobPropertyId propId,
  [out] VARIANT         *propValue
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*propid* \[ dans\]
</dt> <dd>

ID de propriété requis à récupérer. Seul **DOJobPropertyId_ExtendedErrorInfo** de type VT_BSTR est pris en charge.

</dd> <dt>

*propvalue* \[ à\]
</dt> <dd>

Valeur de la propriété résultante, stockée dans un type VARIANT.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cette méthode retourne les valeurs HRESULT suivantes.

| Code de retour                  | Description          |
|------------------------------|----------------------|
| **S_OK**                     | Succès              |
| **DO_E_UNKNOWN_PROPERTY_ID** | ID de propriété inconnu. |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|---------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge  | Windows 10, les applications de bureau version 1803 \[ uniquement\]                                   |
| Serveur minimal pris en charge  | Windows Serveur, version 1709 \[ applications de bureau uniquement\]                               |
| En-tête                    | Deliveryoptimization. h                                                           |
| MIDL                       | DeliveryOptimization. idl                                                         |
| Bibliothèque                   | Dosvc. lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 est défini en tant que 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>Voir aussi

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
