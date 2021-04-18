---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 53e38979-2065-4304-a0ed-0434c8d2efc8
title: DocumentStaple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9fe7edd7385761e779980cf5d1dbea7a979a1f
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106522520"
---
# <a name="documentstaple"></a><span data-ttu-id="75d6f-104">DocumentStaple</span><span class="sxs-lookup"><span data-stu-id="75d6f-104">DocumentStaple</span></span>

<span data-ttu-id="75d6f-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="75d6f-105">This topic is not current.</span></span> <span data-ttu-id="75d6f-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="75d6f-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="75d6f-107">Décrit les caractéristiques de l’agrafage de la sortie.</span><span class="sxs-lookup"><span data-stu-id="75d6f-107">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="75d6f-108">Chaque document est agrafé séparément.</span><span class="sxs-lookup"><span data-stu-id="75d6f-108">Each document is stapled separately.</span></span> <span data-ttu-id="75d6f-109">Les mots clés JobStapleAllDocuments et DocumentStaple s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="75d6f-109">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="75d6f-110">Il revient au pilote de déterminer la gestion des contraintes entre ces mots clés.</span><span class="sxs-lookup"><span data-stu-id="75d6f-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="75d6f-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="75d6f-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="75d6f-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="75d6f-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="75d6f-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="75d6f-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="75d6f-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="75d6f-114">Element Information</span></span>



| <span data-ttu-id="75d6f-115">Nom</span><span class="sxs-lookup"><span data-stu-id="75d6f-115">Name</span></span>                       |                                                                                |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="75d6f-116">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="75d6f-116">Element Type</span></span> <br/>   | <span data-ttu-id="75d6f-117">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="75d6f-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="75d6f-118">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="75d6f-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="75d6f-119">Document</span><span class="sxs-lookup"><span data-stu-id="75d6f-119">Document</span></span><br/>                                                            |
| <span data-ttu-id="75d6f-120">Notes</span><span class="sxs-lookup"><span data-stu-id="75d6f-120">Notes</span></span> <br/>          | <span data-ttu-id="75d6f-121">Haut, bas, gauche et droite sont relatifs à PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="75d6f-121">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="75d6f-122">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="75d6f-122">Structural Content</span></span>

<span data-ttu-id="75d6f-123">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="75d6f-123">The XML structure of this element is:</span></span>

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

## <a name="structure-variables"></a><span data-ttu-id="75d6f-124">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="75d6f-124">Structure Variables</span></span>

<span data-ttu-id="75d6f-125">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="75d6f-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="75d6f-126">Nom</span><span class="sxs-lookup"><span data-stu-id="75d6f-126">Name</span></span>                               | <span data-ttu-id="75d6f-127">Type de données</span><span class="sxs-lookup"><span data-stu-id="75d6f-127">Data type</span></span>          | <span data-ttu-id="75d6f-128">Unité</span><span class="sxs-lookup"><span data-stu-id="75d6f-128">Unit</span></span>                       | <span data-ttu-id="75d6f-129">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="75d6f-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="75d6f-130">Résumé</span><span class="sxs-lookup"><span data-stu-id="75d6f-130">Summary</span></span>                                                                                                                                                     |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75d6f-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="75d6f-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="75d6f-132">string</span><span class="sxs-lookup"><span data-stu-id="75d6f-132">string</span></span><br/>  | <span data-ttu-id="75d6f-133">caractères</span><span class="sxs-lookup"><span data-stu-id="75d6f-133">characters</span></span><br/>      | <span data-ttu-id="75d6f-134">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="75d6f-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="75d6f-135">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="75d6f-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="75d6f-136">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="75d6f-136">The name of the option.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="75d6f-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="75d6f-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="75d6f-138">string</span><span class="sxs-lookup"><span data-stu-id="75d6f-138">string</span></span><br/>  | <span data-ttu-id="75d6f-139">n/a</span><span class="sxs-lookup"><span data-stu-id="75d6f-139">n/a</span></span><br/>             | <span data-ttu-id="75d6f-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="75d6f-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="75d6f-141">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="75d6f-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                |
| <span data-ttu-id="75d6f-142">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="75d6f-142">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="75d6f-143">entier</span><span class="sxs-lookup"><span data-stu-id="75d6f-143">integer</span></span><br/> | <span data-ttu-id="75d6f-144">degrés</span><span class="sxs-lookup"><span data-stu-id="75d6f-144">degrees</span></span><br/>         | <span data-ttu-id="75d6f-145">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="75d6f-145">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="75d6f-146">Spécifie l’angle de l’agrafage par rapport à la direction X du PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="75d6f-146">Specifies the staple angle, relative to the X direction of the PageImageableSize.</span></span> <span data-ttu-id="75d6f-147">L’angle de l’agrafage est mesuré dans un sens dans le sens inverse des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="75d6f-147">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="75d6f-148">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="75d6f-148">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="75d6f-149">entier</span><span class="sxs-lookup"><span data-stu-id="75d6f-149">integer</span></span><br/> | <span data-ttu-id="75d6f-150">feuilles de média</span><span class="sxs-lookup"><span data-stu-id="75d6f-150">sheets of media</span></span><br/> | <span data-ttu-id="75d6f-151">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="75d6f-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="75d6f-152">Spécifie le nombre de feuilles prises en charge par l’option d’agrafage pour le MediaType actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="75d6f-152">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                                |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="75d6f-153">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="75d6f-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="75d6f-154">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="75d6f-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="75d6f-155">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="75d6f-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="75d6f-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75d6f-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75d6f-157">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="75d6f-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




