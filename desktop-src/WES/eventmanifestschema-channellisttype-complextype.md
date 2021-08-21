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
ms.openlocfilehash: a8602594bdbdf6d39532213b0be660b5b3cfb6a90cd8281d9555ed2ff3a9d401
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121049"
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



## <a name="remarks"></a>Remarques

Vous pouvez spécifier jusqu’à huit canaux (n’importe quelle combinaison de canaux ou canaux importés que vous définissez).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





