---
description: Recherche des informations sur l’élément PrintTicket. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b279ff681704a63f6547738c73fb9192d6f8a65d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120074"
---
# <a name="printticket"></a><span data-ttu-id="a4a3f-105">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="a4a3f-105">PrintTicket</span></span>

<span data-ttu-id="a4a3f-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="a4a3f-106">This topic is not current.</span></span> <span data-ttu-id="a4a3f-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="a4a3f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="a4a3f-108">Un élément PrintTicket est l’élément racine du document PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="a4a3f-108">A PrintTicket element is the root element of the PrintTicket document.</span></span> <span data-ttu-id="a4a3f-109">Un élément PrintTicket contient toutes les informations de mise en forme du travail requises pour générer un travail.</span><span class="sxs-lookup"><span data-stu-id="a4a3f-109">A PrintTicket element contains all job formatting information required to output a job.</span></span>

## <a name="element-tag"></a><span data-ttu-id="a4a3f-110">Balise d’élément</span><span class="sxs-lookup"><span data-stu-id="a4a3f-110">Element Tag</span></span>

<PrintTicket>

## <a name="xml-attributes"></a><span data-ttu-id="a4a3f-111">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="a4a3f-111">XML Attributes</span></span>

<span data-ttu-id="a4a3f-112">Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.</span><span class="sxs-lookup"><span data-stu-id="a4a3f-112">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="a4a3f-113">Attribut XML</span><span class="sxs-lookup"><span data-stu-id="a4a3f-113">XML Attribute</span></span>      | <span data-ttu-id="a4a3f-114">Détails</span><span class="sxs-lookup"><span data-stu-id="a4a3f-114">Details</span></span>                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a3f-115">version</span><span class="sxs-lookup"><span data-stu-id="a4a3f-115">version</span></span><br/> | <span data-ttu-id="a4a3f-116">Spécifie la version du schéma qui définit les types d’éléments et leur structure, un littéral de type entier.</span><span class="sxs-lookup"><span data-stu-id="a4a3f-116">Specifies the version of the schema that defines element types and their structure, a literal of type integer.</span></span> <span data-ttu-id="a4a3f-117">La version actuelle du schéma est « 1 ».</span><span class="sxs-lookup"><span data-stu-id="a4a3f-117">The current schema version is "1".</span></span> <span data-ttu-id="a4a3f-118">Cet attribut est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="a4a3f-118">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="a4a3f-119">Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="a4a3f-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="a4a3f-120">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="a4a3f-120">Element Information</span></span>

<span data-ttu-id="a4a3f-121">Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="a4a3f-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="a4a3f-122">Category</span><span class="sxs-lookup"><span data-stu-id="a4a3f-122">Category</span></span>                   | <span data-ttu-id="a4a3f-123">Détails</span><span class="sxs-lookup"><span data-stu-id="a4a3f-123">Details</span></span>                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4a3f-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a4a3f-124">Parent elements</span></span><br/> | <span data-ttu-id="a4a3f-125">Racine du document uniquement.</span><span class="sxs-lookup"><span data-stu-id="a4a3f-125">Document root only.</span></span><br/>                                                                                     |
| <span data-ttu-id="a4a3f-126">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a4a3f-126">Child elements</span></span><br/>  | <span data-ttu-id="a4a3f-127">*Fonctionnalité* (zéro ou plus)</span><span class="sxs-lookup"><span data-stu-id="a4a3f-127">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="a4a3f-128">*ParameterInit* (zéro ou plus)</span><span class="sxs-lookup"><span data-stu-id="a4a3f-128">*ParameterInit* (zero or more)</span></span><br/> <span data-ttu-id="a4a3f-129">*Property* (zéro, un ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="a4a3f-129">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="a4a3f-130">Élément This</span><span class="sxs-lookup"><span data-stu-id="a4a3f-130">This element</span></span><br/>    | <span data-ttu-id="a4a3f-131">Aucune donnée de caractères n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="a4a3f-131">No character data is permitted.</span></span><br/> <span data-ttu-id="a4a3f-132">Les frères enfants en double ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="a4a3f-132">Duplicate child siblings are not permitted.</span></span><br/>                  |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="a4a3f-133">Dépendances de configuration</span><span class="sxs-lookup"><span data-stu-id="a4a3f-133">Configuration Dependencies</span></span>

<span data-ttu-id="a4a3f-134">Les dépendances de configuration s’appliquent uniquement aux éléments d’un document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="a4a3f-134">Configuration dependencies are applicable only to elements in a PrintCapabilities document.</span></span>

## <a name="example"></a><span data-ttu-id="a4a3f-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="a4a3f-135">Example</span></span>

<span data-ttu-id="a4a3f-136">Consultez l' [exemple PrintTicket](printticket-example.md).</span><span class="sxs-lookup"><span data-stu-id="a4a3f-136">See [PrintTicket Example](printticket-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4a3f-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a4a3f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4a3f-138">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="a4a3f-138">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




