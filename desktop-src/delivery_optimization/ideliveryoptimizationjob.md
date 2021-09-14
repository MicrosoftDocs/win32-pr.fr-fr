---
title: Interface IDeliveryOptimizationJob (Deliveryoptimization. h)
description: Utilisez l’interface IDeliveryOptimizationJob pour télécharger des plages d’un fichier.
ms.assetid: 7549F3B2-47E9-44DA-BD9C-AEFB0C36FF15
keywords:
- Interface IDeliveryOptimizationJob
- Interface IDeliveryOptimizationJob, Description
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ee2ce35b8089e9b05b7291f535361e39140f856
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921747"
---
# <a name="ideliveryoptimizationjob-interface"></a>Interface IDeliveryOptimizationJob

Utilisez l’interface **IDeliveryOptimizationJob** pour télécharger des plages d’un fichier.

## <a name="members"></a>Membres

L’interface **IDeliveryOptimizationJob** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDeliveryOptimizationJob** a également les types de membres suivants :

- [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IDeliveryOptimizationJob** possède ces méthodes.



| Méthode                                                                  | Description                                                                                         |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [**AddFileWithRanges**](ideliveryoptimizationjob-addfilewithranges.md) | Ajoute un fichier à un travail de téléchargement et spécifie les plages du fichier que vous souhaitez télécharger.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationJob est défini comme EE2584CF-A69C-4848-B633-2649962B3EF7<br/>         |



 

