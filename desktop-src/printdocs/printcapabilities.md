---
description: En savoir plus sur l’élément PrintCapabilities, qui représente la racine du document PrintCapabilities.
ms.assetid: f503b62f-02e1-4621-8799-a8b6ad12f489
title: PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2158fd651849df2e4ea24c640065f1041569741a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407022"
---
# <a name="printcapabilities"></a><span data-ttu-id="276d3-103">PrintCapabilities</span><span class="sxs-lookup"><span data-stu-id="276d3-103">PrintCapabilities</span></span>

<span data-ttu-id="276d3-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="276d3-104">This topic is not current.</span></span> <span data-ttu-id="276d3-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="276d3-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="276d3-106">Un élément PrintCapabilities représente la racine du document PrintCapabilities.</span><span class="sxs-lookup"><span data-stu-id="276d3-106">A PrintCapabilities element represents the root of the PrintCapabilities document.</span></span> <span data-ttu-id="276d3-107">Le document PrintCapabilities contient toutes les informations nécessaires pour décrire les attributs des appareils pris en charge, en fonction d’une configuration d’appareil particulière.</span><span class="sxs-lookup"><span data-stu-id="276d3-107">The PrintCapabilities document contains all of the information needed to describe the supported device attributes, given a particular device configuration.</span></span>

## <a name="element-tag"></a><span data-ttu-id="276d3-108">Balise d’élément</span><span class="sxs-lookup"><span data-stu-id="276d3-108">Element Tag</span></span>

<PrintCapabilities>

## <a name="xml-attributes"></a><span data-ttu-id="276d3-109">Attributs XML</span><span class="sxs-lookup"><span data-stu-id="276d3-109">XML Attributes</span></span>

<span data-ttu-id="276d3-110">Le tableau suivant répertorie les attributs XML qui peuvent être liés à cet élément.</span><span class="sxs-lookup"><span data-stu-id="276d3-110">The following table lists the XML attributes that may be pertain to this element.</span></span>



| <span data-ttu-id="276d3-111">Attribut XML</span><span class="sxs-lookup"><span data-stu-id="276d3-111">XML Attribute</span></span>      | <span data-ttu-id="276d3-112">Détails</span><span class="sxs-lookup"><span data-stu-id="276d3-112">Details</span></span>                                                                                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="276d3-113">version</span><span class="sxs-lookup"><span data-stu-id="276d3-113">version</span></span><br/> | <span data-ttu-id="276d3-114">Spécifie la version du schéma qui définit les types d’éléments et leur structure.</span><span class="sxs-lookup"><span data-stu-id="276d3-114">Specifies the version of the schema that defines element types and their structure.</span></span> <span data-ttu-id="276d3-115">L’attribut version est de type entier.</span><span class="sxs-lookup"><span data-stu-id="276d3-115">The version attribute is of type integer.</span></span> <span data-ttu-id="276d3-116">La version actuelle du schéma est « 1 ».</span><span class="sxs-lookup"><span data-stu-id="276d3-116">The current schema version is designated "1".</span></span> <span data-ttu-id="276d3-117">Cet attribut est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="276d3-117">This attribute is required.</span></span> <br/> |



 

<span data-ttu-id="276d3-118">Pour plus d’informations, consultez la section [attributs XML](xml-attributes.md) .</span><span class="sxs-lookup"><span data-stu-id="276d3-118">For more information, please see [XML Attributes](xml-attributes.md) section.</span></span>

## <a name="element-information"></a><span data-ttu-id="276d3-119">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="276d3-119">Element Information</span></span>

<span data-ttu-id="276d3-120">Le tableau suivant répertorie les éléments qui peuvent être des parents de cet élément, les éléments qui peuvent être des enfants de cet élément, ainsi que toutes les restrictions applicables à l’élément lui-même.</span><span class="sxs-lookup"><span data-stu-id="276d3-120">The following table lists the elements that may be parents of this element, the elements that may be children of this element, and any restrictions on the element itself.</span></span>



| <span data-ttu-id="276d3-121">Category</span><span class="sxs-lookup"><span data-stu-id="276d3-121">Category</span></span>                   | <span data-ttu-id="276d3-122">Détails</span><span class="sxs-lookup"><span data-stu-id="276d3-122">Details</span></span>                                                                                                           |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="276d3-123">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="276d3-123">Parent elements</span></span><br/> | <span data-ttu-id="276d3-124">Racine du document uniquement.</span><span class="sxs-lookup"><span data-stu-id="276d3-124">Document root only.</span></span><br/>                                                                                    |
| <span data-ttu-id="276d3-125">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="276d3-125">Child elements</span></span><br/>  | <span data-ttu-id="276d3-126">*Fonctionnalité* (zéro ou plus)</span><span class="sxs-lookup"><span data-stu-id="276d3-126">*Feature* (zero or more)</span></span><br/> <span data-ttu-id="276d3-127">*ParameterDef* (zéro ou plus)</span><span class="sxs-lookup"><span data-stu-id="276d3-127">*ParameterDef* (zero or more)</span></span><br/> <span data-ttu-id="276d3-128">*Property* (zéro, un ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="276d3-128">*Property* (zero or more)</span></span><br/> |
| <span data-ttu-id="276d3-129">Élément This</span><span class="sxs-lookup"><span data-stu-id="276d3-129">This element</span></span><br/>    | <span data-ttu-id="276d3-130">Aucune donnée de caractères n’est autorisée.</span><span class="sxs-lookup"><span data-stu-id="276d3-130">No character data is permitted.</span></span><br/> <span data-ttu-id="276d3-131">Les frères enfants en double ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="276d3-131">Duplicate child siblings are not permitted.</span></span><br/>                 |



 

## <a name="configuration-dependencies"></a><span data-ttu-id="276d3-132">Dépendances de configuration</span><span class="sxs-lookup"><span data-stu-id="276d3-132">Configuration Dependencies</span></span>

<span data-ttu-id="276d3-133">L’élément racine ne peut pas avoir de dépendances de configuration.</span><span class="sxs-lookup"><span data-stu-id="276d3-133">The root element may not have any configuration dependencies.</span></span>

## <a name="example"></a><span data-ttu-id="276d3-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="276d3-134">Example</span></span>

<span data-ttu-id="276d3-135">Consultez l' [exemple de document PrintCapabilities](printcapabilities-document-example.md).</span><span class="sxs-lookup"><span data-stu-id="276d3-135">See [PrintCapabilities Document Example](printcapabilities-document-example.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="276d3-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="276d3-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="276d3-137">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="276d3-137">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




