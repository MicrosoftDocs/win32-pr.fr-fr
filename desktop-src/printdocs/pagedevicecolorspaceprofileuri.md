---
description: En savoir plus sur le paramètre PageDeviceColorSpaceProfileURI. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: ab26850e-554a-4a1b-9250-edb0b4e17fe2
title: PageDeviceColorSpaceProfileURI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21420dec2e3057de903b1e04c55a7c6d234343b0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396644"
---
# <a name="pagedevicecolorspaceprofileuri"></a><span data-ttu-id="7a98b-105">PageDeviceColorSpaceProfileURI</span><span class="sxs-lookup"><span data-stu-id="7a98b-105">PageDeviceColorSpaceProfileURI</span></span>

<span data-ttu-id="7a98b-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="7a98b-106">This topic is not current.</span></span> <span data-ttu-id="7a98b-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="7a98b-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7a98b-108">Spécifie un URI relatif à la racine du package pour un profil ICC contenu dans un document XPS.</span><span class="sxs-lookup"><span data-stu-id="7a98b-108">Specifies a relative URI to the package root to an ICC profile contained in an XPS Document.</span></span> <span data-ttu-id="7a98b-109">Le traitement de cette option dépend de la configuration de la fonctionnalité PageDeviceColorSpaceUsage.</span><span class="sxs-lookup"><span data-stu-id="7a98b-109">The processing of this option depends of the setting of the PageDeviceColorSpaceUsage feature.</span></span> <span data-ttu-id="7a98b-110">Tous les éléments qui utilisent ce profil sont supposés être déjà dans l’espace de couleurs approprié du périphérique et ne sont pas gérés par la couleur dans le pilote ou le périphérique.</span><span class="sxs-lookup"><span data-stu-id="7a98b-110">All elements using that profile are assumed to be already in the appropriate device color space, and will not be color managed in the driver or device.</span></span>

-   [<span data-ttu-id="7a98b-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7a98b-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="7a98b-112">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="7a98b-112">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="7a98b-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="7a98b-113">Element Information</span></span>



| <span data-ttu-id="7a98b-114">Nom</span><span class="sxs-lookup"><span data-stu-id="7a98b-114">Name</span></span> | <span data-ttu-id="7a98b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a98b-115">Value</span></span> |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a98b-116">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="7a98b-116">Element Type</span></span> <br/>   | <span data-ttu-id="7a98b-117">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="7a98b-117">ParameterDef</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="7a98b-118">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="7a98b-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="7a98b-119">Page</span><span class="sxs-lookup"><span data-stu-id="7a98b-119">Page</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="7a98b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="7a98b-120">Notes</span></span> <br/>          | <span data-ttu-id="7a98b-121">Cela s’applique uniquement aux documents XPS et ne doit pas être utilisé dans des des PrintTicket arbitraires.</span><span class="sxs-lookup"><span data-stu-id="7a98b-121">This applies to XPS Documents only and should not be used in arbitrary PrintTickets.</span></span><br/> <span data-ttu-id="7a98b-122">Les consommateurs compatibles XPS doivent s’assurer qu’une référence URI à une ressource telle qu’une image ou un profil de couleurs dans un document de fonctionnalités d’impression ou un PrintTicket doit faire référence à un nom de partie (un URI relatif à la racine du package) dans le même package de document XPS qui contient le PrintTicket résultant.</span><span class="sxs-lookup"><span data-stu-id="7a98b-122">XPS-compliant consumers MUST enforce that a URI reference to a resource such as an image or color profile in either a Print Capabilities document or PrintTicket MUST refer to a part name (a relative URI to the package root) within the same XPS Document package that contains the resultant PrintTicket.</span></span> <span data-ttu-id="7a98b-123">Un consommateur XPS conforme ne doit pas utiliser un URI qui n’est pas conforme à la syntaxe du nom de la partie.</span><span class="sxs-lookup"><span data-stu-id="7a98b-123">A compliant XPS consumer MUST NOT use a URI that is not compliant with the part name syntax.</span></span> <span data-ttu-id="7a98b-124">Ces paramètres sont spécifiques à XPS.</span><span class="sxs-lookup"><span data-stu-id="7a98b-124">These settings are XPS specific.</span></span> <br/> <span data-ttu-id="7a98b-125">Les URI référencés dans un document de fonctionnalités d’impression ou un PrintTicket ne doivent pas être résolus en tant qu’URL.</span><span class="sxs-lookup"><span data-stu-id="7a98b-125">URIs which are referenced in either a Print Capabilities document or PrintTicket MUST NOT be resolved as URLs.</span></span> <span data-ttu-id="7a98b-126">Cela ne peut pas être résolu comme prévu et peut créer des risques de sécurité néfastes pour le pilote et le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7a98b-126">This is unsafe as they may not resolve as intended and may create harmful security risks for the driver and operating system.</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="7a98b-127">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="7a98b-127">Structure Content</span></span>

<span data-ttu-id="7a98b-128">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="7a98b-128">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="7a98b-129">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="7a98b-129">Structure Properties</span></span>

<span data-ttu-id="7a98b-130">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="7a98b-130">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="7a98b-131">Propriété</span><span class="sxs-lookup"><span data-stu-id="7a98b-131">Property</span></span>                | <span data-ttu-id="7a98b-132">xsi:type</span><span class="sxs-lookup"><span data-stu-id="7a98b-132">xsi:type</span></span>           | <span data-ttu-id="7a98b-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a98b-133">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="7a98b-134">DataType</span><span class="sxs-lookup"><span data-stu-id="7a98b-134">DataType</span></span><br/>     | <span data-ttu-id="7a98b-135">string</span><span class="sxs-lookup"><span data-stu-id="7a98b-135">string</span></span><br/>  | <span data-ttu-id="7a98b-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="7a98b-136">xs:string</span></span><br/>       |
| <span data-ttu-id="7a98b-137">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="7a98b-137">DefaultValue</span></span><br/> | <span data-ttu-id="7a98b-138">string</span><span class="sxs-lookup"><span data-stu-id="7a98b-138">string</span></span><br/>  | <span data-ttu-id="7a98b-139">non défini</span><span class="sxs-lookup"><span data-stu-id="7a98b-139">undefined</span></span><br/>       |
| <span data-ttu-id="7a98b-140">MaxLength</span><span class="sxs-lookup"><span data-stu-id="7a98b-140">MaxLength</span></span><br/>    | <span data-ttu-id="7a98b-141">entier</span><span class="sxs-lookup"><span data-stu-id="7a98b-141">integer</span></span><br/> | <span data-ttu-id="7a98b-142">non défini</span><span class="sxs-lookup"><span data-stu-id="7a98b-142">undefined</span></span><br/>       |
| <span data-ttu-id="7a98b-143">MinLength</span><span class="sxs-lookup"><span data-stu-id="7a98b-143">MinLength</span></span><br/>    | <span data-ttu-id="7a98b-144">integer</span><span class="sxs-lookup"><span data-stu-id="7a98b-144">integer</span></span><br/> | <span data-ttu-id="7a98b-145">1</span><span class="sxs-lookup"><span data-stu-id="7a98b-145">1</span></span><br/>               |
| <span data-ttu-id="7a98b-146">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7a98b-146">Mandatory</span></span><br/>    | <span data-ttu-id="7a98b-147">string</span><span class="sxs-lookup"><span data-stu-id="7a98b-147">string</span></span><br/>  | <span data-ttu-id="7a98b-148">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="7a98b-148">psk:Conditional</span></span><br/> |
| <span data-ttu-id="7a98b-149">Unité</span><span class="sxs-lookup"><span data-stu-id="7a98b-149">UnitType</span></span><br/>     | <span data-ttu-id="7a98b-150">string</span><span class="sxs-lookup"><span data-stu-id="7a98b-150">string</span></span><br/>  | <span data-ttu-id="7a98b-151">caractères</span><span class="sxs-lookup"><span data-stu-id="7a98b-151">characters</span></span><br/>      |



 

## <a name="related-topics"></a><span data-ttu-id="7a98b-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7a98b-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a98b-153">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="7a98b-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




