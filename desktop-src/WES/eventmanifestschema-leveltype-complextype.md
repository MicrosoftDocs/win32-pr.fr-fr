---
title: Type complexe LevelType
description: Définit une valeur de gravité qui détermine le niveau de détail des événements journalisés.
ms.assetid: c71aedef-7c43-4343-9d6d-94eb45da49b9
keywords:
- LevelType type complexe EventLog
topic_type:
- apiref
api_name:
- LevelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b80e034f6b77f869207ecb785edbb935841eed2dba6bde73ad88c441dabf15cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055937"
---
# <a name="leveltype-complex-type"></a>Type complexe LevelType

Définit une valeur de gravité qui détermine le niveau de détail des événements journalisés.

``` syntax
<xs:complexType name="LevelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="xs:string"
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
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributs



| Nom    | Type                                                              | Description                                                                                                                                                                                                                                                                                                        |
|---------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nom complet localisé du niveau. La chaîne de message fait référence à une chaîne localisée dans la section [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) du manifeste. <br/>                                                                                                    |
| name    | **QName**                                                         | Nom à assigner à ce niveau. Ce nom doit être unique dans l’étendue du fournisseur.<br/>                                                                                                                                                                                                            |
| symbole  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Symbole à utiliser pour référencer le niveau dans votre application. Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le niveau dans le fichier d’en-tête généré par le compilateur. Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.<br/> |
| value   | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Valeur de niveau. Vous pouvez spécifier des valeurs comprises dans la plage comprise entre 16 et 255. Pour les valeurs de niveau prédéfinies, consultez la section Notes.<br/>                                                                                                                                                                                               |



## <a name="remarks"></a>Remarques

Voici les valeurs de niveau prédéfinies que vous pouvez utiliser. ces valeurs sont définies dans le fichier Winmeta.xml inclus dans le SDK Windows.



| Nom              | Valeur | Symbole                    | Description                                                             |
|-------------------|-------|---------------------------|-------------------------------------------------------------------------|
| win:Critical      | 1     | \_niveau WINEVENT \_ critique | Identifie un événement de sortie ou d’arrêt anormal.<br/>            |
| win:Error         | 2     | \_erreur de niveau WINEVENT \_    | Identifie un événement d’erreur grave.<br/>                             |
| win:Warning       | 3     | \_avertissement de niveau WINEVENT \_  | Identifie un événement d’avertissement, tel qu’un échec d’allocation.<br/>    |
| win:Informational | 4     | \_informations de niveau WINEVENT \_     | Identifie un événement qui n’est pas une erreur, tel qu’un événement d’entrée ou de sortie.<br/> |
| win:Verbose       | 5     | WINEVENT \_ niveau de \_ détail  | Identifie un événement de trace détaillé.<br/>                           |



 

Des nombres plus élevés impliquent également des niveaux inférieurs. Par exemple, si vous spécifiez Win : Warning, vous recevez tous les événements d’avertissement, d’erreur et critiques.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





