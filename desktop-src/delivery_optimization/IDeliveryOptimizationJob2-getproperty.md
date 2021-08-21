---
title: 'IDeliveryOptimizationJob2 :: GetProperty, méthode'
description: Retourne une seule propriété du travail DO.
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
ms.openlocfilehash: cdca86cb374eded0eabcc1d623d2218a6dc1f4cd5613a18e16b4ec9ab93156b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811250"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a>IDeliveryOptimizationJob2 :: GetProperty, méthode

Cette méthode retourne une seule propriété du travail DO.

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

## <a name="return-value"></a>Valeur retournée

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
