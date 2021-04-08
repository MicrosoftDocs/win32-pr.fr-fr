---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: a6721c13-a3dc-4273-b40f-2a28184b04a9
title: JobStapleAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b3576611dcdc746342b8ed1b2c3d7ebf8fb779
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "103953515"
---
# <a name="jobstaplealldocuments"></a><span data-ttu-id="01972-104">JobStapleAllDocuments</span><span class="sxs-lookup"><span data-stu-id="01972-104">JobStapleAllDocuments</span></span>

<span data-ttu-id="01972-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="01972-105">This topic is not current.</span></span> <span data-ttu-id="01972-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="01972-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="01972-107">Décrit les caractéristiques de l’agrafage de la sortie.</span><span class="sxs-lookup"><span data-stu-id="01972-107">Describes the stapling characteristics of the output.</span></span> <span data-ttu-id="01972-108">Tous les documents du travail sont agrafés ensemble.</span><span class="sxs-lookup"><span data-stu-id="01972-108">All documents in the job are stapled together.</span></span> <span data-ttu-id="01972-109">Les mots clés JobStapleAllDocuments et DocumentStaple s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="01972-109">The JobStapleAllDocuments and DocumentStaple keywords are mutually exclusive.</span></span> <span data-ttu-id="01972-110">Il revient au pilote de déterminer la gestion des contraintes entre ces mots clés.</span><span class="sxs-lookup"><span data-stu-id="01972-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="01972-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="01972-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="01972-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="01972-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="01972-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="01972-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="01972-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="01972-114">Element Information</span></span>



| <span data-ttu-id="01972-115">Nom</span><span class="sxs-lookup"><span data-stu-id="01972-115">Name</span></span>                       |                                                                                |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="01972-116">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="01972-116">Element Type</span></span> <br/>   | <span data-ttu-id="01972-117">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="01972-117">Feature</span></span><br/>                                                             |
| <span data-ttu-id="01972-118">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="01972-118">Scoping Prefix</span></span> <br/> | <span data-ttu-id="01972-119">Travail</span><span class="sxs-lookup"><span data-stu-id="01972-119">Job</span></span><br/>                                                                 |
| <span data-ttu-id="01972-120">Notes</span><span class="sxs-lookup"><span data-stu-id="01972-120">Notes</span></span> <br/>          | <span data-ttu-id="01972-121">Haut, bas, gauche et droite sont relatifs à PageImageableSize</span><span class="sxs-lookup"><span data-stu-id="01972-121">Top, Bottom, Left, and Right are relative to the PageImageableSize</span></span> <br/> |



 

## <a name="structural-content"></a><span data-ttu-id="01972-122">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="01972-122">Structural Content</span></span>

<span data-ttu-id="01972-123">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="01972-123">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:Feature name="psk:JobStapleAllDocuments">
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

## <a name="structure-variables"></a><span data-ttu-id="01972-124">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="01972-124">Structure Variables</span></span>

<span data-ttu-id="01972-125">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="01972-125">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="01972-126">Nom</span><span class="sxs-lookup"><span data-stu-id="01972-126">Name</span></span>                               | <span data-ttu-id="01972-127">Type de données</span><span class="sxs-lookup"><span data-stu-id="01972-127">Data type</span></span>          | <span data-ttu-id="01972-128">Unité</span><span class="sxs-lookup"><span data-stu-id="01972-128">Unit</span></span>                       | <span data-ttu-id="01972-129">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="01972-129">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="01972-130">Résumé</span><span class="sxs-lookup"><span data-stu-id="01972-130">Summary</span></span>                                                                                                                                               |
|------------------------------------|--------------------|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01972-131">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="01972-131">\_OptionName\_</span></span><br/>          | <span data-ttu-id="01972-132">string</span><span class="sxs-lookup"><span data-stu-id="01972-132">string</span></span><br/>  | <span data-ttu-id="01972-133">Caractères</span><span class="sxs-lookup"><span data-stu-id="01972-133">Characters</span></span><br/>      | <span data-ttu-id="01972-134">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="01972-134">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="01972-135">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="01972-135">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="01972-136">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="01972-136">The name of the option.</span></span><br/>                                                                                                                    |
| <span data-ttu-id="01972-137">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="01972-137">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="01972-138">string</span><span class="sxs-lookup"><span data-stu-id="01972-138">string</span></span><br/>  | <span data-ttu-id="01972-139">n/a</span><span class="sxs-lookup"><span data-stu-id="01972-139">n/a</span></span><br/>             | <span data-ttu-id="01972-140">True, False.</span><span class="sxs-lookup"><span data-stu-id="01972-140">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="01972-141">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="01972-141">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                          |
| <span data-ttu-id="01972-142">\_AngleValue\_</span><span class="sxs-lookup"><span data-stu-id="01972-142">\_AngleValue\_</span></span><br/>          | <span data-ttu-id="01972-143">entier</span><span class="sxs-lookup"><span data-stu-id="01972-143">integer</span></span><br/> | <span data-ttu-id="01972-144">degrés</span><span class="sxs-lookup"><span data-stu-id="01972-144">degrees</span></span><br/>         | <span data-ttu-id="01972-145">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="01972-145">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="01972-146">Spécifie l’angle de l’agrafage par rapport à la largeur du PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="01972-146">Specifies the staple angle, relative to the width of the PageImageableSize.</span></span> <span data-ttu-id="01972-147">L’angle de l’agrafage est mesuré dans un sens dans le sens inverse des aiguilles d’une montre.</span><span class="sxs-lookup"><span data-stu-id="01972-147">The staple angle is measured in a counter-clockwise direction.</span></span><br/> |
| <span data-ttu-id="01972-148">\_SheetCapacityValue\_</span><span class="sxs-lookup"><span data-stu-id="01972-148">\_SheetCapacityValue\_</span></span><br/>  | <span data-ttu-id="01972-149">entier</span><span class="sxs-lookup"><span data-stu-id="01972-149">integer</span></span><br/> | <span data-ttu-id="01972-150">feuilles de média</span><span class="sxs-lookup"><span data-stu-id="01972-150">sheets of media</span></span><br/> | <span data-ttu-id="01972-151">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="01972-151">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="01972-152">Spécifie le nombre de feuilles prises en charge par l’option d’agrafage pour le MediaType actuellement sélectionné.</span><span class="sxs-lookup"><span data-stu-id="01972-152">Specifies number of sheets supported by the stapling option for the currently selected MediaType.</span></span><br/>                                          |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="01972-153">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="01972-153">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="01972-154">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="01972-154">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="01972-155">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="01972-155">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobStapleAllDocuments">
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
  <psf:Option name="psk:None">
    <psf:ScoredProperty name="psk:Angle">
      <psf:Value xsi:type="xs:integer">0</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:SheetCapacity" >
      <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
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

## <a name="related-topics"></a><span data-ttu-id="01972-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01972-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01972-157">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="01972-157">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




