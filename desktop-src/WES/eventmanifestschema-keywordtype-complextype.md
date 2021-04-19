---
title: Type complexe KeywordType
description: Définit un mot clé qui identifie une catégorie d’événements. | Type complexe KeywordType
ms.assetid: 6bd41d4a-1d55-4cce-a1f8-136f749fde2a
keywords:
- KeywordType type complexe EventLog
topic_type:
- apiref
api_name:
- KeywordType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c41a9ad4b1fde0a741a022eb6cfd20823643eeef
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106529244"
---
# <a name="keywordtype-complex-type"></a>Type complexe KeywordType

Définit un mot clé qui identifie une catégorie d’événements. Un mot clé est une balise que vous attachez à un événement pour regrouper des événements en fonction de leur utilisation.

``` syntax
<xs:complexType name="KeywordType"
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
            <xs:attribute name="mask"
                type="HexInt64Type"
                use="required"
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



| Nom    | Type                                                              | Description                                                                                                                                                                                                                                                                                                            |
|---------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| masque    | [**HexInt64Type**](eventmanifestschema-hex64type-simpletype.md)  | Masque de bits qui ne doit avoir qu’un seul bit défini. Le bit représente une catégorie d’événements (par exemple, des événements de lecture ou des événements d’écriture). Vous pouvez spécifier des valeurs de bit dans la plage comprise entre 0x0000000000000001 et 0x0000800000000000 (bits 0 à 47).<br/>                                                         |
| message | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nom complet localisé du mot clé. La chaîne de message fait référence à une chaîne localisée dans la section [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) du manifeste.<br/>                                                                                                       |
| name    | **QName**                                                         | Nom du mot clé. Le nom doit être unique dans la liste des mots clés définis par le fournisseur.<br/>                                                                                                                                                                                                     |
| symbole  | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Symbole à utiliser pour référencer le mot clé dans votre application. Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le mot clé dans le fichier d’en-tête généré par le compilateur. Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.<br/> |



## <a name="remarks"></a>Notes

Le fichier Winmeta.xml inclus dans le SDK Windows contient une liste de mots clés. Ces mots clés sont réservés et ne doivent pas être utilisés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

 





