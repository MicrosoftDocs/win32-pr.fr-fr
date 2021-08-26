---
title: Type complexe ChannelLoggingType
description: Définit les propriétés du fichier journal qui stocke le canal, par exemple sa capacité et s’il est séquentiel ou circulaire. | Type complexe ChannelLoggingType
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- ChannelLoggingType type complexe EventLog
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e696837b1132a0b82ad428e7404892ae73de88e4435325d988b7936b3a6ba534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032279"
---
# <a name="channelloggingtype-complex-type"></a>Type complexe ChannelLoggingType

Définit les propriétés du fichier journal qui stocke le canal, par exemple sa capacité et s’il est séquentiel ou circulaire.

``` syntax
<xs:complexType name="ChannelLoggingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="autoBackup"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="retention"
            type="boolean"
            default="0"
            minOccurs="0"
         />
        <xs:element name="maxSize"
            type="UInt64Type"
            default="1048576"
            minOccurs="0"
         />
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



| Élément                                                                         | Type                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**La sauvegarde automatique**](eventmanifestschema-autobackup-channelloggingtype-element.md) | boolean                                                           | Détermine s’il est impossible de créer un nouveau fichier journal lorsque le fichier journal actuel atteint sa taille maximale. Affectez la valeur **true** pour demander que le service crée un nouveau fichier lorsque le fichier journal atteint sa taille maximale ; Sinon, **false**. Vous ne pouvez définir la [**sauvegarde autosauvegarde**](eventmanifestschema-autobackup-channelloggingtype-element.md) que sur **true** si la [**rétention**](eventmanifestschema-retention-channelloggingtype-element.md) est définie sur **true**. La valeur par défaut est **false**.<br/> Il n’existe aucune limite au nombre de fichiers de sauvegarde que le service peut créer (limité uniquement par l’espace disque disponible). Les noms des fichiers de sauvegarde se présentent sous la forme Archive-*channelName* - *timestamp*. evtx et se trouvent dans le dossier% windir% \\ system32 \\ winevt \\ logs.<br/> |
| [**maxSize**](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [**UInt64Type**](eventmanifestschema-hexint64type-simpletype.md) | Taille maximale, en octets, du fichier journal. La valeur par défaut (et la valeur minimale) est 1 Mo. Si la taille du journal physique est inférieure à la taille maximale configurée et que l’espace supplémentaire est requis dans le journal pour stocker les événements, le service alloue un autre bloc d’espace même si la taille physique résultante du journal est supérieure à la taille maximale configurée. Le service alloue des blocs de 1 Mo, de sorte que la taille physique peut croître jusqu’à 1 Mo de plus que la taille maximale configurée. <br/>                                                                                                                                                                                                                                                      |
| [**fixation**](eventmanifestschema-retention-channelloggingtype-element.md)   | boolean                                                           | Détermine si le fichier journal est un fichier journal séquentiel ou circulaire. Affectez la valeur **true** à un fichier journal séquentiel et la **valeur false** à un fichier journal circulaire. La valeur par défaut est **false** pour les types de canaux d’administration et opérationnels, et **true** pour les types de canaux d’analyse et de débogage.<br/> Pour interroger un journal circulaire, vous devez d’abord désactiver le canal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Remarques

Vous pouvez spécifier l’attribut **MaxSize** pour tout type de canal.

Vous pouvez spécifier l’attribut **Autobackup** uniquement pour les types de canaux d’administration et opérationnels.

Vous pouvez affecter la valeur false (journalisation circulaire) à l’attribut de **rétention** pour les types de canaux opérationnels et d’administration. vous pouvez définir l’attribut de **rétention** sur false (enregistrement circulaire) pour les types de canaux d’analyse et de débogage, mais pour afficher les événements dans le observateur d’événements Windows, vous devez d’abord désactiver le canal. Notez que lorsque vous réactivez le canal, les événements sont supprimés du canal.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





