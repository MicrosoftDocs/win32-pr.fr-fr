---
title: Interface IDeliveryOptimizationFile2
description: IDeliveryOptimizationFile2 prend en charge le paramétrage et l’obtention des propriétés de fichier facultatives.
keywords:
- Interface IDeliveryOptimizationFile2
- Interface IDeliveryOptimizationFile2, Description
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a45efd821116b24e883ec29d494a1d588559f57a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032629"
---
# <a name="ideliveryoptimizationfile2-interface"></a>Interface IDeliveryOptimizationFile2

**IDeliveryOptimizationFile2** prend en charge le paramétrage et l’obtention des propriétés de fichier facultatives. 

## <a name="members"></a>Membres

L’interface **IDeliveryOptimizationFile2** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDeliveryOptimizationFile2** a également les types de membres suivants :

- [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDeliveryOptimizationFile2** possède ces méthodes.

| Méthode                                                 | Description                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [**GetProperty**](ideliveryoptimizationfile2-getproperty.md)  | Cette méthode retourne une seule propriété du fichier DO. |
| [**SetProperty**](ideliveryoptimizationfile2-setproperty.md)  | Cette méthode définit une seule propriété du fichier DO.    |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------|-----------------------------------------------------------------------------------|
| Client minimal pris en charge      | Applications de bureau Windows 10, version 1803 \[ uniquement\]                                    |
| Serveur minimal pris en charge      | Windows Server, version 1709, \[ applications de bureau uniquement\]                                |
| En-tête                        | Deliveryoptimization. h                                                            |
| MIDL                           | DeliveryOptimization. idl                                                          |
| Bibliothèque                       | Dosvc. lib                                                                         |
| DLL                           | Dosvc.dll                                                                         |
| IID                           | IID_IDeliveryOptimizationFile2 est défini en tant que 3A87296F-6EC2-4126-AB29-E3F8DC4CC390 |
