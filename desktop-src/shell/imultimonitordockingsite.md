---
description: Implémenté par le navigateur. Expose des méthodes qui gèrent le moniteur qui contient la barre des tâches Windows sur un système à plusieurs écrans.
title: Interface IMultiMonitorDockingSite
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite
api_type:
- COM
api_location: ''
ms.assetid: af9a7a9e-bd7c-4b17-9cb6-008df5c820d8
ms.openlocfilehash: 3aa1ccb1c25fd2896ce9e18ba52ea3f46b1882af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991821"
---
# <a name="imultimonitordockingsite-interface"></a>Interface IMultiMonitorDockingSite

Implémenté par le navigateur. Expose des méthodes qui gèrent le moniteur qui contient la barre des tâches Windows sur un système à plusieurs écrans.

## <a name="members"></a>Membres

L’interface **IMultiMonitorDockingSite** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMultiMonitorDockingSite** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IMultiMonitorDockingSite** possède ces méthodes.



| Méthode                                                            | Description                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**GetMonitor**](imultimonitordockingsite-getmonitor.md)         | Obtient l’analyseur par défaut actuel.<br/>                                               |
| [**RequestMonitor**](imultimonitordockingsite-requestmonitor.md) | Vérifie que le moniteur est actif et disponible.<br/>                              |
| [**SetMonitor**](imultimonitordockingsite-setmonitor.md)         | Modifie l’analyse qui est utilisée pour les barres d’outils ancrées sur un système à plusieurs écrans.<br/> |



 

## <a name="remarks"></a>Notes

En général, vous n’implémentez pas l’interface **IMultiMonitorDockingSite** . Le navigateur de l’interpréteur de commandes implémente cette interface pour prendre en charge plusieurs analyses.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                   |



 

 
