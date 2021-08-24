---
title: Interface IDeliveryOptimizationFile
description: Implémentez l’interface IDeliveryOptimizationFile pour identifier l’état d’un fichier spécifique.
ms.assetid: 4D1D82E1-B39C-4634-A0B7-BC4322796AB2
keywords:
- Interface IDeliveryOptimizationFile
- Interface IDeliveryOptimizationFile, Description
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 880cc982d32e2a81b4263c3cba55331ea5524643adfc8483ed96465154d47cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635739"
---
# <a name="ideliveryoptimizationfile-interface"></a>Interface IDeliveryOptimizationFile

Implémentez l’interface **IDeliveryOptimizationFile** pour identifier l’état d’un fichier spécifique.

## <a name="members"></a>Membres

L’interface **IDeliveryOptimizationFile** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDeliveryOptimizationFile** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDeliveryOptimizationFile** possède ces méthodes.



| Méthode                                                 | Description                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [**GetStats**](ideliveryoptimizationfile-getstats.md) | Retourne les statistiques de téléchargement et de téléchargement pour un fichier spécifique.<br/> |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge      | Windows 10, les applications de bureau version 1709 \[ uniquement\]                                   |
| Serveur minimal pris en charge      | Windows Serveur, version 1709 \[ applications de bureau uniquement\]                               |
| En-tête                        | Deliveryoptimization. h                                                           |
| MIDL                           | DeliveryOptimization. idl                                                         |
| Bibliothèque                       | Dosvc. lib                                                                        |
| DLL                           | Dosvc.dll                                                                        |
| IID                           | IID_IDeliveryOptimizationFile est défini en tant que B76B9699-E99E-4101-803F-A20E325D93E2 |
