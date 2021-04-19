---
description: Est l’élément racine d’un fichier de script XML du générateur de code WSDAPI.
ms.assetid: 3d40172b-6ba1-4e42-9a1a-519c8e88c2b1
title: élément wsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656f2273926dc3420ec84d6b9f24759f8e3587e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519606"
---
# <a name="wsdcodegen-element"></a><span data-ttu-id="5b3d3-103">élément wsdCodeGen</span><span class="sxs-lookup"><span data-stu-id="5b3d3-103">wsdCodeGen element</span></span>

<span data-ttu-id="5b3d3-104">Est l’élément racine d’un fichier de script XML du générateur de code WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-104">Is the root element of an WSDAPI code generator XML script file.</span></span>

## <a name="usage"></a><span data-ttu-id="5b3d3-105">Utilisation</span><span class="sxs-lookup"><span data-stu-id="5b3d3-105">Usage</span></span>

``` syntax
<wsdCodeGen
  ConfigFileVersion = "Any character string.">
  child elements
</wsdCodeGen>
```

## <a name="attributes"></a><span data-ttu-id="5b3d3-106">Attributs</span><span class="sxs-lookup"><span data-stu-id="5b3d3-106">Attributes</span></span>



| <span data-ttu-id="5b3d3-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="5b3d3-107">Attribute</span></span>                        | <span data-ttu-id="5b3d3-108">Type</span><span class="sxs-lookup"><span data-stu-id="5b3d3-108">Type</span></span>                             | <span data-ttu-id="5b3d3-109">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5b3d3-109">Required</span></span>       | <span data-ttu-id="5b3d3-110">Description</span><span class="sxs-lookup"><span data-stu-id="5b3d3-110">Description</span></span>                                                                                  |
|----------------------------------|----------------------------------|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b3d3-111">**ConfigFileVersion**</span><span class="sxs-lookup"><span data-stu-id="5b3d3-111">**ConfigFileVersion**</span></span><br/> | <span data-ttu-id="5b3d3-112">Toute chaîne de caractères.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-112">Any character string.</span></span><br/> | <span data-ttu-id="5b3d3-113">Oui</span><span class="sxs-lookup"><span data-stu-id="5b3d3-113">Yes</span></span><br/> | <span data-ttu-id="5b3d3-114">Version du fichier de configuration.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-114">The version of the configuration file.</span></span> <span data-ttu-id="5b3d3-115">La seule valeur valide est « 1,0 ».</span><span class="sxs-lookup"><span data-stu-id="5b3d3-115">The only valid value is "1.0".</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="5b3d3-116">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5b3d3-116">Child elements</span></span>



| <span data-ttu-id="5b3d3-117">Élément</span><span class="sxs-lookup"><span data-stu-id="5b3d3-117">Element</span></span>                                                         | <span data-ttu-id="5b3d3-118">Description</span><span class="sxs-lookup"><span data-stu-id="5b3d3-118">Description</span></span>                                                                                                                                                                                                                 |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b3d3-119">**autostatique**</span><span class="sxs-lookup"><span data-stu-id="5b3d3-119">**autoStatic**</span></span>](autostatic.md)<br/>                     | <span data-ttu-id="5b3d3-120">Indique si WsdCodeGen doit essayer d’indicateur automatique de certains champs générés comme statiques.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-120">Indicates whether or not WsdCodeGen should try to automatically flag certain generated fields as static.</span></span> <span data-ttu-id="5b3d3-121">Cette option est activée par défaut.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-121">This is enabled by default.</span></span><br/> <br/>                                                                 |
| [<span data-ttu-id="5b3d3-122">**fichier**</span><span class="sxs-lookup"><span data-stu-id="5b3d3-122">**file**</span></span>](file.md)<br/>                                 | <span data-ttu-id="5b3d3-123">Indique au générateur de code de générer un fichier.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-123">Directs the code generator to generate a file.</span></span><br/> <br/>                                                                                                                                                       |
| [<span data-ttu-id="5b3d3-124">**hostMetadata**</span><span class="sxs-lookup"><span data-stu-id="5b3d3-124">**hostMetadata**</span></span>](hostmetadata.md)<br/>                 | <span data-ttu-id="5b3d3-125">Métadonnées d’hébergement pour l’appareil à implémenter.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-125">The hosting metadata for the device to be implemented.</span></span> <span data-ttu-id="5b3d3-126">Cet élément est utilisé uniquement pour les implémentations d’appareils (hôtes).</span><span class="sxs-lookup"><span data-stu-id="5b3d3-126">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                                 |
| [<span data-ttu-id="5b3d3-127">**layerNumber**</span><span class="sxs-lookup"><span data-stu-id="5b3d3-127">**layerNumber**</span></span>](layernumber.md)<br/>                   | <span data-ttu-id="5b3d3-128">Numéro de la couche de code à générer.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-128">The number of the code layer to be generated.</span></span> <span data-ttu-id="5b3d3-129">Les numéros de couche sont utilisés dans les tables du runtime pour distinguer une couche de code d’une autre.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-129">Layer numbers are used in runtime tables to distinguish one layer of code for another.</span></span> <span data-ttu-id="5b3d3-130">WSDAPI utilise le code généré qui a un numéro de couche 0.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-130">WSDAPI itself uses generated code that has a layer number of 0.</span></span><br/> <br/> |
| [<span data-ttu-id="5b3d3-131">**layerPrefix**</span><span class="sxs-lookup"><span data-stu-id="5b3d3-131">**layerPrefix**</span></span>](layerprefix.md)<br/>                   | <span data-ttu-id="5b3d3-132">Préfixe à utiliser dans le code généré pour garantir l’unicité des symboles générés.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-132">The prefix to use in the generated code to assure uniqueness of generated symbols.</span></span> <span data-ttu-id="5b3d3-133">WSDAPI utilise le préfixe « WSD ».</span><span class="sxs-lookup"><span data-stu-id="5b3d3-133">WSDAPI uses the prefix "WSD".</span></span><br/> <br/>                                                                                     |
| [<span data-ttu-id="5b3d3-134">**macrovirus**</span><span class="sxs-lookup"><span data-stu-id="5b3d3-134">**macro**</span></span>](macro.md)<br/>                               | <span data-ttu-id="5b3d3-135">Définit le texte ou CDATA à réutiliser par l’élément [**include**](include.md) .</span><span class="sxs-lookup"><span data-stu-id="5b3d3-135">Defines text or CDATA to be reused by the [**include**](include.md) element.</span></span><br/> <br/>                                                                                                                        |
| [<span data-ttu-id="5b3d3-136">**Joint**</span><span class="sxs-lookup"><span data-stu-id="5b3d3-136">**nameSpace**</span></span>](namespace.md)<br/>                       | <span data-ttu-id="5b3d3-137">Décrit un espace de noms à utiliser pour la génération de code.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-137">Describes a namespace to be used for code generation.</span></span><br/> <br/>                                                                                                                                                |
| [<span data-ttu-id="5b3d3-138">**relationshipMetadata**</span><span class="sxs-lookup"><span data-stu-id="5b3d3-138">**relationshipMetadata**</span></span>](relationshipmetadata.md)<br/> | <span data-ttu-id="5b3d3-139">Décrit l’hôte et les métadonnées hébergées pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-139">Describes the host and hosted metadata for the device.</span></span><br/> <br/>                                                                                                                                               |
| [<span data-ttu-id="5b3d3-140">**thisModelMetadata**</span><span class="sxs-lookup"><span data-stu-id="5b3d3-140">**thisModelMetadata**</span></span>](thismodelmetadata.md)<br/>       | <span data-ttu-id="5b3d3-141">Métadonnées du fabricant et du modèle pour l’appareil à implémenter.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-141">The manufacturer and model metadata for the device to be implemented.</span></span> <span data-ttu-id="5b3d3-142">Cet élément est utilisé uniquement pour les implémentations d’appareils (hôtes).</span><span class="sxs-lookup"><span data-stu-id="5b3d3-142">This element is used for device implementations (hosts) only.</span></span><br/> <br/>                                                                  |
| [<span data-ttu-id="5b3d3-143">**WSDL**</span><span class="sxs-lookup"><span data-stu-id="5b3d3-143">**wsdl**</span></span>](wsdl.md)<br/>                                 | <span data-ttu-id="5b3d3-144">Spécifie un fichier WSDL à traiter pour les informations de contrat.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-144">Specifies a WSDL file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |
| [<span data-ttu-id="5b3d3-145">**XSD**</span><span class="sxs-lookup"><span data-stu-id="5b3d3-145">**xsd**</span></span>](xsd.md)<br/>                                   | <span data-ttu-id="5b3d3-146">Spécifie un fichier XSD à traiter pour les informations de contrat.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-146">Specifies an XSD file to process for contract information.</span></span><br/> <br/>                                                                                                                                           |



### <a name="child-element-sequence"></a><span data-ttu-id="5b3d3-147">Séquence d’éléments enfants</span><span class="sxs-lookup"><span data-stu-id="5b3d3-147">Child element sequence</span></span>

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

## <a name="parent-elements"></a><span data-ttu-id="5b3d3-148">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="5b3d3-148">Parent elements</span></span>

<span data-ttu-id="5b3d3-149">Il n’y a pas d’éléments parents.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-149">There are no parent elements.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b3d3-150">Notes</span><span class="sxs-lookup"><span data-stu-id="5b3d3-150">Remarks</span></span>

<span data-ttu-id="5b3d3-151">En général, les éléments de [**fichier**](file.md) doivent se produire en dernier, car ils génèrent du code qui utilise des données spécifiées par les autres éléments.</span><span class="sxs-lookup"><span data-stu-id="5b3d3-151">In general, [**file**](file.md) elements should occur last because they generate code which uses data specified by the other elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="5b3d3-152">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="5b3d3-152">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="5b3d3-153">Système minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b3d3-153">Minimum supported system</span></span><br/> | <span data-ttu-id="5b3d3-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b3d3-154">Windows Vista</span></span> |
| <span data-ttu-id="5b3d3-155">Peut être vide</span><span class="sxs-lookup"><span data-stu-id="5b3d3-155">Can be empty</span></span>                        | <span data-ttu-id="5b3d3-156">Oui</span><span class="sxs-lookup"><span data-stu-id="5b3d3-156">Yes</span></span>           |



 

 




