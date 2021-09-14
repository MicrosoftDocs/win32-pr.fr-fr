---
title: Objet TaskVariables
description: Objet de script qui définit les variables de tâche qui peuvent être passées en tant que paramètres aux gestionnaires de tâches et aux exécutables externes qui sont lancés par les tâches.
ms.assetid: 194babe0-16bd-4a78-af45-139c9c7eacbe
keywords:
- Objet TaskVariables Planificateur de tâches
- Planificateur de tâches d’objets TaskVariables, Description
topic_type:
- apiref
api_name:
- TaskVariables
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00fe20153b0d6d66ca6c7f263a8e76d5a4d480b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008648"
---
# <a name="taskvariables-object"></a>Objet TaskVariables

Objet de script qui définit les variables de tâche qui peuvent être passées en tant que paramètres aux gestionnaires de tâches et aux exécutables externes qui sont lancés par les tâches.

## <a name="members"></a>Membres

L’objet **TaskVariables** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’objet **TaskVariables** a ces méthodes.



| Méthode                                         | Description                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**GetContext**](taskvariables-getcontext.md) | Utilisé pour partager le contexte entre différentes étapes et tâches qui se trouvent dans la même instance de tâche.<br/> |
| [**GetInput**](taskvariables-getinput.md)     | Obtient les variables d’entrée pour une tâche.<br/>                                                           |
| [**SetOutput**](taskvariables-setoutput.md)   | Définit les variables de sortie pour une tâche.<br/>                                                          |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





