---
description: L’interface IMonitorEventer fournit des méthodes pour soumettre des événements et allouer et libérer des ressources de surveillance.
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: Interface IMonitorEventer (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 2af49529a74c23e0f4d4e77e0d2608cd44d12028d93022750fbbd3af891e2e77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118365487"
---
# <a name="imonitoreventer-interface"></a>Interface IMonitorEventer

L’interface **IMonitorEventer** fournit des méthodes pour soumettre des événements et allouer et libérer des ressources de surveillance.

## <a name="members"></a>Membres

L’interface **IMonitorEventer** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMonitorEventer** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IMonitorEventer** possède ces méthodes.



| Méthode                                                 | Description                                        |
|:-------------------------------------------------------|:---------------------------------------------------|
| [**FreeEventData**](imonitoreventer-freeeventdata.md) | Libère de l’espace alloué pour les données du moniteur.<br/> |
| [**GetEventData**](imonitoreventer-geteventdata.md)   | Alloue de l’espace pour les données du moniteur.<br/>       |
| [**SendNMEvent**](imonitoreventer-sendnmevent.md)     | Envoie des événements à WMI.<br/>                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

