---
title: Interface IRDVTaskPlugin
description: L’interface IRDVTaskPlugin est implémentée par un agent de tâche de mise à jour de machine virtuelle pour permettre à l’agent de tâche de gérer les mises à jour système pour un ordinateur virtuel.
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IRDVTaskPlugin
- Services Bureau à distance de l’interface IRDVTaskPlugin, Description
topic_type:
- apiref
api_name:
- IRDVTaskPlugin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe76f0b0b92286d5a4b7db5126706fd55bdb6f580c11fda1dcaa55a47be4678c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129168"
---
# <a name="irdvtaskplugin-interface"></a>Interface IRDVTaskPlugin

L’interface **IRDVTaskPlugin** est implémentée par un agent de *tâche* de mise à jour de machine virtuelle pour permettre à l’agent de tâche de gérer les mises à jour système pour un ordinateur virtuel. Cette interface est utilisée par l' *agent déclencheur*, qui est implémenté par le système hôte.

## <a name="members"></a>Membres

L’interface **IRDVTaskPlugin** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IRDVTaskPlugin** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **IRDVTaskPlugin** possède ces méthodes.



| Méthode                                          | Description                                                        |
|:------------------------------------------------|:-------------------------------------------------------------------|
| [**Initialiser**](irdvtaskplugin-initialize.md) | Appelé pour initialiser l’agent de tâche.<br/>                    |
| [**StartTask**](irdvtaskplugin-starttask.md)   | Appelé pour démarrer la tâche de mise à jour sur la machine virtuelle.<br/> |
| [**Terminate**](irdvtaskplugin-terminate.md)   | Appelé lorsque l’agent de tâche est arrêté.<br/>          |



 

### <a name="properties"></a>Propriétés

L’interface **IRDVTaskPlugin** possède les propriétés suivantes.



| Propriété                                                   | Type d’accès          | Description                                             |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------|
| [**PluginName**](irdvtaskplugin-pluginname.md)<br/> | Lecture seule<br/> | Contient le nom complet de l’agent de tâche.<br/> |



 

## <a name="remarks"></a>Remarques

L’agent de tâche est exécuté sur l’ordinateur virtuel lorsque cet ordinateur virtuel est planifié pour une mise à jour du système. L’agent de tâche met à jour l’ordinateur virtuel lorsque la méthode [**StartTask**](irdvtaskplugin-starttask.md) est appelée.

Pour inscrire l’agent de tâche, ajoutez la clé suivante au registre de l’ordinateur virtuel :

**HKEY \_ \_** plug-ins des tâches de l’ordinateur LOCAL \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Terminal Server** \\  \\  \\ **TaskAgentName**

Sous cette clé de Registre, ajoutez les valeurs suivantes :



| Nom                     | Type                      | Description                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| **IDENTIFICATEUR**<br/>     | **SZ de REG \_**<br/>    | Chaîne qui représente le **CLSID** de l’agent de tâche.<br/>          |
| **IsEnabled**<br/> | **\_valeur DWORD reg**<br/> | 0 si l’agent de tâche est désactivé ou 1 si l’agent de tâche est activé.<br/> |



 

> [!Note]  
> Plusieurs agents de tâche peuvent être inscrits, mais un seul agent de tâche sera utilisé. Si plusieurs agents de tâche sont activés, seul le premier est utilisé.

 

Bien que cette interface soit prise en charge sur les systèmes d’exploitation identifiés dans la configuration requise ci-dessous, elle est utilisée uniquement si la machine virtuelle est hébergée sur Windows Server 2012.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------|
| Client minimal pris en charge<br/> | Windows 7 Entreprise<br/>   |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/> |



 

