---
title: Type complexe ImportChannelType
description: Identifie un canal qui a été défini par un autre fournisseur ou dans un manifeste qui contient une section de métadonnées.
ms.assetid: da14d837-0ed8-4d85-9820-46c77753768d
keywords:
- ImportChannelType type complexe EventLog
topic_type:
- apiref
api_name:
- ImportChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 66136ee767c16aa85bfcef33fd23d5d42817f844fc309f7633d2a3d2bd35f2e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471049"
---
# <a name="importchanneltype-complex-type"></a>Type complexe ImportChannelType

Identifie un canal qui a été défini par un autre fournisseur ou dans un manifeste qui contient une section de métadonnées.

``` syntax
<xs:complexType name="ImportChannelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="chid"
                type="token"
                use="optional"
             />
            <xs:attribute name="name"
                type="anyURI"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributs



| Nom   | Type                                                              | Description                                                                                                                                                                                                                                                                                                            |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enfants   | token                                                             | Identificateur qui identifie de façon unique le canal dans la liste des canaux que le fournisseur définit ou importe. Utilisez cette valeur lors du référencement de ce canal dans une définition d’événement. Si vous ne spécifiez pas d’identificateur de canal, utilisez le nom du canal pour référencer ce canal dans une définition d’événement.<br/>  |
| name   | anyURI                                                            | Nom du canal à importer.<br/>                                                                                                                                                                                                                                                                          |
| symbole | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Symbole à utiliser pour référencer le canal dans votre application. Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le canal dans le fichier d’en-tête généré par le compilateur. Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.<br/> |



## <a name="remarks"></a>Remarques

Le manifeste qui a défini le canal importé doit être installé avant que votre fournisseur n’écrive des événements ; dans le cas contraire, les événements ne peuvent pas être écrits dans le canal (l’opération d’écriture a abouti, les événements ne sont tout simplement pas écrits sur le canal).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





