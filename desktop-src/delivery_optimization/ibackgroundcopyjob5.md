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
ms.openlocfilehash: 593f06f74dde7e6891417871cd16dc3730ef005fb90a0a1b6cf5377fda7ebcd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461969"
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
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 est défini comme E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





