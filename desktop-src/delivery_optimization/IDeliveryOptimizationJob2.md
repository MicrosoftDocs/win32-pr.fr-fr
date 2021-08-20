---
title: Interface IDeliveryOptimizationJob2
description: 'En savoir plus sur : interface IDeliveryOptimizationJob2'
keywords:
- Interface IDeliveryOptimizationJob2
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4960b754d70aa8ff16e60fc8614fba455f57768caa261d3b50c8c78093919626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811140"
---
# <a name="ideliveryoptimizationjob2-interface"></a>Interface IDeliveryOptimizationJob2

Le IDeliveryOptimizationJob2 permet d’ajouter un seul fichier au travail de téléchargement et de récupérer le fichier immédiatement. Cette interface prend également en charge la définition et l’obtention des propriétés de travaux facultatives.

## <a name="members"></a>Membres

L’interface **IDeliveryOptimizationJob2** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDeliveryOptimizationJob2** a également les types de membres suivants :

- [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDeliveryOptimizationJob2** possède ces méthodes.

| Méthode                                              | Description                                                          |
|:----------------------------------------------------|----------------------------------------------------------------------|
| [**AddFile**](ideliveryoptimizationjob2-addfile.md) | La méthode AddFile ajoute un seul fichier à une tâche DO existante.         |
| [**GetProperty**](ideliveryoptimizationjob2-getproperty.md) | La méthode AddFile ajoute un seul fichier à une tâche DO existante. |
| [**SetProperty**](ideliveryoptimizationjob2-setproperty.md) | Cette méthode n’est pas utilisée.                                       |

## <a name="requirements"></a>Conditions requises

| Condition requise | Valeur |
|--------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows 10, les applications de bureau version 1803 \[ uniquement\]                                   |
| Serveur minimal pris en charge | Windows Serveur, version 1709 \[ applications de bureau uniquement\]                               |
| En-tête                   | Deliveryoptimization. h                                                           |
| MIDL                      | DeliveryOptimization. idl                                                         |
| Bibliothèque                  | Dosvc. lib                                                                        |
| DLL                      | Dosvc.dll                                                                        |
| IID                      | IID_IDeliveryOptimizationJob2 est défini en tant que 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |
