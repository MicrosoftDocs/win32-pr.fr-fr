---
title: Type complexe SystemPropertiesType
description: Définit les informations qui identifient le fournisseur et comment il a été activé, l’événement, le canal vers lequel l’événement a été écrit et les informations système telles que les ID de processus et de thread.
ms.assetid: f86f7940-86cf-49ba-8f09-bf6f473d60fd
keywords:
- SystemPropertiesType type complexe EventLog
topic_type:
- apiref
api_name:
- SystemPropertiesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f7391362938502f0c307faab4d7b9166633647b093e5154b3aa56512c6ee4e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620239"
---
# <a name="systempropertiestype-complex-type"></a>Type complexe SystemPropertiesType

Définit les informations qui identifient le fournisseur et comment il a été activé, l’événement, le canal vers lequel l’événement a été écrit et les informations système telles que les ID de processus et de thread.

``` syntax
<xs:complexType name="SystemPropertiesType">
    <xs:sequence>
        <xs:element name="Provider">
            <xs:complexType>
                <xs:attribute name="Name"
                    type="anyURI"
                    use="optional"
                 />
                <xs:attribute name="Guid"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="EventSourceName"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="EventID">
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedShort"
                    >
                        <xs:attribute name="Qualifiers"
                            type="unsignedShort"
                            use="optional"
                         />
                    </xs:extension>
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Version"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="unsignedShort"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            type="HexInt64Type"
            minOccurs="0"
         />
        <xs:element name="TimeCreated"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="SystemTime"
                    type="dateTime"
                    use="optional"
                 />
                <xs:attribute name="RawTime"
                    type="unsignedLong"
                    use="optional"
                 />
            </xs:complexType>
            <xs:key name="uniqueAtt">
                <xs:selector
                    xpath="."
                 />
                <xs:field
                    xpath="@SystemTime|@RawTime"
                 />
            </xs:key>
        </xs:element>
        <xs:element name="EventRecordID"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedLong"
                     />
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Correlation"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ActivityID"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="RelatedActivityID"
                    type="GUIDType"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Execution"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ProcessID"
                    type="unsignedInt"
                    use="required"
                 />
                <xs:attribute name="ThreadID"
                    type="unsignedInt"
                    use="required"
                 />
                <xs:attribute name="ProcessorID"
                    type="unsignedByte"
                    use="optional"
                 />
                <xs:attribute name="SessionID"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="KernelTime"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="UserTime"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="ProcessorTime"
                    type="unsignedInt"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Channel"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="Computer"
            type="string"
         />
        <xs:element name="Security"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="UserID"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                         | Type                                                        | Description                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Channel**](eventschema-channel-systempropertiestype-element.md)             | anyURI                                                      | Canal dans lequel l’événement a été enregistré.<br/>                                                                                                                                                                                                                                                                                        |
| [**Computer**](eventschema-computer-systempropertiestype-element.md)           | string                                                      | nom de l'ordinateur sur lequel l'événement s'est produit.<br/>                                                                                                                                                                                                                                                                             |
| [**Corrélation**](eventschema-correlation-systempropertiestype-element.md)     |                                                             | Identificateurs d’activité que les consommateurs peuvent utiliser pour regrouper des événements connexes.<br/>                                                                                                                                                                                                                                                 |
| [**1001**](eventschema-eventid-systempropertiestype-element.md)             |                                                             | Identificateur que le fournisseur a utilisé pour identifier l’événement.<br/>                                                                                                                                                                                                                                                                      |
| [**EventRecordID**](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | Numéro d’enregistrement affecté à l’événement lorsqu’il a été enregistré.<br/>                                                                                                                                                                                                                                                                       |
| [**Exécution**](eventschema-execution-systempropertiestype-element.md)         |                                                             | Contient des informations sur le processus et le thread qui a consigné l’événement.<br/>                                                                                                                                                                                                                                                          |
| [**Mot**](eventschema-keywords-systempropertiestype-element.md)           | [**HexInt64Type**](eventschema-hexint64type-simpletype.md) | Masque de masque des mots clés définis dans l’événement. Les mots clés sont utilisés pour classer les types d’événements (par exemple, les événements associés à la lecture de données).<br/>                                                                                                                                                                                 |
| [**Niveau**](eventschema-level-systempropertiestype-element.md)                 | unsignedByte                                                | Niveau de gravité défini dans l’événement.<br/>                                                                                                                                                                                                                                                                                          |
| [**OpCode**](eventschema-opcode-systempropertiestype-element.md)               | unsignedByte                                                | Opcode défini dans l’événement. Task et opcode sont des typcially utilisés pour identifier l’emplacement dans l’application à partir duquel l’événement a été enregistré.<br/>                                                                                                                                                                                  |
| [**Fournisseur**](eventschema-provider-systempropertiestype-element.md)           |                                                             | Identifie le fournisseur qui a consigné l’événement. Les attributs **Name** et **GUID** sont inclus si le fournisseur a utilisé un manifeste d’instrumentation pour définir ses événements. dans le cas contraire, l’attribut **EventSourceName** est inclus si un fournisseur d’événements hérité (à l’aide de l’API de [journalisation des événements](/windows/desktop/EventLog/event-logging) ) a enregistré l’événement.<br/> |
| [**Sécurité**](eventschema-security-systempropertiestype-element.md)           |                                                             | Identifie l’utilisateur qui a enregistré l’événement.<br/>                                                                                                                                                                                                                                                                                        |
| [**Tâche**](eventschema-task-systempropertiestype-element.md)                   | unsignedShort                                               | Tâche définie dans l’événement. La tâche et l’opcode sont généralement utilisés pour identifier l’emplacement dans l’application à partir duquel l’événement a été enregistré.<br/>                                                                                                                                                                                    |
| [**TimeCreated**](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | Horodatage qui identifie le moment où l’événement a été enregistré. L’horodatage inclura l’attribut **SystemTime** ou l’attribut **RawTime** .<br/>                                                                                                                                                                           |
| [**Version**](schema-version-systempropertiestype-element.md)                  | unsignedByte                                                | Numéro de version de la définition de l’événement.<br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a>Attributs



| Nom              | Type                                                | Description                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ActivityID        | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificateur global unique qui identifie l’activité en cours. Les événements qui sont publiés avec cet identificateur font partie de la même activité.<br/>                                                                                                                                         |
| EventSourceName   | string                                              | Nom de la source d’événements qui a publié l’événement (si la source de l’événement provient de l’API de [journalisation des événements](/windows/desktop/EventLog/event-logging) héritée).<br/>                                                                                                                                                      |
| Guid              | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificateur global unique qui identifie le fournisseur de manière unique.<br/>                                                                                                                                                                                                                        |
| KernelTime        | unsignedInt                                         | Durée d’exécution écoulée pour les instructions en mode noyau, en unités de temps processeur. Si vous utilisez une session privée ETW, utilisez la valeur du membre ProcessorTime à la place. Disponible uniquement pour les événements consignés dans un fichier journal de suivi d’événements (fichier. ETL).<br/>                                               |
| Nom              | anyURI                                              | Nom du fournisseur.<br/>                                                                                                                                                                                                                                                                    |
| ProcessID         | unsignedInt                                         | Identifie le processus qui a généré l’événement.<br/>                                                                                                                                                                                                                                             |
| ProcessorID       | unsignedByte                                        | Numéro d’identification du processeur qui a traité l’événement. Disponible uniquement pour les événements consignés dans un fichier journal de suivi d’événements (fichier. ETL).<br/>                                                                                                                                             |
| ProcessorTime     | unsignedInt                                         | Pour les sessions privées ETW, le temps d’exécution écoulé pour les instructions en mode utilisateur, en graduations de l’UC. Disponible uniquement pour les événements consignés dans un fichier journal de suivi d’événements (fichier. ETL).<br/>                                                                                                                    |
| Qualificateurs        | **unsignedShort**                                   | Un fournisseur hérité utilise un nombre 32 bits pour identifier ses événements. Si l’événement est enregistré par un fournisseur hérité, la valeur de l’élément **eventID** contient les 16 bits de poids faible de l’identificateur d’événement et l’attribut de **qualificateur** contient les 16 bits de poids fort de l’identificateur d’événement.<br/> |
| RawTime           | unsignedLong                                        | Valeur d’horodatage brute ; le format de l’horodatage dépend de la source de temps utilisée pour collecter la trace. L’horodatage brut offre une plus grande précision que l’heure système. La sortie de l’événement rendu ne contiendra que du temps brut si vous utilisez TraceRpt.exe avec le commutateur-RTS.<br/>                 |
| RelatedActivityID | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificateur global unique qui identifie l’activité à laquelle le contrôle a été transféré. Les événements connexes ont alors cet identificateur comme identificateur ActivityID.<br/>                                                                                                            |
| SessionID         | unsignedInt                                         | Numéro d’identification de la session Terminal Server dans laquelle l’événement s’est produit. Disponible uniquement pour les événements consignés dans un fichier journal de suivi d’événements (fichier. ETL).<br/>                                                                                                                            |
| SystemTime        | dateTime                                            | Heure système de la journalisation de l’événement.<br/>                                                                                                                                                                                                                                                |
| ThreadID          | unsignedInt                                         | Identifie le thread qui a généré l’événement.<br/>                                                                                                                                                                                                                                              |
| UserID            | string                                              | Identificateur de sécurité (SID) de l’utilisateur sous forme de chaîne.<br/>                                                                                                                                                                                                                                    |
| UserTime          | unsignedInt                                         | Durée d’exécution écoulée pour les instructions en mode utilisateur, en unités de temps processeur. Si vous utilisez une session privée ETW, utilisez la valeur du membre ProcessorTime à la place. Disponible uniquement pour les événements consignés dans un fichier journal de suivi d’événements (fichier. ETL).<br/>                                                 |



## <a name="remarks"></a>Remarques

Par défaut, l’événement contient le nom de domaine complet (FQDN) d’un ordinateur. Pour utiliser le nom NETBIOS plutôt que le nom de domaine complet (FQDN), vous devez créer une valeur de Registre DWORD nommée CompatFlags sous la clé de Registre suivante et définir la valeur de CompatFlags sur 0X2.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               WINEVT
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

