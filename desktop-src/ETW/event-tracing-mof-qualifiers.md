---
description: Utilisez les qualificateurs définis dans cette section lors de la création de votre classe de fournisseur MOF, de la classe MOF de l’événement, de la classe MOF du type d’événement et des propriétés de la classe MOF du type d’événement.
ms.assetid: 3bc82074-05a7-411f-884f-5da1fd08112b
title: Qualificateurs MOF de suivi d’événements
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e118f5315316386426cff89fa1405b92b6dadb70
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885045"
---
# <a name="event-tracing-mof-qualifiers"></a>Qualificateurs MOF de suivi d’événements

Utilisez les qualificateurs définis dans cette section lors de la création de votre [classe de fournisseur MOF](#provider-mof-class-qualifiers), de la classe MOF de l' [événement](#event-mof-class-qualifiers), de la [classe MOF du type d’événement](#event-type-mof-class-qualifiers)et [des propriétés de la classe MOF du type d’événement](#property-qualifiers). Pour obtenir un exemple qui inclut certains de ces qualificateurs, consultez [publication de votre schéma d’événement](publishing-your-event-schema.md).

## <a name="provider-mof-class-qualifiers"></a>Qualificateurs de classe du fournisseur MOF

Le tableau suivant répertorie les qualificateurs que vous pouvez spécifier sur une classe de fournisseur MOF.



| Qualificateur | Type de données  | Description                                                                                                                                                                                                                                                  |
|-----------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Guid**  | **Chaîne** | Obligatoire. GUID de chaîne qui identifie de façon unique un fournisseur. Par exemple, Guid ("{3F92E6E0-9886-434e-85DB-0D11D3904C0A}"). Il s’agit du même GUID que celui que vous utilisez lorsque vous appelez la fonction [**RegisterTraceGuids**](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa) pour inscrire votre fournisseur. |



 

## <a name="event-mof-class-qualifiers"></a>Qualificateurs de classe de l’événement MOF

Le tableau suivant répertorie les qualificateurs que vous pouvez spécifier sur une classe d’événements (classe parente qui regroupe des classes de type d’événement connexes).

| Qualificateur        | Type de données   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Guid**         | **Chaîne**  | Obligatoire. GUID de chaîne qui identifie une classe d’événements. Par exemple, Guid ("{3F92E6E0-9886-434e-85DB-0D11D3904C0A}"). Les fournisseurs d’événements utilisent le GUID pour définir l' [**\_ \_ en-tête de suivi d’événement. Membre GUID**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header) , afin que les consommateurs puissent déterminer la classe des événements qu’ils reçoivent.                                                                                                                                                                                                                                                                                  |
| **EventVersion** | **Integer** | Ce qualificateur est facultatif pour la version la plus récente d’une classe de trace d’événements et est requis pour toutes les versions antérieures de la classe. La version la plus récente de la classe ne spécifie pas le qualificateur **EventVersion** ou a le numéro de version le plus élevé. Les numéros de version commencent par 0, par exemple EventVersion (0). En règle générale, lorsque vous créez une nouvelle version de la classe, vous renommez également la version précédente en &lt; className &gt; \_ VN, où n est un nombre incrémentiel commençant à 0. Pour obtenir un exemple, consultez [**FileIO**](fileio.md) et [**FileIO \_ v0**](fileio-v0.md).<br/> |



 

## <a name="event-type-mof-class-qualifiers"></a>Qualificateurs de classe MOF de type d’événement

Le tableau suivant répertorie les qualificateurs que vous pouvez spécifier sur une classe de type d’événement (la classe qui définit les données de propriété d’événement).



| Qualificateur         | Valeur       | Description                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **EventType**     | **Integer** | Obligatoire. Identifie la classe de type d’événement. Par exemple, EventType (1). Le fournisseur d’événements utilise la même valeur de type d’événement pour définir l' [**\_ en-tête de suivi d’événement \_ . Class. type**](/windows/win32/api/evntrace/ns-evntrace-event_trace_header). Si la même classe MOF est utilisée pour plusieurs types d’événements (parce qu’elles utilisent les mêmes données d’événement), spécifiez la valeur de type d’événement sous la forme d’un tableau d’entiers, par exemple EventType {12,15} . |
| **EventTypeName** | **Chaîne**  | Facultatif. Décrit le type d’événement. Par exemple, EventTypeName (« Start »). Si la même classe MOF est utilisée pour plusieurs types d’événements (parce qu’elles utilisent les mêmes données d’événement), spécifiez la valeur du nom du type d’événement sous la forme d’un tableau de chaînes, par exemple, EventTypeName {"Start", "End"}. Les éléments du tableau EventTypeName correspondent directement au tableau EventType.                 |



 

## <a name="property-qualifiers"></a>Qualificateurs de propriété

Le tableau suivant répertorie les qualificateurs que vous pouvez spécifier sur une propriété.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Qualificateur</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Pixels</strong></td>
<td>Spécifie les positions de bits qui sont mappées à des valeurs de chaîne. Si vous spécifiez ce qualificateur, vous devez également spécifier le qualificateur <strong>BitValue</strong> .</td>
</tr>
<tr class="even">
<td><strong>BitValue</strong></td>
<td>Valeurs de chaîne. Si le qualificateur de <strong>bitmap</strong> est également spécifié, les chaînes correspondent directement aux valeurs dans le qualificateur de <strong>bitmap</strong> . Dans le cas contraire, supposons que la valeur de propriété est un index de base un dans les chaînes de valeur (le bit 1 correspond à la première chaîne de la liste).</td>
</tr>
<tr class="odd">
<td><strong>Extension</strong></td>
<td>Fournit des informations supplémentaires sur l’utilisation (interprétation) des données. La valeur de l’extension ne respecte pas la casse. Incluez la valeur entre guillemets, par exemple extension ( &quot; GUID &quot; ). Les valeurs d’extension possibles sont les suivantes : <dl> <dt><span id="Guid"></span><span id="guid"></span><span id="GUID"></span>Uniques</dt> <dd> Indique que les données de propriété sont un GUID. Le type de données MOF doit être <strong>Object</strong>. La charge utile est supposée être une structure <strong>GUID</strong> .<br/> </dd> <dt><span id="IPAddr_and_IPAddrV4"></span><span id="ipaddr_and_ipaddrv4"></span><span id="IPADDR_AND_IPADDRV4"></span>IPAddr et IPAddrV4</dt> <dd> Les données sont une adresse IP V4. Le type de données MOF doit être <strong>Object</strong>. La charge utile est supposée être un entier long non signé. Chaque octet de type long non signé représente l’une des quatre parties de l’adresse IP (P1. P2. P3. P4). L’octet de poids faible contient la valeur de P1, l’octet suivant contient la valeur de P2, et ainsi de suite.<br/> <strong>avant Windows Vista :</strong> L’extension IPAddrV4 n’est pas prise en charge.<br/> </dd> <dt><span id="IPAddrV6"></span><span id="ipaddrv6"></span><span id="IPADDRV6"></span>IPAddrV6</dt> <dd> Les données sont une adresse IP V6. Le type de données MOF doit être <strong>Object</strong>. La charge utile est supposée être une structure de <strong>IN6_ADDR</strong> . <br/> <strong>avant Windows Vista :</strong> L’extension IPAddrV6 n’est pas prise en charge.<br/> </dd> <dt><span id="NoPrint"></span><span id="noprint"></span><span id="NOPRINT"></span>Noprint</dt> <dd> Indique que le consommateur ne doit pas imprimer ces données.<br/> </dd> <dt><span id="Port"></span><span id="port"></span><span id="PORT"></span>Importer</dt> <dd> Les données identifient un numéro de port. Le type de données MOF doit être <strong>Object</strong>. La charge utile est supposée être une valeur non signée Short.<br/> </dd> <dt><span id="RString"></span><span id="rstring"></span><span id="RSTRING"></span>RString</dt> <dd> Les caractères de saut de ligne ont été remplacés par des espaces. La charge utile est supposée être une chaîne ANSI se terminant par un caractère null.<br/> </dd> <dt><span id="RWString"></span><span id="rwstring"></span><span id="RWSTRING"></span>RWString</dt> <dd> Les caractères de saut de ligne ont été remplacés par des espaces. La charge utile est supposée être une chaîne de caractères larges se terminant par un caractère null.<br/> </dd> <dt><span id="Sid"></span><span id="sid"></span><span id="SID"></span>Sid</dt> <dd> Les données représentent un SID blob binaire. Le type de données MOF doit être <strong>Object</strong>. <br/> Le SID est de longueur variable. La valeur contenue dans les quatre premiers octets (<strong>ULong</strong>) indique si l’objet BLOB contient un SID. Si le premier 4 octets (<strong>ULong</strong>) de l’objet blob est différent de zéro, l’objet BLOB contient un SID. La première partie de l’objet BLOB contient le TOKEN_USER (la structure est alignée sur une limite de 8 octets) et la deuxième partie contient le SID. Pour traiter la partie SID de l’objet BLOB :<br/>
<ul>
<li>Définir un pointeur d’octet au début de l’objet BLOB</li>
<li>Multipliez la taille du pointeur du journal des événements par 2 et ajoutez le produit au pointeur d’octet (le membre <strong>PointerSize</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a> contient la valeur de la taille du pointeur)</li>
</ul>
<br/> Vous pouvez utiliser la macro suivante pour déterminer la longueur du SID. <br/>
<pre class="syntax" data-space="preserve"><code>#define SeLengthSid( Sid ) \
  (8 + (4 * ((SID *)Sid)->SubAuthorityCount))</code></pre>
</dd> <dt><span id="SizeT"></span><span id="sizet"></span><span id="SIZET"></span>SizeT</dt> <dd> Indique que la propriété contient une valeur de pointeur. La taille de la valeur du pointeur dépend du système d’exploitation utilisé pour enregistrer l’événement. la charge utile contient une valeur de 4 octets pour les systèmes 32 bits ou une valeur de 8 octets pour les systèmes 64 bits. Le type de données MOF doit être <strong>Object</strong>.<br/> Les consommateurs doivent ignorer le type de données et le qualificateur de <strong>format</strong> si la propriété inclut l’extension <strong>sizet</strong> . Pour déterminer la taille des données à lire pour la propriété, utilisez :
<ul>
<li>Membre <strong>PointerSize</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a></li>
<li>Membre <strong>Flags</strong> de <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a></li>
</ul>
<br/> <strong>avant Windows Vista :</strong> La valeur <strong>PointerSize</strong> peut ne pas être exacte. Par exemple, sur un ordinateur 64 bits, une application 32 bits enregistre les pointeurs de 4 octets ; Toutefois, la session affecte la valeur 8 à <strong>PointerSize</strong> .<br/> </dd> <dt><span id="Variant"></span><span id="variant"></span><span id="VARIANT"></span>Différent</dt> <dd> Les données représentent un objet BLOB. Les quatre premiers octets (UInt32) indiquent la taille de l’objet BLOB. Le type de données MOF doit être <strong>Object</strong>. <br/> </dd> <dt><span id="WmiTime"></span><span id="wmitime"></span><span id="WMITIME"></span>WmiTime</dt> <dd> Traduit l’horodatage en heure système. Le type de données MOF doit être <strong>Object</strong>. La charge utile est supposée être un entier 64 bits non signé.<br/> <strong>avant Windows Vista :</strong> Non disponible.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Format</strong></td>
<td>Définit le format des données de propriété. Par exemple, l’inclusion du format ( &quot; w &quot; ) sur une propriété de type chaîne indique que la chaîne est une chaîne étendue. Les valeurs possibles sont les suivantes :
<table>
<thead>
<tr class="header">
<th>Terme</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="c"></span><span id="C"></span>secteur<br/></td>
<td>Affichez la valeur de la propriété sous la forme d’un caractère ASCII. Vous pouvez utiliser ce qualificateur avec les types de données <strong>UInt8</strong> .<br/></td>
</tr>
<tr class="even">
<td><span id="s"></span><span id="S"></span>x<br/></td>
<td>Traitez le tableau de caractères comme une chaîne terminée par le caractère null. La chaîne est une chaîne de caractères larges si le type de données est <strong>char16</strong>; dans le cas contraire, la chaîne est une chaîne de caractères ASCII.<br/></td>
</tr>
<tr class="odd">
<td><span id="w"></span><span id="W"></span>s<br/></td>
<td>La valeur de la propriété est une chaîne de caractères larges. Vous pouvez utiliser ce qualificateur avec des types de données <strong>String</strong> . <br/></td>
</tr>
<tr class="even">
<td><span id="x"></span><span id="X"></span>x<br/></td>
<td>Affiche la valeur de la propriété sous la forme d’un nombre hexadécimal. Vous pouvez utiliser ce qualificateur avec des types de données entiers 16, 32 et 64 bits.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><strong>Pointeur</strong></td>
<td><p>Indique que la propriété contient une valeur de pointeur. La taille de la valeur du pointeur dépend du système d’exploitation utilisé pour enregistrer l’événement. la charge utile contient une valeur de 4 octets pour les systèmes 32 bits ou une valeur de 8 octets pour les systèmes 64 bits. Le type de données MOF doit être <strong>Object</strong>.</p>
<p>Les consommateurs doivent ignorer le type de données et le qualificateur de <strong>format</strong> si la propriété inclut l’extension <strong>sizet</strong> . Pour déterminer la taille des données à lire pour la propriété, utilisez :</p>
<ul>
<li>Membre <strong>PointerSize</strong> de <a href="/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header"><strong>TRACE_LOGFILE_HEADER</strong></a></li>
<li>Membre <strong>Flags</strong> de <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header"><strong>EVENT_HEADER</strong></a></li>
</ul>
<p><strong>avant Windows Vista :</strong> La valeur <strong>PointerSize</strong> peut ne pas être exacte. Par exemple, sur un ordinateur 64 bits, une application 32 bits enregistre les pointeurs de 4 octets ; Toutefois, la session affecte la valeur 8 à <strong>PointerSize</strong> .</p>
<p>Notez que certains événements utilisent <strong>PointerType</strong> au lieu du <strong>pointeur</strong>; n’utilisez pas <strong>PointerType</strong>.</p></td>
</tr>
<tr class="even">
<td><strong>StringTermination</strong></td>
<td>Indique comment la propriété de type chaîne est terminée. Par exemple, StringTermination ( &quot; NullTerminated &quot; ) indique que la propriété de type chaîne se termine par un caractère null. Les valeurs possibles sont les suivantes :
<dl> <dt><span id="Counted"></span><span id="counted"></span><span id="COUNTED"></span><strong>Inventorié</strong></dt> <dd>
<p>La longueur de la chaîne est incorporée au début de la chaîne sous la forme d’une valeur <strong>UShort</strong> .</p>
</dd> <dt><span id="NotCounted"></span><span id="notcounted"></span><span id="NOTCOUNTED"></span><strong>NotCounted</strong></dt> <dd>
<p>La chaîne ne se termine pas par un caractère null et la longueur de la chaîne n’est pas incorporée au début de la chaîne. Dans ce cas, la chaîne doit être le dernier élément et occuper tout l’espace jusqu’à la fin des données d’événement.</p>
</dd> <dt><span id="NullTerminated"></span><span id="nullterminated"></span><span id="NULLTERMINATED"></span><strong>NullTerminated</strong></dt> <dd>
<p>La chaîne se termine par un caractère null. Si vous ne spécifiez pas le qualificateur <strong>StringTermination</strong> , la chaîne est supposée se terminer par un caractère null.</p>
</dd> <dt><span id="ReverseCounted"></span><span id="reversecounted"></span><span id="REVERSECOUNTED"></span><strong>ReverseCounted</strong></dt> <dd>
<p>La longueur de la chaîne est incorporée au début de la chaîne sous la forme d’une valeur <strong>UShort</strong> au format Big-endian.</p>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ValueDescriptions</strong></td>
<td>Fournit des descriptions pour chaque valeur dans le qualificateur <strong>values</strong> . Les fonctions <a href="/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation"><strong>TdhEnumerateProviderFieldInformation</strong></a> et <a href="/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation"><strong>TdhQueryProviderFieldInformation</strong></a> retournent ces descriptions lorsque vous essayez d’extraire des informations de mot clé et de niveau. Les descriptions sont facultatives. Si vous ne fournissez pas les descriptions, les fonctions retournent la <strong>valeur null</strong>. Pour plus d’informations <a href="#specifying-level-and-enable-flags-values-for-a-provider">, consultez Spécification du niveau et activation des valeurs d’indicateur pour un fournisseur</a> .</td>
</tr>
<tr class="even">
<td><strong>ValueMap</strong></td>
<td>Spécifie l’index entier ou les valeurs d’indicateur qui mappent aux valeurs de chaîne. Si vous spécifiez ce qualificateur, vous devez également spécifier le qualificateur <strong>values</strong> et, éventuellement, le qualificateur <strong>ValueType</strong> . Notez que ETW ne prend pas en charge l’option WMI de posséder des chaînes pour les valeurs de mappage de valeur.
<p>L’exemple suivant montre comment utiliser les qualificateurs ValueMap, values et ValueType.</p>
<pre class="syntax" data-space="preserve"><code>ValueType(&quot;flag&quot;),
ValueMap {&quot;0x01&quot;, &quot;0x02&quot;, &quot;0x04&quot;, &quot;0x08&quot;},
Values {&quot;ValueMapFlag1&quot;, &quot;ValueMapFlag2&quot;, &quot;ValueMapFlag4&quot;, &quot;ValueMapFlag8&quot;}]</code></pre></td>
</tr>
<tr class="odd">
<td><strong>Valeurs</strong></td>
<td>Valeurs de chaîne. Si le qualificateur <strong>ValueMap</strong> est également spécifié, les chaînes correspondent directement aux valeurs du qualificateur <strong>ValueMap</strong> . Dans le cas contraire, supposez que la valeur de la propriété est un index de base zéro dans les chaînes de valeur.</td>
</tr>
<tr class="even">
<td><strong>ValueType</strong></td>
<td>Indique si les valeurs <strong>ValueMap</strong> sont des valeurs d’index d’entier ou des valeurs d’indicateur de bit. Si vous ne spécifiez pas ce qualificateur, les valeurs d’index entières sont supposées. Pour spécifier que les valeurs sont des valeurs d’index entières, utilisez ValueType ( &quot; index &quot; ). Pour spécifier que les valeurs sont des valeurs d’indicateur de bit, utilisez ValueType ( &quot; Flag &quot; ).</td>
</tr>
<tr class="odd">
<td><strong>WmiDataId</strong></td>
<td>Chaque propriété doit contenir le qualificateur <strong>WmiDataId</strong> . <strong>WmiDataId</strong> définit l’ordre dans lequel le consommateur lit les données d’événement. La valeur de <strong>WmiDataId</strong> démarre à 1 et s’incrémente pour chaque propriété de la classe. Par exemple, WmiDataId (1).</td>
</tr>
<tr class="even">
<td><strong>XMLFragment</strong></td>
<td>Indique que les données sont au format XML et prêtes à être affichées sans mise en forme supplémentaire.</td>
</tr>
</tbody>
</table>



 

## <a name="specifying-level-and-enable-flags-values-for-a-provider"></a>Spécification du niveau et activation des valeurs d’indicateurs pour un fournisseur

Pour documenter le niveau et activer les indicateurs qu’un contrôleur utilise pour activer votre fournisseur, incluez les propriétés « Level » et « flags » dans votre classe MOF du fournisseur. Les noms des propriétés Level et Flags respectent la casse. Les propriétés doivent inclure les qualificateurs **values** et **ValueMap** , qui spécifient le niveau possible et activent les valeurs d’indicateur. Le **ValueMap** pour les valeurs d’indicateur d’activation doit être des valeurs de bit (indicateur). Le qualificateur **ValueDescriptions** est facultatif, mais vous devez l’utiliser pour fournir des descriptions pour chaque valeur possible. Les descriptions sont utilisées quand quelqu’un appelle les fonctions [**TdhEnumerateProviderFieldInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhenumerateproviderfieldinformation) et [**TdhQueryProviderFieldInformation**](/windows/desktop/api/Tdh/nf-tdh-tdhqueryproviderfieldinformation) pour obtenir le niveau possible et activer les valeurs d’indicateurs (Mots clés) pour le fournisseur.

L’exemple suivant illustre une classe de fournisseur qui spécifie le niveau possible et active les valeurs d’indicateurs.

``` syntax
[Dynamic,
 Description("IIS_Trace") : amended,
 guid("{3a2a4e84-4c21-4981-ae10-3fda0d9b0f83}"),
 locale("MS\\0x409")]
class IIS_Trace : EventTrace
{
    [Description ("Enable Flags") : amended,
        ValueDescriptions{
             "Allow_tracing_only_selected_requests ",
             "IIS_authentication_events ",
             "IIS_security_events ",
             "IIS_filter_events ",
             "IIS_static_file_events ",
             "IIS_CGI_events ",
             "IIS_compression_events ",
             "IIS_cache_events ",
             "IIS_request_notifications_events ",
             "IIS_module_events ",
             "IIS_FastCGI_events "},
        DefineValues{
             "UseUrlFilter",
             "IISAuthentication",
             "IISSecurity",
             "IISFilter",
             "IISStaticFile",
             "IISCGI",
             "IISCompression",
             "IISCache",
             "IISRequestNotification",
             "IISModule",
             "IISFastCGI"},
        Values{
             "UseUrlFilter",
             "IISAuthentication",
             "IISSecurity",
             "IISFilter",
             "IISStaticFile",
             "IISCGI",
             "IISCompression",
             "IISCache",
             "IISRequestNotification",
             "IISModule",
             "IISFastCGI"},
        ValueMap{
             "0x00000001",
             "0x00000002",
             "0x00000004",
             "0x00000008",
             "0x00000010",
             "0x00000020",
             "0x00000040",
             "0x00000080",
             "0x00000100",
             "0x00000200",
             "0x00001000"}: amended
    ]
    uint32 Flags;

    [Description ("Levels") : amended,
        ValueDescriptions{
            "Abnormal exit or termination",
            "Severe errors that need logging",
            "Warnings such as allocation failure",
            "Includes non-error cases",
            "Detailed traces from intermediate steps" } : amended,
         DefineValues{
            "TRACE_LEVEL_FATAL",
            "TRACE_LEVEL_ERROR",
            "TRACE_LEVEL_WARNING"
            "TRACE_LEVEL_INFORMATION",
            "TRACE_LEVEL_VERBOSE" },
        Values{
            "Fatal",
            "Error",
            "Warning",
            "Information",
            "Verbose" },
        ValueMap{
            "0x1",
            "0x2",
            "0x3",
            "0x4",
            "0x5" },
        ValueType("index")
    ]
    uint32 Level;
};
```

 

 
