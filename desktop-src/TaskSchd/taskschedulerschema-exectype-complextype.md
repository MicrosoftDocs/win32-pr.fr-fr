---
title: Type complexe execType
description: Définit les éléments enfants et les informations de séquencement de l’élément exec (actionGroup).
ms.assetid: ab23801a-453d-4fab-8584-30c5c9d57dff
keywords:
- Planificateur de tâches de type complexe execType
topic_type:
- apiref
api_name:
- execType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e0726930f902ec0458f42fff9cdce39026cf63ddab92982bc30da33ca671712
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796629"
---
# <a name="exectype-complex-type"></a>Type complexe execType

Définit les éléments enfants et les informations de séquencement de l’élément [**Exec (actionGroup)**](taskschedulerschema-exec-actiongroup-element.md) .

``` syntax
<xs:complexType name="execType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Command"
                    type="pathType"
                 />
                <xs:element name="Arguments"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="WorkingDirectory"
                    type="pathType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                           | Type                                                        | Description                                                                                                  |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**Arguments**](taskschedulerschema-arguments-exectype-element.md)               | **string**                                                  | Spécifie les arguments associés à l’opération de ligne de commande. <br/>                              |
| [**Commande**](taskschedulerschema-command-exectype-element.md)                   | [**pathType**](taskschedulerschema-pathtype-simpletype.md) | Spécifie le fichier exécutable ou le document à exécuter.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | [**pathType**](taskschedulerschema-pathtype-simpletype.md) | Spécifie le répertoire dans lequel le fichier exécutable ou les fichiers utilisés par l’exécutable existent.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types complexes de schéma Planificateur de tâches](task-scheduler-schema-complex-types.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





