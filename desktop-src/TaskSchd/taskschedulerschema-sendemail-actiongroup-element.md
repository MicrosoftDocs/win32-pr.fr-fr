---
title: SendEmail (actionGroup), élément
description: Représente une action qui envoie un message électronique.
ms.assetid: 83416b02-8327-47b3-9dfc-1bf5b9365728
keywords:
- Élément SendEmail Planificateur de tâches
topic_type:
- apiref
api_name:
- SendEmail
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 81f6f3437521dea2c5cf6e157ad7997718632081
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942580"
---
# <a name="sendemail-actiongroup-element"></a>SendEmail (actionGroup), élément

Représente une action qui envoie un message électronique.

``` syntax
<xs:element name="SendEmail"
    type="sendEmailType"
 />
```

L’élément **SendEmail** est défini par [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                         | Dérivé de                                                       | Description                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Actions**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contient les actions effectuées par la tâche.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                        | Type                                                                         | Description                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Pièces jointes**](taskschedulerschema-attachments-sendemailtype-element.md)   | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md)   | Spécifie une liste de pièces jointes dans le message électronique.<br/>                                 |
| [**Cci**](taskschedulerschema-bcc-sendemailtype-element.md)                   | **string**                                                                   | Spécifie les adresses de messagerie utilisées sur la ligne CCI d’un message électronique.<br/>               |
| [**body**](taskschedulerschema-body-sendemailtype-element.md)                 | **string**                                                                   | Spécifie le texte dans le corps du message électronique.<br/>                                  |
| [**CC**](taskschedulerschema-cc-sendemailtype-element.md)                     | **string**                                                                   | Spécifie les adresses de messagerie utilisées sur la ligne CC d’un message électronique.<br/>                |
| [**De**](taskschedulerschema-from-sendemailtype-element.md)                 | **string**                                                                   | Spécifie l’adresse de messagerie de l’expéditeur.<br/>                                            |
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | Spécifie les champs d’en-tête et leurs valeurs utilisées dans l’en-tête du message électronique.<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **string**                                                                   | Spécifie les adresses de messagerie auxquelles il est répondu dans le message électronique.<br/>               |
| [**Serveur**](taskschedulerschema-server-sendemailtype-element.md)             | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)      | Spécifie le serveur de messagerie utilisé pour envoyer le message électronique. <br/>                           |
| [**Objet**](taskschedulerschema-subject-sendemailtype-element.md)           | **string**                                                                   | Spécifie l’objet du message électronique.<br/>                                           |
| [**Pour**](taskschedulerschema-to-sendemailtype-element.md)                     | **string**                                                                   | Spécifie les adresses de messagerie auxquelles le courrier électronique sera envoyé.<br/>                        |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez l’interface [**IEmailAction**](/windows/win32/api/taskschd/nn-taskschd-iemailaction) .

Pour le développement de scripts, consultez l’objet [**EmailAction**](emailaction.md) .

**Windows 8 et Windows Server 2012 :** Cet élément a été supprimé. Utilisez IExecAction avec l’applet de commande PowerShell [**Send-MailMessage**](/powershell/module/microsoft.powershell.utility/send-mailmessage) comme solution de contournement.

## <a name="examples"></a>Exemples

Pour obtenir un exemple complet du code XML d’une tâche qui spécifie une action de messagerie, consultez [exemple de déclencheur d’événements (XML)](/previous-versions//aa446889(v=vs.85)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |
| Fin de la prise en charge des clients<br/>    | Windows 7<br/>                                 |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2008 R2<br/>                    |



 

