---
description: Ces éléments composent le schéma XML utilisé dans le manifeste de transfert de l’Assistant de publication Web et de commandes d’impression en ligne.
title: Schéma de manifeste de transfert
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 488b6fc9-ff85-4860-9cd5-61d5de7e15e8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d0b57f1eb81169674c6c8d36e66c8a3cd21cf0e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991693"
---
# <a name="transfer-manifest-schema"></a><span data-ttu-id="dea77-103">Schéma de manifeste de transfert</span><span class="sxs-lookup"><span data-stu-id="dea77-103">Transfer Manifest Schema</span></span>

<span data-ttu-id="dea77-104">Ces éléments composent le schéma XML utilisé dans le manifeste de transfert de l’Assistant de publication Web et de commandes d’impression en ligne.</span><span class="sxs-lookup"><span data-stu-id="dea77-104">These elements make up the XML schema used in the Web Publishing and Online Print Ordering wizards' transfer manifest.</span></span>

<span data-ttu-id="dea77-105">Les éléments suivants sont définis pour le manifeste de transfert.</span><span class="sxs-lookup"><span data-stu-id="dea77-105">The following elements are defined for the transfer manifest.</span></span>

-   [<span data-ttu-id="dea77-106">cancelledpage</span><span class="sxs-lookup"><span data-stu-id="dea77-106">cancelledpage</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-107">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-108">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-108">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-110">failurepage</span><span class="sxs-lookup"><span data-stu-id="dea77-110">failurepage</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-111">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-112">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-112">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-113">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-114">passion</span><span class="sxs-lookup"><span data-stu-id="dea77-114">favorite</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-115">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-115">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-116">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-116">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-117">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-117">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-118">file</span><span class="sxs-lookup"><span data-stu-id="dea77-118">file</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-119">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-119">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-120">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-120">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-121">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-121">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-122">filelist</span><span class="sxs-lookup"><span data-stu-id="dea77-122">filelist</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-123">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-123">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-124">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-124">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-125">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-125">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-126">Répertoire</span><span class="sxs-lookup"><span data-stu-id="dea77-126">folder</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-127">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-127">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-128">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-129">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-129">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-130">folderlist</span><span class="sxs-lookup"><span data-stu-id="dea77-130">folderlist</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-131">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-131">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-132">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-132">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-133">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-133">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-134">formdata</span><span class="sxs-lookup"><span data-stu-id="dea77-134">formdata</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-135">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-135">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-136">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-136">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-137">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-137">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-138">htmlui</span><span class="sxs-lookup"><span data-stu-id="dea77-138">htmlui</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-139">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-139">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-140">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-140">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-141">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-141">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-142">imageproperty</span><span class="sxs-lookup"><span data-stu-id="dea77-142">imageproperty</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-143">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-143">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-144">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-144">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-145">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-145">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-146">métadonnées</span><span class="sxs-lookup"><span data-stu-id="dea77-146">metadata</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-147">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-147">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-148">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-148">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-149">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-149">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-150">emplacement</span><span class="sxs-lookup"><span data-stu-id="dea77-150">netplace</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-151">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-151">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-152">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-152">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-153">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-153">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-154">Publier</span><span class="sxs-lookup"><span data-stu-id="dea77-154">post</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-155">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-155">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-156">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-156">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-157">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-157">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-158">redimensionner</span><span class="sxs-lookup"><span data-stu-id="dea77-158">resize</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-159">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-159">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-160">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-160">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-161">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-161">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-162">successpage</span><span class="sxs-lookup"><span data-stu-id="dea77-162">successpage</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-163">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-163">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-164">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-164">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-165">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-165">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-166">cible</span><span class="sxs-lookup"><span data-stu-id="dea77-166">target</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-167">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-167">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-168">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-168">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-169">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-169">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-170">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="dea77-170">transfermanifest</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-171">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-171">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-172">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-172">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-173">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-173">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="dea77-174">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="dea77-174">uploadinfo</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-175">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-175">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="dea77-176">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-176">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="dea77-177">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-177">Element Information</span></span>](#element-information)

## <a name="cancelledpage"></a><span data-ttu-id="dea77-178">cancelledpage</span><span class="sxs-lookup"><span data-stu-id="dea77-178">cancelledpage</span></span>

<span data-ttu-id="dea77-179">Spécifie la page HTML côté serveur à afficher avant la fermeture de l’Assistant lorsque l’utilisateur clique sur le bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="dea77-179">Specifies the server-side HTML page to display before the wizard is closed when the user clicks the **Cancel** button.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-180">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-180">Syntax</span></span>


```
<cancelledpage
    href = "string"
>
<!-- child elements -->
</cancelledpage>                  
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-181">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-181">Attributes</span></span>



| <span data-ttu-id="dea77-182">Attribut</span><span class="sxs-lookup"><span data-stu-id="dea77-182">Attribute</span></span> | <span data-ttu-id="dea77-183">Description</span><span class="sxs-lookup"><span data-stu-id="dea77-183">Description</span></span>                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea77-184">href</span><span class="sxs-lookup"><span data-stu-id="dea77-184">href</span></span>      | <span data-ttu-id="dea77-185">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-185">Required.</span></span> <span data-ttu-id="dea77-186">URL de la page HTML côté serveur à afficher lorsque l’utilisateur clique sur le bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="dea77-186">The URL of the server-side HTML page to display when the user clicks the **Cancel** button.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="dea77-187">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-187">Element Information</span></span>



| <span data-ttu-id="dea77-188">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-188">Parent Element</span></span>        | <span data-ttu-id="dea77-189">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-189">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="dea77-190">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="dea77-190">uploadinfo</span></span>](#syntax) | <span data-ttu-id="dea77-191">Aucun</span><span class="sxs-lookup"><span data-stu-id="dea77-191">None</span></span>           |



 

## <a name="failurepage"></a><span data-ttu-id="dea77-192">failurepage</span><span class="sxs-lookup"><span data-stu-id="dea77-192">failurepage</span></span>

<span data-ttu-id="dea77-193">Spécifie la page HTML côté serveur à afficher si le chargement échoue.</span><span class="sxs-lookup"><span data-stu-id="dea77-193">Specifies the server-side HTML page to display if the upload is not successful.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-194">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-194">Syntax</span></span>


```
<failurepage
    href = "string"
>
<!-- child elements -->
</failurepage>                    
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-195">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-195">Attributes</span></span>



| <span data-ttu-id="dea77-196">Attribut</span><span class="sxs-lookup"><span data-stu-id="dea77-196">Attribute</span></span> | <span data-ttu-id="dea77-197">Description</span><span class="sxs-lookup"><span data-stu-id="dea77-197">Description</span></span>                                                                                |
|-----------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea77-198">href</span><span class="sxs-lookup"><span data-stu-id="dea77-198">href</span></span>      | <span data-ttu-id="dea77-199">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-199">Required.</span></span> <span data-ttu-id="dea77-200">URL de la page HTML côté serveur à afficher si le chargement échoue.</span><span class="sxs-lookup"><span data-stu-id="dea77-200">The URL of the server-side HTML page to display if the upload is not successful.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="dea77-201">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-201">Element Information</span></span>



| <span data-ttu-id="dea77-202">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-202">Parent Element</span></span>        | <span data-ttu-id="dea77-203">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-203">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="dea77-204">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="dea77-204">uploadinfo</span></span>](#syntax) | <span data-ttu-id="dea77-205">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dea77-205">None.</span></span> <span data-ttu-id="dea77-206">Le texte est autorisé.</span><span class="sxs-lookup"><span data-stu-id="dea77-206">Text is allowed.</span></span> |



 

## <a name="favorite"></a><span data-ttu-id="dea77-207">passion</span><span class="sxs-lookup"><span data-stu-id="dea77-207">favorite</span></span>

<span data-ttu-id="dea77-208">Indique à l’Assistant de créer une entrée de site Web favori dans le menu **favoris** pour l’URL donnée.</span><span class="sxs-lookup"><span data-stu-id="dea77-208">Instructs the wizard to create a favorite website entry in the **Favorites** menu for the given URL.</span></span> <span data-ttu-id="dea77-209">Si cet élément n’est pas spécifié, l’élément [htmlui](#syntax) est utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="dea77-209">If this element is not specified, then the [htmlui](#syntax) element is used in its place.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-210">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-210">Syntax</span></span>


```
<favorite
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</favorite>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-211">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-211">Attributes</span></span>



| <span data-ttu-id="dea77-212">Attribut</span><span class="sxs-lookup"><span data-stu-id="dea77-212">Attribute</span></span> | <span data-ttu-id="dea77-213">Description</span><span class="sxs-lookup"><span data-stu-id="dea77-213">Description</span></span>                                                            |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="dea77-214">comment</span><span class="sxs-lookup"><span data-stu-id="dea77-214">comment</span></span>   | <span data-ttu-id="dea77-215">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-215">Required.</span></span> <span data-ttu-id="dea77-216">Commentaire associé à l’entrée **favoris** .</span><span class="sxs-lookup"><span data-stu-id="dea77-216">The comment associated with the **Favorites** entry.</span></span>         |
| <span data-ttu-id="dea77-217">href</span><span class="sxs-lookup"><span data-stu-id="dea77-217">href</span></span>      | <span data-ttu-id="dea77-218">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-218">Required.</span></span> <span data-ttu-id="dea77-219">URL de l’entrée **favoris** .</span><span class="sxs-lookup"><span data-stu-id="dea77-219">The URL of the **Favorites** entry.</span></span>                          |
| <span data-ttu-id="dea77-220">name</span><span class="sxs-lookup"><span data-stu-id="dea77-220">name</span></span>      | <span data-ttu-id="dea77-221">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-221">Required.</span></span> <span data-ttu-id="dea77-222">Nom de l’URL qui s’affiche dans le menu **favoris** .</span><span class="sxs-lookup"><span data-stu-id="dea77-222">The name for the URL that appears in the **Favorites** menu.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="dea77-223">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-223">Element Information</span></span>



| <span data-ttu-id="dea77-224">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-224">Parent Element</span></span>        | <span data-ttu-id="dea77-225">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-225">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="dea77-226">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="dea77-226">uploadinfo</span></span>](#syntax) | <span data-ttu-id="dea77-227">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dea77-227">None.</span></span> <span data-ttu-id="dea77-228">Le texte est autorisé.</span><span class="sxs-lookup"><span data-stu-id="dea77-228">Text is allowed.</span></span> |



 

## <a name="file"></a><span data-ttu-id="dea77-229">fichier</span><span class="sxs-lookup"><span data-stu-id="dea77-229">file</span></span>

<span data-ttu-id="dea77-230">Décrit un fichier unique à copier.</span><span class="sxs-lookup"><span data-stu-id="dea77-230">Describes a single file to be copied.</span></span> <span data-ttu-id="dea77-231">Plusieurs éléments de [fichier](#syntax) peuvent être contenus sous un seul nœud [filelist](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="dea77-231">Multiple [file](#syntax) elements may be contained under a single [filelist](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-232">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-232">Syntax</span></span>


```
<file
    contenttype = "string"
    destination = "string"
    extension = "string"
    id = "string"
    size = "string"
    source = "string"
>
<!-- child elements -->
</file>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-233">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-233">Attributes</span></span>



| <span data-ttu-id="dea77-234">Attribut</span><span class="sxs-lookup"><span data-stu-id="dea77-234">Attribute</span></span>   | <span data-ttu-id="dea77-235">Description</span><span class="sxs-lookup"><span data-stu-id="dea77-235">Description</span></span>                                                                                                                                                                  |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea77-236">Indiquez</span><span class="sxs-lookup"><span data-stu-id="dea77-236">contenttype</span></span> | <span data-ttu-id="dea77-237">facultatif.</span><span class="sxs-lookup"><span data-stu-id="dea77-237">Optional.</span></span> <span data-ttu-id="dea77-238">Type MIME du fichier.</span><span class="sxs-lookup"><span data-stu-id="dea77-238">The MIME type of the file.</span></span>                                                                                                                                         |
| <span data-ttu-id="dea77-239">destination</span><span class="sxs-lookup"><span data-stu-id="dea77-239">destination</span></span> | <span data-ttu-id="dea77-240">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-240">Required.</span></span> <span data-ttu-id="dea77-241">Chemin d’accès suggéré pour le fichier une fois qu’il a été téléchargé.</span><span class="sxs-lookup"><span data-stu-id="dea77-241">A suggested path for the file once it is uploaded.</span></span> <span data-ttu-id="dea77-242">Ce chemin d’accès est relatif à l’URL de destination du site de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="dea77-242">This path is relative to the upload site's destination URL.</span></span> <span data-ttu-id="dea77-243">Le site de chargement peut modifier cette valeur si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="dea77-243">The upload site can modify this value as necessary.</span></span> |
| <span data-ttu-id="dea77-244">extension</span><span class="sxs-lookup"><span data-stu-id="dea77-244">extension</span></span>   | <span data-ttu-id="dea77-245">facultatif.</span><span class="sxs-lookup"><span data-stu-id="dea77-245">Optional.</span></span> <span data-ttu-id="dea77-246">Extension de nom de fichier du fichier.</span><span class="sxs-lookup"><span data-stu-id="dea77-246">The file name extension of the file.</span></span>                                                                                                                               |
| <span data-ttu-id="dea77-247">id</span><span class="sxs-lookup"><span data-stu-id="dea77-247">id</span></span>          | <span data-ttu-id="dea77-248">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-248">Required.</span></span> <span data-ttu-id="dea77-249">Index numérique du fichier.</span><span class="sxs-lookup"><span data-stu-id="dea77-249">The numerical index of the file.</span></span>                                                                                                                                   |
| <span data-ttu-id="dea77-250">est</span><span class="sxs-lookup"><span data-stu-id="dea77-250">size</span></span>        | <span data-ttu-id="dea77-251">facultatif.</span><span class="sxs-lookup"><span data-stu-id="dea77-251">Optional.</span></span> <span data-ttu-id="dea77-252">Taille du fichier, en octets.</span><span class="sxs-lookup"><span data-stu-id="dea77-252">The size of the file, in bytes.</span></span>                                                                                                                                    |
| <span data-ttu-id="dea77-253">source</span><span class="sxs-lookup"><span data-stu-id="dea77-253">source</span></span>      | <span data-ttu-id="dea77-254">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-254">Required.</span></span> <span data-ttu-id="dea77-255">Chemin d’accès complet du système de fichiers pour le fichier.</span><span class="sxs-lookup"><span data-stu-id="dea77-255">The full file system path for the file.</span></span>                                                                                                                            |



 

### <a name="element-information"></a><span data-ttu-id="dea77-256">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-256">Element Information</span></span>



| <span data-ttu-id="dea77-257">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-257">Parent Element</span></span>      | <span data-ttu-id="dea77-258">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-258">Child Elements</span></span>                                          |
|---------------------|---------------------------------------------------------|
| [<span data-ttu-id="dea77-259">filelist</span><span class="sxs-lookup"><span data-stu-id="dea77-259">filelist</span></span>](#syntax) | <span data-ttu-id="dea77-260">[métadonnées](#syntax), [publication](#syntax), [redimensionnement](#syntax)</span><span class="sxs-lookup"><span data-stu-id="dea77-260">[metadata](#syntax), [post](#syntax), [resize](#syntax)</span></span> |



 

## <a name="filelist"></a><span data-ttu-id="dea77-261">filelist</span><span class="sxs-lookup"><span data-stu-id="dea77-261">filelist</span></span>

<span data-ttu-id="dea77-262">Conteneur pour les éléments décrivant les fichiers à copier.</span><span class="sxs-lookup"><span data-stu-id="dea77-262">A container for elements describing the files to be copied.</span></span> <span data-ttu-id="dea77-263">Plusieurs éléments [filelist](#syntax) peuvent être contenus sous un seul nœud [transfermanifest](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="dea77-263">Multiple [filelist](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-264">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-264">Syntax</span></span>


```
<filelist
    usesfolders = "1"
>
<!-- child elements -->
</filelist>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-265">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-265">Attributes</span></span>



| <span data-ttu-id="dea77-266">Attribut</span><span class="sxs-lookup"><span data-stu-id="dea77-266">Attribute</span></span>   | <span data-ttu-id="dea77-267">Description</span><span class="sxs-lookup"><span data-stu-id="dea77-267">Description</span></span>      |
|-------------|------------------|
| <span data-ttu-id="dea77-268">usesfolders</span><span class="sxs-lookup"><span data-stu-id="dea77-268">usesfolders</span></span> | <span data-ttu-id="dea77-269">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="dea77-269">Not implemented.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="dea77-270">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-270">Element Information</span></span>



| <span data-ttu-id="dea77-271">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-271">Parent Element</span></span>              | <span data-ttu-id="dea77-272">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-272">Child Elements</span></span>  |
|-----------------------------|-----------------|
| [<span data-ttu-id="dea77-273">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="dea77-273">transfermanifest</span></span>](#syntax) | [<span data-ttu-id="dea77-274">file</span><span class="sxs-lookup"><span data-stu-id="dea77-274">file</span></span>](#syntax) |



 

## <a name="folder"></a><span data-ttu-id="dea77-275">dossier</span><span class="sxs-lookup"><span data-stu-id="dea77-275">folder</span></span>

<span data-ttu-id="dea77-276">Décrit un dossier dans lequel les fichiers sont stockés.</span><span class="sxs-lookup"><span data-stu-id="dea77-276">Describes a folder in which files are stored.</span></span> <span data-ttu-id="dea77-277">Plusieurs éléments de [dossier](#syntax) peuvent être contenus sous un seul nœud [folderlist](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="dea77-277">Multiple [folder](#syntax) elements may be contained under a single [folderlist](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-278">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-278">Syntax</span></span>


```
<folder
    destination = "string"
>
<!-- child elements -->
</folder>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-279">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-279">Attributes</span></span>



| <span data-ttu-id="dea77-280">Attribut</span><span class="sxs-lookup"><span data-stu-id="dea77-280">Attribute</span></span>   | <span data-ttu-id="dea77-281">Description</span><span class="sxs-lookup"><span data-stu-id="dea77-281">Description</span></span>                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea77-282">destination</span><span class="sxs-lookup"><span data-stu-id="dea77-282">destination</span></span> | <span data-ttu-id="dea77-283">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-283">Required.</span></span> <span data-ttu-id="dea77-284">Chemin d’accès suggéré pour le dossier une fois téléchargé.</span><span class="sxs-lookup"><span data-stu-id="dea77-284">A suggested path for the folder once it is uploaded.</span></span> <span data-ttu-id="dea77-285">Ce chemin d’accès est relatif à l’URL de destination du site de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="dea77-285">This path is relative to the upload site's destination URL.</span></span> <span data-ttu-id="dea77-286">Le site de chargement peut modifier cette valeur si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="dea77-286">The upload site can modify this value as necessary.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="dea77-287">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-287">Element Information</span></span>



| <span data-ttu-id="dea77-288">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-288">Parent Element</span></span>        | <span data-ttu-id="dea77-289">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-289">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="dea77-290">folderlist</span><span class="sxs-lookup"><span data-stu-id="dea77-290">folderlist</span></span>](#syntax) | <span data-ttu-id="dea77-291">Aucun</span><span class="sxs-lookup"><span data-stu-id="dea77-291">None</span></span>           |



 

## <a name="folderlist"></a><span data-ttu-id="dea77-292">folderlist</span><span class="sxs-lookup"><span data-stu-id="dea77-292">folderlist</span></span>

<span data-ttu-id="dea77-293">Conteneur pour les éléments décrivant les fichiers à copier.</span><span class="sxs-lookup"><span data-stu-id="dea77-293">A container for elements describing the files to be copied.</span></span> <span data-ttu-id="dea77-294">Plusieurs éléments [folderlist](#syntax) peuvent être contenus sous un seul nœud [transfermanifest](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="dea77-294">Multiple [folderlist](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-295">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-295">Syntax</span></span>


```
<folderlist>
<!-- child elements -->
</folderlist>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-296">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-296">Attributes</span></span>

<span data-ttu-id="dea77-297">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dea77-297">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="dea77-298">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-298">Element Information</span></span>



| <span data-ttu-id="dea77-299">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-299">Parent Element</span></span>              | <span data-ttu-id="dea77-300">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-300">Child Elements</span></span>    |
|-----------------------------|-------------------|
| [<span data-ttu-id="dea77-301">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="dea77-301">transfermanifest</span></span>](#syntax) | [<span data-ttu-id="dea77-302">Répertoire</span><span class="sxs-lookup"><span data-stu-id="dea77-302">folder</span></span>](#syntax) |



 

## <a name="formdata"></a><span data-ttu-id="dea77-303">formdata</span><span class="sxs-lookup"><span data-stu-id="dea77-303">formdata</span></span>

<span data-ttu-id="dea77-304">Décrit les données de formulaire encodées en HTML facultatives qui peuvent être transférées avec les fichiers.</span><span class="sxs-lookup"><span data-stu-id="dea77-304">Describes optional HTML encoded form data that may be transferred with the files.</span></span> <span data-ttu-id="dea77-305">Cet élément est ajouté par le service s’il choisit de télécharger les fichiers en tant que publication en plusieurs parties.</span><span class="sxs-lookup"><span data-stu-id="dea77-305">This element is added by the service if it elects to upload the files as a multi-part post.</span></span> <span data-ttu-id="dea77-306">Les données de formulaire, ainsi que les informations de l’élément de [publication](#syntax) , sont utilisées pour créer l’en-tête de publication.</span><span class="sxs-lookup"><span data-stu-id="dea77-306">The form data, together with information from the [post](#syntax) element, is used to create the post header.</span></span>

<span data-ttu-id="dea77-307">Plusieurs éléments [FormData](#syntax) peuvent être contenus sous un seul nœud [uploadinfo](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="dea77-307">Multiple [formdata](#syntax) elements may be contained under a single [uploadinfo](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-308">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-308">Syntax</span></span>


```
<formdata
    name = "string"
>
<!-- child elements -->
</formdata>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-309">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-309">Attributes</span></span>



| <span data-ttu-id="dea77-310">Attribut</span><span class="sxs-lookup"><span data-stu-id="dea77-310">Attribute</span></span> | <span data-ttu-id="dea77-311">Description</span><span class="sxs-lookup"><span data-stu-id="dea77-311">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dea77-312">name</span><span class="sxs-lookup"><span data-stu-id="dea77-312">name</span></span>      | <span data-ttu-id="dea77-313">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-313">Required.</span></span> <span data-ttu-id="dea77-314">Définit le nom des données de formulaire associé à cette section du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="dea77-314">Defines the form data name associated with this section of the upload.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="dea77-315">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-315">Element Information</span></span>



| <span data-ttu-id="dea77-316">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-316">Parent Element</span></span>        | <span data-ttu-id="dea77-317">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-317">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="dea77-318">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="dea77-318">uploadinfo</span></span>](#syntax) | <span data-ttu-id="dea77-319">Aucun</span><span class="sxs-lookup"><span data-stu-id="dea77-319">None</span></span>           |



 

## <a name="htmlui"></a><span data-ttu-id="dea77-320">htmlui</span><span class="sxs-lookup"><span data-stu-id="dea77-320">htmlui</span></span>

<span data-ttu-id="dea77-321">URL de la page HTML côté serveur à afficher lorsque l’Assistant est fermé.</span><span class="sxs-lookup"><span data-stu-id="dea77-321">The URL of the server-side HTML page to display when the wizard is closed.</span></span> <span data-ttu-id="dea77-322">Cet élément crée une entrée de page Web favorite dans le menu **favoris** si l’élément [favori](#syntax) est absent et que le nom convivial du site de chargement est spécifié.</span><span class="sxs-lookup"><span data-stu-id="dea77-322">This element creates a favorite webpage entry in the **Favorites** menu if the [favorite](#syntax) element is absent and the upload site's friendly name is specified.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-323">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-323">Syntax</span></span>


```
<htmlui
    href = "string"
>
<!-- child elements -->
</htmlui>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-324">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-324">Attributes</span></span>



| <span data-ttu-id="dea77-325">Attribut</span><span class="sxs-lookup"><span data-stu-id="dea77-325">Attribute</span></span> | <span data-ttu-id="dea77-326">Description</span><span class="sxs-lookup"><span data-stu-id="dea77-326">Description</span></span>                                                                          |
|-----------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="dea77-327">href</span><span class="sxs-lookup"><span data-stu-id="dea77-327">href</span></span>      | <span data-ttu-id="dea77-328">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-328">Required.</span></span> <span data-ttu-id="dea77-329">URL de la page HTML côté serveur à afficher lorsque l’Assistant est fermé.</span><span class="sxs-lookup"><span data-stu-id="dea77-329">The URL of the server-side HTML page to display when the wizard is closed.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="dea77-330">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-330">Element Information</span></span>



| <span data-ttu-id="dea77-331">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-331">Parent Element</span></span>        | <span data-ttu-id="dea77-332">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-332">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="dea77-333">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="dea77-333">uploadinfo</span></span>](#syntax) | <span data-ttu-id="dea77-334">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dea77-334">None.</span></span> <span data-ttu-id="dea77-335">Le texte est autorisé.</span><span class="sxs-lookup"><span data-stu-id="dea77-335">Text is allowed.</span></span> |



 

## <a name="imageproperty"></a><span data-ttu-id="dea77-336">imageproperty</span><span class="sxs-lookup"><span data-stu-id="dea77-336">imageproperty</span></span>

<span data-ttu-id="dea77-337">Spécifie une propriété d’image relative au fichier.</span><span class="sxs-lookup"><span data-stu-id="dea77-337">Specifies an image property relating to the file.</span></span> <span data-ttu-id="dea77-338">Plusieurs éléments [ImageProperty](#syntax) peuvent être contenus sous un seul nœud de [métadonnées](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="dea77-338">Multiple [imageproperty](#syntax) elements may be contained under a single [metadata](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-339">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-339">Syntax</span></span>


```
<imageproperty
    id = "string"
>
<!-- child elements -->
</imageproperty>                  
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-340">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-340">Attributes</span></span>



| <span data-ttu-id="dea77-341">Attribut</span><span class="sxs-lookup"><span data-stu-id="dea77-341">Attribute</span></span> | <span data-ttu-id="dea77-342">Description</span><span class="sxs-lookup"><span data-stu-id="dea77-342">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="dea77-343">id</span><span class="sxs-lookup"><span data-stu-id="dea77-343">id</span></span>        | <span data-ttu-id="dea77-344">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-344">Required.</span></span> <span data-ttu-id="dea77-345">ID de la propriété particulière.</span><span class="sxs-lookup"><span data-stu-id="dea77-345">The ID of the particular property.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="dea77-346">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-346">Element Information</span></span>



| <span data-ttu-id="dea77-347">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-347">Parent Element</span></span>      | <span data-ttu-id="dea77-348">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-348">Child Elements</span></span>         |
|---------------------|------------------------|
| [<span data-ttu-id="dea77-349">métadonnées</span><span class="sxs-lookup"><span data-stu-id="dea77-349">metadata</span></span>](#syntax) | <span data-ttu-id="dea77-350">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dea77-350">None.</span></span> <span data-ttu-id="dea77-351">Le texte est autorisé.</span><span class="sxs-lookup"><span data-stu-id="dea77-351">Text is allowed.</span></span> |



 

## <a name="metadata"></a><span data-ttu-id="dea77-352">metadata</span><span class="sxs-lookup"><span data-stu-id="dea77-352">metadata</span></span>

<span data-ttu-id="dea77-353">Conteneur pour les éléments et le texte définissant les métadonnées pour le fichier particulier.</span><span class="sxs-lookup"><span data-stu-id="dea77-353">A container for elements and text defining metadata for the particular file.</span></span> <span data-ttu-id="dea77-354">Plusieurs éléments de [métadonnées](#syntax) peuvent être contenus sous un seul nœud de [fichier](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="dea77-354">Multiple [metadata](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-355">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-355">Syntax</span></span>


```
<metadata>
<!-- child elements -->
</metadata>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-356">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-356">Attributes</span></span>

<span data-ttu-id="dea77-357">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dea77-357">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="dea77-358">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-358">Element Information</span></span>



| <span data-ttu-id="dea77-359">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-359">Parent Element</span></span>  | <span data-ttu-id="dea77-360">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-360">Child Elements</span></span>           |
|-----------------|--------------------------|
| [<span data-ttu-id="dea77-361">file</span><span class="sxs-lookup"><span data-stu-id="dea77-361">file</span></span>](#syntax) | [<span data-ttu-id="dea77-362">imageproperty</span><span class="sxs-lookup"><span data-stu-id="dea77-362">imageproperty</span></span>](#syntax) |



 

## <a name="netplace"></a><span data-ttu-id="dea77-363">emplacement</span><span class="sxs-lookup"><span data-stu-id="dea77-363">netplace</span></span>

<span data-ttu-id="dea77-364">Définit la cible d’un emplacement réseau créé dans favoris **réseau** lorsque le téléchargement est terminé.</span><span class="sxs-lookup"><span data-stu-id="dea77-364">Defines the target for a network place that is created in **My Network Places** when the upload is complete.</span></span> <span data-ttu-id="dea77-365">La création d’un emplacement réseau peut être évitée à l’aide de la méthode [**IPublishingWizard :: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) .</span><span class="sxs-lookup"><span data-stu-id="dea77-365">Creation of a network place can be prevented through the [**IPublishingWizard::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) method.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-366">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-366">Syntax</span></span>


```
<netplace
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</netplace>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-367">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-367">Attributes</span></span>



| <span data-ttu-id="dea77-368">Attribut</span><span class="sxs-lookup"><span data-stu-id="dea77-368">Attribute</span></span> | <span data-ttu-id="dea77-369">Description</span><span class="sxs-lookup"><span data-stu-id="dea77-369">Description</span></span>                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea77-370">comment</span><span class="sxs-lookup"><span data-stu-id="dea77-370">comment</span></span>   | <span data-ttu-id="dea77-371">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-371">Required.</span></span> <span data-ttu-id="dea77-372">Commentaire affiché pour l’icône d’emplacement réseau lorsque le curseur est placé sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="dea77-372">The comment displayed for the network place icon when the cursor rests on it.</span></span>         |
| <span data-ttu-id="dea77-373">href</span><span class="sxs-lookup"><span data-stu-id="dea77-373">href</span></span>      | <span data-ttu-id="dea77-374">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-374">Required.</span></span> <span data-ttu-id="dea77-375">URL de l’entrée d’emplacement réseau.</span><span class="sxs-lookup"><span data-stu-id="dea77-375">The URL of the network place entry.</span></span>                                                   |
| <span data-ttu-id="dea77-376">name</span><span class="sxs-lookup"><span data-stu-id="dea77-376">name</span></span>      | <span data-ttu-id="dea77-377">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-377">Required.</span></span> <span data-ttu-id="dea77-378">Nom de l’icône d’emplacement réseau qui apparaît dans le dossier **Favoris réseau** .</span><span class="sxs-lookup"><span data-stu-id="dea77-378">The name for the network place icon that appears in the **My Network Places** folder.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="dea77-379">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-379">Element Information</span></span>



| <span data-ttu-id="dea77-380">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-380">Parent Element</span></span>        | <span data-ttu-id="dea77-381">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-381">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="dea77-382">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="dea77-382">uploadinfo</span></span>](#syntax) | <span data-ttu-id="dea77-383">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dea77-383">None.</span></span> <span data-ttu-id="dea77-384">Le texte est autorisé.</span><span class="sxs-lookup"><span data-stu-id="dea77-384">Text is allowed.</span></span> |



 

## <a name="post"></a><span data-ttu-id="dea77-385">post</span><span class="sxs-lookup"><span data-stu-id="dea77-385">post</span></span>

<span data-ttu-id="dea77-386">URL vers laquelle le fichier doit être publié.</span><span class="sxs-lookup"><span data-stu-id="dea77-386">URL to which the file should be posted.</span></span> <span data-ttu-id="dea77-387">Cet élément est ajouté par le service lorsque le transfert est effectué sous la forme d’une publication en plusieurs parties et, avec [FormData](#syntax), est utilisé pour générer l’en-tête de publication.</span><span class="sxs-lookup"><span data-stu-id="dea77-387">This element is added by the service when the transfer is done as a multi-part post and, with [formdata](#syntax), is used to build the post header.</span></span> <span data-ttu-id="dea77-388">Si le service choisit d’effectuer le transfert de fichiers à l’aide d’World Wide Web Distributed Creation and Versioning (WebDAV), il ne doit pas ajouter cet élément.</span><span class="sxs-lookup"><span data-stu-id="dea77-388">If the service chooses to perform the file transfer using World Wide Web Distributed Authoring and Versioning (WebDAV), it should not add this element.</span></span> <span data-ttu-id="dea77-389">Plusieurs éléments de [publication](#syntax) peuvent être contenus sous un seul nœud de [fichier](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="dea77-389">Multiple [post](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-390">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-390">Syntax</span></span>


```
<post
    filename = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</post>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-391">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-391">Attributes</span></span>



| <span data-ttu-id="dea77-392">Attribut</span><span class="sxs-lookup"><span data-stu-id="dea77-392">Attribute</span></span> | <span data-ttu-id="dea77-393">Description</span><span class="sxs-lookup"><span data-stu-id="dea77-393">Description</span></span>                                                                    |
|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="dea77-394">nom_fichier</span><span class="sxs-lookup"><span data-stu-id="dea77-394">filename</span></span>  | <span data-ttu-id="dea77-395">facultatif.</span><span class="sxs-lookup"><span data-stu-id="dea77-395">Optional.</span></span> <span data-ttu-id="dea77-396">Nom de fichier du fichier publié.</span><span class="sxs-lookup"><span data-stu-id="dea77-396">The file name for the posted file.</span></span>                                   |
| <span data-ttu-id="dea77-397">href</span><span class="sxs-lookup"><span data-stu-id="dea77-397">href</span></span>      | <span data-ttu-id="dea77-398">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-398">Required.</span></span> <span data-ttu-id="dea77-399">URL du dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="dea77-399">The URL of the destination folder.</span></span>                                   |
| <span data-ttu-id="dea77-400">name</span><span class="sxs-lookup"><span data-stu-id="dea77-400">name</span></span>      | <span data-ttu-id="dea77-401">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-401">Required.</span></span> <span data-ttu-id="dea77-402">Définit le nom des données de formulaire associé à cette section de la publication.</span><span class="sxs-lookup"><span data-stu-id="dea77-402">Defines the form data name associated with this section of the post.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="dea77-403">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-403">Element Information</span></span>



| <span data-ttu-id="dea77-404">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-404">Parent Element</span></span>  | <span data-ttu-id="dea77-405">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-405">Child Elements</span></span>      |
|-----------------|---------------------|
| [<span data-ttu-id="dea77-406">file</span><span class="sxs-lookup"><span data-stu-id="dea77-406">file</span></span>](#syntax) | [<span data-ttu-id="dea77-407">formdata</span><span class="sxs-lookup"><span data-stu-id="dea77-407">formdata</span></span>](#syntax) |



 

## <a name="resize"></a><span data-ttu-id="dea77-408">resize</span><span class="sxs-lookup"><span data-stu-id="dea77-408">resize</span></span>

<span data-ttu-id="dea77-409">Définit la mise à l’échelle et la recompression d’un fichier image au format JPEG.</span><span class="sxs-lookup"><span data-stu-id="dea77-409">Defines the scaling and recompression of an image file into JPEG format.</span></span> <span data-ttu-id="dea77-410">Si le fichier source est déjà au format JPEG et qu’il est inférieur ou égal à la largeur et à la hauteur spécifiées, il n’est pas dimensionné.</span><span class="sxs-lookup"><span data-stu-id="dea77-410">If the source file is already in JPEG format and is less than or equal to the specified width and height, it is not sized.</span></span> <span data-ttu-id="dea77-411">Si le fichier source n’est pas un fichier JPEG, il est converti.</span><span class="sxs-lookup"><span data-stu-id="dea77-411">If the source file is not a JPEG file, it is converted.</span></span> <span data-ttu-id="dea77-412">La mise à l’échelle, la recompression et la conversion du fichier peuvent être évitées à l’aide de la méthode [**IPublishingWizard :: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) .</span><span class="sxs-lookup"><span data-stu-id="dea77-412">Scaling, recompression, and conversion of the file can be prevented through the [**IPublishingWizard::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) method.</span></span> <span data-ttu-id="dea77-413">Plusieurs éléments de [redimensionnement](#syntax) peuvent être contenus sous un seul nœud de [fichier](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="dea77-413">Multiple [resize](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-414">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-414">Syntax</span></span>


```
<resize
    cx = "string"
    cy = "string"
    quality = "string"
>
<!-- child elements -->
</resize>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-415">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-415">Attributes</span></span>



| <span data-ttu-id="dea77-416">Attribut</span><span class="sxs-lookup"><span data-stu-id="dea77-416">Attribute</span></span> | <span data-ttu-id="dea77-417">Description</span><span class="sxs-lookup"><span data-stu-id="dea77-417">Description</span></span>                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea77-418">adéquat</span><span class="sxs-lookup"><span data-stu-id="dea77-418">cx</span></span>        | <span data-ttu-id="dea77-419">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-419">Required.</span></span> <span data-ttu-id="dea77-420">Largeur de l’image, en pixels, après le chargement.</span><span class="sxs-lookup"><span data-stu-id="dea77-420">The width of the image, in pixels, after uploading.</span></span> <span data-ttu-id="dea77-421">Si cette valeur est égale à 0, **CX** est calculé à partir de la valeur **CY** pour conserver les dimensions relatives.</span><span class="sxs-lookup"><span data-stu-id="dea77-421">If this value is 0, then **cx** is calculated from the **cy** value to preserve relative dimensions.</span></span>  |
| <span data-ttu-id="dea77-422">cy</span><span class="sxs-lookup"><span data-stu-id="dea77-422">cy</span></span>        | <span data-ttu-id="dea77-423">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-423">Required.</span></span> <span data-ttu-id="dea77-424">Hauteur de l’image, en pixels, après le chargement.</span><span class="sxs-lookup"><span data-stu-id="dea77-424">The height of the image, in pixels, after uploading.</span></span> <span data-ttu-id="dea77-425">Si cette valeur est 0, **ca** est calculé à partir de la valeur **CX** pour conserver les dimensions relatives.</span><span class="sxs-lookup"><span data-stu-id="dea77-425">If this value is 0, then **cy** is calculated from the **cx** value to preserve relative dimensions.</span></span> |
| <span data-ttu-id="dea77-426">qualité</span><span class="sxs-lookup"><span data-stu-id="dea77-426">quality</span></span>   | <span data-ttu-id="dea77-427">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-427">Required.</span></span> <span data-ttu-id="dea77-428">Valeur de qualité JPEG, comprise entre 0 et 100, avec 100 de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="dea77-428">The JPEG quality value, between 0 and 100, with 100 being the highest quality.</span></span>                                                                            |



 

### <a name="element-information"></a><span data-ttu-id="dea77-429">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-429">Element Information</span></span>



| <span data-ttu-id="dea77-430">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-430">Parent Element</span></span>  | <span data-ttu-id="dea77-431">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-431">Child Elements</span></span> |
|-----------------|----------------|
| [<span data-ttu-id="dea77-432">file</span><span class="sxs-lookup"><span data-stu-id="dea77-432">file</span></span>](#syntax) | <span data-ttu-id="dea77-433">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dea77-433">None.</span></span>          |



 

## <a name="successpage"></a><span data-ttu-id="dea77-434">successpage</span><span class="sxs-lookup"><span data-stu-id="dea77-434">successpage</span></span>

<span data-ttu-id="dea77-435">Spécifie la page HTML côté serveur à afficher si le chargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="dea77-435">Specifies the server-side HTML page to display if the upload is successful.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-436">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-436">Syntax</span></span>


```
<successpage
    href = "string"
>
<!-- child elements -->
</successpage>                    
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-437">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-437">Attributes</span></span>



| <span data-ttu-id="dea77-438">Attribut</span><span class="sxs-lookup"><span data-stu-id="dea77-438">Attribute</span></span> | <span data-ttu-id="dea77-439">Description</span><span class="sxs-lookup"><span data-stu-id="dea77-439">Description</span></span>                                                                            |
|-----------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dea77-440">href</span><span class="sxs-lookup"><span data-stu-id="dea77-440">href</span></span>      | <span data-ttu-id="dea77-441">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-441">Required.</span></span> <span data-ttu-id="dea77-442">URL de la page HTML côté serveur à afficher si le chargement a réussi.</span><span class="sxs-lookup"><span data-stu-id="dea77-442">The URL of the server-side HTML page to display if the upload is successful.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="dea77-443">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-443">Element Information</span></span>



| <span data-ttu-id="dea77-444">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-444">Parent Element</span></span>        | <span data-ttu-id="dea77-445">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-445">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="dea77-446">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="dea77-446">uploadinfo</span></span>](#syntax) | <span data-ttu-id="dea77-447">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dea77-447">None.</span></span> <span data-ttu-id="dea77-448">Le texte est autorisé.</span><span class="sxs-lookup"><span data-stu-id="dea77-448">Text is allowed.</span></span> |



 

## <a name="target"></a><span data-ttu-id="dea77-449">target</span><span class="sxs-lookup"><span data-stu-id="dea77-449">target</span></span>

<span data-ttu-id="dea77-450">Un dossier de destination spécifié au format UNC (Universal Naming Convention) ou en tant que serveur WebDAV.</span><span class="sxs-lookup"><span data-stu-id="dea77-450">A destination folder specified in Universal Naming Convention (UNC) format or as a WebDAV server.</span></span> <span data-ttu-id="dea77-451">Le service ajoute cette cible pour spécifier un dossier de destination si le transfert utilise un protocole WebDAV ou le protocole de système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="dea77-451">The service adds this target to specify a destination folder if the transfer uses a WebDAV or file system protocol.</span></span> <span data-ttu-id="dea77-452">Si le service choisit d’effectuer le transfert de fichiers en tant que publication en plusieurs parties, il ne doit pas ajouter cet élément.</span><span class="sxs-lookup"><span data-stu-id="dea77-452">If the service chooses to perform the file transfer as a multi-part post, it should not add this element.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-453">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-453">Syntax</span></span>


```
<target
    href = "string"
>
<!-- child elements -->
</target>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-454">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-454">Attributes</span></span>



| <span data-ttu-id="dea77-455">Attribut</span><span class="sxs-lookup"><span data-stu-id="dea77-455">Attribute</span></span> | <span data-ttu-id="dea77-456">Description</span><span class="sxs-lookup"><span data-stu-id="dea77-456">Description</span></span>                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dea77-457">href</span><span class="sxs-lookup"><span data-stu-id="dea77-457">href</span></span>      | <span data-ttu-id="dea77-458">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-458">Required.</span></span> <span data-ttu-id="dea77-459">URL du dossier de destination.</span><span class="sxs-lookup"><span data-stu-id="dea77-459">The URL of the destination folder.</span></span> <span data-ttu-id="dea77-460">Utilisez le formulaire **https://** pour WebDAV ou le formulaire de **\\ \\ \\ partage de serveur** pour UNC.</span><span class="sxs-lookup"><span data-stu-id="dea77-460">Use the **https://** form for WebDAV or the **\\\\server\\share** form for UNC.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="dea77-461">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-461">Element Information</span></span>



| <span data-ttu-id="dea77-462">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-462">Parent Element</span></span>        | <span data-ttu-id="dea77-463">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-463">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="dea77-464">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="dea77-464">uploadinfo</span></span>](#syntax) | <span data-ttu-id="dea77-465">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dea77-465">None.</span></span> <span data-ttu-id="dea77-466">Le texte est autorisé.</span><span class="sxs-lookup"><span data-stu-id="dea77-466">Text is allowed.</span></span> |



 

## <a name="transfermanifest"></a><span data-ttu-id="dea77-467">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="dea77-467">transfermanifest</span></span>

<span data-ttu-id="dea77-468">Nœud parent du fichier de manifeste de transfert.</span><span class="sxs-lookup"><span data-stu-id="dea77-468">The parent node of the transfer manifest file.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-469">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-469">Syntax</span></span>


```
<transfermanifest>
<!-- child elements -->
</transfermanifest>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-470">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-470">Attributes</span></span>

<span data-ttu-id="dea77-471">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dea77-471">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="dea77-472">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-472">Element Information</span></span>



| <span data-ttu-id="dea77-473">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-473">Parent Element</span></span> | <span data-ttu-id="dea77-474">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-474">Child Elements</span></span>                                                    |
|----------------|-------------------------------------------------------------------|
| <span data-ttu-id="dea77-475">Aucun</span><span class="sxs-lookup"><span data-stu-id="dea77-475">None</span></span>           | <span data-ttu-id="dea77-476">[filelist](#syntax), [folderlist](#syntax), [uploadinfo](#syntax)</span><span class="sxs-lookup"><span data-stu-id="dea77-476">[filelist](#syntax), [folderlist](#syntax), [uploadinfo](#syntax)</span></span> |



 

## <a name="uploadinfo"></a><span data-ttu-id="dea77-477">uploadinfo</span><span class="sxs-lookup"><span data-stu-id="dea77-477">uploadinfo</span></span>

<span data-ttu-id="dea77-478">Conteneur pour les éléments fournissant des informations à partir du site de chargement utilisé dans la transaction.</span><span class="sxs-lookup"><span data-stu-id="dea77-478">A container for elements providing information from the upload site used in the transaction.</span></span> <span data-ttu-id="dea77-479">Plusieurs éléments [uploadinfo](#syntax) peuvent être contenus sous un seul nœud [transfermanifest](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="dea77-479">Multiple [uploadinfo](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="dea77-480">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dea77-480">Syntax</span></span>


```
<uploadinfo
    friendlyname = "string"
>
<!-- child elements -->
</uploadinfo>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="dea77-481">Attributs</span><span class="sxs-lookup"><span data-stu-id="dea77-481">Attributes</span></span>



| <span data-ttu-id="dea77-482">Attribut</span><span class="sxs-lookup"><span data-stu-id="dea77-482">Attribute</span></span>    | <span data-ttu-id="dea77-483">Description</span><span class="sxs-lookup"><span data-stu-id="dea77-483">Description</span></span>                                                                 |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="dea77-484">convivial</span><span class="sxs-lookup"><span data-stu-id="dea77-484">friendlyname</span></span> | <span data-ttu-id="dea77-485">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="dea77-485">Required.</span></span> <span data-ttu-id="dea77-486">Nom convivial du site Web qui s’affiche dans l’Assistant.</span><span class="sxs-lookup"><span data-stu-id="dea77-486">A friendly name for the website which is displayed in the wizard.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="dea77-487">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="dea77-487">Element Information</span></span>



| <span data-ttu-id="dea77-488">Élément parent</span><span class="sxs-lookup"><span data-stu-id="dea77-488">Parent Element</span></span>              | <span data-ttu-id="dea77-489">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dea77-489">Child Elements</span></span>                                                                                                                                           |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dea77-490">transfermanifest</span><span class="sxs-lookup"><span data-stu-id="dea77-490">transfermanifest</span></span>](#syntax) | <span data-ttu-id="dea77-491">[cancelledpage](#syntax), [failurepage](#syntax), [favori](#syntax), [htmlui](#syntax), [netplace](#syntax), [SuccessPage](#syntax), [cible](#syntax)</span><span class="sxs-lookup"><span data-stu-id="dea77-491">[cancelledpage](#syntax), [failurepage](#syntax), [favorite](#syntax), [htmlui](#syntax), [netplace](#syntax), [successpage](#syntax), [target](#syntax)</span></span> |



 

 

 



