---
title: Type complexe ChannelType
description: Définit un canal auquel les fournisseurs peuvent enregistrer des événements.
ms.assetid: 882506e5-222b-45c8-af4b-59db8baa1dae
keywords:
- ChannelType type complexe EventLog
topic_type:
- apiref
api_name:
- ChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b780d68d419fa29d5ee13995f1b66a412fc89323
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627965"
---
# <a name="channeltype-complex-type"></a>Type complexe ChannelType

Définit un canal auquel les fournisseurs peuvent enregistrer des événements.

``` syntax
<xs:complexType name="ChannelType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="logging"
            type="ChannelLoggingType"
            minOccurs="0"
         />
        <xs:element name="publishing"
            type="ChannelPublishingType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="chid"
        type="token"
        use="optional"
     />
    <xs:attribute name="type"
        type="string"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="access"
        type="string"
        use="optional"
     />
    <xs:attribute name="isolation"
        type="string"
        use="optional"
     />
    <xs:attribute name="enabled"
        type="boolean"
        default="false"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt8Type"
        use="optional"
     />
    <xs:attribute name="message"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Éléments enfants



| Élément                                                                  | Type                                                                                   | Description                                                                                                                                                                                                |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**fermeture**](eventmanifestschema-logging-channeltype-element.md)       | [**ChannelLoggingType**](eventmanifestschema-channelloggingtype-complextype.md)       | Définit les propriétés du fichier journal qui stocke le canal, par exemple sa capacité et si le fichier journal est séquentiel ou circulaire.<br/>                                                         |
| [**publiée**](eventmanifestschema-publishing-channeltype-element.md) | [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) | Définit les propriétés de journalisation pour la session utilisée par le canal. Seuls les canaux de débogage et d’analyse et les canaux qui utilisent l’isolation personnalisée peuvent spécifier des propriétés de journalisation pour leur session.<br/> |



## <a name="attributes"></a>Attributs



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>access</td>
<td>string</td>
<td>Descripteur d’accès SDDL ( <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> ) qui contrôle l’accès au fichier journal qui stocke le canal. Si l’attribut isolation est défini sur application ou système, le descripteur <strong>d'</strong> accès contrôle l’accès en lecture au fichier (les autorisations d’écriture sont ignorées). Si l’attribut <strong>isolation</strong> est défini sur personnalisé, le descripteur d’accès contrôle l’accès en écriture au canal et l’accès en lecture au fichier.<br/></td>
</tr>
<tr class="even">
<td>enfants</td>
<td>token</td>
<td>Identificateur qui identifie de façon unique le canal dans la liste des canaux que le fournisseur définit ou importe. Utilisez cette valeur lorsque vous référencez le canal dans un événement. Si vous ne spécifiez pas d’identificateur de canal, utilisez le nom du canal pour référencer ce canal dans une définition d’événement.<br/></td>
</tr>
<tr class="odd">
<td>enabled</td>
<td>boolean</td>
<td>Détermine si le canal est activé. Affectez la valeur <strong>true</strong> pour autoriser la journalisation sur le canal ; Sinon, <strong>false</strong>. La valeur par défaut est <strong>false</strong> (la journalisation est désactivée).<br/> Étant donné que les types de canal de débogage et d’analyse sont des canaux de volume élevés, vous devez activer le canal uniquement lors de l’examen d’un problème lié à un composant qui écrit sur ce canal. dans le cas contraire, le canal doit rester désactivé.<br/> Chaque fois que vous activez un canal de débogage et d’analyse, le service efface les événements du canal.<br/></td>
</tr>
<tr class="even">
<td>isolation</td>
<td>string</td>
<td>La valeur d’isolation définit les autorisations d’accès par défaut pour le canal. Vous pouvez spécifier l'une des valeurs suivantes :
<ul>
<li><strong>Application</strong></li>
<li><strong>Système</strong></li>
<li><strong>Personnalisée</strong></li>
</ul>
L’isolation par défaut est <strong>application</strong>. Les autorisations par défaut pour l' <strong>application</strong> sont (illustrées à l’aide de SDDL) : <br/> <span data-codelanguage="Text"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Texte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system               (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins            (read, write, clear)
            L&quot;(A;;0x7;;;SO)&quot;                    // server operators           (read, write, clear)
            L&quot;(A;;0x3;;;IU)&quot;                    // INTERACTIVE LOGON          (read, write)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON             (read, write)
            L&quot;(A;;0x3;;;S-1-5-3)&quot;               // BATCH LOGON                (read, write)
            L&quot;(A;;0x3;;;S-1-5-33)&quot;              // write restricted service   (read, write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers          (read) </code></pre></td>
</tr>
</tbody>
</table>

<p>Les autorisations par défaut pour <strong>System</strong> sont (illustrées à l’aide de SDDL) :</p>
<div class="code">
<span data-codelanguage="Text"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Texte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            L&quot;O:BAG:SYD:&quot;
            L&quot;(A;;0xf0007;;;SY)&quot;                // local system             (read, write, clear)
            L&quot;(A;;0x7;;;BA)&quot;                    // built-in admins          (read, write, clear)
            L&quot;(A;;0x3;;;BO)&quot;                    // backup operators         (read, write)
            L&quot;(A;;0x5;;;SO)&quot;                    // server operators         (read, clear) 
            L&quot;(A;;0x1;;;IU)&quot;                    // INTERACTIVE LOGON        (read)
            L&quot;(A;;0x3;;;SU)&quot;                    // SERVICES LOGON           (read, write)
            L&quot;(A;;0x1;;;S-1-5-3)&quot;               // BATCH LOGON              (read)
            L&quot;(A;;0x2;;;S-1-5-33)&quot;              // write restricted service (write)
            L&quot;(A;;0x1;;;S-1-5-32-573)&quot;;         // event log readers        (read)</code></pre></td>
</tr>
</tbody>
</table>

</div>
<p>Les autorisations par défaut pour l’isolation <strong>personnalisée</strong> sont les mêmes que celles de l’application.</p>
<p>Les canaux qui spécifient l’isolation des <strong>applications</strong> utilisent la même session ETW. Il en va de même pour l’isolation du <strong>système</strong> . Toutefois, si vous spécifiez l’isolation <strong>personnalisée</strong> , le service crée une session ETW distincte pour le canal. L’utilisation de l’isolation <strong>personnalisée</strong> vous permet de contrôler les autorisations d’accès pour le canal et le fichier de sauvegarde. Étant donné que seules les sessions ETW 64 sont disponibles, vous devez limiter votre utilisation de l’isolation <strong>personnalisée</strong> .</p></td>
</tr>
<tr class="odd">
<td>message</td>
<td>string</td>
<td><p>Nom complet localisé pour le canal. La chaîne de message fait référence à une chaîne localisée dans la section <a href="eventmanifestschema-stringtable-resources-element.md"><strong>STRINGTABLE</strong></a> du manifeste.</p></td>
</tr>
<tr class="even">
<td>name</td>
<td>anyURI</td>
<td><p>Nom du canal. Le nom doit être unique dans la liste des canaux utilisés par le fournisseur. La Convention d’affectation de noms de canaux consiste à ajouter le type de canal au nom du fournisseur. Par exemple, Si le nom du fournisseur est société-produit et que vous définissez un canal opérationnel, le nom serait société-produit-composant/opérationnel.</p>
<p>Les noms de canaux doivent comporter moins de 255 caractères et ne peuvent pas contenir les caractères suivants : ' > ', '<', '&', '&quot;', '|', '\', ':', '`', '?', '*', or characters with codes less than 31.</p></td>
</tr>
<tr class="odd">
<td>symbole</td>
<td><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></td>
<td><p>Symbole à utiliser pour référencer le canal dans votre application. Le <a href="message-compiler--mc-exe-.md"><strong>compilateur de message (MC.exe)</strong></a> utilise le symbole pour créer une constante pour le canal dans le fichier d’en-tête généré par le compilateur. Si vous ne spécifiez pas de symbole, le compilateur génère le nom pour vous.</p></td>
</tr>
<tr class="even">
<td>type</td>
<td>string</td>
<td><p>Identifie le type du canal. Vous pouvez spécifier l’un des types suivants :</p>
<ul>
<li><strong>Administrateur</strong></li>
<li><strong>En fonctionnement</strong></li>
<li><strong>Analytiques</strong></li>
<li><strong>Déboguer</strong></li>
</ul>
<p>Les canaux de type administrateur prennent en charge les événements qui ciblent les utilisateurs finaux, les administrateurs et le personnel de support. Les événements écrits dans les canaux d’administration doivent avoir une solution bien définie sur laquelle l’administrateur peut agir. Un exemple d’événement d’administration est un événement qui se produit lorsqu’une application ne parvient pas à se connecter à une imprimante. Ces événements sont bien documentés ou sont associés à un message qui donne aux lecteurs des instructions directes sur ce qui doit être fait pour résoudre le problème.</p>
<p>Les canaux de type opérationnel prennent en charge les événements qui sont utilisés pour analyser et diagnostiquer un problème ou une occurrence. Ils peuvent être utilisés pour déclencher des outils ou des tâches selon le problème ou l'occurrence. Un exemple d'événement opérationnel est un événement qui se produit lorsqu'une imprimante est ajoutée ou supprimée d'un système.</p>
<p>Les canaux de type analytique prennent en charge les événements publiés dans un volume élevé. Ils décrivent une opération de programme et indiquent des problèmes qui ne peuvent pas être pris en charge par une intervention de l'utilisateur.</p>
<p>Les canaux de type de débogage prennent en charge les événements qui sont utilisés uniquement par les développeurs pour diagnostiquer un problème de débogage.</p>
<p>Les canaux d’analyse et de débogage sont désactivés par défaut et ne doivent être activés que pour déterminer la cause d’un problème. Par exemple, vous activez le canal, exécutez le scénario qui est à l’origine du problème, désactivez le canal, puis interrogez les événements. Notez que l’activation du canal efface le canal des événements existants. Si le canal d’analyse et de débogage utilise un fichier de sauvegarde circulaire, vous devez désactiver le canal pour interroger ses événements.</p>
<p>Tous les canaux d’administration utilisent la même session ETW. Il en va de même pour les canaux opérationnels. Toutefois, chaque canal d’analyse et de débogage utilise une session ETW distincte, qui est une autre raison d’activer uniquement ces types de canaux quand cela est nécessaire (il existe un nombre limité de sessions ETW disponibles).</p></td>
</tr>
<tr class="odd">
<td>value</td>
<td><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></td>
<td><p>Identificateur numérique qui identifie de façon unique le canal dans la liste des canaux que le fournisseur définit. Le compilateur de message affecte la valeur si elle n’est pas spécifiée.</p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Remarques

si le nom du canal suit la convention d’affectation de noms de canaux, le Windows observateur d’événements répertorie le canal à l’aide de la chaîne qui suit la barre oblique inverse. Par exemple, si le nom de canal est société-produit-composant/opérationnel, le observateur d’événements répertorie le canal comme opérationnel sous le fournisseur de composants de produit de la société. Dans le cas contraire, le nom de canal entier est affiché sous le fournisseur. Le nom complet localisé est utilisé, s’il est fourni.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 




`
