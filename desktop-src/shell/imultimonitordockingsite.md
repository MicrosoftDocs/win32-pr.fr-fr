---
description: Implémenté par le navigateur. expose des méthodes qui gèrent le moniteur qui contient la barre des tâches Windows sur un système à plusieurs écrans.
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
ms.openlocfilehash: a5a17e8206af8f0821833f4b2ea250606de29b6fbe74b7a29ced6c5b5dc13ed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458219"
---
# <a name="imultimonitordockingsite-interface"></a>Interface IMultiMonitorDockingSite

Implémenté par le navigateur. expose des méthodes qui gèrent le moniteur qui contient la barre des tâches Windows sur un système à plusieurs écrans.

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



 

## <a name="remarks"></a>Remarques

En général, vous n’implémentez pas l’interface **IMultiMonitorDockingSite** . Le navigateur de l’interpréteur de commandes implémente cette interface pour prendre en charge plusieurs analyses.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                   |



 

 
