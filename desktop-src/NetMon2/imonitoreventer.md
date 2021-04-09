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
ms.openlocfilehash: 7d4ca58b5a0787638eee54b7733b4e1a8fbf7ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862410"
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



 

