---
description: Active l’achèvement des tâches.
ms.assetid: 323343D6-FC4A-4A5F-B065-DD72B6077F99
title: Interface TaskCompletionClient
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: d03e52a15e6689b7f1ea98a2f1021874cab6a8967dd148b7eaf685ff3984e8cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773649"
---
# <a name="taskcompletionclient-interface"></a>Interface TaskCompletionClient

Active l’achèvement des tâches.

## <a name="members"></a>Membres

L’interface **TaskCompletionClient** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **TaskCompletionClient** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **TaskCompletionClient** possède ces méthodes.



| Méthode                                                                    | Description                            |
|:--------------------------------------------------------------------------|:---------------------------------------|
| [**ApplyTaskCompletion**](taskcompletionclient-applytaskcompletion.md)   | Commence l’achèvement de la tâche.<br/> |
| [**RevokeTaskCompletion**](taskcompletionclient-revoketaskcompletion.md) | Met fin à l’achèvement de la tâche.<br/>   |



 

## <a name="remarks"></a>Remarques

Le GUID de cette interface est « E97D552D-9AE9-46AA-9151-D2DA4BBB5E96 ».

Cette API est déconseillée et peut ne pas être disponible dans les versions ultérieures de Windows. Les applications doivent utiliser les API dans le [**Windows. Espace de noms ApplicationModel. ExtendedExecution**](/uwp/api/Windows.ApplicationModel.ExtendedExecution?view=winrt-19041) à la place.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



 

 
