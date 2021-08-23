---
title: EmailAction, objet
description: Objet de script qui représente une action qui envoie un message électronique.
ms.assetid: edc0dc4d-eda0-47e0-981f-8521ac4678eb
keywords:
- Objet EmailAction Planificateur de tâches
- Planificateur de tâches d’objets EmailAction, Description
topic_type:
- apiref
api_name:
- EmailAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c918065515322696a33114d2d9b09b7b72d12eb6b74e120a7963835a23321fe5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002477"
---
# <a name="emailaction-object"></a>EmailAction, objet

\[Cet objet n’est plus pris en charge. Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) comme solution de contournement.\]

Objet de script qui représente une action qui envoie un message électronique.

## <a name="members"></a>Membres

L’objet **EmailAction** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **EmailAction** a ces propriétés.



| Propriété                                                    | Type d’accès           | Description                                                                                               |
|:------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**Pièces jointes**](emailaction-attachments.md)<br/>   | Lecture/écriture<br/> | Obtient ou définit un tableau des pièces jointes qui sont envoyées avec le message électronique.<br/>                      |
| [**Cci**](emailaction-bcc.md)<br/>                   | Lecture/écriture<br/> | Obtient ou définit l’adresse ou les adresses de messagerie que vous souhaitez CCI dans le message électronique.<br/>         |
| [**Organismes**](emailaction-body.md)<br/>                 | Lecture/écriture<br/> | Obtient ou définit le corps de l’e-mail qui contient le message électronique.<br/>                            |
| [**CC**](emailaction-cc.md)<br/>                     | Lecture/écriture<br/> | Obtient ou définit l’adresse ou les adresses de messagerie que vous souhaitez envoyer en copie dans le message électronique.<br/>          |
| [**De**](emailaction-from.md)<br/>                 | Lecture/écriture<br/> | Obtient ou définit l’adresse de messagerie à partir de laquelle vous souhaitez envoyer le message électronique.<br/>                           |
| [**HeaderFields**](emailaction-headerfields.md)<br/> | Lecture/écriture<br/> | Obtient ou définit les informations d’en-tête dans le message électronique que vous souhaitez envoyer.<br/>                        |
| [**Identifi**](action-id.md)<br/>                          | Lecture/écriture<br/> | Hérité de l’objet d' [**action**](action.md) . Obtient ou définit l’identificateur de l’action.<br/> |
| [**ReplyTo**](emailaction-replyto.md)<br/>           | Lecture/écriture<br/> | Obtient ou définit l’adresse de messagerie à laquelle vous souhaitez répondre.<br/>                                      |
| [**Serveur**](emailaction-server.md)<br/>             | Lecture/écriture<br/> | Obtient ou définit le nom du serveur que vous utilisez pour envoyer des messages électroniques.<br/>                           |
| [**Objet**](emailaction-subject.md)<br/>           | Lecture/écriture<br/> | Obtient ou définit l’objet du message électronique.<br/>                                                 |
| [**À**](emailaction-to.md)<br/>                     | Lecture/écriture<br/> | Obtient ou définit l’adresse e-mail à laquelle vous souhaitez envoyer le message électronique.<br/>                |
| [**Type**](/windows/win32/api/taskschd/nf-taskschd-iaction-get_type)<br/>                     | Lecture seule<br/>  | Hérité de l’objet d' [**action**](action.md) . Obtient le type d'action.<br/>                   |



 

## <a name="remarks"></a>Remarques

L’action de messagerie doit avoir une valeur valide pour les propriétés [**Server**](emailaction-server.md), [**from**](emailaction-from.md)et [**to**](emailaction-to.md) ou [**CC**](emailaction-cc.md) pour que la tâche s’inscrive et s’exécute correctement.

Lors de la lecture ou de l’écriture de votre propre XML pour une tâche, une action de messagerie est spécifiée à l’aide de l’élément [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) du schéma planificateur de tâches.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclencheur d’événements (script)](/previous-versions//aa446887(v=vs.85)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                                                    |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2008 R2<br/>                                                       |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

