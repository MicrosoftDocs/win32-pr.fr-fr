---
title: Objet ShowMessageAction
description: Pour les scripts, représente une action qui affiche une boîte de message lorsqu’une tâche est activée.
ms.assetid: fdd22eef-965c-4a81-954c-66011c435ab9
keywords:
- Objet ShowMessageAction Planificateur de tâches
- Planificateur de tâches d’objets ShowMessageAction, Description
topic_type:
- apiref
api_name:
- ShowMessageAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2daec97e66c160cc9da1369e44970f5d9e9ee7c5dcbbcea14cee1e4847a9df0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132364"
---
# <a name="showmessageaction-object"></a>Objet ShowMessageAction

\[Cet objet n’est plus pris en charge. vous pouvez utiliser IExecAction avec la fonction Windows scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) pour afficher un message dans la session utilisateur.\]

Pour les scripts, représente une action qui affiche une boîte de message lorsqu’une tâche est activée.

## <a name="members"></a>Membres

L’objet **ShowMessageAction** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **ShowMessageAction** a ces propriétés.



| Propriété                                                        | Type d’accès           | Description                                                                                               |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Identifi**](action-id.md)<br/>                              | Lecture/écriture<br/> | Hérité de l’objet d' [**action**](action.md) . Obtient ou définit l’identificateur de l’action.<br/> |
| [**MessageBody**](showmessageaction-messagebody.md)<br/> | Lecture/écriture<br/> | Obtient ou définit le texte du message affiché dans le corps de la boîte de message.<br/>                |
| [**Titre**](showmessageaction-title.md)<br/>             | Lecture/écriture<br/> | Obtient ou définit le titre de la boîte de message.<br/>                                                     |
| [**Type**](action-type.md)<br/>                          | Lecture seule<br/>  | Hérité de l’objet d' [**action**](action.md) . Obtient le type d'action.<br/>               |



 

## <a name="remarks"></a>Remarques

Pour une tâche, qui contient une action de MessageBox, la boîte de message s’affiche si la tâche est activée et que la tâche a un type de connexion interactive. Pour définir le type d’ouverture de session de la tâche sur interactif, spécifiez 3 (**\_ \_ \_ jeton interactif d’ouverture de session**) ou 4 (**\_ \_ groupe d’ouverture de session de tâche**) dans la propriété [**LogonType**](principal-logontype.md) du principal de la tâche, ou dans le paramètre *LogonType* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).

Lors de la lecture ou de l’écriture de votre propre code XML pour une tâche, une action de MessageBox est spécifiée à l’aide de l’élément [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) du schéma planificateur de tâches.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez exemple de MessageBox [(script)](/previous-versions//aa381916(v=vs.85)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                    |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2008 R2<br/>                                                       |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

