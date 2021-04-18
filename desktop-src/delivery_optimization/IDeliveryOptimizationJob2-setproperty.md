---
title: 'IDeliveryOptimizationJob2 :: SetProperty, méthode'
description: Cette méthode n’est pas utilisée.
keywords:
- SetProperty (méthode)
- SetProperty, méthode, interface IDeliveryOptimizationJob2
- Interface IDeliveryOptimizationJob2, méthode SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41375ac3949dd4bcbdd22944f1f1a11d461fc3ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384776"
---
# <a name="ideliveryoptimizationjob2setproperty-method"></a>IDeliveryOptimizationJob2 :: SetProperty, méthode

Cette méthode n’est pas utilisée.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT SetProperty(
  [in]               DOJobPropertyId propId,
  [in, unique] const VARIANT         *propValue
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*propid* \[ dans\]
</dt> <dd>

Inutilisé.

</dd> <dt>

*propvalue* \[ dans\]
</dt> <dd>

Inutilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si propId est **DOJobPropertyId_ExtendedErrorInfo**, la valeur retournée est **DO_E_READ_ONLY_PROPERTY**; sinon, la fonction retourne **DO_E_UNKNOWN_PROPERTY_ID**.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|---------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge  | Applications de bureau Windows 10, version 1803 \[ uniquement\]                                   |
| Serveur minimal pris en charge  | Windows Server, version 1709, \[ applications de bureau uniquement\]                               |
| En-tête                    | Deliveryoptimization. h                                                           |
| MIDL                       | DeliveryOptimization. idl                                                         |
| Bibliothèque                   | Dosvc. lib                                                                        |
| DLL                       | Dosvc.dll                                                                        |
| IID                       | IID_IDeliveryOptimizationJob2 est défini en tant que 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |

## <a name="see-also"></a>Voir aussi

[**IDeliveryOptimizationJob2**](ideliveryoptimizationjob2.md)
