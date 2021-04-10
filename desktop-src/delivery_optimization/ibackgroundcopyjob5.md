---
title: Interface IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Utilisez cette interface pour interroger ou définir plusieurs comportements facultatifs d’un travail.
ms.assetid: C4706E10-40E6-489B-9772-59D581781038
keywords:
- Interface IBackgroundCopyJob5
- Interface IBackgroundCopyJob5, Description
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e76898f7bbfe4d4dc34aec035b842e6671091630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105325"
---
# <a name="ibackgroundcopyjob5-interface"></a>Interface IBackgroundCopyJob5

Utilisez cette interface pour interroger ou définir plusieurs comportements facultatifs d’un travail.

Pour accéder à cette interface, appelez la méthode **méthode ibackgroundcopyjob :: QueryInterface** en utilisant `__uuidof(IBackgroundCopyJob5)` comme identificateur d’interface.

## <a name="members"></a>Membres

L’interface **IBackgroundCopyJob5** hérite de [**méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md). **IBackgroundCopyJob5** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IBackgroundCopyJob5** possède ces méthodes.



| Méthode                                                 | Description                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [**GetProperty**](ibackgroundcopyjob5-getproperty.md) | Méthode générique pour l’obtention des propriétés de tâche DO.<br/> |
| [**SetProperty**](ibackgroundcopyjob5-setproperty.md) | Méthode générique pour définir les propriétés d’un travail.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 est défini comme E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





