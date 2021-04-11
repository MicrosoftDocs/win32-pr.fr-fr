---
title: Type complexe registrationInfoType
description: Définit les éléments enfants et les informations de séquencement pour l’élément RegistrationInfo.
ms.assetid: 855eb0a4-6037-4868-ae09-6c9f01d91545
keywords:
- Planificateur de tâches de type complexe registrationInfoType
topic_type:
- apiref
api_name:
- registrationInfoType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe98a06daf84ec753c26903cc09787cec65c8d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942421"
---
# <a name="registrationinfotype-complex-type"></a>Type complexe registrationInfoType

Définit les éléments enfants et les informations de séquencement pour l’élément [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) .

``` syntax
<xs:complexType name="registrationInfoType">
    <xs:all>
        <xs:element name="URI"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="SecurityDescriptor"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Source"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Date"
            type="dateTime"
            minOccurs="0"
         />
        <xs:element name="Author"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Version"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Description"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Documentation"
            type="string"
            minOccurs="0"
         />
    </xs:all>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                           | Type     | Description                                                                                                        |
|---------------------------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------|
| [**Auteur**](taskschedulerschema-author-registrationinfotype-element.md)                         | string   | Spécifie l’auteur de la tâche.<br/>                                                                       |
| [**Date**](taskschedulerschema-date-registrationinfotype-element.md)                             | dateTime | Spécifie la date et l’heure d’enregistrement de la tâche.<br/>                                                |
| [**Description**](taskschedulerschema-description-registrationinfotype-element.md)               | string   | Spécifie la description de la tâche.<br/>                                                                  |
| [**Correspondante**](taskschedulerschema-documentation-registrationinfotype-element.md)           | string   | Spécifie toute documentation supplémentaire pour la tâche.<br/>                                                    |
| [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) | string   | Spécifie le descripteur de sécurité de la tâche.<br/>                                                          |
| [**Code**](taskschedulerschema-source-registrationinfotype-element.md)                         | string   | Spécifie l’origine de la tâche. Par exemple, à partir d’un composant, d’un service, d’une application ou d’un utilisateur.<br/> |
| [**URI**](taskschedulerschema-uri-registrationinfotype-element.md)                               | anyURI   | Spécifie l’URI de la tâche.<br/>                                                                          |
| [**Version**](taskschedulerschema-version-registrationinfotype-element.md)                       | string   | Spécifie le numéro de version de la tâche.<br/>                                                               |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types complexes de schéma Planificateur de tâches](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





