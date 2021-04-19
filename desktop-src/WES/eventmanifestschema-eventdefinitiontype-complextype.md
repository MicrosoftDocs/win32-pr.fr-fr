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
# <a name="eventdefinitiontype-complex-type"></a><span data-ttu-id="337e3-104">Type complexe EventDefinitionType</span><span class="sxs-lookup"><span data-stu-id="337e3-104">EventDefinitionType Complex Type</span></span>

<span data-ttu-id="337e3-105">Définit un événement que votre fournisseur peut écrire.</span><span class="sxs-lookup"><span data-stu-id="337e3-105">Defines an event that your provider can write.</span></span>

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

## <a name="attributes"></a><span data-ttu-id="337e3-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="337e3-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="337e3-107">Nom</span><span class="sxs-lookup"><span data-stu-id="337e3-107">Name</span></span></th>
<th><span data-ttu-id="337e3-108">Type</span><span class="sxs-lookup"><span data-stu-id="337e3-108">Type</span></span></th>
<th><span data-ttu-id="337e3-109">Description</span><span class="sxs-lookup"><span data-stu-id="337e3-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="337e3-110">channel</span><span class="sxs-lookup"><span data-stu-id="337e3-110">channel</span></span></td>
<td><span data-ttu-id="337e3-111">token</span><span class="sxs-lookup"><span data-stu-id="337e3-111">token</span></span></td>
<td><span data-ttu-id="337e3-112">Identificateur qui identifie le canal vers lequel l’événement est écrit.</span><span class="sxs-lookup"><span data-stu-id="337e3-112">An identifier that identifies the channel to where the event is written.</span></span> <span data-ttu-id="337e3-113">Spécifiez un identificateur de canal de l’un des canaux que vous avez définis ou importés.</span><span class="sxs-lookup"><span data-stu-id="337e3-113">Specify a channel identifier of one of the channels that you defined or imported.</span></span> <span data-ttu-id="337e3-114">Si le canal ne spécifie pas d’identificateur de canal, utilisez le nom du canal.</span><span class="sxs-lookup"><span data-stu-id="337e3-114">If the channel does not specify a channel identifier, use the channel's name.</span></span> <span data-ttu-id="337e3-115">Pour plus d’informations sur la définition ou l’importation d’un canal, consultez le type complexe <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="337e3-115">For details on defining or importing a channel, see the <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> complex type.</span></span><br/> <span data-ttu-id="337e3-116">Si vous ne spécifiez pas de canal, l’événement n’est pas écrit dans un canal.</span><span class="sxs-lookup"><span data-stu-id="337e3-116">If you do not specify a channel, the event is not written to a channel.</span></span> <span data-ttu-id="337e3-117">En règle générale, la seule raison pour laquelle il n’est pas nécessaire de spécifier un canal est que vous écriviez des événements uniquement dans une session ETW.</span><span class="sxs-lookup"><span data-stu-id="337e3-117">Typically, the only reason not to specify a channel is if you are writing events only to an ETW session.</span></span> <span data-ttu-id="337e3-118">Pour plus d’informations, consultez Création d’une session ETW, consultez <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">contrôle des sessions de suivi d’événements</a>.</span><span class="sxs-lookup"><span data-stu-id="337e3-118">For details, see creating an ETW session, see <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">Controlling Event Tracing Sessions</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="337e3-119">mots clés</span><span class="sxs-lookup"><span data-stu-id="337e3-119">keywords</span></span></td>
<td><span data-ttu-id="337e3-120"><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a></span><span class="sxs-lookup"><span data-stu-id="337e3-120"><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a></span></span></td>
<td><span data-ttu-id="337e3-121">Liste séparée par des espaces de noms de mots clés qui identifient la catégorie d’événements à laquelle cet événement appartient.</span><span class="sxs-lookup"><span data-stu-id="337e3-121">A space-separated list of keyword names that identify the category of events to which this event belongs.</span></span> <span data-ttu-id="337e3-122">Spécifiez un nom de mot clé dans la liste des mots clés que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="337e3-122">Specify a keyword name from the list of keywords that you define.</span></span> <span data-ttu-id="337e3-123">Pour plus d’informations sur la définition de mots clés, consultez le type complexe <a href="eventmanifestschema-keywordtype-complextype.md"><strong>KeywordType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="337e3-123">For details on defining keywords, see the <a href="eventmanifestschema-keywordtype-complextype.md"><strong>KeywordType</strong></a> complex type.</span></span><br/> <span data-ttu-id="337e3-124">Si vous ne spécifiez pas de mots clés, le descripteur d’événement contient un zéro pour les mots clés.</span><span class="sxs-lookup"><span data-stu-id="337e3-124">If you do not specify keywords, the event descriptor will contain a zero for keywords.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="337e3-125">niveau</span><span class="sxs-lookup"><span data-stu-id="337e3-125">level</span></span></td>
<td><span data-ttu-id="337e3-126"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="337e3-126"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="337e3-127">Niveau de commentaires à utiliser lors de l’écriture de l’événement.</span><span class="sxs-lookup"><span data-stu-id="337e3-127">The level of verbosity to use when writing the event.</span></span> <span data-ttu-id="337e3-128">Spécifiez le nom d’un niveau que vous avez défini dans le manifeste ou l’un des niveaux définis dans le fichier \Include\Winmeta.xml inclus dans le SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="337e3-128">Specify the name of a level that you defined in the manifest or one of the levels defined in the \Include\Winmeta.xml file that is included in the Windows SDK.</span></span> <span data-ttu-id="337e3-129">Pour plus d’informations sur la définition d’un niveau, consultez le type complexe <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="337e3-129">For details on defining a level, see the <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> complex type.</span></span><br/> <span data-ttu-id="337e3-130">Si vous ne spécifiez pas de niveau, le descripteur d’événement contient un zéro pour le niveau.</span><span class="sxs-lookup"><span data-stu-id="337e3-130">If you do not specify a level, the event descriptor will contain a zero for level.</span></span><br/> <span data-ttu-id="337e3-131">Vous devez spécifier un niveau si le type de canal dans lequel l’événement est écrit est admin ; le niveau doit être l’un des niveaux suivants définis dans Winmeata.xml :</span><span class="sxs-lookup"><span data-stu-id="337e3-131">You must specify a level if the channel type to which the event is written is Admin; the level must be one of the following levels defined in Winmeata.xml:</span></span>
<ul>
<li><span data-ttu-id="337e3-132">win:Critical</span><span class="sxs-lookup"><span data-stu-id="337e3-132">win:Critical</span></span></li>
<li><span data-ttu-id="337e3-133">win:Error</span><span class="sxs-lookup"><span data-stu-id="337e3-133">win:Error</span></span></li>
<li><span data-ttu-id="337e3-134">win:Warning</span><span class="sxs-lookup"><span data-stu-id="337e3-134">win:Warning</span></span></li>
<li><span data-ttu-id="337e3-135">win:Informational</span><span class="sxs-lookup"><span data-stu-id="337e3-135">win:Informational</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="337e3-136">message</span><span class="sxs-lookup"><span data-stu-id="337e3-136">message</span></span></td>
<td><span data-ttu-id="337e3-137"><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></span><span class="sxs-lookup"><span data-stu-id="337e3-137"><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></span></span></td>
<td><span data-ttu-id="337e3-138">Message localisé pour l’événement.</span><span class="sxs-lookup"><span data-stu-id="337e3-138">The localized message for the event.</span></span> <span data-ttu-id="337e3-139">La chaîne de message fait référence à une chaîne localisée dans la section <a href="eventmanifestschema-stringtable-resources-element.md"><strong>STRINGTABLE</strong></a> du manifeste.</span><span class="sxs-lookup"><span data-stu-id="337e3-139">The message string references a localized string in the <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> section of the manifest.</span></span><br/> <span data-ttu-id="337e3-140">Vous devez spécifier un message si le type de canal dans lequel l’événement est écrit est admin.</span><span class="sxs-lookup"><span data-stu-id="337e3-140">You must specify a message if the channel type to which the event is written is Admin.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="337e3-141">notLogged</span><span class="sxs-lookup"><span data-stu-id="337e3-141">notLogged</span></span></td>
<td><span data-ttu-id="337e3-142">boolean</span><span class="sxs-lookup"><span data-stu-id="337e3-142">boolean</span></span></td>
<td><span data-ttu-id="337e3-143">Détermine si le fournisseur enregistre cet événement.</span><span class="sxs-lookup"><span data-stu-id="337e3-143">Determines whether the provider logs this event.</span></span> <span data-ttu-id="337e3-144">Spécifiez true si le fournisseur enregistre cet événement ; Sinon, false.</span><span class="sxs-lookup"><span data-stu-id="337e3-144">Specify true if the provider logs this event; otherwise, false.</span></span> <span data-ttu-id="337e3-145">Utilisez cet attribut pour indiquer que le fournisseur n’enregistre plus cet événement au lieu de supprimer l’événement du manifeste.</span><span class="sxs-lookup"><span data-stu-id="337e3-145">Use this attribute to indicate that the provider is no longer logging this event instead of removing the event from the manifest.</span></span> <span data-ttu-id="337e3-146">La conservation de l’événement dans le manifeste permettra aux consommateurs de décoder des fichiers ETL plus anciens qui incluent l’événement.</span><span class="sxs-lookup"><span data-stu-id="337e3-146">Retaining the event in the manifest will let consumers decode older etl files that include the event.</span></span><br/> <span data-ttu-id="337e3-147"><strong>Windows Server 2008 et Windows Vista :</strong> Cet attribut n’est pas pris en charge dans les versions du compilateur de messages qui sont fournies avant la version Windows 7 du SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="337e3-147"><strong>Windows Server 2008 and Windows Vista:</strong> This attribute is not supported in versions of the message compiler that shipped prior to the Windows 7 version of the Windows SDK.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="337e3-148">OpCode</span><span class="sxs-lookup"><span data-stu-id="337e3-148">opcode</span></span></td>
<td><span data-ttu-id="337e3-149"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="337e3-149"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="337e3-150">Nom d’un opcode qui identifie une opération dans la tâche.</span><span class="sxs-lookup"><span data-stu-id="337e3-150">The name of an opcode that identifies an operation within the task.</span></span> <span data-ttu-id="337e3-151">Spécifiez le nom d’un opcode que vous avez défini dans le manifeste ou l’un des OpCodes définis dans Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="337e3-151">Specify the name of an opcode that you defined in the manifest or one of the opcodes defined in Winmeta.xml.</span></span> <span data-ttu-id="337e3-152">Pour plus d’informations sur la définition d’un opcode, consultez le type complexe <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpcodeType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="337e3-152">For details on defining an opcode, see the <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpcodeType</strong></a> complex type.</span></span><br/> <span data-ttu-id="337e3-153">Si la tâche que vous référencez contient des OpCodes spécifiques à la tâche (locaux), vous pouvez spécifier l’un de ses OpCodes spécifiques à la tâche ou un opcode défini au niveau du fournisseur (OpCode global).</span><span class="sxs-lookup"><span data-stu-id="337e3-153">If the task that you reference contains task-specific (local) opcodes, you can specify one of its task-specific opcodes or an opcode defined at the provider level (a global opcode).</span></span> <span data-ttu-id="337e3-154">Si vous spécifiez un opcode global, la valeur de l’opcode global ne peut pas être identique à l’un des OpCodes locaux de la tâche.</span><span class="sxs-lookup"><span data-stu-id="337e3-154">If you specify a global opcode, the value of the global opcode cannot be the same as one of the local opcodes for the task.</span></span><br/> <span data-ttu-id="337e3-155">Si vous référencez un opcode local, l’attribut de tâche doit faire référence à la tâche à laquelle appartient l’opcode local.</span><span class="sxs-lookup"><span data-stu-id="337e3-155">If you reference a local opcode, the task attribute must reference the task to which the local opcode belongs.</span></span><br/> <span data-ttu-id="337e3-156">Si vous ne spécifiez pas d’opcode, le descripteur d’événement contient un zéro pour OpCode.</span><span class="sxs-lookup"><span data-stu-id="337e3-156">If you do not specify an opcode, the event descriptor will contain a zero for opcode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="337e3-157">symbole</span><span class="sxs-lookup"><span data-stu-id="337e3-157">symbol</span></span></td>
<td><span data-ttu-id="337e3-158"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="337e3-158"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="337e3-159">Symbole à utiliser pour référencer le descripteur d’événement de cet événement dans votre application.</span><span class="sxs-lookup"><span data-stu-id="337e3-159">The symbol to use to reference the event descriptor for this event in your application.</span></span> <span data-ttu-id="337e3-160">Le <a href="message-compiler--mc-exe-.md"><strong>compilateur de message (MC.exe)</strong></a> utilise le symbole pour créer une constante pour le descripteur d’événement dans le fichier d’en-tête généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="337e3-160">The <a href="message-compiler--mc-exe-.md"><strong>Message Compiler (MC.exe)</strong></a> uses the symbol to create a constant for the event descriptor in the header file that the compiler generates.</span></span> <span data-ttu-id="337e3-161">Si vous ne spécifiez pas de symbole, le compilateur en génère un pour vous.</span><span class="sxs-lookup"><span data-stu-id="337e3-161">If you do not specify a symbol, the compiler generates one for you.</span></span> <span data-ttu-id="337e3-162">Vous utilisez le descripteur lorsque vous appelez la fonction <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> pour écrire l’événement.</span><span class="sxs-lookup"><span data-stu-id="337e3-162">You use the descriptor when you call the <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> function to write the event.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="337e3-163">tâche</span><span class="sxs-lookup"><span data-stu-id="337e3-163">task</span></span></td>
<td><span data-ttu-id="337e3-164"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="337e3-164"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="337e3-165">Nom d’une tâche qui identifie le composant ou le sous-composant qui génère cet événement.</span><span class="sxs-lookup"><span data-stu-id="337e3-165">The name of a task that identifies the component or subcomponent that generates this event.</span></span> <span data-ttu-id="337e3-166">Spécifiez le nom d’une tâche que vous avez définie dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="337e3-166">Specify the name of a task that you defined in the manifest.</span></span> <span data-ttu-id="337e3-167">Pour plus d’informations sur la définition d’une tâche, consultez le type complexe <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="337e3-167">For details on defining a task, see the <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> complex type.</span></span><br/> <span data-ttu-id="337e3-168">Si vous ne spécifiez pas de tâche, le descripteur d’événement contient un zéro pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="337e3-168">If you do not specify a task, the event descriptor will contain a zero for task.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="337e3-169">template</span><span class="sxs-lookup"><span data-stu-id="337e3-169">template</span></span></td>
<td><span data-ttu-id="337e3-170">token</span><span class="sxs-lookup"><span data-stu-id="337e3-170">token</span></span></td>
<td><span data-ttu-id="337e3-171">Identificateur de modèle du modèle qui définit les éléments de données inclus dans cet événement.</span><span class="sxs-lookup"><span data-stu-id="337e3-171">The template identifier of the template that defines the data items that this event includes.</span></span> <span data-ttu-id="337e3-172">Spécifiez l’identificateur d’un modèle que vous avez défini dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="337e3-172">Specify the identifier of a template that you defined in the manifest.</span></span> <span data-ttu-id="337e3-173">Pour plus d’informations sur la définition d’un modèle, consultez le type complexe <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="337e3-173">For details on defining a template, see the <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> complex type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="337e3-174">value</span><span class="sxs-lookup"><span data-stu-id="337e3-174">value</span></span></td>
<td><span data-ttu-id="337e3-175"><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="337e3-175"><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="337e3-176">Identificateur de l'événement.</span><span class="sxs-lookup"><span data-stu-id="337e3-176">The event identifier.</span></span> <span data-ttu-id="337e3-177">L’identificateur doit être unique dans la liste des événements que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="337e3-177">The identifier must be unique within the list of events that you define.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="337e3-178">version</span><span class="sxs-lookup"><span data-stu-id="337e3-178">version</span></span></td>
<td><span data-ttu-id="337e3-179">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="337e3-179">unsignedByte</span></span></td>
<td><span data-ttu-id="337e3-180">Numéro de version d’un octet de la définition de l’événement.</span><span class="sxs-lookup"><span data-stu-id="337e3-180">A one-byte version number of the event definition.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="337e3-181">Notes</span><span class="sxs-lookup"><span data-stu-id="337e3-181">Remarks</span></span>

<span data-ttu-id="337e3-182">Si vous utilisez [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) pour mettre en forme la chaîne de message de l’événement (ou si vous utilisez l’observateur d’événements pour afficher la chaîne de message), la chaîne de message peut contenir des chaînes d’insertion et toute chaîne de format prise en charge par la fonction Win32 **FormatMessage** .</span><span class="sxs-lookup"><span data-stu-id="337e3-182">If you use [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) to format the message string for the event (or use the Event Viewer to view the message string), the message string can contain insertion strings and any of the format strings that the Win32 **FormatMessage** function supports.</span></span> <span data-ttu-id="337e3-183">Les chaînes d’insertion sont limitées à%*n* ou%*n*! s !</span><span class="sxs-lookup"><span data-stu-id="337e3-183">The insertion strings are limited to %*n* or %*n*!s!</span></span> <span data-ttu-id="337e3-184">(par exemple, %1), où *n* est la référence basée sur un, les éléments de données définis dans le modèle de l’événement.</span><span class="sxs-lookup"><span data-stu-id="337e3-184">(for example, %1) where *n* is the one-based reference the data items defined in the event's template.</span></span> <span data-ttu-id="337e3-185">La chaîne de message peut également contenir des chaînes d’insertion de paramètres sous la forme%%*n* (par exemple,% %4).</span><span class="sxs-lookup"><span data-stu-id="337e3-185">The message string can also contain parameter insertion strings in the form %%*n* (for example, %%4).</span></span> <span data-ttu-id="337e3-186">Le nombre maximal de chaînes d’insertion que le message peut contenir est 100.</span><span class="sxs-lookup"><span data-stu-id="337e3-186">The maximum number of insertion strings that the message can contain is 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="337e3-187">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="337e3-187">Requirements</span></span>



| <span data-ttu-id="337e3-188">Condition requise</span><span class="sxs-lookup"><span data-stu-id="337e3-188">Requirement</span></span> | <span data-ttu-id="337e3-189">Valeur</span><span class="sxs-lookup"><span data-stu-id="337e3-189">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="337e3-190">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="337e3-190">Minimum supported client</span></span><br/> | <span data-ttu-id="337e3-191">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="337e3-191">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="337e3-192">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="337e3-192">Minimum supported server</span></span><br/> | <span data-ttu-id="337e3-193">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="337e3-193">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

