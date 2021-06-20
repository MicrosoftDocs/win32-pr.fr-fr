---
description: En savoir plus sur l’élément JobStapleAllDocuments, qui décrit les caractéristiques de l’agrafage de la sortie.
ms.assetid: 53e38979-2065-4304-a0ed-0434c8d2efc8
title: DocumentStaple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2cda02c452ebb053c71811fb2642cea7371b2f
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409132"
---
# <a name="documentstaple"></a><span data-ttu-id="6b546-103">DocumentStaple</span><span class="sxs-lookup"><span data-stu-id="6b546-103">DocumentStaple</span></span>

<span data-ttu-id="6b546-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="6b546-104">This topic is not current.</span></span> <span data-ttu-id="6b546-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="6b546-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6b546-106">Décrit les caractéristiques de l’agrafage de la sortie.</span><span class="sxs-lookup"><span data-stu-id="6b546-106">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="6b546-107">Chaque document est agrafé séparément.</span><span class="sxs-lookup"><span data-stu-id="6b546-107">Each document is stapled separately.</span></span> <span data-ttu-id="6b546-108">Les mots clés JobStapleAllDocuments et DocumentStaple s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="6b546-108">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="6b546-109">Il revient au pilote de déterminer la gestion des contraintes entre ces mots clés.</span><span class="sxs-lookup"><span data-stu-id="6b546-109">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="6b546-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="6b546-110">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="6b546-111">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="6b546-111">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="6b546-112">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="6b546-112">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="6b546-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="6b546-113">Element Information</span></span>



| <span data-ttu-id="6b546-114">Nom</span><span class="sxs-lookup"><span data-stu-id="6b546-114">Name</span></span> | <span data-ttu-id="6b546-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b546-115">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="6b546-116">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="6b546-116">Element Type</span></span> <br/>   | <span data-ttu-id="6b546-117">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="6b546-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="6b546-118">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="6b546-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="6b546-119">Document</span><span class="sxs-lookup"><span data-stu-id="6b546-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="6b546-120">Notes</span><span class="sxs-lookup"><span data-stu-id="6b546-120">Notes</span></span> <br/>          | <span data-ttu-id="6b546-121">Haut, bas, gauche et droite sont relatifs à PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="6b546-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="6b546-122">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="6b546-122">Structural Content</span></span>

<span data-ttu-id="6b546-123">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="6b546-123">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:DocumentStaple">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:Angle" >
      <psf:Value xsi:type="xs:integer">_AngleValue_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_SheetCapacityValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
      
```

## <a name="structure-variables"></a><span data-ttu-id="6b546-124">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="6b546-124">Structure Variables</span></span>

<span data-ttu-id="6b546-125">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="6b546-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="6b546-126">Nom</span><span class="sxs-lookup"><span data-stu-id="6b546-126">Name</span></span>                               | <span data-ttu-id="6b546-127">Type de données</span><span class="sxs-lookup"><span data-stu-id="6b546-127">Data type</span></span>          | <span data-ttu-id="6b546-128">Unité</span><span class="sxs-lookup"><span data-stu-id="6b546-128">Unit</span></span>                       | <span data-ttu-id="6b546-129">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="6b546-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="6b546-130">Résumé</span><span class="sxs-lookup"><span data-stu-id="6b546-130">Summary</span></span>                                                                                                                                                     |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b546-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="6b546-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="6b546-132">string</span><span class="sxs-lookup"><span data-stu-id="6b546-132">string</span></span><br/>  | <span data-ttu-id="6b546-133">caractères</span><span class="sxs-lookup"><span data-stu-id="6b546-133">characters</span></span><br/>      | <span data-ttu-id="6b546-134">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="6b546-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="6b546-135">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="6b546-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="6b546-136">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="6b546-136">The name of the option.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="6b546-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="6b546-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="6b546-138">string</span><span class="sxs-lookup"><span data-stu-id="6b546-138">string</span></span><br/>  | <span data-ttu-id="6b546-139">n/a</span><span class="sxs-lookup"><span data-stu-id="6b546-139">n/a</span></span><br/>             | <span data-ttu-id="6b546-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="6b546-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="6b546-141">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="6b546-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                |
| <span data-ttu-id="6b546-142">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="6b546-142">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="6b546-143">entier</span><span class="sxs-lookup"><span data-stu-id="6b546-143">integer</span></span><br/> | <span data-ttu-id="6b546-144">degrés</span><span class="sxs-lookup"><span data-stu-id="6b546-144">degrees</span></span><br/>         | <span data-ttu-id="6b546-145">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="6b546-145">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="6b546-146">Spécifie l’angle de l’agrafage par rapport à la direction X du PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="6b546-146">Specifies the staple angle, relative to the X direction of the PageImageableSize.</span></span> <span data-ttu-id="6b546-147">L’angle de l’agrafage est mesuré dans un sens dans le sens inverse des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="6b546-147">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="6b546-148">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="6b546-148">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="6b546-149">entier</span><span class="sxs-lookup"><span data-stu-id="6b546-149">integer</span></span><br/> | <span data-ttu-id="6b546-150">feuilles de média</span><span class="sxs-lookup"><span data-stu-id="6b546-150">sheets of media</span></span><br/> | <span data-ttu-id="6b546-151">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="6b546-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="6b546-152">Spécifie le nombre de feuilles prises en charge par l’option d’agrafage pour le MediaType actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="6b546-152">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                                |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="6b546-153">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="6b546-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="6b546-154">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="6b546-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="6b546-155">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="6b546-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:DocumentStaple">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies saddle stitch stapling -->
  <psf:Option name="psk:SaddleStitch">
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, left corner. -->
  <psf:Option name="psk:StapleBottomLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the bottom, right corner. -->
  <psf:Option name="psk:StapleBottomRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the left edge. -->
  <psf:Option name="psk:StapleDualLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the right edge. -->
  <psf:Option name="psk:StapleDualRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the top edge. -->
  <psf:Option name="psk:StapleDualTop">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no stapling. -->
  <psf:Option name="psk:None" />
  <!-- Specifies a single staple in the top, left corner. -->
  <psf:Option name="psk:StapleTopLeft">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a single staple in the top, right corner. -->
  <psf:Option name="psk:StapleTopRight">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies two staples along the bottom edge. -->
  <psf:Option name="psk:StapleDualBottom">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="6b546-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6b546-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b546-157">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="6b546-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




