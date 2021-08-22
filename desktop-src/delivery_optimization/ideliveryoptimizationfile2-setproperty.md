---
title: 'IDeliveryOptimizationFile2 :: SetProperty, méthode'
description: 'Cette méthode retourne une seule propriété du fichier DO. | IDeliveryOptimizationFile2 :: SetProperty, méthode'
keywords:
- SetProperty (méthode)
- SetProperty, méthode, interface IDeliveryOptimizationFile2
- Interface IDeliveryOptimizationFile2, méthode SetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 99ed42acb94f260e229abfe9df428aaa61d3658cb887892b84bb73fd6e7e63e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635719"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a>IDeliveryOptimizationFile2 :: SetProperty, méthode

Cette méthode retourne une seule propriété du fichier DO.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT SetProperty(
  [in]               DOFilePropertyId propId,
  [in, unique] const VARIANT          *propValue
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*propid* \[ dans\]
</dt> <dd>

ID de propriété requis à définir de type DOFilePropertyId.

</dd> <dt>

*propvalue* \[ dans\]
</dt> <dd>

Valeur de la propriété à définir, de type VARIANT.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs HRESULT suivantes.

| Code de retour                  | Description                                                        |
|------------------------------|--------------------------------------------------------------------|
| **S_OK**                     | Succès                                                            |
| **DO_E_UNKNOWN_PROPERTY_ID** | ID de propriété inconnu                                                |
| **DO_E_INVALID_STATE**       | Le travail n’est pas actuellement dans un État qui autorise un paramètre de propriété |

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

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
