---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e10c6dd8ce98b071f1eb239762544a9b72160035
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106539806"
---
# <a name="printcapabilities"></a><span data-ttu-id="c1370-104">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="c1370-104">PrintCapabilities</span></span>

<span data-ttu-id="c1370-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="c1370-105">This topic is not current.</span></span> <span data-ttu-id="c1370-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="c1370-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="c1370-107">Un élément PrintCapabilities représente la racine du document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="c1370-107">A PrintCapabilities element represents the root of the PrintCapabilities document.</span></span> <span data-ttu-id="c1370-108">Le document PrintCapabilities contient toutes les informations nécessaires pour décrire les attributs des appareils pris en charge, en fonction d’une configuration d’appareil particulière.</span><span class="sxs-lookup"><span data-stu-id="c1370-108">The PrintCapabilities document contains all of the information needed to describe the supported device attributes, given a particular device configuration.</span></span>

## <a name="element-tag"></a><span data-ttu-id="c1370-109">Balise d’élément</span><span class="sxs-lookup"><span data-stu-id="c1370-109">Element Tag</span></span>

<PrintCapabilities>

## <a name="xml-attributes"></a><span data-ttu-id="c1370-110">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="c1370-110">XML Attributes</span></span>

<span data-ttu-id="c1370-111">Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.</span><span class="sxs-lookup"><span data-stu-id="c1370-111">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="c1370-112">Attribut XML</span><span class="sxs-lookup"><span data-stu-id="c1370-112">XML Attribute</span></span>      | <span data-ttu-id="c1370-113">Détails</span><span class="sxs-lookup"><span data-stu-id="c1370-113">Details</span></span>                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1370-114">version</span><span class="sxs-lookup"><span data-stu-id="c1370-114">version</span></span><br/> | <span data-ttu-id="c1370-115">Spécifie la version du schéma qui définit les types d’éléments et leur structure.</span><span class="sxs-lookup"><span data-stu-id="c1370-115">Specifies the version of the schema that defines element types and their structure.</span></span> <span data-ttu-id="c1370-116">L’attribut version est de type entier.</span><span class="sxs-lookup"><span data-stu-id="c1370-116">The version attribute is of type integer.</span></span> <span data-ttu-id="c1370-117">La version actuelle du schéma est « 1 ».</span><span class="sxs-lookup"><span data-stu-id="c1370-117">The current schema version is designated "1".</span></span> <span data-ttu-id="c1370-118">Cet attribut est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c1370-118">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="c1370-119">Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="c1370-119">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="c1370-120">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c1370-120">Element Information</span></span>

<span data-ttu-id="c1370-121">Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="c1370-121">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="c1370-122">Category</span><span class="sxs-lookup"><span data-stu-id="c1370-122">Category</span></span>                   | <span data-ttu-id="c1370-123">Détails</span><span class="sxs-lookup"><span data-stu-id="c1370-123">Details</span></span>                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1370-124">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c1370-124">Parent elements</span></span><br/> | <span data-ttu-id="c1370-125">Racine du document uniquement.</span><span class="sxs-lookup"><span data-stu-id="c1370-125">Document root only.</span></span><br/>                                                                                    |
| <span data-ttu-id="c1370-126">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c1370-126">Child elements</span></span><br/>  | <span data-ttu-id="c1370-127">*Fonctionnalité* (zéro ou plus)</span><span class="sxs-lookup"><span data-stu-id="c1370-127">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="c1370-128">*ParameterDef* (zéro ou plus)</span><span class="sxs-lookup"><span data-stu-id="c1370-128">*ParameterDef* (zero or more)</span></span><br/> <span data-ttu-id="c1370-129">*Property* (zéro, un ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="c1370-129">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="c1370-130">Élément This</span><span class="sxs-lookup"><span data-stu-id="c1370-130">This element</span></span><br/>    | <span data-ttu-id="c1370-131">Aucune donnée de caractères n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="c1370-131">No character data is permitted.</span></span><br/> <span data-ttu-id="c1370-132">Les frères enfants en double ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="c1370-132">Duplicate child siblings are not permitted.</span></span><br/>                 |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="c1370-133">Dépendances de configuration</span><span class="sxs-lookup"><span data-stu-id="c1370-133">Configuration Dependencies</span></span>

<span data-ttu-id="c1370-134">L’élément racine ne peut pas avoir de dépendances de configuration.</span><span class="sxs-lookup"><span data-stu-id="c1370-134">The root element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="c1370-135">Exemple</span><span class="sxs-lookup"><span data-stu-id="c1370-135">Example</span></span>

<span data-ttu-id="c1370-136">Consultez l' [exemple de document PrintCapabilities](printcapabilities-document-example.md).</span><span class="sxs-lookup"><span data-stu-id="c1370-136">See [PrintCapabilities Document Example](printcapabilities-document-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1370-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c1370-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1370-138">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="c1370-138">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




