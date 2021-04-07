---
description: L’interface IMonitor fournit des méthodes qui contrôlent l’opération de surveillance. Ces méthodes sont appelées par le service de contrôle d’analyse (MCSVC).
ms.assetid: 53140e7d-c3a1-45cd-aaa4-c6f5021a6102
title: Interface IMonitor (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 1b6ba91860905010fd14a46cd4608eaee3da80fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863270"
---
# <a name="imonitor-interface"></a>Interface IMonitor

L’interface **Imonitor** fournit des méthodes qui contrôlent l’opération de surveillance. Ces méthodes sont appelées par le [*service de contrôle d’analyse*](m.md) (MCSVC).

## <a name="members"></a>Membres

L’interface **Imonitor** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Imonitor** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **Imonitor** possède ces méthodes.



| Méthode                                        | Description                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**Configurer**](imonitor-doconfigure.md)   | Met à jour la configuration de l’analyse.<br/>                                                                           |
| [**Ininitialize**](imonitor-doinitialize.md) | Initialise une analyse.<br/>                                                                                   |
| [**OnFrames**](imonitor-onframes.md)         | Indique l’état d’un événement Frame.<br/>                                                                   |
| [**OnStart**](imonitor-onstart.md)           | Indique que l’analyse a été correctement configurée et que la capture de données va commencer.<br/> |
| [**OnStatus**](imonitor-onstatus.md)         | Indique un événement de statut NPP.<br/>                                                                           |
| [**OnStop**](imonitor-onstop.md)             | Indique la fin de la capture des données.<br/>                                                                       |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

