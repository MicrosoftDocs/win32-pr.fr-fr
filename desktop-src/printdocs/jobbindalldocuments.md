---
description: En savoir plus sur l’élément JobBindAllDocuments, qui décrit la méthode de liaison. Tous les documents du travail sont liés ensemble.
ms.assetid: f21199e2-2220-40c4-9429-72aa2a34a5f2
title: JobBindAllDocuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5abff455756b2abc1d84bf2cff470fa49c93278
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409082"
---
# <a name="jobbindalldocuments"></a><span data-ttu-id="cb980-104">JobBindAllDocuments</span><span class="sxs-lookup"><span data-stu-id="cb980-104">JobBindAllDocuments</span></span>

<span data-ttu-id="cb980-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="cb980-105">This topic is not current.</span></span> <span data-ttu-id="cb980-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="cb980-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="cb980-107">Décrit la méthode de liaison.</span><span class="sxs-lookup"><span data-stu-id="cb980-107">Describes the method of binding.</span></span> <span data-ttu-id="cb980-108">Tous les documents du travail sont liés ensemble.</span><span class="sxs-lookup"><span data-stu-id="cb980-108">All documents in the job are bound together.</span></span> <span data-ttu-id="cb980-109">JobBindAllDocuments et DocumentBinding s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="cb980-109">JobBindAllDocuments and DocumentBinding are mutually exclusive.</span></span> <span data-ttu-id="cb980-110">Il revient au pilote de déterminer la gestion des contraintes entre ces mots clés.</span><span class="sxs-lookup"><span data-stu-id="cb980-110">It is up to the driver to determine constraint handling between these keywords.</span></span>

-   [<span data-ttu-id="cb980-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="cb980-111">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="cb980-112">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="cb980-112">Structural Content</span></span>](#structural-content)
-   [<span data-ttu-id="cb980-113">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="cb980-113">Extensible Markup Language (XML) Content</span></span>](#extensible-markup-language-xml-content)

## <a name="element-information"></a><span data-ttu-id="cb980-114">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="cb980-114">Element Information</span></span>



| <span data-ttu-id="cb980-115">Nom</span><span class="sxs-lookup"><span data-stu-id="cb980-115">Name</span></span> | <span data-ttu-id="cb980-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb980-116">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="cb980-117">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="cb980-117">Element Type</span></span> <br/>   | <span data-ttu-id="cb980-118">Fonctionnalité</span><span class="sxs-lookup"><span data-stu-id="cb980-118">Feature</span></span><br/>                                                             |
| <span data-ttu-id="cb980-119">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="cb980-119">Scoping Prefix</span></span> <br/> | <span data-ttu-id="cb980-120">Travail</span><span class="sxs-lookup"><span data-stu-id="cb980-120">Job</span></span><br/>                                                                 |
| <span data-ttu-id="cb980-121">Notes</span><span class="sxs-lookup"><span data-stu-id="cb980-121">Notes</span></span> <br/>          | <span data-ttu-id="cb980-122">Haut, bas, gauche et droite sont relatifs à PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="cb980-122">Top, Bottom, Left, and Right are relative to the PageImageableSize.</span></span><br/> |



 

## <a name="structural-content"></a><span data-ttu-id="cb980-123">Contenu structurel</span><span class="sxs-lookup"><span data-stu-id="cb980-123">Structural Content</span></span>

<span data-ttu-id="cb980-124">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="cb980-124">The XML structure of this element is:</span></span>

``` syntax
<psf:Feature name="psk:JobBindAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option name="psk:_OptionName_">
    <psf:Property name="psf:IdentityOption">
      <psf:Value xsi:type="xs:string">_IdentityOptionValue_</psf:Value>
    </psf:Property>
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:Value xsi:type="xs:integer">_BindingGutterValue_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option>
</psf:Feature>
```

## <a name="structure-variables"></a><span data-ttu-id="cb980-125">Variables de structure</span><span class="sxs-lookup"><span data-stu-id="cb980-125">Structure Variables</span></span>

<span data-ttu-id="cb980-126">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="cb980-126">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="cb980-127">Nom</span><span class="sxs-lookup"><span data-stu-id="cb980-127">Name</span></span>                               | <span data-ttu-id="cb980-128">Type de données</span><span class="sxs-lookup"><span data-stu-id="cb980-128">Data type</span></span>          | <span data-ttu-id="cb980-129">Unité</span><span class="sxs-lookup"><span data-stu-id="cb980-129">Unit</span></span>                  | <span data-ttu-id="cb980-130">Valeurs prises en charge</span><span class="sxs-lookup"><span data-stu-id="cb980-130">Supported values</span></span>                                                                                                                                                                      | <span data-ttu-id="cb980-131">Résumé</span><span class="sxs-lookup"><span data-stu-id="cb980-131">Summary</span></span>                                                                                                                                                                |
|------------------------------------|--------------------|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb980-132">\_OptionName\_</span><span class="sxs-lookup"><span data-stu-id="cb980-132">\_OptionName\_</span></span><br/>          | <span data-ttu-id="cb980-133">string</span><span class="sxs-lookup"><span data-stu-id="cb980-133">string</span></span><br/>  | <span data-ttu-id="cb980-134">caractères</span><span class="sxs-lookup"><span data-stu-id="cb980-134">characters</span></span><br/> | <span data-ttu-id="cb980-135">Nom complet valide tel que défini par les [espaces de noms dans XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span><span class="sxs-lookup"><span data-stu-id="cb980-135">Valid fully qualified name as defined by [Namespaces in XML](https://www.w3.org/TR/1999/REC-xml-names-19990114/).</span></span> <span data-ttu-id="cb980-136">Si aucun espace de noms n’est spécifié, l’espace de noms par défaut est utilisé.</span><span class="sxs-lookup"><span data-stu-id="cb980-136">If no namespace is specified, default namespace is assumed.</span></span><br/> | <span data-ttu-id="cb980-137">Nom de l'option.</span><span class="sxs-lookup"><span data-stu-id="cb980-137">The name of the option.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="cb980-138">\_IdentityOptionValue\_</span><span class="sxs-lookup"><span data-stu-id="cb980-138">\_IdentityOptionValue\_</span></span><br/> | <span data-ttu-id="cb980-139">string</span><span class="sxs-lookup"><span data-stu-id="cb980-139">string</span></span><br/>  | <span data-ttu-id="cb980-140">n/a</span><span class="sxs-lookup"><span data-stu-id="cb980-140">n/a</span></span><br/>        | <span data-ttu-id="cb980-141">True, False.</span><span class="sxs-lookup"><span data-stu-id="cb980-141">True, False.</span></span><br/>                                                                                                                                                               | <span data-ttu-id="cb980-142">Définit une option qui, lorsqu’elle est sélectionnée, désactive cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="cb980-142">Defines an Option which when selected would disable this feature.</span></span><br/>                                                                                           |
| <span data-ttu-id="cb980-143">\_BindingGutterValue\_</span><span class="sxs-lookup"><span data-stu-id="cb980-143">\_BindingGutterValue\_</span></span><br/>  | <span data-ttu-id="cb980-144">entier</span><span class="sxs-lookup"><span data-stu-id="cb980-144">integer</span></span><br/> | <span data-ttu-id="cb980-145">microns</span><span class="sxs-lookup"><span data-stu-id="cb980-145">microns</span></span><br/>    | <span data-ttu-id="cb980-146">Supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="cb980-146">Greater than 0.</span></span><br/>                                                                                                                                                            | <span data-ttu-id="cb980-147">Définit la marge de liaison minimale pour la liaison de finition spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cb980-147">Defines minimum binding gutter for the specified finishing binding.</span></span> <span data-ttu-id="cb980-148">La reliure est mesurée en microns par rapport au bord de la dimension de support physique.</span><span class="sxs-lookup"><span data-stu-id="cb980-148">The gutter is measured in microns relative to the edge of the physical media dimension.</span></span><br/> |



 

## <a name="extensible-markup-language-xml-content"></a><span data-ttu-id="cb980-149">Contenu Extensible Markup Language (XML)</span><span class="sxs-lookup"><span data-stu-id="cb980-149">Extensible Markup Language (XML) Content</span></span>

<span data-ttu-id="cb980-150">Les mots clés de schéma d’impression publics sont définis dans l' https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords espace de noms.</span><span class="sxs-lookup"><span data-stu-id="cb980-150">The public Print Schema keywords are defined in the https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords namespace.</span></span> <span data-ttu-id="cb980-151">Le contenu de la Extensible Markup Language publique (XML) pour ce mot clé est défini ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="cb980-151">The public Extensible Markup Language (XML) content for this keyword is defined below:</span></span>

``` syntax
<psf:Feature name="psk:JobBindAllDocuments">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <!-- Specifies bale binding. -->
  <psf:Option name="psk:Bale">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the bottom edge. -->
  <psf:Option name="psk:BindBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the left edge. -->
  <psf:Option name="psk:BindLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the right edge. -->
  <psf:Option name="psk:BindRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies binding along the top edge. -->
  <psf:Option name="psk:BindTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies booklet binding. -->
  <psf:Option name="psk:Booklet" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the bottom edge. -->
  <psf:Option name="psk:EdgeStitchBottom">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the left edge. -->
  <psf:Option name="psk:EdgeStitchLeft">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the right edge. -->
  <psf:Option name="psk:EdgeStitchRight">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies edge stitching along the top edge. -->
  <psf:Option name="psk:EdgeStitchTop">
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies a folded binding. -->
  <psf:Option name="psk:Fold" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies jog offset binding. -->
  <psf:Option name="psk:JogOffset" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies trimming binding. -->
  <psf:Option name="psk:Trim" />
    <psf:ScoredProperty name="psk:BindingGutter">
      <psf:ParameterRef name="psk:JobBindAllDocumentsGutter" />
    </psf:ScoredProperty>
  </psf:Option>
  <!-- Specifies no binding. -->
  <psf:Option name="psk:None" />
</psf:Feature>
```

## <a name="related-topics"></a><span data-ttu-id="cb980-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cb980-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb980-153">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="cb980-153">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




