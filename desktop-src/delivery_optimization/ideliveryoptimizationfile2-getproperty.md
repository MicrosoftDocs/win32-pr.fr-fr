---
title: 'IDeliveryOptimizationFile2 :: GetProperty, méthode'
description: 'Cette méthode retourne une seule propriété du fichier DO. | IDeliveryOptimizationFile2 :: GetProperty, méthode'
keywords:
- GetProperty, méthode
- Méthode GetProperty, interface IDeliveryOptimizationFile2
- Interface IDeliveryOptimizationFile2, méthode GetProperty
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c53167287cf821ceca26782dab9b8011d40a1785
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322466"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a>IDeliveryOptimizationFile2 :: GetProperty, méthode

Cette méthode retourne une seule propriété du fichier DO.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*propid* \[ dans\]
</dt> <dd>

ID de propriété requis pour la récupération de type DOFilePropertyId.

</dd> <dt>

*propvalue* \[ à\]
</dt> <dd>

Valeur de propriété stockée dans un VARIANT.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs HRESULT suivantes.

| Code de retour                  | Description                                         |
|------------------------------|-----------------------------------------------------|
| **S_OK**                     | Succès                                             |
| **DO_E_UNKNOWN_PROPERTY_ID** | ID de propriété inconnu.                                |
| **DO_E_WRITE_ONLY_PROPERTY** | La propriété est en écriture seule et ne peut pas être lue.      |
| **E_NOT_SET**                | Aucune propriété n’a été définie par le biais de la méthode SetProperty. |
| **E_OUTOFMEMORY**            |  Échec d’allocation de mémoire                          |

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

[**IDeliveryOptimizationFile2**](ideliveryoptimizationfile2.md)
