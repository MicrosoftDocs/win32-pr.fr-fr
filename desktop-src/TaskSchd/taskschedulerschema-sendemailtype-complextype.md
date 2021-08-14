---
title: Type complexe sendEmailType
description: Définit le type d’action utilisé pour spécifier qu’un courrier électronique sera envoyé lors de l’exécution d’une tâche. Ce type définit tous les éléments utilisés pour modéliser le message électronique.
ms.assetid: e384971f-e7e4-4206-9d15-9555dfcbac2f
keywords:
- Planificateur de tâches de type complexe sendEmailType
topic_type:
- apiref
api_name:
- sendEmailType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0242700b2f22050741d9de175b7dae532cc5ef4bb2097fadb23799ce3b2f82b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356341"
---
# <a name="sendemailtype-complex-type"></a>Type complexe sendEmailType

Définit le type d’action utilisé pour spécifier qu’un courrier électronique sera envoyé lors de l’exécution d’une tâche. Ce type définit tous les éléments utilisés pour modéliser le message électronique.

``` syntax
<xs:complexType name="sendEmailType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Server"
                    type="nonEmptyString"
                 />
                <xs:element name="Subject"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="To"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Cc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Bcc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="ReplyTo"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="From"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="HeaderFields"
                    type="headerFieldsType"
                    minOccurs="0"
                 />
                <xs:element name="Body"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Attachments"
                    type="attachmentsType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                        | Type                                                                         | Description                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**Pièces jointes**](taskschedulerschema-attachments-sendemailtype-element.md)   | [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md)   | Spécifie une liste de pièces jointes dans le message électronique.<br/>                                 |
| [**Cci**](taskschedulerschema-bcc-sendemailtype-element.md)                   | **string**                                                                   | Spécifie les adresses de messagerie utilisées sur la ligne CCI d’un message électronique.<br/>               |
| [**Organismes**](taskschedulerschema-body-sendemailtype-element.md)                 | **string**                                                                   | Spécifie le texte dans le corps du message électronique.<br/>                                  |
| [**CC**](taskschedulerschema-cc-sendemailtype-element.md)                     | **string**                                                                   | Spécifie les adresses de messagerie utilisées sur la ligne CC d’un message électronique.<br/>                |
| [**De**](taskschedulerschema-from-sendemailtype-element.md)                 | **string**                                                                   | Spécifie l’adresse de messagerie de l’expéditeur.<br/>                                            |
| [**HeaderFields**](taskschedulerschema-headerfields-sendemailtype-element.md) | [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) | Spécifie les champs d’en-tête et leurs valeurs utilisées dans l’en-tête du message électronique.<br/> |
| [**ReplyTo**](taskschedulerschema-replyto-sendemailtype-element.md)           | **string**                                                                   | Spécifie les adresses de messagerie auxquelles il est répondu dans le message électronique.<br/>               |
| [**Serveur**](taskschedulerschema-server-sendemailtype-element.md)             | [**nonEmptyString**](taskschedulerschema-nonemptystring-simpletype.md)      | Spécifie le serveur de messagerie utilisé pour envoyer le message électronique. <br/>                           |
| [**Objet**](taskschedulerschema-subject-sendemailtype-element.md)           | **string**                                                                   | Spécifie l’objet du message électronique.<br/>                                           |
| [**À**](taskschedulerschema-to-sendemailtype-element.md)                     | **string**                                                                   | Spécifie les adresses de messagerie auxquelles le courrier électronique sera envoyé.<br/>                        |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





