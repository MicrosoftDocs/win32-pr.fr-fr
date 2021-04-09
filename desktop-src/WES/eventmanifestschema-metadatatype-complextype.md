---
title: Type complexe de type de données
description: Définit les types de métadonnées que vous pouvez définir dans la section métadonnées du manifeste.
ms.assetid: 602bafe7-940e-4313-9da5-54c6aa7f60a2
keywords:
- Journal des événements de type complexe de type de données
topic_type:
- apiref
api_name:
- MetadataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69b140a2b65d47d563fd88f49d6818efc13613f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033217"
---
# <a name="metadatatype-complex-type"></a><span data-ttu-id="87ce3-104">Type complexe de type de données</span><span class="sxs-lookup"><span data-stu-id="87ce3-104">MetadataType Complex Type</span></span>

<span data-ttu-id="87ce3-105">Définit les types de métadonnées que vous pouvez définir dans la section métadonnées du manifeste.</span><span class="sxs-lookup"><span data-stu-id="87ce3-105">Defines the metadata types that you can define in the metadata section of the manifest.</span></span>

``` syntax
<xs:complexType name="MetadataType">
    <xs:sequence>
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
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="KeywordListType"
            minOccurs="0"
         />
        <xs:element name="types"
            type="TypeListType"
            minOccurs="0"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
            minOccurs="0"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="87ce3-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="87ce3-106">Child elements</span></span>



| <span data-ttu-id="87ce3-107">Élément</span><span class="sxs-lookup"><span data-stu-id="87ce3-107">Element</span></span>                                                                       | <span data-ttu-id="87ce3-108">Type</span><span class="sxs-lookup"><span data-stu-id="87ce3-108">Type</span></span>                                                                       | <span data-ttu-id="87ce3-109">Description</span><span class="sxs-lookup"><span data-stu-id="87ce3-109">Description</span></span>                                                                                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87ce3-110">**couche**</span><span class="sxs-lookup"><span data-stu-id="87ce3-110">**channels**</span></span>](eventmanifestschema-channels-metadatatype-element.md)         | [<span data-ttu-id="87ce3-111">**ChannelListType**</span><span class="sxs-lookup"><span data-stu-id="87ce3-111">**ChannelListType**</span></span>](eventmanifestschema-channellisttype-complextype.md) | <span data-ttu-id="87ce3-112">Définit une liste de canaux auxquels les fournisseurs peuvent enregistrer des événements.</span><span class="sxs-lookup"><span data-stu-id="87ce3-112">Defines a list of channels to which providers can log events.</span></span> <span data-ttu-id="87ce3-113">Un fournisseur peut ensuite importer un ou plusieurs canaux dans son manifeste.</span><span class="sxs-lookup"><span data-stu-id="87ce3-113">A provider can then import one or more of the channels in their manifest.</span></span><br/>               |
| [<span data-ttu-id="87ce3-114">**mot**</span><span class="sxs-lookup"><span data-stu-id="87ce3-114">**keywords**</span></span>](eventmanifestschema-keywords-metadatatype-element.md)         | [<span data-ttu-id="87ce3-115">**KeywordListType**</span><span class="sxs-lookup"><span data-stu-id="87ce3-115">**KeywordListType**</span></span>](eventmanifestschema-keywordlisttype-complextype.md) | <span data-ttu-id="87ce3-116">Définit une liste de mots clés qui déterminent la catégorie d’événements que le fournisseur écrit.</span><span class="sxs-lookup"><span data-stu-id="87ce3-116">Defines a list of keywords that determine the category of events that the provider writes.</span></span><br/>                                                            |
| [<span data-ttu-id="87ce3-117">**Balance**</span><span class="sxs-lookup"><span data-stu-id="87ce3-117">**levels**</span></span>](eventmanifestschema-levels-metadatatype-element.md)             | [<span data-ttu-id="87ce3-118">**LevelListType**</span><span class="sxs-lookup"><span data-stu-id="87ce3-118">**LevelListType**</span></span>](eventmanifestschema-levellisttype-complextype.md)     | <span data-ttu-id="87ce3-119">Définit une liste de niveaux qui spécifient la gravité d’un événement.</span><span class="sxs-lookup"><span data-stu-id="87ce3-119">Defines a list of levels that specify the severity of an event.</span></span><br/>                                                                                       |
| <span data-ttu-id="87ce3-120">**message**</span><span class="sxs-lookup"><span data-stu-id="87ce3-120">**message**</span></span>                                                                   |                                                                            | <span data-ttu-id="87ce3-121">Définit une chaîne de message.</span><span class="sxs-lookup"><span data-stu-id="87ce3-121">Defines a message string.</span></span><br/>                                                                                                                             |
| <span data-ttu-id="87ce3-122">**messageTable**</span><span class="sxs-lookup"><span data-stu-id="87ce3-122">**messageTable**</span></span>                                                              |                                                                            | <span data-ttu-id="87ce3-123">Définit une liste de chaînes de message.</span><span class="sxs-lookup"><span data-stu-id="87ce3-123">Defines a list of message strings.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="87ce3-124">**namedQueries**</span><span class="sxs-lookup"><span data-stu-id="87ce3-124">**namedQueries**</span></span>](eventmanifestschema-namedqueries-metadatatype-element.md) | [<span data-ttu-id="87ce3-125">**NamedQueryType**</span><span class="sxs-lookup"><span data-stu-id="87ce3-125">**NamedQueryType**</span></span>](eventmanifestschema-namedquerytype-complextype.md)   | <span data-ttu-id="87ce3-126">Définit une liste de requêtes nommées qui utilisent des expressions régulières pour effectuer des actions de recherche et de remplacement dans la chaîne de message d’un événement.</span><span class="sxs-lookup"><span data-stu-id="87ce3-126">Defines a list of named queries that use regular expressions to perform find and replace actions on an event's message string.</span></span><br/>                        |
| [<span data-ttu-id="87ce3-127">**OpCodes**</span><span class="sxs-lookup"><span data-stu-id="87ce3-127">**opcodes**</span></span>](eventmanifestschema-opcodes-metadatatype-element.md)           | [<span data-ttu-id="87ce3-128">**OpcodeListType**</span><span class="sxs-lookup"><span data-stu-id="87ce3-128">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md)   | <span data-ttu-id="87ce3-129">Définit une liste d’OpCodes que vous pouvez utiliser pour regrouper des événements au sein d’une tâche.</span><span class="sxs-lookup"><span data-stu-id="87ce3-129">Defines a list of opcodes that you can use to group events within a task.</span></span><br/>                                                                             |
| <span data-ttu-id="87ce3-130">**tasks**</span><span class="sxs-lookup"><span data-stu-id="87ce3-130">**tasks**</span></span>                                                                     | [<span data-ttu-id="87ce3-131">**TaskListType**</span><span class="sxs-lookup"><span data-stu-id="87ce3-131">**TaskListType**</span></span>](eventmanifestschema-tasklisttype-complextype.md)       | <span data-ttu-id="87ce3-132">Définit une liste de tâches qu’un fournisseur peut utiliser pour regrouper des événements.</span><span class="sxs-lookup"><span data-stu-id="87ce3-132">Defines a list of tasks that a provider can use to group events.</span></span> <span data-ttu-id="87ce3-133">En général, vous utilisez des tâches pour regrouper des événements pour une fonctionnalité ou un composant du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="87ce3-133">Typically, you use tasks to group events for a feature or component of the provider.</span></span><br/> |
| [<span data-ttu-id="87ce3-134">**modes**</span><span class="sxs-lookup"><span data-stu-id="87ce3-134">**types**</span></span>](eventmanifestschema-types-metadatatype-element.md)               | [<span data-ttu-id="87ce3-135">**TypeListType**</span><span class="sxs-lookup"><span data-stu-id="87ce3-135">**TypeListType**</span></span>](eventmanifestschema-typelisttype-complextype.md)       | <span data-ttu-id="87ce3-136">Définit une liste de types XML.</span><span class="sxs-lookup"><span data-stu-id="87ce3-136">Defines a list of XML types.</span></span><br/>                                                                                                                          |



## <a name="attributes"></a><span data-ttu-id="87ce3-137">Attributs</span><span class="sxs-lookup"><span data-stu-id="87ce3-137">Attributes</span></span>



| <span data-ttu-id="87ce3-138">Nom</span><span class="sxs-lookup"><span data-stu-id="87ce3-138">Name</span></span>    | <span data-ttu-id="87ce3-139">Type</span><span class="sxs-lookup"><span data-stu-id="87ce3-139">Type</span></span>                                                              | <span data-ttu-id="87ce3-140">Description</span><span class="sxs-lookup"><span data-stu-id="87ce3-140">Description</span></span>                                                                                        |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87ce3-141">message</span><span class="sxs-lookup"><span data-stu-id="87ce3-141">message</span></span> | [<span data-ttu-id="87ce3-142">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="87ce3-142">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="87ce3-143">Référence à la chaîne localisée dans la table de chaînes.</span><span class="sxs-lookup"><span data-stu-id="87ce3-143">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="87ce3-144">mid</span><span class="sxs-lookup"><span data-stu-id="87ce3-144">mid</span></span>     | <span data-ttu-id="87ce3-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="87ce3-145">xs:string</span></span>                                                         | <span data-ttu-id="87ce3-146">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="87ce3-146">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="87ce3-147">name</span><span class="sxs-lookup"><span data-stu-id="87ce3-147">name</span></span>    | <span data-ttu-id="87ce3-148">anyURI</span><span class="sxs-lookup"><span data-stu-id="87ce3-148">anyURI</span></span>                                                            | <span data-ttu-id="87ce3-149">URI du fichier méta.</span><span class="sxs-lookup"><span data-stu-id="87ce3-149">The URI of the meta file.</span></span> <br/>                                                              |
| <span data-ttu-id="87ce3-150">symbole</span><span class="sxs-lookup"><span data-stu-id="87ce3-150">symbol</span></span>  | [<span data-ttu-id="87ce3-151">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="87ce3-151">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="87ce3-152">Nom symbolique que vous souhaitez que le compilateur de message crée pour cette chaîne de message.</span><span class="sxs-lookup"><span data-stu-id="87ce3-152">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="87ce3-153">value</span><span class="sxs-lookup"><span data-stu-id="87ce3-153">value</span></span>   | [<span data-ttu-id="87ce3-154">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="87ce3-154">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="87ce3-155">Nombre à utiliser comme identificateur de message pour ce message.</span><span class="sxs-lookup"><span data-stu-id="87ce3-155">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="remarks"></a><span data-ttu-id="87ce3-156">Notes</span><span class="sxs-lookup"><span data-stu-id="87ce3-156">Remarks</span></span>

<span data-ttu-id="87ce3-157">Bien que vous puissiez créer un manifeste qui contient une section de métadonnées, le service ne l’utilise pas. les seules métadonnées reconnues par le service sont les métadonnées trouvées dans le fichier Winmeta.xml.</span><span class="sxs-lookup"><span data-stu-id="87ce3-157">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="requirements"></a><span data-ttu-id="87ce3-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87ce3-158">Requirements</span></span>



| <span data-ttu-id="87ce3-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87ce3-159">Requirement</span></span> | <span data-ttu-id="87ce3-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="87ce3-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="87ce3-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87ce3-161">Minimum supported client</span></span><br/> | <span data-ttu-id="87ce3-162">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87ce3-162">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="87ce3-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87ce3-163">Minimum supported server</span></span><br/> | <span data-ttu-id="87ce3-164">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87ce3-164">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





