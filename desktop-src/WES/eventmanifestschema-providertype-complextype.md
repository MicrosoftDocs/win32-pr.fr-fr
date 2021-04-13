---
title: Type complexe ProviderType
description: Définit un fournisseur et les métadonnées qu’il utilise pour définir ses événements. | Type complexe ProviderType
ms.assetid: 70199cf5-a6d0-4780-9ff1-ed083a5b49ac
keywords:
- Type de journal complexe ProviderType
topic_type:
- apiref
api_name:
- ProviderType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c258b3ff48cdd2f00f632fdce770b58182a531c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322325"
---
# <a name="providertype-complex-type"></a><span data-ttu-id="eba10-105">Type complexe ProviderType</span><span class="sxs-lookup"><span data-stu-id="eba10-105">ProviderType Complex Type</span></span>

<span data-ttu-id="eba10-106">Définit un fournisseur et les métadonnées qu’il utilise pour définir ses événements.</span><span class="sxs-lookup"><span data-stu-id="eba10-106">Defines a provider and the metadata that it uses to define its events.</span></span>

``` syntax
<xs:complexType name="ProviderType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
         />
        <xs:element name="keywords"
            type="KeywordListType"
         />
        <xs:element name="maps"
            type="MapType"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
         />
        <xs:element name="templates"
            type="TemplateListType"
         />
        <xs:element name="events"
            type="DefinitionType"
         />
        <xs:element name="filters"
            type="FilterListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="guid"
        type="GUIDType"
        use="required"
     />
    <xs:attribute name="resourceFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="messageFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="parameterFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="helpLink"
        type="anyURI"
        use="optional"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="required"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:attribute name="source"
        use="optional"
        default="Xml"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="Xml"
                 />
                <xs:enumeration
                    value="Wbem"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="warnOnApplicationCompatibilityError"
        type="xs:boolean"
        use="optional"
        default="false"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="eba10-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eba10-107">Child elements</span></span>



| <span data-ttu-id="eba10-108">Élément</span><span class="sxs-lookup"><span data-stu-id="eba10-108">Element</span></span>                                                                       | <span data-ttu-id="eba10-109">Type</span><span class="sxs-lookup"><span data-stu-id="eba10-109">Type</span></span>                                                                         | <span data-ttu-id="eba10-110">Description</span><span class="sxs-lookup"><span data-stu-id="eba10-110">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eba10-111">**couche**</span><span class="sxs-lookup"><span data-stu-id="eba10-111">**channels**</span></span>](eventmanifestschema-channels-providertype-element.md)         | [<span data-ttu-id="eba10-112">**ChannelListType**</span><span class="sxs-lookup"><span data-stu-id="eba10-112">**ChannelListType**</span></span>](eventmanifestschema-channellisttype-complextype.md)   | <span data-ttu-id="eba10-113">Définit une liste de canaux auxquels les fournisseurs peuvent enregistrer des événements.</span><span class="sxs-lookup"><span data-stu-id="eba10-113">Defines a list of channels to which providers can log events.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="eba10-114">**événements**</span><span class="sxs-lookup"><span data-stu-id="eba10-114">**events**</span></span>](eventmanifestschema-events-providertype-element.md)             | [<span data-ttu-id="eba10-115">**DefinitionType**</span><span class="sxs-lookup"><span data-stu-id="eba10-115">**DefinitionType**</span></span>](eventmanifestschema-definitiontype-complextype.md)     | <span data-ttu-id="eba10-116">Définit une liste de définitions d’événements des événements que le fournisseur peut journaliser.</span><span class="sxs-lookup"><span data-stu-id="eba10-116">Defines a list of event definitions of the events that the provider can log.</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="eba10-117">**filtres**</span><span class="sxs-lookup"><span data-stu-id="eba10-117">**filters**</span></span>                                                                   | [<span data-ttu-id="eba10-118">**FilterListType**</span><span class="sxs-lookup"><span data-stu-id="eba10-118">**FilterListType**</span></span>](eventmanifestschema-filterlisttype-complextype.md)     | <span data-ttu-id="eba10-119">Définit une liste de filtres que votre fournisseur prend en charge.</span><span class="sxs-lookup"><span data-stu-id="eba10-119">Defines a list of filters that your provider supports.</span></span> <span data-ttu-id="eba10-120">Vous pouvez utiliser les filtres, comme vous le feriez pour le niveau et les mots clés, pour déterminer si vous souhaitez écrire un événement.</span><span class="sxs-lookup"><span data-stu-id="eba10-120">You can use the filters, as you would level and keywords, to determine if you want to write an event.</span></span> <br/> <span data-ttu-id="eba10-121">**Windows Server 2008 et Windows Vista :** Non pris en charge jusqu’à Windows 7.</span><span class="sxs-lookup"><span data-stu-id="eba10-121">**Windows Server 2008 and Windows Vista:** Not supported until Windows 7.</span></span><br/> |
| [<span data-ttu-id="eba10-122">**mot**</span><span class="sxs-lookup"><span data-stu-id="eba10-122">**keywords**</span></span>](eventmanifestschema-keywords-providertype-element.md)         | [<span data-ttu-id="eba10-123">**KeywordListType**</span><span class="sxs-lookup"><span data-stu-id="eba10-123">**KeywordListType**</span></span>](eventmanifestschema-keywordlisttype-complextype.md)   | <span data-ttu-id="eba10-124">Définit une liste de mots clés qui classent les événements.</span><span class="sxs-lookup"><span data-stu-id="eba10-124">Defines a list of keywords that categorize events.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="eba10-125">**Balance**</span><span class="sxs-lookup"><span data-stu-id="eba10-125">**levels**</span></span>](eventmanifestschema-levels-providertype-element.md)             | [<span data-ttu-id="eba10-126">**LevelListType**</span><span class="sxs-lookup"><span data-stu-id="eba10-126">**LevelListType**</span></span>](eventmanifestschema-levellisttype-complextype.md)       | <span data-ttu-id="eba10-127">Définit une liste de niveaux qui spécifient la gravité d’un événement.</span><span class="sxs-lookup"><span data-stu-id="eba10-127">Defines a list of levels that specify the severity of an event.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="eba10-128">**Mount**</span><span class="sxs-lookup"><span data-stu-id="eba10-128">**maps**</span></span>](eventmanifestschema-maps-providertype-element.md)                 | [<span data-ttu-id="eba10-129">**MapType**</span><span class="sxs-lookup"><span data-stu-id="eba10-129">**MapType**</span></span>](eventmanifestschema-maptype-complextype.md)                   | <span data-ttu-id="eba10-130">Définit une liste de paires nom/valeur que vous pouvez référencer dans la section de modèle du manifeste.</span><span class="sxs-lookup"><span data-stu-id="eba10-130">Defines a list of name/value pairs that you can reference in the template section of the manifest.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="eba10-131">**namedQueries**</span><span class="sxs-lookup"><span data-stu-id="eba10-131">**namedQueries**</span></span>](eventmanifestschema-namedqueries-providertype-element.md) | [<span data-ttu-id="eba10-132">**NamedQueryType**</span><span class="sxs-lookup"><span data-stu-id="eba10-132">**NamedQueryType**</span></span>](eventmanifestschema-namedquerytype-complextype.md)     | <span data-ttu-id="eba10-133">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="eba10-133">Not used.</span></span> <span data-ttu-id="eba10-134">Définit une liste de requêtes nommées qui interrogent la chaîne de message d’événement pour obtenir une valeur et effectuent une action spécifiée si elle est trouvée.</span><span class="sxs-lookup"><span data-stu-id="eba10-134">Defines a list of named queries that query the event message string for a value and perform a specified action if found.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="eba10-135">**OpCodes**</span><span class="sxs-lookup"><span data-stu-id="eba10-135">**opcodes**</span></span>](eventmanifestschema-opcodes-providertype-element.md)           | [<span data-ttu-id="eba10-136">**OpcodeListType**</span><span class="sxs-lookup"><span data-stu-id="eba10-136">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md)     | <span data-ttu-id="eba10-137">Définit une liste d’OpCodes que vous pouvez utiliser pour regrouper des événements au sein d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="eba10-137">Defines a list of opcodes that you can use to group events within a task.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="eba10-138">**décrites**</span><span class="sxs-lookup"><span data-stu-id="eba10-138">**tasks**</span></span>](eventmanifestschema-tasks-providertype-element.md)               | [<span data-ttu-id="eba10-139">**TaskListType**</span><span class="sxs-lookup"><span data-stu-id="eba10-139">**TaskListType**</span></span>](eventmanifestschema-tasklisttype-complextype.md)         | <span data-ttu-id="eba10-140">Définit une liste de tâches qu’un fournisseur peut utiliser pour regrouper des événements.</span><span class="sxs-lookup"><span data-stu-id="eba10-140">Defines a list of tasks that a provider can use to group events.</span></span> <span data-ttu-id="eba10-141">En général, vous utilisez des tâches pour regrouper des événements pour une fonctionnalité ou un composant du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="eba10-141">Typically, you use tasks to group events for a feature or component of the provider.</span></span><br/>                                                                                              |
| [<span data-ttu-id="eba10-142">**ceux**</span><span class="sxs-lookup"><span data-stu-id="eba10-142">**templates**</span></span>](eventmanifestschema-templates-providertype-element.md)       | [<span data-ttu-id="eba10-143">**TemplateListType**</span><span class="sxs-lookup"><span data-stu-id="eba10-143">**TemplateListType**</span></span>](eventmanifestschema-templatelisttype-complextype.md) | <span data-ttu-id="eba10-144">Définit une liste de modèles qui spécifient les données à inclure avec les événements.</span><span class="sxs-lookup"><span data-stu-id="eba10-144">Defines a list of templates that specify the data to include with the events.</span></span><br/>                                                                                                                                                                      |



## <a name="attributes"></a><span data-ttu-id="eba10-145">Attributs</span><span class="sxs-lookup"><span data-stu-id="eba10-145">Attributes</span></span>



| <span data-ttu-id="eba10-146">Nom</span><span class="sxs-lookup"><span data-stu-id="eba10-146">Name</span></span>                                | <span data-ttu-id="eba10-147">Type</span><span class="sxs-lookup"><span data-stu-id="eba10-147">Type</span></span>                                                              | <span data-ttu-id="eba10-148">Description</span><span class="sxs-lookup"><span data-stu-id="eba10-148">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eba10-149">guid</span><span class="sxs-lookup"><span data-stu-id="eba10-149">guid</span></span>                                | [<span data-ttu-id="eba10-150">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="eba10-150">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="eba10-151">GUID qui identifie de façon unique le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="eba10-151">A GUID that uniquely identifies the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="eba10-152">helpLink</span><span class="sxs-lookup"><span data-stu-id="eba10-152">helpLink</span></span>                            | <span data-ttu-id="eba10-153">anyURI</span><span class="sxs-lookup"><span data-stu-id="eba10-153">anyURI</span></span>                                                            | <span data-ttu-id="eba10-154">URL ou MS Help lien vers du contenu qui fournit des informations sur les événements déclenchés par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="eba10-154">The URL or MS help link to content that provides information about the events that the provider raises.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="eba10-155">message</span><span class="sxs-lookup"><span data-stu-id="eba10-155">message</span></span>                             | [<span data-ttu-id="eba10-156">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="eba10-156">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="eba10-157">Nom complet localisé pour le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="eba10-157">The localized display name for the provider.</span></span> <span data-ttu-id="eba10-158">La chaîne de message fait référence à une chaîne localisée dans la section [**STRINGTABLE**](eventmanifestschema-stringtable-resources-element.md) du manifeste.</span><span class="sxs-lookup"><span data-stu-id="eba10-158">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="eba10-159">messageFileName</span><span class="sxs-lookup"><span data-stu-id="eba10-159">messageFileName</span></span>                     | [<span data-ttu-id="eba10-160">**cheminfichier**</span><span class="sxs-lookup"><span data-stu-id="eba10-160">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="eba10-161">Chemin d’accès complet au fichier qui contient les ressources de message localisées du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="eba10-161">The full path to the file that contains the provider's localized message resources.</span></span> <span data-ttu-id="eba10-162">Le fichier peut être un fichier exécutable ou un fichier DLL.</span><span class="sxs-lookup"><span data-stu-id="eba10-162">The file can be an executable file or DLL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="eba10-163">name</span><span class="sxs-lookup"><span data-stu-id="eba10-163">name</span></span>                                | <span data-ttu-id="eba10-164">anyURI</span><span class="sxs-lookup"><span data-stu-id="eba10-164">anyURI</span></span>                                                            | <span data-ttu-id="eba10-165">Nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="eba10-165">The name of the provider.</span></span> <span data-ttu-id="eba10-166">Le nom doit se présenter sous la forme composant du produit de la *société* -  - .</span><span class="sxs-lookup"><span data-stu-id="eba10-166">The name should be of the form, *Company*-*Product*-*Component*.</span></span><br/> <span data-ttu-id="eba10-167">Le nom ne peut pas comporter plus de 255 caractères et ne peut pas contenir les caractères suivants : ' > ', ' < ', ' & ', ' "', ' ', ' ', ' \| \\ : ', ' ', ' ? ', ' \* 'ou des caractères avec des codes inférieurs à 31.</span><span class="sxs-lookup"><span data-stu-id="eba10-167">The name cannot be longer than 255 characters, and cannot contain the characters: '>', '<', '&', '"', '\|', '\\', ':', '', '?', '\*', or characters with codes less than 31.</span></span> <span data-ttu-id="eba10-168">En outre, le nom doit respecter les contraintes générales sur les noms de fichiers et de clés de registre.</span><span class="sxs-lookup"><span data-stu-id="eba10-168">In addition, the name must follow the general constraints on file and registry key names.</span></span> <span data-ttu-id="eba10-169">Ces contraintes se trouvent dans [nommer un fichier](/windows/desktop/FileIO/naming-a-file)et les [limites de taille des éléments du registre](/windows/desktop/SysInfo/registry-element-size-limits).</span><span class="sxs-lookup"><span data-stu-id="eba10-169">These constraints can be found at [Naming a File](/windows/desktop/FileIO/naming-a-file), and [Registry Element Size Limits](/windows/desktop/SysInfo/registry-element-size-limits).</span></span><br/> |
| <span data-ttu-id="eba10-170">parameterFileName</span><span class="sxs-lookup"><span data-stu-id="eba10-170">parameterFileName</span></span>                   | [<span data-ttu-id="eba10-171">**cheminfichier**</span><span class="sxs-lookup"><span data-stu-id="eba10-171">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="eba10-172">Chemin d’accès complet au fichier qui contient les ressources de chaîne de paramètres du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="eba10-172">The full path to the file that contain the provider's parameter string resources.</span></span> <span data-ttu-id="eba10-173">Le fichier peut être un fichier exécutable ou un fichier DLL.</span><span class="sxs-lookup"><span data-stu-id="eba10-173">The file can be an executable file or DLL file.</span></span> <span data-ttu-id="eba10-174">Vous pouvez spécifier plusieurs fichiers de paramètres séparés par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="eba10-174">You can specify more than one parameter file separated by a semicolon.</span></span> <span data-ttu-id="eba10-175">Le fichier est recherché lorsque la chaîne de message d’un événement contient une chaîne de paramètres.</span><span class="sxs-lookup"><span data-stu-id="eba10-175">The file is searched when an event's message string contains a parameter string.</span></span> <span data-ttu-id="eba10-176">Les paramètres vous permettent de fournir des chaînes d’insertion localisables.</span><span class="sxs-lookup"><span data-stu-id="eba10-176">Parameters let you provide localizable insert strings.</span></span> <span data-ttu-id="eba10-177">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="eba10-177">See Remarks for more information.</span></span><br/>                                                                                                                                                |
| <span data-ttu-id="eba10-178">resourceFileName</span><span class="sxs-lookup"><span data-stu-id="eba10-178">resourceFileName</span></span>                    | [<span data-ttu-id="eba10-179">**cheminfichier**</span><span class="sxs-lookup"><span data-stu-id="eba10-179">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="eba10-180">Chemin d’accès complet au fichier qui contient les ressources de métadonnées du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="eba10-180">The full path to the file that contains the provider's metadata resources.</span></span> <span data-ttu-id="eba10-181">Le fichier peut être un fichier exécutable ou un fichier DLL.</span><span class="sxs-lookup"><span data-stu-id="eba10-181">The file can be an executable file or DLL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="eba10-182">source</span><span class="sxs-lookup"><span data-stu-id="eba10-182">source</span></span>                              |                                                                   | <span data-ttu-id="eba10-183">À usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="eba10-183">For internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="eba10-184">symbole</span><span class="sxs-lookup"><span data-stu-id="eba10-184">symbol</span></span>                              | [<span data-ttu-id="eba10-185">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="eba10-185">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="eba10-186">Symbole à utiliser pour référencer le GUID du fournisseur dans votre application.</span><span class="sxs-lookup"><span data-stu-id="eba10-186">The symbol to use to reference the provider's GUID in your application.</span></span> <span data-ttu-id="eba10-187">Le [**compilateur de message (MC.exe)**](message-compiler--mc-exe-.md) utilise le symbole pour créer une constante pour le GUID du fournisseur dans le fichier d’en-tête généré par le compilateur.</span><span class="sxs-lookup"><span data-stu-id="eba10-187">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the provider's GUID in the header file that the compiler generates.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="eba10-188">warnOnApplicationCompatibilityError</span><span class="sxs-lookup"><span data-stu-id="eba10-188">warnOnApplicationCompatibilityError</span></span> | <span data-ttu-id="eba10-189">**xs:boolean**</span><span class="sxs-lookup"><span data-stu-id="eba10-189">**xs:boolean**</span></span>                                                    | <span data-ttu-id="eba10-190">À usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="eba10-190">For internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="eba10-191">Notes</span><span class="sxs-lookup"><span data-stu-id="eba10-191">Remarks</span></span>

<span data-ttu-id="eba10-192">Le observateur d’événements Windows (Eventvwr.exe) utilise la chaîne de message localisée si elle est disponible ; dans le cas contraire, elle utilise la chaîne de l’attribut Name.</span><span class="sxs-lookup"><span data-stu-id="eba10-192">The Windows Event Viewer (Eventvwr.exe) will use the localized message string if available; otherwise, it uses the string from the name attribute.</span></span>

<span data-ttu-id="eba10-193">Les chemins d’accès pour resourceFileName, messageFileName et parameterFileName peuvent contenir des variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="eba10-193">The paths for resourceFileName, messageFileName, and parameterFileName can contain environment variables.</span></span> <span data-ttu-id="eba10-194">Si vous définissez une nouvelle variable d’environnement à utiliser dans le chemin d’accès, vous devez redémarrer l’ordinateur afin que le service journal des événements puisse sélectionner la nouvelle variable. dans le cas contraire, le service ne pourra pas trouver les ressources de votre fournisseur.</span><span class="sxs-lookup"><span data-stu-id="eba10-194">If you define a new environment variable to use in the path, you must restart the computer so that the event log service can pick up the new variable; otherwise, the service will not be able to find your provider's resources.</span></span>

<span data-ttu-id="eba10-195">La chaîne de message d’un événement peut contenir des chaînes d’insertion et des chaînes de paramètres.</span><span class="sxs-lookup"><span data-stu-id="eba10-195">An event's message string can contain insertion strings and parameter strings.</span></span> <span data-ttu-id="eba10-196">Une chaîne d’insertion se présente sous la forme%*n*, où *n* est un index de base un qui identifie un élément de données à partir du modèle de données de l’événement que vous souhaitez insérer dans le message.</span><span class="sxs-lookup"><span data-stu-id="eba10-196">An insertion string is of the form %*n*, where *n* is a one-based index that identifies a data item from the event's data template that you want to insert into the message.</span></span> <span data-ttu-id="eba10-197">Une chaîne de paramètres (Voir l’attribut **parameterFileName** ) se présente sous la forme%%*n*, où n est l’identificateur d’un message dans la table des messages.</span><span class="sxs-lookup"><span data-stu-id="eba10-197">A parameter string (see the **parameterFileName** attribute) is of the form %%*n*, where n is the identifier of a message in the message table.</span></span> <span data-ttu-id="eba10-198">Si la chaîne de message de l’événement contenait « %1% %11 = %2% %12 » et que les valeurs des éléments de données pour %1 et %2 étaient 8 et 2, respectivement, et que les chaînes de paramètres pour% %11 et% %12 étaient respectivement « quarts » et « gallons »</span><span class="sxs-lookup"><span data-stu-id="eba10-198">If the event's message string contained "%1 %%11 = %2 %%12" and the data item values for %1 and %2 were 8 and 2, respectively, and the parameter strings for %%11 and %%12 were "quarts" and "gallons", respectively, the formatted string would be "8 quarts = 2 gallons".</span></span>

## <a name="requirements"></a><span data-ttu-id="eba10-199">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eba10-199">Requirements</span></span>



| <span data-ttu-id="eba10-200">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eba10-200">Requirement</span></span> | <span data-ttu-id="eba10-201">Valeur</span><span class="sxs-lookup"><span data-stu-id="eba10-201">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eba10-202">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eba10-202">Minimum supported client</span></span><br/> | <span data-ttu-id="eba10-203">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eba10-203">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eba10-204">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eba10-204">Minimum supported server</span></span><br/> | <span data-ttu-id="eba10-205">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eba10-205">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

