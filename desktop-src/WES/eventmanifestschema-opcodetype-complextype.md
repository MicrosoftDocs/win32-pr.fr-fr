---
title: Type complexe OpcodeType
description: Définit une opération dans un composant de l’application.
ms.assetid: d97953df-669b-4c55-b1a8-925022b339b7
keywords:
- OpcodeType type complexe EventLog
topic_type:
- apiref
api_name:
- OpcodeType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e5abaa11373086fe7f1237e10daf3e0a3df1cdb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106024"
---
# <a name="opcodetype-complex-type"></a>Type complexe OpcodeType

Définit une opération dans un composant de l’application. Utilisé conjointement à une tâche pour identifier la section de l’application qui enregistre l’événement.

``` syntax
<xs:complexType name="OpcodeType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="name"
                type="QName"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="value"
                type="UInt8Type"
                use="required"
             />
            <xs:attribute name="mofValue"
                type="UInt8Type"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:anyAttribute
                processContents="lax"
                namespace="##other"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributs



| Nom     | Type                                                              | Description                                                                                                                                                                                                                                                                                                          |
|----------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message  | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nom complet localisé pour l’opcode. La chaîne de message fait référence à une chaîne localisée dans la section [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) du manifeste. <br/>                                                                                                     |
| mofValue | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Réservé à un usage interne uniquement.<br/>                                                                                                                                                                                                                                                                           |
| name     | **QName**                                                         | Nom de l’opcode. Ce nom doit être unique dans l’étendue de ce fournisseur. <br/>                                                                                                                                                                                                                      |
| symbole   | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Symbole à utiliser pour référencer l’opcode dans votre application. Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour l’opcode dans le fichier d’en-tête généré par le compilateur. Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.<br/> |
| value    | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Valeur de l’opcode. Vous pouvez spécifier des valeurs dans la plage 10 et 239. Pour obtenir la liste des valeurs opcode prédéfinies, consultez la section Notes.<br/>                                                                                                                                                                                    |



## <a name="remarks"></a>Notes

Voici les valeurs opcode prédéfinies que vous pouvez utiliser. Ces valeurs sont définies dans le fichier Winmeta.xml inclus dans le SDK Windows.



| Nom          | Valeur | Symbole                      | Description                                                                                            |
|---------------|-------|-----------------------------|--------------------------------------------------------------------------------------------------------|
| Win : info      | 0     | \_informations sur l’OPCODE WINEVENT \_      | Événement d'informations.                                                                                |
| Win : Démarrer     | 1     | début de l' \_ OPCODE WINEVENT \_     | Événement qui représente le démarrage d’une activité.                                                         |
| Win : arrêter      | 2     | arrêt de l' \_ OPCODE WINEVENT \_      | Événement qui représente l’arrêt d’une activité. L’événement correspond au dernier événement de début non couplé. |
| Win : DC \_ Start | 3     | WINEVENT \_ OPCODE \_ DC \_ Start | Événement qui représente le démarrage de la collecte de données. Il s’agit des types d’événements d’arrêt.                      |
| Win : \_ arrêt DC  | 4     | WINEVENT \_ OPCODE \_ DC \_ Stop  | Événement qui représente l’arrêt de la collecte de données. Il s’agit des types d’événements d’arrêt.                      |
| Win : extension | 5     | \_extension OPCODE \_ WINEVENT | Evénement d'extension.                                                                                    |
| Win : répondre     | 6     | \_réponse OPCODE \_ WINEVENT     | Événement de réponse.                                                                                         |
| Win : reprendre    | 7     | WINEVENT \_ OPCODE \_ Resume    | Événement qui représente une activité qui reprend après avoir été suspendue.                                   |
| Win : suspendre   | 8     | WINEVENT \_ OPCODE \_ suspend   | Événement qui représente l’activité en cours de suspension en attente de la fin d’une autre activité.           |
| Win : envoyer      | 9     | WINEVENT \_ OPCODE \_ Send      | Événement qui représente le transfert de l’activité vers un autre composant.                                   |
| Win : recevoir   | 240   | réception de l' \_ OPCODE WINEVENT \_   | Événement qui représente la réception d’un transfert d’activité à partir d’un autre composant.                        |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





