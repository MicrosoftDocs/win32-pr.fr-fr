---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: PageDeviceColorSpaceProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4536251150851ad02abf41ca26ffaa36699281db
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106531268"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="4fdd1-104">PageDeviceColorSpaceProfileURI</span><span class="sxs-lookup"><span data-stu-id="4fdd1-104">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="4fdd1-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="4fdd1-105">This topic is not current.</span></span> <span data-ttu-id="4fdd1-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4fdd1-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4fdd1-107">Spécifie un URI relatif à la racine du package pour un profil ICC contenu dans un document XPS.</span><span class="sxs-lookup"><span data-stu-id="4fdd1-107">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="4fdd1-108">Le traitement de cette option dépend de la configuration de la fonctionnalité PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="4fdd1-108">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="4fdd1-109">Tous les éléments qui utilisent ce profil sont supposés être déjà dans l’espace de couleurs approprié du périphérique et ne sont pas gérés par la couleur dans le pilote ou le périphérique.</span><span class="sxs-lookup"><span data-stu-id="4fdd1-109">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="4fdd1-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4fdd1-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="4fdd1-111">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="4fdd1-111">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="4fdd1-112">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4fdd1-112">Element Information</span></span>



| <span data-ttu-id="4fdd1-113">Nom</span><span class="sxs-lookup"><span data-stu-id="4fdd1-113">Name</span></span>                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fdd1-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="4fdd1-114">Element Type</span></span> <br/>   | <span data-ttu-id="4fdd1-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="4fdd1-115">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="4fdd1-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="4fdd1-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="4fdd1-117">Page</span><span class="sxs-lookup"><span data-stu-id="4fdd1-117">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="4fdd1-118">Notes</span><span class="sxs-lookup"><span data-stu-id="4fdd1-118">Notes</span></span> <br/>          | <span data-ttu-id="4fdd1-119">Cela s’applique uniquement aux documents XPS et ne doit pas être utilisé dans des des PrintTicket arbitraires.</span><span class="sxs-lookup"><span data-stu-id="4fdd1-119">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="4fdd1-120">Les consommateurs compatibles XPS doivent s’assurer qu’une référence URI à une ressource telle qu’une image ou un profil de couleurs dans un document de fonctionnalités d’impression ou un PrintTicket doit faire référence à un nom de partie (un URI relatif à la racine du package) dans le même package de document XPS qui contient le PrintTicket résultant.</span><span class="sxs-lookup"><span data-stu-id="4fdd1-120">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="4fdd1-121">Un consommateur XPS conforme ne doit pas utiliser un URI qui n’est pas conforme à la syntaxe du nom de la partie.</span><span class="sxs-lookup"><span data-stu-id="4fdd1-121">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="4fdd1-122">Ces paramètres sont spécifiques à XPS.</span><span class="sxs-lookup"><span data-stu-id="4fdd1-122">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="4fdd1-123">Les URI référencés dans un document de fonctionnalités d’impression ou un PrintTicket ne doivent pas être résolus en tant qu’URL.</span><span class="sxs-lookup"><span data-stu-id="4fdd1-123">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="4fdd1-124">Cela ne peut pas être résolu comme prévu et peut créer des risques de sécurité néfastes pour le pilote et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="4fdd1-124">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="4fdd1-125">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="4fdd1-125">Structure Content</span></span>

<span data-ttu-id="4fdd1-126">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="4fdd1-126">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageDeviceColorSpaceProfileURI">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:string</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxLength">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinLength">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">characters</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="4fdd1-127">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="4fdd1-127">Structure Properties</span></span>

<span data-ttu-id="4fdd1-128">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="4fdd1-128">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="4fdd1-129">Propriété</span><span class="sxs-lookup"><span data-stu-id="4fdd1-129">Property</span></span>                | <span data-ttu-id="4fdd1-130">xsi:type</span><span class="sxs-lookup"><span data-stu-id="4fdd1-130">xsi:type</span></span>           | <span data-ttu-id="4fdd1-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="4fdd1-131">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="4fdd1-132">DataType</span><span class="sxs-lookup"><span data-stu-id="4fdd1-132">DataType</span></span><br/>     | <span data-ttu-id="4fdd1-133">string</span><span class="sxs-lookup"><span data-stu-id="4fdd1-133">string</span></span><br/>  | <span data-ttu-id="4fdd1-134">xs:string</span><span class="sxs-lookup"><span data-stu-id="4fdd1-134">xs:string</span></span><br/>       |
| <span data-ttu-id="4fdd1-135">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4fdd1-135">DefaultValue</span></span><br/> | <span data-ttu-id="4fdd1-136">string</span><span class="sxs-lookup"><span data-stu-id="4fdd1-136">string</span></span><br/>  | <span data-ttu-id="4fdd1-137">non défini</span><span class="sxs-lookup"><span data-stu-id="4fdd1-137">undefined</span></span><br/>       |
| <span data-ttu-id="4fdd1-138">MaxLength</span><span class="sxs-lookup"><span data-stu-id="4fdd1-138">MaxLength</span></span><br/>    | <span data-ttu-id="4fdd1-139">entier</span><span class="sxs-lookup"><span data-stu-id="4fdd1-139">integer</span></span><br/> | <span data-ttu-id="4fdd1-140">non défini</span><span class="sxs-lookup"><span data-stu-id="4fdd1-140">undefined</span></span><br/>       |
| <span data-ttu-id="4fdd1-141">MinLength</span><span class="sxs-lookup"><span data-stu-id="4fdd1-141">MinLength</span></span><br/>    | <span data-ttu-id="4fdd1-142">integer</span><span class="sxs-lookup"><span data-stu-id="4fdd1-142">integer</span></span><br/> | <span data-ttu-id="4fdd1-143">1</span><span class="sxs-lookup"><span data-stu-id="4fdd1-143">1</span></span><br/>               |
| <span data-ttu-id="4fdd1-144">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4fdd1-144">Mandatory</span></span><br/>    | <span data-ttu-id="4fdd1-145">string</span><span class="sxs-lookup"><span data-stu-id="4fdd1-145">string</span></span><br/>  | <span data-ttu-id="4fdd1-146">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="4fdd1-146">psk:Conditional</span></span><br/> |
| <span data-ttu-id="4fdd1-147">Unité</span><span class="sxs-lookup"><span data-stu-id="4fdd1-147">UnitType</span></span><br/>     | <span data-ttu-id="4fdd1-148">string</span><span class="sxs-lookup"><span data-stu-id="4fdd1-148">string</span></span><br/>  | <span data-ttu-id="4fdd1-149">caractères</span><span class="sxs-lookup"><span data-stu-id="4fdd1-149">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="4fdd1-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4fdd1-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4fdd1-151">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="4fdd1-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




