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
ms.openlocfilehash: 81158306285631748830d8aaaaf9cf329d7c0af1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466259"
---
# <a name="channeltype-complex-type"></a><span data-ttu-id="94e20-104">Type complexe ChannelType</span><span class="sxs-lookup"><span data-stu-id="94e20-104">ChannelType Complex Type</span></span>

<span data-ttu-id="94e20-105">Définit un canal auquel les fournisseurs peuvent enregistrer des événements.</span><span class="sxs-lookup"><span data-stu-id="94e20-105">Defines a channel to which providers can log events.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="94e20-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="94e20-106">Child elements</span></span>



| <span data-ttu-id="94e20-107">Élément</span><span class="sxs-lookup"><span data-stu-id="94e20-107">Element</span></span>                                                                  | <span data-ttu-id="94e20-108">Type</span><span class="sxs-lookup"><span data-stu-id="94e20-108">Type</span></span>                                                                                   | <span data-ttu-id="94e20-109">Description</span><span class="sxs-lookup"><span data-stu-id="94e20-109">Description</span></span>                                                                                                                                                                                                |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94e20-110">**fermeture**</span><span class="sxs-lookup"><span data-stu-id="94e20-110">**logging**</span></span>](eventmanifestschema-logging-channeltype-element.md)       | [<span data-ttu-id="94e20-111">**ChannelLoggingType**</span><span class="sxs-lookup"><span data-stu-id="94e20-111">**ChannelLoggingType**</span></span>](eventmanifestschema-channelloggingtype-complextype.md)       | <span data-ttu-id="94e20-112">Définit les propriétés du fichier journal qui stocke le canal, par exemple sa capacité et si le fichier journal est séquentiel ou circulaire.</span><span class="sxs-lookup"><span data-stu-id="94e20-112">Defines the properties of the log file that backs the channel, such as its capacity and whether the log file is sequential or circular.</span></span><br/>                                                         |
| [<span data-ttu-id="94e20-113">**publiée**</span><span class="sxs-lookup"><span data-stu-id="94e20-113">**publishing**</span></span>](eventmanifestschema-publishing-channeltype-element.md) | [<span data-ttu-id="94e20-114">**ChannelPublishingType**</span><span class="sxs-lookup"><span data-stu-id="94e20-114">**ChannelPublishingType**</span></span>](eventmanifestschema-channelpublishingtype-complextype.md) | <span data-ttu-id="94e20-115">Définit les propriétés de journalisation pour la session utilisée par le canal.</span><span class="sxs-lookup"><span data-stu-id="94e20-115">Defines the logging properties for the session that the channel uses.</span></span> <span data-ttu-id="94e20-116">Seuls les canaux de débogage et d’analyse et les canaux qui utilisent l’isolation personnalisée peuvent spécifier des propriétés de journalisation pour leur session.</span><span class="sxs-lookup"><span data-stu-id="94e20-116">Only Debug and Analytic channels and channels that use Custom isolation can specify logging properties for their session.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="94e20-117">Attributs</span><span class="sxs-lookup"><span data-stu-id="94e20-117">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="94e20-118">Nom</span><span class="sxs-lookup"><span data-stu-id="94e20-118">Name</span></span></th>
<th><span data-ttu-id="94e20-119">Type</span><span class="sxs-lookup"><span data-stu-id="94e20-119">Type</span></span></th>
<th><span data-ttu-id="94e20-120">Description</span><span class="sxs-lookup"><span data-stu-id="94e20-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="94e20-121">access</span><span class="sxs-lookup"><span data-stu-id="94e20-121">access</span></span></td>
<td><span data-ttu-id="94e20-122">string</span><span class="sxs-lookup"><span data-stu-id="94e20-122">string</span></span></td>
<td><span data-ttu-id="94e20-123">Descripteur d’accès SDDL ( <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> ) qui contrôle l’accès au fichier journal qui stocke le canal.</span><span class="sxs-lookup"><span data-stu-id="94e20-123">A <a href="/windows/desktop/SecAuthZ/security-descriptor-definition-language">Security Descriptor Definition Language</a> (SDDL) access descriptor that controls access to the log file that backs the channel.</span></span> <span data-ttu-id="94e20-124">Si l’attribut isolation est défini sur application ou système, le descripteur <strong>d'</strong> accès contrôle l’accès en lecture au fichier (les autorisations d’écriture sont ignorées).</span><span class="sxs-lookup"><span data-stu-id="94e20-124">If the <strong>isolation</strong> attribute is set to Application or System, the access descriptor controls read access to the file (the write permissions are ignored).</span></span> <span data-ttu-id="94e20-125">Si l’attribut <strong>isolation</strong> est défini sur personnalisé, le descripteur d’accès contrôle l’accès en écriture au canal et l’accès en lecture au fichier.</span><span class="sxs-lookup"><span data-stu-id="94e20-125">If the <strong>isolation</strong> attribute is set to Custom, the access descriptor controls write access to the channel and read access to the file.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94e20-126">enfants</span><span class="sxs-lookup"><span data-stu-id="94e20-126">chid</span></span></td>
<td><span data-ttu-id="94e20-127">token</span><span class="sxs-lookup"><span data-stu-id="94e20-127">token</span></span></td>
<td><span data-ttu-id="94e20-128">Identificateur qui identifie de façon unique le canal dans la liste des canaux que le fournisseur définit ou importe.</span><span class="sxs-lookup"><span data-stu-id="94e20-128">An identifier that uniquely identifies the channel in the list of channels that the provider defines or imports.</span></span> <span data-ttu-id="94e20-129">Utilisez cette valeur lorsque vous référencez le canal dans un événement.</span><span class="sxs-lookup"><span data-stu-id="94e20-129">Use this value when referencing the channel in an event.</span></span> <span data-ttu-id="94e20-130">Si vous ne spécifiez pas d’identificateur de canal, utilisez le nom du canal pour référencer ce canal dans une définition d’événement.</span><span class="sxs-lookup"><span data-stu-id="94e20-130">If you do not specify a channel identifier, use the channel's name to reference this channel in an event definition.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="94e20-131">enabled</span><span class="sxs-lookup"><span data-stu-id="94e20-131">enabled</span></span></td>
<td><span data-ttu-id="94e20-132">boolean</span><span class="sxs-lookup"><span data-stu-id="94e20-132">boolean</span></span></td>
<td><span data-ttu-id="94e20-133">Détermine si le canal est activé.</span><span class="sxs-lookup"><span data-stu-id="94e20-133">Determines whether the channel is enabled.</span></span> <span data-ttu-id="94e20-134">Affectez la valeur <strong>true</strong> pour autoriser la journalisation sur le canal ; Sinon, <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="94e20-134">Set to <strong>true</strong> to allow logging to the channel; otherwise, <strong>false</strong>.</span></span> <span data-ttu-id="94e20-135">La valeur par défaut est <strong>false</strong> (la journalisation est désactivée).</span><span class="sxs-lookup"><span data-stu-id="94e20-135">The default is <strong>false</strong> (logging is disabled).</span></span><br/> <span data-ttu-id="94e20-136">Étant donné que les types de canal de débogage et d’analyse sont des canaux de volume élevés, vous devez activer le canal uniquement lors de l’examen d’un problème lié à un composant qui écrit sur ce canal. dans le cas contraire, le canal doit rester désactivé.</span><span class="sxs-lookup"><span data-stu-id="94e20-136">Because Debug and Analytic channel types are high volume channels, you should enable the channel only when investigating an issue with a component that writes to that channel; otherwise, the channel should remain disabled.</span></span><br/> <span data-ttu-id="94e20-137">Chaque fois que vous activez un canal de débogage et d’analyse, le service efface les événements du canal.</span><span class="sxs-lookup"><span data-stu-id="94e20-137">Each time you enable a Debug and Analytic channel, the service clears the events from the channel.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94e20-138">isolation</span><span class="sxs-lookup"><span data-stu-id="94e20-138">isolation</span></span></td>
<td><span data-ttu-id="94e20-139">string</span><span class="sxs-lookup"><span data-stu-id="94e20-139">string</span></span></td>
<td><span data-ttu-id="94e20-140">La valeur d’isolation définit les autorisations d’accès par défaut pour le canal.</span><span class="sxs-lookup"><span data-stu-id="94e20-140">The isolation value defines the default access permissions for the channel.</span></span> <span data-ttu-id="94e20-141">Vous pouvez spécifier l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="94e20-141">You can specify one of the following values:</span></span>
<ul>
<li><span data-ttu-id="94e20-142"><strong>Application</strong></span><span class="sxs-lookup"><span data-stu-id="94e20-142"><strong>Application</strong></span></span></li>
<li><span data-ttu-id="94e20-143"><strong>Système</strong></span><span class="sxs-lookup"><span data-stu-id="94e20-143"><strong>System</strong></span></span></li>
<li><span data-ttu-id="94e20-144"><strong>Personnalisée</strong></span><span class="sxs-lookup"><span data-stu-id="94e20-144"><strong>Custom</strong></span></span></li>
</ul>
<span data-ttu-id="94e20-145">L’isolation par défaut est <strong>application</strong>.</span><span class="sxs-lookup"><span data-stu-id="94e20-145">The default isolation is <strong>Application</strong>.</span></span> <span data-ttu-id="94e20-146">Les autorisations par défaut pour l' <strong>application</strong> sont (illustrées à l’aide de SDDL) :</span><span class="sxs-lookup"><span data-stu-id="94e20-146">The default permissions for <strong>Application</strong> are (shown using SDDL):</span></span> <br/> <span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="94e20-147">Texte</span><span class="sxs-lookup"><span data-stu-id="94e20-147">Text</span></span></th>
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

<p><span data-ttu-id="94e20-148">Les autorisations par défaut pour <strong>System</strong> sont (illustrées à l’aide de SDDL) :</span><span class="sxs-lookup"><span data-stu-id="94e20-148">The default permissions for <strong>System</strong> are (shown using SDDL):</span></span></p>
<div class="code">
<span data-codelanguage="Text"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="94e20-149">Texte</span><span class="sxs-lookup"><span data-stu-id="94e20-149">Text</span></span></th>
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
<p><span data-ttu-id="94e20-150">Les autorisations par défaut pour l’isolation <strong>personnalisée</strong> sont les mêmes que celles de l’application.</span><span class="sxs-lookup"><span data-stu-id="94e20-150">The default permissions for <strong>Custom</strong> isolation is the same as Application.</span></span></p>
<p><span data-ttu-id="94e20-151">Les canaux qui spécifient l’isolation des <strong>applications</strong> utilisent la même session ETW.</span><span class="sxs-lookup"><span data-stu-id="94e20-151">Channels that specify <strong>Application</strong> isolation use the same ETW session.</span></span> <span data-ttu-id="94e20-152">Il en va de même pour l’isolation du <strong>système</strong> .</span><span class="sxs-lookup"><span data-stu-id="94e20-152">The same is true for <strong>System</strong> isolation.</span></span> <span data-ttu-id="94e20-153">Toutefois, si vous spécifiez l’isolation <strong>personnalisée</strong> , le service crée une session ETW distincte pour le canal.</span><span class="sxs-lookup"><span data-stu-id="94e20-153">However, if you specify <strong>Custom</strong> isolation, the service creates a separate ETW session for the channel.</span></span> <span data-ttu-id="94e20-154">L’utilisation de l’isolation <strong>personnalisée</strong> vous permet de contrôler les autorisations d’accès pour le canal et le fichier de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="94e20-154">Using <strong>Custom</strong> isolation lets you control the access permissions for the channel and backing file.</span></span> <span data-ttu-id="94e20-155">Étant donné que seules les sessions ETW 64 sont disponibles, vous devez limiter votre utilisation de l’isolation <strong>personnalisée</strong> .</span><span class="sxs-lookup"><span data-stu-id="94e20-155">Because there are only 64 ETW sessions available, you should limit your use of <strong>Custom</strong> isolation.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="94e20-156">message</span><span class="sxs-lookup"><span data-stu-id="94e20-156">message</span></span></td>
<td><span data-ttu-id="94e20-157">string</span><span class="sxs-lookup"><span data-stu-id="94e20-157">string</span></span></td>
<td><p><span data-ttu-id="94e20-158">Nom complet localisé pour le canal.</span><span class="sxs-lookup"><span data-stu-id="94e20-158">The localized display name for the channel.</span></span> <span data-ttu-id="94e20-159">La chaîne de message fait référence à une chaîne localisée dans la section <a href="eventmanifestschema-stringtable-resources-element.md"><strong>STRINGTABLE</strong></a> du manifeste.</span><span class="sxs-lookup"><span data-stu-id="94e20-159">The message string references a localized string in the <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> section of the manifest.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94e20-160">name</span><span class="sxs-lookup"><span data-stu-id="94e20-160">name</span></span></td>
<td><span data-ttu-id="94e20-161">anyURI</span><span class="sxs-lookup"><span data-stu-id="94e20-161">anyURI</span></span></td>
<td><p><span data-ttu-id="94e20-162">Nom du canal.</span><span class="sxs-lookup"><span data-stu-id="94e20-162">The name of the channel.</span></span> <span data-ttu-id="94e20-163">Le nom doit être unique dans la liste des canaux utilisés par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="94e20-163">The name must be unique within the list of channels that the provider uses.</span></span> <span data-ttu-id="94e20-164">La Convention d’affectation de noms de canaux consiste à ajouter le type de canal au nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="94e20-164">The convention for naming channels is to append the channel type to the provider's name.</span></span> <span data-ttu-id="94e20-165">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="94e20-165">For example.</span></span> <span data-ttu-id="94e20-166">Si le nom du fournisseur est société-produit et que vous définissez un canal opérationnel, le nom serait société-produit-composant/opérationnel.</span><span class="sxs-lookup"><span data-stu-id="94e20-166">if the provider's name is Company-Product-Component and you are defining an operational channel, the name would be Company-Product-Component/Operational.</span></span></p>
<p><span data-ttu-id="94e20-167">Les noms de canaux doivent comporter moins de 255 caractères et ne peuvent pas contenir les caractères suivants : ' > ', '</span><span class="sxs-lookup"><span data-stu-id="94e20-167">Channel names must be less that 255 characters and cannot contain the following characters: '>', '</span></span><', '&', '&quot;', '|', '\', ':', '`', '?', '*', or characters with codes less than 31.</p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="94e20-168">symbole</span><span class="sxs-lookup"><span data-stu-id="94e20-168">symbol</span></span></td>
<td><span data-ttu-id="94e20-169"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="94e20-169"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span></span></td>
<td><p><span data-ttu-id="94e20-170">Symbole à utiliser pour référencer le canal dans votre application.</span><span class="sxs-lookup"><span data-stu-id="94e20-170">The symbol to use to reference the channel in your application.</span></span> <span data-ttu-id="94e20-171">Le <a href="message-compiler--mc-exe-.md"><strong>compilateur de message (MC.exe)</strong></a> utilise le symbole pour créer une constante pour le canal dans le fichier d’en-tête généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="94e20-171">The <a href="message-compiler--mc-exe-.md"><strong>Message Compiler (MC.exe)</strong></a> uses the symbol to create a constant for the channel in the header file that the compiler generates.</span></span> <span data-ttu-id="94e20-172">Si vous ne spécifiez pas de symbole, le compilateur génère le nom pour vous.</span><span class="sxs-lookup"><span data-stu-id="94e20-172">If you do not specify a symbol, the compiler generates the name for you.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="94e20-173">type</span><span class="sxs-lookup"><span data-stu-id="94e20-173">type</span></span></td>
<td><span data-ttu-id="94e20-174">string</span><span class="sxs-lookup"><span data-stu-id="94e20-174">string</span></span></td>
<td><p><span data-ttu-id="94e20-175">Identifie le type du canal.</span><span class="sxs-lookup"><span data-stu-id="94e20-175">Identifies the channel's type.</span></span> <span data-ttu-id="94e20-176">Vous pouvez spécifier l’un des types suivants :</span><span class="sxs-lookup"><span data-stu-id="94e20-176">You can specify one of the following types:</span></span></p>
<ul>
<li><span data-ttu-id="94e20-177"><strong>Administrateur</strong></span><span class="sxs-lookup"><span data-stu-id="94e20-177"><strong>Admin</strong></span></span></li>
<li><span data-ttu-id="94e20-178"><strong>En fonctionnement</strong></span><span class="sxs-lookup"><span data-stu-id="94e20-178"><strong>Operational</strong></span></span></li>
<li><span data-ttu-id="94e20-179"><strong>Analytiques</strong></span><span class="sxs-lookup"><span data-stu-id="94e20-179"><strong>Analytic</strong></span></span></li>
<li><span data-ttu-id="94e20-180"><strong>Déboguer</strong></span><span class="sxs-lookup"><span data-stu-id="94e20-180"><strong>Debug</strong></span></span></li>
</ul>
<p><span data-ttu-id="94e20-181">Les canaux de type administrateur prennent en charge les événements qui ciblent les utilisateurs finaux, les administrateurs et le personnel de support.</span><span class="sxs-lookup"><span data-stu-id="94e20-181">Admin type channels support events that target end users, administrators, and support personnel.</span></span> <span data-ttu-id="94e20-182">Les événements écrits dans les canaux d’administration doivent avoir une solution bien définie sur laquelle l’administrateur peut agir. Un exemple d’événement d’administration est un événement qui se produit lorsqu’une application ne parvient pas à se connecter à une imprimante.</span><span class="sxs-lookup"><span data-stu-id="94e20-182">Events written to the Admin channels should have a well-defined solution on which the administrator can act. An example of an admin event is an event that occurs when an application fails to connect to a printer.</span></span> <span data-ttu-id="94e20-183">Ces événements sont bien documentés ou sont associés à un message qui donne aux lecteurs des instructions directes sur ce qui doit être fait pour résoudre le problème.</span><span class="sxs-lookup"><span data-stu-id="94e20-183">These events are either well-documented or have a message associated with them that gives the reader direct instructions of what must be done to rectify the problem.</span></span></p>
<p><span data-ttu-id="94e20-184">Les canaux de type opérationnel prennent en charge les événements qui sont utilisés pour analyser et diagnostiquer un problème ou une occurrence.</span><span class="sxs-lookup"><span data-stu-id="94e20-184">Operational type channels support events that are used for analyzing and diagnosing a problem or occurrence.</span></span> <span data-ttu-id="94e20-185">Ils peuvent être utilisés pour déclencher des outils ou des tâches selon le problème ou l'occurrence.</span><span class="sxs-lookup"><span data-stu-id="94e20-185">They can be used to trigger tools or tasks based on the problem or occurrence.</span></span> <span data-ttu-id="94e20-186">Un exemple d'événement opérationnel est un événement qui se produit lorsqu'une imprimante est ajoutée ou supprimée d'un système.</span><span class="sxs-lookup"><span data-stu-id="94e20-186">An example of an operational event is an event that occurs when a printer is added or removed from a system.</span></span></p>
<p><span data-ttu-id="94e20-187">Les canaux de type analytique prennent en charge les événements publiés dans un volume élevé.</span><span class="sxs-lookup"><span data-stu-id="94e20-187">Analytic type channels support events that are published in high volume.</span></span> <span data-ttu-id="94e20-188">Ils décrivent une opération de programme et indiquent des problèmes qui ne peuvent pas être pris en charge par une intervention de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="94e20-188">They describe program operation and indicate problems that cannot be handled by user intervention.</span></span></p>
<p><span data-ttu-id="94e20-189">Les canaux de type de débogage prennent en charge les événements qui sont utilisés uniquement par les développeurs pour diagnostiquer un problème de débogage.</span><span class="sxs-lookup"><span data-stu-id="94e20-189">Debug type channels support events that are used solely by developers to diagnose a problem for debugging.</span></span></p>
<p><span data-ttu-id="94e20-190">Les canaux d’analyse et de débogage sont désactivés par défaut et ne doivent être activés que pour déterminer la cause d’un problème.</span><span class="sxs-lookup"><span data-stu-id="94e20-190">Analytic and debug channels are disabled by default and should only enabled to determine the cause of an issue.</span></span> <span data-ttu-id="94e20-191">Par exemple, vous activez le canal, exécutez le scénario qui est à l’origine du problème, désactivez le canal, puis interrogez les événements.</span><span class="sxs-lookup"><span data-stu-id="94e20-191">For example, you would enable the channel, run the scenario that is causing the issue, disable the channel, and then query the events.</span></span> <span data-ttu-id="94e20-192">Notez que l’activation du canal efface le canal des événements existants.</span><span class="sxs-lookup"><span data-stu-id="94e20-192">Note that enabling the channel clears the channel of existing events.</span></span> <span data-ttu-id="94e20-193">Si le canal d’analyse et de débogage utilise un fichier de sauvegarde circulaire, vous devez désactiver le canal pour interroger ses événements.</span><span class="sxs-lookup"><span data-stu-id="94e20-193">If the analytic and debug channel uses a circular backing file, you must disable the channel to query its events.</span></span></p>
<p><span data-ttu-id="94e20-194">Tous les canaux d’administration utilisent la même session ETW. Il en va de même pour les canaux opérationnels.</span><span class="sxs-lookup"><span data-stu-id="94e20-194">All Admin channels use the same ETW session; the same is true for Operational channels.</span></span> <span data-ttu-id="94e20-195">Toutefois, chaque canal d’analyse et de débogage utilise une session ETW distincte, qui est une autre raison d’activer uniquement ces types de canaux quand cela est nécessaire (il existe un nombre limité de sessions ETW disponibles).</span><span class="sxs-lookup"><span data-stu-id="94e20-195">However, each Analytic and Debug channel uses a separate ETW session, which is another reason to only enable these channel types when needed (there is a limited number of ETW sessions available).</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="94e20-196">value</span><span class="sxs-lookup"><span data-stu-id="94e20-196">value</span></span></td>
<td><span data-ttu-id="94e20-197"><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="94e20-197"><a href="eventmanifestschema-hexint8type-simpletype.md"><strong>UInt8Type</strong></a></span></span></td>
<td><p><span data-ttu-id="94e20-198">Identificateur numérique qui identifie de façon unique le canal dans la liste des canaux que le fournisseur définit.</span><span class="sxs-lookup"><span data-stu-id="94e20-198">A numeric identifier that uniquely identifies the channel within the list of channels that the provider defines.</span></span> <span data-ttu-id="94e20-199">Le compilateur de message affecte la valeur si elle n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="94e20-199">The message compiler assigns the value if not specified.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="94e20-200">Notes</span><span class="sxs-lookup"><span data-stu-id="94e20-200">Remarks</span></span>

<span data-ttu-id="94e20-201">Si le nom du canal suit la Convention d’affectation de noms de canaux, le observateur d’événements Windows répertorie le canal à l’aide de la chaîne qui suit la barre oblique inverse.</span><span class="sxs-lookup"><span data-stu-id="94e20-201">If the channel's name follows the channel naming convention, the Windows Event Viewer will list the channel using the string that follows the backslash.</span></span> <span data-ttu-id="94e20-202">Par exemple, si le nom de canal est société-produit-composant/opérationnel, le observateur d’événements répertorie le canal comme opérationnel sous le fournisseur de composants de produit de la société.</span><span class="sxs-lookup"><span data-stu-id="94e20-202">For example, if the channel name is Company-Product-Component/Operational, then the Event Viewer will list the channel as Operational under the Company-Product-Component provider.</span></span> <span data-ttu-id="94e20-203">Dans le cas contraire, le nom de canal entier est affiché sous le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="94e20-203">Otherwise, the entire channel name is shown under the provider.</span></span> <span data-ttu-id="94e20-204">Le nom complet localisé est utilisé, s’il est fourni.</span><span class="sxs-lookup"><span data-stu-id="94e20-204">The localized display name is used if provided.</span></span>

## <a name="requirements"></a><span data-ttu-id="94e20-205">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94e20-205">Requirements</span></span>



| <span data-ttu-id="94e20-206">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94e20-206">Requirement</span></span> | <span data-ttu-id="94e20-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="94e20-207">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="94e20-208">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94e20-208">Minimum supported client</span></span><br/> | <span data-ttu-id="94e20-209">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94e20-209">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="94e20-210">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="94e20-210">Minimum supported server</span></span><br/> | <span data-ttu-id="94e20-211">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94e20-211">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




`
