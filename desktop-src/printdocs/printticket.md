---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: fe6bd921-cbf3-4cca-afae-82d3822206ba
title: PrintTicket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d2e225eb38584e290db55c33594be80d0d7999
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106544385"
---
# <a name="printticket"></a><span data-ttu-id="fc2d4-104">PrintTicket</span><span class="sxs-lookup"><span data-stu-id="fc2d4-104">PrintTicket</span></span>

<span data-ttu-id="fc2d4-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-105">This topic is not current.</span></span> <span data-ttu-id="fc2d4-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="fc2d4-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="fc2d4-107">Un élément PrintTicket est l’élément racine du document PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-107">A PrintTicket element is the root element of the PrintTicket document.</span></span> <span data-ttu-id="fc2d4-108">Un élément PrintTicket contient toutes les informations de mise en forme du travail requises pour générer un travail.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-108">A PrintTicket element contains all job formatting information required to output a job.</span></span>

## <a name="element-tag"></a><span data-ttu-id="fc2d4-109">Balise d’élément</span><span class="sxs-lookup"><span data-stu-id="fc2d4-109">Element Tag</span></span>

<PrintTicket>

## <a name="xml-attributes"></a><span data-ttu-id="fc2d4-110">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="fc2d4-110">XML Attributes</span></span>

<span data-ttu-id="fc2d4-111">Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="fc2d4-112">Attribut XML</span><span class="sxs-lookup"><span data-stu-id="fc2d4-112">XML Attribute</span></span>      | <span data-ttu-id="fc2d4-113">Détails</span><span class="sxs-lookup"><span data-stu-id="fc2d4-113">Details</span></span>                                                                                                                                                                                   |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc2d4-114">version</span><span class="sxs-lookup"><span data-stu-id="fc2d4-114">version</span></span><br/> | <span data-ttu-id="fc2d4-115">Spécifie la version du schéma qui définit les types d’éléments et leur structure, un littéral de type entier.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-115">Specifies the version of the schema that defines element types and their structure, a literal of type integer.</span></span> <span data-ttu-id="fc2d4-116">La version actuelle du schéma est « 1 ».</span><span class="sxs-lookup"><span data-stu-id="fc2d4-116">The current schema version is "1".</span></span> <span data-ttu-id="fc2d4-117">Cet attribut est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-117">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="fc2d4-118">Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="fc2d4-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="fc2d4-119">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="fc2d4-119">Element Information</span></span>

<span data-ttu-id="fc2d4-120">Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="fc2d4-121">Category</span><span class="sxs-lookup"><span data-stu-id="fc2d4-121">Category</span></span>                   | <span data-ttu-id="fc2d4-122">Détails</span><span class="sxs-lookup"><span data-stu-id="fc2d4-122">Details</span></span>                                                                                                            |
|----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc2d4-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fc2d4-123">Parent elements</span></span><br/> | <span data-ttu-id="fc2d4-124">Racine du document uniquement.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-124">Document root only.</span></span><br/>                                                                                     |
| <span data-ttu-id="fc2d4-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fc2d4-125">Child elements</span></span><br/>  | <span data-ttu-id="fc2d4-126">*Fonctionnalité* (zéro ou plus)</span><span class="sxs-lookup"><span data-stu-id="fc2d4-126">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="fc2d4-127">*ParameterInit* (zéro ou plus)</span><span class="sxs-lookup"><span data-stu-id="fc2d4-127">*ParameterInit* (zero or more)</span></span><br/> <span data-ttu-id="fc2d4-128">*Property* (zéro, un ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="fc2d4-128">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="fc2d4-129">Élément This</span><span class="sxs-lookup"><span data-stu-id="fc2d4-129">This element</span></span><br/>    | <span data-ttu-id="fc2d4-130">Aucune donnée de caractères n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-130">No character data is permitted.</span></span><br/> <span data-ttu-id="fc2d4-131">Les frères enfants en double ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-131">Duplicate child siblings are not permitted.</span></span><br/>                  |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="fc2d4-132">Dépendances de configuration</span><span class="sxs-lookup"><span data-stu-id="fc2d4-132">Configuration Dependencies</span></span>

<span data-ttu-id="fc2d4-133">Les dépendances de configuration s’appliquent uniquement aux éléments d’un document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="fc2d4-133">Configuration dependencies are applicable only to elements in a PrintCapabilities document.</span></span>

## <a name="example"></a><span data-ttu-id="fc2d4-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="fc2d4-134">Example</span></span>

<span data-ttu-id="fc2d4-135">Consultez l' [exemple PrintTicket](printticket-example.md).</span><span class="sxs-lookup"><span data-stu-id="fc2d4-135">See [PrintTicket Example](printticket-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc2d4-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc2d4-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc2d4-137">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="fc2d4-137">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




