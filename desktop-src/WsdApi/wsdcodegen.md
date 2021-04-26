---
description: Est l’élément racine d’un fichier de script XML du générateur de code WSDAPI.
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: élément wsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9861617854e0e75575f2993717f5b2a86515fb0f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994676"
---
# <a name="wsdcodegen-element"></a><span data-ttu-id="51fb1-103">élément wsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="51fb1-103">wsdCodeGen element</span></span>

<span data-ttu-id="51fb1-104">Est l’élément racine d’un fichier de script XML du générateur de code WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="51fb1-104">Is the root element of an WSDAPI code generator XML script file.</span></span>

## <a name="usage"></a><span data-ttu-id="51fb1-105">Usage</span><span class="sxs-lookup"><span data-stu-id="51fb1-105">Usage</span></span>

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a><span data-ttu-id="51fb1-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="51fb1-106">Attributes</span></span>



| <span data-ttu-id="51fb1-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="51fb1-107">Attribute</span></span>                        | <span data-ttu-id="51fb1-108">Type</span><span class="sxs-lookup"><span data-stu-id="51fb1-108">Type</span></span>                             | <span data-ttu-id="51fb1-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="51fb1-109">Required</span></span>       | <span data-ttu-id="51fb1-110">Description</span><span class="sxs-lookup"><span data-stu-id="51fb1-110">Description</span></span>                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="51fb1-111">**ConfigFileVersion**</span><span class="sxs-lookup"><span data-stu-id="51fb1-111">**ConfigFileVersion**</span></span><br/> | <span data-ttu-id="51fb1-112">Toute chaîne de caractères.</span><span class="sxs-lookup"><span data-stu-id="51fb1-112">Any character string.</span></span><br/> | <span data-ttu-id="51fb1-113">Oui</span><span class="sxs-lookup"><span data-stu-id="51fb1-113">Yes</span></span><br/> | <span data-ttu-id="51fb1-114">Version du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="51fb1-114">The version of the configuration file.</span></span> <span data-ttu-id="51fb1-115">La seule valeur valide est « 1,0 ».</span><span class="sxs-lookup"><span data-stu-id="51fb1-115">The only valid value is "1.0".</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="51fb1-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="51fb1-116">Child elements</span></span>



| <span data-ttu-id="51fb1-117">Élément</span><span class="sxs-lookup"><span data-stu-id="51fb1-117">Element</span></span>                                                         | <span data-ttu-id="51fb1-118">Description</span><span class="sxs-lookup"><span data-stu-id="51fb1-118">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51fb1-119">**autostatique**</span><span class="sxs-lookup"><span data-stu-id="51fb1-119">**autoStatic**</span></span>](autostatic.md)<br/>                     | <span data-ttu-id="51fb1-120">Indique si WsdCodeGen doit essayer d’indicateur automatique de certains champs générés comme statiques.</span><span class="sxs-lookup"><span data-stu-id="51fb1-120">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="51fb1-121">Cette option est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="51fb1-121">This is enabled by default.</span></span><br/> <br/>                                                                 |
| [<span data-ttu-id="51fb1-122">**txt**</span><span class="sxs-lookup"><span data-stu-id="51fb1-122">**file**</span></span>](file.md)<br/>                                 | <span data-ttu-id="51fb1-123">Indique au générateur de code de générer un fichier.</span><span class="sxs-lookup"><span data-stu-id="51fb1-123">Directs the code generator to generate a file.</span></span><br/> <br/>                                                                                                                                                       |
| [<span data-ttu-id="51fb1-124">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="51fb1-124">**hostMetadata**</span></span>](hostmetadata.md)<br/>                 | <span data-ttu-id="51fb1-125">Métadonnées d’hébergement pour l’appareil à implémenter.</span><span class="sxs-lookup"><span data-stu-id="51fb1-125">The hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="51fb1-126">Cet élément est utilisé uniquement pour les implémentations d’appareils (hôtes).</span><span class="sxs-lookup"><span data-stu-id="51fb1-126">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                                 |
| [<span data-ttu-id="51fb1-127">**layerNumber**</span><span class="sxs-lookup"><span data-stu-id="51fb1-127">**layerNumber**</span></span>](layernumber.md)<br/>                   | <span data-ttu-id="51fb1-128">Numéro de la couche de code à générer.</span><span class="sxs-lookup"><span data-stu-id="51fb1-128">The number of the code layer to be generated.</span></span> <span data-ttu-id="51fb1-129">Les numéros de couche sont utilisés dans les tables du runtime pour distinguer une couche de code d’une autre.</span><span class="sxs-lookup"><span data-stu-id="51fb1-129">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="51fb1-130">WSDAPI utilise le code généré qui a un numéro de couche 0.</span><span class="sxs-lookup"><span data-stu-id="51fb1-130">WSDAPI itself uses generated code that has a layer number of 0.</span></span><br/> <br/> |
| [<span data-ttu-id="51fb1-131">**layerPrefix**</span><span class="sxs-lookup"><span data-stu-id="51fb1-131">**layerPrefix**</span></span>](layerprefix.md)<br/>                   | <span data-ttu-id="51fb1-132">Préfixe à utiliser dans le code généré pour garantir l’unicité des symboles générés.</span><span class="sxs-lookup"><span data-stu-id="51fb1-132">The prefix to use in the generated code to assure uniqueness of generated symbols.</span></span> <span data-ttu-id="51fb1-133">WSDAPI utilise le préfixe « WSD ».</span><span class="sxs-lookup"><span data-stu-id="51fb1-133">WSDAPI uses the prefix "WSD".</span></span><br/> <br/>                                                                                     |
| [<span data-ttu-id="51fb1-134">**macrovirus**</span><span class="sxs-lookup"><span data-stu-id="51fb1-134">**macro**</span></span>](macro.md)<br/>                               | <span data-ttu-id="51fb1-135">Définit le texte ou CDATA à réutiliser par l’élément [**include**](include.md) .</span><span class="sxs-lookup"><span data-stu-id="51fb1-135">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span><br/> <br/>                                                                                                                        |
| [<span data-ttu-id="51fb1-136">**Joint**</span><span class="sxs-lookup"><span data-stu-id="51fb1-136">**nameSpace**</span></span>](namespace.md)<br/>                       | <span data-ttu-id="51fb1-137">Décrit un espace de noms à utiliser pour la génération de code.</span><span class="sxs-lookup"><span data-stu-id="51fb1-137">Describes a namespace to be used for code generation.</span></span><br/> <br/>                                                                                                                                                |
| [<span data-ttu-id="51fb1-138">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="51fb1-138">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="51fb1-139">Décrit l’hôte et les métadonnées hébergées pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="51fb1-139">Describes the host and hosted metadata for the device.</span></span><br/> <br/>                                                                                                                                               |
| [<span data-ttu-id="51fb1-140">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="51fb1-140">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/>       | <span data-ttu-id="51fb1-141">Métadonnées du fabricant et du modèle pour l’appareil à implémenter.</span><span class="sxs-lookup"><span data-stu-id="51fb1-141">The manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="51fb1-142">Cet élément est utilisé uniquement pour les implémentations d’appareils (hôtes).</span><span class="sxs-lookup"><span data-stu-id="51fb1-142">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                  |
| [<span data-ttu-id="51fb1-143">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="51fb1-143">**wsdl**</span></span>](wsdl.md)<br/>                                 | <span data-ttu-id="51fb1-144">Spécifie un fichier WSDL à traiter pour les informations de contrat.</span><span class="sxs-lookup"><span data-stu-id="51fb1-144">Specifies a WSDL file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |
| [<span data-ttu-id="51fb1-145">**XSD**</span><span class="sxs-lookup"><span data-stu-id="51fb1-145">**xsd**</span></span>](xsd.md)<br/>                                   | <span data-ttu-id="51fb1-146">Spécifie un fichier XSD à traiter pour les informations de contrat.</span><span class="sxs-lookup"><span data-stu-id="51fb1-146">Specifies an XSD file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a><span data-ttu-id="51fb1-147">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="51fb1-147">Child element sequence</span></span>

``` syntax
(
  layerNumber?, 
  layerPrefix?, 
  autoStatic?, 
  hostMetadata?, 
  thisModelMetadata?, 
  nameSpace*, 
  wsdl*, 
  xsd*, 
  file*, 
  macro*, 
  relationshipMetadata*
)
```

## <a name="parent-elements"></a><span data-ttu-id="51fb1-148">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="51fb1-148">Parent elements</span></span>

<span data-ttu-id="51fb1-149">Il n’y a pas d’éléments parents.</span><span class="sxs-lookup"><span data-stu-id="51fb1-149">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="51fb1-150">Remarques</span><span class="sxs-lookup"><span data-stu-id="51fb1-150">Remarks</span></span>

<span data-ttu-id="51fb1-151">En général, les éléments de [**fichier**](file.md) doivent se produire en dernier, car ils génèrent du code qui utilise des données spécifiées par les autres éléments.</span><span class="sxs-lookup"><span data-stu-id="51fb1-151">In general, [**file**](file.md) elements should occur last because they generate code which uses data specified by the other elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="51fb1-152">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="51fb1-152">Element information</span></span>



| <span data-ttu-id="51fb1-153">Étiquette</span><span class="sxs-lookup"><span data-stu-id="51fb1-153">Label</span></span> | <span data-ttu-id="51fb1-154">Value</span><span class="sxs-lookup"><span data-stu-id="51fb1-154">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="51fb1-155">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51fb1-155">Minimum supported system</span></span><br/> | <span data-ttu-id="51fb1-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51fb1-156">Windows Vista</span></span> |
| <span data-ttu-id="51fb1-157">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="51fb1-157">Can be empty</span></span>                        | <span data-ttu-id="51fb1-158">Oui</span><span class="sxs-lookup"><span data-stu-id="51fb1-158">Yes</span></span>           |



 

 




