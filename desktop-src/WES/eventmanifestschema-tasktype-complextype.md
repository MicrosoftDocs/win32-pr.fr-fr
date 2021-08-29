---
title: Type complexe TaskType
description: Définit un composant ou un sous-composant d’une application. | Type complexe TaskType
ms.assetid: d117636d-6363-43b6-ac5a-52234ac7c729
keywords:
- TaskType type complexe EventLog
topic_type:
- apiref
api_name:
- TaskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42a8b3dfd91b879eec37040c314d15b8b3c802b2c4b674f7a573314659d5d51b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005809"
---
# <a name="tasktype-complex-type"></a>Type complexe TaskType

Définit un composant ou un sous-composant d’une application.

``` syntax
<xs:complexType name="TaskType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt16Type"
        use="required"
     />
    <xs:attribute name="eventGUID"
        type="GUIDType"
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
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                         | Type                                                                     | Description                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**OpCodes**](eventmanifestschema-opcodes-tasktype-element.md) | [**OpcodeListType**](eventmanifestschema-opcodelisttype-complextype.md) | Définit une liste d’OpCodes spécifiques à une tâche. Vous ne pouvez pas utiliser les valeurs opcode définies dans Winmeta.xml pour les OpCodes spécifiques à la tâche.<br/> |



## <a name="attributes"></a>Attributs



| Nom      | Type                                                              | Description                                                                                                                                                                                                                                                                                                      |
|-----------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| eventGUID | [**GUIDType**](eventmanifestschema-guidtype-simpletype.md)       | Identificateur global unique, au format de Registre, qui identifie la tâche. Cet attribut est requis si vous utilisez l’argument-MOF message compiler pour générer une classe MOF pour la prise en charge de niveau inférieur.<br/>                                                                                                   |
| message   | [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) | Nom complet localisé de la tâche. La chaîne de message fait référence à une chaîne localisée dans la section [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) du manifeste. <br/>                                                                                                   |
| name      | **QName**                                                         | Nom de la tâche.<br/>                                                                                                                                                                                                                                                                                 |
| symbole    | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Symbole à utiliser pour référencer la tâche dans votre application. Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour la tâche dans le fichier d’en-tête généré par le compilateur. Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.<br/> |
| valeur     | [**UInt16Type**](eventmanifestschema-hexint16type-simpletype.md) | Valeur numérique qui identifie de façon unique cette tâche dans la liste des tâches que le fournisseur définit. La valeur doit être comprise entre 1 et 239.<br/>                                                                                                                                             |



## <a name="examples"></a>Exemples

L’exemple suivant montre comment spécifier une tâche.


```XML
<tasks>
  <task name="printspool:Disconnect" 
         symbol="PRINTSPOOL_TASK_DISCONNECT"
         value="0" 
         message="$(string.disconnect)"/>
 
  <task name="printspool:Connect" 
         symbol="PRINTSPOOL_TASK_CONNECT"
         value="1" 
         message="$(string.connect)">
       <opcodes>
          <opcode name="ReadRegistry" 
                  symbol="MYOPCODE_READ_REGISTRY" value="11"
                  message="$(string.ReadRegistry)"/>
       </opcodes>
   </task>
</tasks>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





