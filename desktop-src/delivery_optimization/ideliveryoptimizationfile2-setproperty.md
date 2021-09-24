---
title: 'IDeliveryOptimizationFile2 :: SetProperty, méthode'
description: 'Cette méthode retourne une seule propriété du fichier d’optimisation de la remise. | IDeliveryOptimizationFile2 :: SetProperty, méthode'
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
ms.openlocfilehash: c9c392c603ed067520b0f189dfbf547bc12ee80a
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128520821"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a>IDeliveryOptimizationFile2 :: SetProperty, méthode

Cette méthode retourne une seule propriété du fichier d’optimisation de la remise.

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

## <a name="return-value"></a>Valeur de retour

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
