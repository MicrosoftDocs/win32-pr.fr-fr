---
title: Interface IRDVTaskPluginNotifySink
description: L’interface IRDVTaskPluginNotifySink est utilisée par l’agent de tâche pour communiquer avec l’agent déclencheur.
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IRDVTaskPluginNotifySink
- Services Bureau à distance de l’interface IRDVTaskPluginNotifySink, Description
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0dadaf387fcf6e8381404440e0d31dd210b9f8a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742069"
---
# <a name="irdvtaskpluginnotifysink-interface"></a>Interface IRDVTaskPluginNotifySink

L’interface **IRDVTaskPluginNotifySink** est utilisée par l’agent de tâche pour communiquer avec l’agent déclencheur. Un pointeur vers cette interface est passé à l’agent de tâche dans la méthode [**IRDVTaskPlugin :: Initialize**](irdvtaskplugin-initialize.md) .

## <a name="members"></a>Membres

L’interface **IRDVTaskPluginNotifySink** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IRDVTaskPluginNotifySink** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IRDVTaskPluginNotifySink** possède ces méthodes.



| Méthode                                                                  | Description                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**DeleteSchedule**](irdvtaskpluginnotifysink-deleteschedule.md)       | Appelé par l’agent de tâche pour supprimer une tâche planifiée.<br/>                   |
| [**OnTaskStateChange**](irdvtaskpluginnotifysink-ontaskstatechange.md) | Permet d’informer l’agent déclencheur que l’état d’une tâche a changé.<br/> |
| [**OnTerminated**](irdvtaskpluginnotifysink-onterminated.md)           | Appelée par l’agent de tâche pour demander que l’agent de tâche soit arrêté.<br/>  |
| [**ScheduleTask,**](irdvtaskpluginnotifysink-scheduletask.md)           | Appelé par l’agent de tâche pour planifier une tâche.<br/>                           |



 

## <a name="remarks"></a>Notes

Bien que cette interface soit prise en charge sur les systèmes d’exploitation identifiés dans la configuration requise ci-dessous, elle n’est utilisée que si la machine virtuelle est hébergée sur Windows Server 2012.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------|
| Client minimal pris en charge<br/> | Windows 7 Entreprise<br/>   |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/> |



 

