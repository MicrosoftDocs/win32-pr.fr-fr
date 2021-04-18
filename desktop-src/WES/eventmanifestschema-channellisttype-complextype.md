---
title: Type complexe ChannelListType
description: Définit une liste de canaux auxquels les fournisseurs peuvent enregistrer des événements. | Type complexe ChannelListType
ms.assetid: 01685955-7149-45ce-a47f-6344fcf07826
keywords:
- ChannelListType type complexe EventLog
topic_type:
- apiref
api_name:
- ChannelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53293687fd4ab0d87155b86edd026189f6d7c925
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106543016"
---
# <a name="channellisttype-complex-type"></a>Type complexe ChannelListType

Définit une liste de canaux auxquels les fournisseurs peuvent enregistrer des événements.

``` syntax
<xs:complexType name="ChannelListType">
    <xs:choice
        minOccurs="0"
        maxOccurs="8"
    >
        <xs:element name="importChannel"
            type="ImportChannelType"
         />
        <xs:element name="channel"
            type="ChannelType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                            | Type                                                                           | Description                                                                                                                  |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**couche**](eventmanifestschema-channel-channellisttype-element.md)             | [**ChannelType**](eventmanifestschema-channeltype-complextype.md)             | Définit un canal dans lequel les événements peuvent être enregistrés.<br/>                                                                  |
| [**importChannel**](eventmanifestschema-importchannel-channellisttype-element.md) | [**ImportChannelType**](eventmanifestschema-importchanneltype-complextype.md) | Identifie un canal qui a été défini par un autre fournisseur ou dans un manifeste qui contient une section de métadonnées.<br/> |



## <a name="remarks"></a>Notes

Vous pouvez spécifier jusqu’à huit canaux (n’importe quelle combinaison de canaux ou canaux importés que vous définissez).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





