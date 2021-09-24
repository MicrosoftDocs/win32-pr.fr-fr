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
ms.openlocfilehash: 7868dc29a746566291a10f6b8f8854f33fe2221f
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128521186"
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
| [**AddFile**](ideliveryoptimizationjob2-addfile.md) | La méthode AddFile ajoute un seul fichier à une tâche d’optimisation de la remise existante.         |
| [**GetProperty**](ideliveryoptimizationjob2-getproperty.md) | La méthode AddFile ajoute un seul fichier à une tâche d’optimisation de la remise existante. |
| [**SetProperty**](ideliveryoptimizationjob2-setproperty.md) | Cette méthode n’est pas utilisée.                                       |

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge | Windows 10, les applications de bureau version 1803 \[ uniquement\]                                   |
| Serveur minimal pris en charge | Windows Serveur, version 1709 \[ applications de bureau uniquement\]                               |
| En-tête                   | Deliveryoptimization. h                                                           |
| MIDL                      | DeliveryOptimization. idl                                                         |
| Bibliothèque                  | Dosvc. lib                                                                        |
| DLL                      | Dosvc.dll                                                                        |
| IID                      | IID_IDeliveryOptimizationJob2 est défini en tant que 18995A26-BF59-4ABE-9F8B-D5092D5A2405 |
