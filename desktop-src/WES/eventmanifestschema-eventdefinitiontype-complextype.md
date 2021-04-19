---
title: Type complexe EventDefinitionType
description: Définit un événement que votre fournisseur peut écrire.
ms.assetid: 09ea89c9-6618-4874-ac72-5ee19cde4040
keywords:
- EventDefinitionType type complexe EventLog
topic_type:
- apiref
api_name:
- EventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7719abea1e97cae88edd47d176e5c578d73f0b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509949"
---
# <a name="eventdefinitiontype-complex-type"></a>Type complexe EventDefinitionType

Définit un événement que votre fournisseur peut écrire.

``` syntax
<xs:complexType name="EventDefinitionType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="level"
                type="QName"
                use="optional"
             />
            <xs:attribute name="template"
                type="token"
                use="optional"
             />
            <xs:attribute name="channel"
                type="token"
                use="optional"
             />
            <xs:attribute name="keywords"
                type="QNameList"
                use="optional"
             />
            <xs:attribute name="task"
                type="QName"
                use="optional"
             />
            <xs:attribute name="opcode"
                type="QName"
                use="optional"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="version"
                type="unsignedByte"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="notLogged"
                type="boolean"
                use="optional"
                default="false"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nom</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>channel</td>
<td>token</td>
<td>Identificateur qui identifie le canal vers lequel l’événement est écrit. Spécifiez un identificateur de canal de l’un des canaux que vous avez définis ou importés. Si le canal ne spécifie pas d’identificateur de canal, utilisez le nom du canal. Pour plus d’informations sur la définition ou l’importation d’un canal, consultez le type complexe <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> .<br/> Si vous ne spécifiez pas de canal, l’événement n’est pas écrit dans un canal. En règle générale, la seule raison pour laquelle il n’est pas nécessaire de spécifier un canal est que vous écriviez des événements uniquement dans une session ETW. Pour plus d’informations, consultez Création d’une session ETW, consultez <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">contrôle des sessions de suivi d’événements</a>.<br/></td>
</tr>
<tr class="even">
<td>mots clés</td>
<td><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a></td>
<td>Liste séparée par des espaces de noms de mots clés qui identifient la catégorie d’événements à laquelle cet événement appartient. Spécifiez un nom de mot clé dans la liste des mots clés que vous définissez. Pour plus d’informations sur la définition de mots clés, consultez le type complexe <a href="eventmanifestschema-keywordtype-complextype.md"><strong>KeywordType</strong></a> .<br/> Si vous ne spécifiez pas de mots clés, le descripteur d’événement contient un zéro pour les mots clés.<br/></td>
</tr>
<tr class="odd">
<td>niveau</td>
<td><strong>QName</strong></td>
<td>Niveau de commentaires à utiliser lors de l’écriture de l’événement. Spécifiez le nom d’un niveau que vous avez défini dans le manifeste ou l’un des niveaux définis dans le fichier \Include\Winmeta.xml inclus dans le SDK Windows. Pour plus d’informations sur la définition d’un niveau, consultez le type complexe <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> .<br/> Si vous ne spécifiez pas de niveau, le descripteur d’événement contient un zéro pour le niveau.<br/> Vous devez spécifier un niveau si le type de canal dans lequel l’événement est écrit est admin ; le niveau doit être l’un des niveaux suivants définis dans Winmeata.xml :
<ul>
<li>win:Critical</li>
<li>win:Error</li>
<li>win:Warning</li>
<li>win:Informational</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>message</td>
<td><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></td>
<td>Message localisé pour l’événement. La chaîne de message fait référence à une chaîne localisée dans la section <a href="eventmanifestschema-stringtable-resources-element.md"><strong>STRINGTABLE</strong></a> du manifeste.<br/> Vous devez spécifier un message si le type de canal dans lequel l’événement est écrit est admin.<br/></td>
</tr>
<tr class="odd">
<td>notLogged</td>
<td>boolean</td>
<td>Détermine si le fournisseur enregistre cet événement. Spécifiez true si le fournisseur enregistre cet événement ; Sinon, false. Utilisez cet attribut pour indiquer que le fournisseur n’enregistre plus cet événement au lieu de supprimer l’événement du manifeste. La conservation de l’événement dans le manifeste permettra aux consommateurs de décoder des fichiers ETL plus anciens qui incluent l’événement.<br/> <strong>Windows Server 2008 et Windows Vista :</strong> Cet attribut n’est pas pris en charge dans les versions du compilateur de messages qui sont fournies avant la version Windows 7 du SDK Windows.<br/></td>
</tr>
<tr class="even">
<td>OpCode</td>
<td><strong>QName</strong></td>
<td>Nom d’un opcode qui identifie une opération dans la tâche. Spécifiez le nom d’un opcode que vous avez défini dans le manifeste ou l’un des OpCodes définis dans Winmeta.xml. Pour plus d’informations sur la définition d’un opcode, consultez le type complexe <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpcodeType</strong></a> .<br/> Si la tâche que vous référencez contient des OpCodes spécifiques à la tâche (locaux), vous pouvez spécifier l’un de ses OpCodes spécifiques à la tâche ou un opcode défini au niveau du fournisseur (OpCode global). Si vous spécifiez un opcode global, la valeur de l’opcode global ne peut pas être identique à l’un des OpCodes locaux de la tâche.<br/> Si vous référencez un opcode local, l’attribut de tâche doit faire référence à la tâche à laquelle appartient l’opcode local.<br/> Si vous ne spécifiez pas d’opcode, le descripteur d’événement contient un zéro pour OpCode.<br/></td>
</tr>
<tr class="odd">
<td>symbole</td>
<td><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></td>
<td>Symbole à utiliser pour référencer le descripteur d’événement de cet événement dans votre application. Le <a href="message-compiler--mc-exe-.md"><strong>compilateur de message (MC.exe)</strong></a> utilise le symbole pour créer une constante pour le descripteur d’événement dans le fichier d’en-tête généré par le compilateur. Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous. Vous utilisez le descripteur lorsque vous appelez la fonction <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> pour écrire l’événement.<br/></td>
</tr>
<tr class="even">
<td>tâche</td>
<td><strong>QName</strong></td>
<td>Nom d’une tâche qui identifie le composant ou le sous-composant qui génère cet événement. Spécifiez le nom d’une tâche que vous avez définie dans le manifeste. Pour plus d’informations sur la définition d’une tâche, consultez le type complexe <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> .<br/> Si vous ne spécifiez pas de tâche, le descripteur d’événement contient un zéro pour la tâche.<br/></td>
</tr>
<tr class="odd">
<td>template</td>
<td>token</td>
<td>Identificateur de modèle du modèle qui définit les éléments de données inclus dans cet événement. Spécifiez l’identificateur d’un modèle que vous avez défini dans le manifeste. Pour plus d’informations sur la définition d’un modèle, consultez le type complexe <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> .<br/></td>
</tr>
<tr class="even">
<td>value</td>
<td><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></td>
<td>Identificateur de l'événement. L’identificateur doit être unique dans la liste des événements que vous définissez.<br/></td>
</tr>
<tr class="odd">
<td>version</td>
<td>unsignedByte</td>
<td>Numéro de version d’un octet de la définition de l’événement.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Notes

Si vous utilisez [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) pour mettre en forme la chaîne de message de l’événement (ou si vous utilisez l’observateur d’événements pour afficher la chaîne de message), la chaîne de message peut contenir des chaînes d’insertion et toute chaîne de format prise en charge par la fonction Win32 **FormatMessage** . Les chaînes d’insertion sont limitées à%*n* ou%*n*! s ! (par exemple, %1), où *n* est la référence basée sur un, les éléments de données définis dans le modèle de l’événement. La chaîne de message peut également contenir des chaînes d’insertion de paramètres sous la forme%%*n* (par exemple,% %4). Le nombre maximal de chaînes d’insertion que le message peut contenir est 100.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



 

