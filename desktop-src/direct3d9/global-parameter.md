---
description: Chaque effet conforme à DXSAS doit définir au minimum un paramètre d’effet global unique avec la sémantique globale.
ms.assetid: 2112db8d-6a11-451d-a9d2-ac1b3cb2da95
title: Paramètre global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647ef789e37cd7c8d6cd2fe554f1f8becbfd5e92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106532065"
---
# <a name="global-parameter"></a><span data-ttu-id="55c3e-103">Paramètre global</span><span class="sxs-lookup"><span data-stu-id="55c3e-103">Global Parameter</span></span>

<span data-ttu-id="55c3e-104">Chaque effet conforme à DXSAS doit définir au minimum un paramètre d’effet global unique avec la sémantique globale.</span><span class="sxs-lookup"><span data-stu-id="55c3e-104">Each DXSAS compliant effect must define, as a minimum, a single global effect parameter with the global semantic.</span></span> <span data-ttu-id="55c3e-105">Le paramètre global peut également utiliser une ou plusieurs annotations facultatives.</span><span class="sxs-lookup"><span data-stu-id="55c3e-105">The global parameter can also use one or more optional annotations.</span></span> <span data-ttu-id="55c3e-106">La syntaxe est la suivante :</span><span class="sxs-lookup"><span data-stu-id="55c3e-106">The syntax is as follows:</span></span>


```
int VariableName : SasGlobal
<
    SasVersion 
    [OptionalAnnotations]
>;
```



<span data-ttu-id="55c3e-107">où :</span><span class="sxs-lookup"><span data-stu-id="55c3e-107">where:</span></span>

-   <span data-ttu-id="55c3e-108">NomVariable est un nom de variable de chaîne de texte ASCII spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="55c3e-108">VariableName is a user-specified, ASCII text string variable name.</span></span>
-   <span data-ttu-id="55c3e-109">SasGlobal est le mot clé sémantique qui identifie ce paramètre en tant que paramètre DXSAS global.</span><span class="sxs-lookup"><span data-stu-id="55c3e-109">SasGlobal is the semantic keyword that identifies this parameter as the global DXSAS parameter.</span></span>
-   <span data-ttu-id="55c3e-110">SasVersion est la seule annotation requise.</span><span class="sxs-lookup"><span data-stu-id="55c3e-110">SasVersion is the only required annotation.</span></span>
-   <span data-ttu-id="55c3e-111">OptionalAnnotations peut inclure les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="55c3e-111">OptionalAnnotations can include the following:</span></span>
    -   [<span data-ttu-id="55c3e-112">SasEffectAuthor</span><span class="sxs-lookup"><span data-stu-id="55c3e-112">SasEffectAuthor</span></span>](#saseffectauthor)
    -   [<span data-ttu-id="55c3e-113">SasEffectAuthoringSoftware</span><span class="sxs-lookup"><span data-stu-id="55c3e-113">SasEffectAuthoringSoftware</span></span>](#saseffectauthoringsoftware)
    -   [<span data-ttu-id="55c3e-114">SasEffectCategory</span><span class="sxs-lookup"><span data-stu-id="55c3e-114">SasEffectCategory</span></span>](#saseffectcategory)
    -   [<span data-ttu-id="55c3e-115">SasEffectCompany</span><span class="sxs-lookup"><span data-stu-id="55c3e-115">SasEffectCompany</span></span>](#saseffectcompany)
    -   [<span data-ttu-id="55c3e-116">SasEffectDescription</span><span class="sxs-lookup"><span data-stu-id="55c3e-116">SasEffectDescription</span></span>](#saseffectdescription)
    -   [<span data-ttu-id="55c3e-117">SasEffectHelp</span><span class="sxs-lookup"><span data-stu-id="55c3e-117">SasEffectHelp</span></span>](#saseffecthelp)
    -   [<span data-ttu-id="55c3e-118">SasEffectRevision</span><span class="sxs-lookup"><span data-stu-id="55c3e-118">SasEffectRevision</span></span>](#saseffectrevision)

## <a name="sasversion"></a><span data-ttu-id="55c3e-119">SasVersion</span><span class="sxs-lookup"><span data-stu-id="55c3e-119">SasVersion</span></span>

<span data-ttu-id="55c3e-120">La seule annotation requise est SasVersion.</span><span class="sxs-lookup"><span data-stu-id="55c3e-120">The only required annotation is SasVersion.</span></span> <span data-ttu-id="55c3e-121">Elle est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="55c3e-121">It is declared like this:</span></span>


```
int3 SasVersion = { major, minor, revision };
```



<span data-ttu-id="55c3e-122">où :</span><span class="sxs-lookup"><span data-stu-id="55c3e-122">where:</span></span>

-   <span data-ttu-id="55c3e-123">Major indique la version principale de DXSAS.</span><span class="sxs-lookup"><span data-stu-id="55c3e-123">major indicates the DXSAS major release.</span></span> <span data-ttu-id="55c3e-124">Les versions majeures de DXSAS peuvent contenir des modifications de l’ensemble de la sémantique et des annotations définies.</span><span class="sxs-lookup"><span data-stu-id="55c3e-124">Major releases of DXSAS can contain sweeping changes to the set of semantics and annotations defined.</span></span> <span data-ttu-id="55c3e-125">La sémantique et les annotations peuvent être ajoutées et supprimées et, en général, la compatibilité descendante avec les versions antérieures n’est pas garantie.</span><span class="sxs-lookup"><span data-stu-id="55c3e-125">Semantics and annotations can be added and removed and, in general, backward compatibility with previous releases is not guaranteed.</span></span>
-   <span data-ttu-id="55c3e-126">mineure indique la version mineure SAS.</span><span class="sxs-lookup"><span data-stu-id="55c3e-126">minor indicates the SAS minor release.</span></span> <span data-ttu-id="55c3e-127">Les versions mineures de DXSAS peuvent inclure l’ajout de nouvelles sémantiques ou annotations.</span><span class="sxs-lookup"><span data-stu-id="55c3e-127">Minor releases of DXSAS can include the addition of new semantics or annotations.</span></span> <span data-ttu-id="55c3e-128">En outre, la sémantique et les annotations peuvent être marquées comme dépréciées dans la norme DXSAS.</span><span class="sxs-lookup"><span data-stu-id="55c3e-128">Additionally, semantics and annotations may be marked as deprecated in the DXSAS standard.</span></span> <span data-ttu-id="55c3e-129">Les annotations et sémantiques déconseillées doivent toujours être prises en charge par les applications hôtes, mais elles peuvent émettre un diagnostic d’avertissement lorsqu’une telle sémantique ou annotation est utilisée.</span><span class="sxs-lookup"><span data-stu-id="55c3e-129">Deprecated semantics and annotations must still be supported by host applications but can emit a warning diagnostic when such a semantic or annotation is used.</span></span> <span data-ttu-id="55c3e-130">Les versions mineures sont à compatibilité descendante avec les versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="55c3e-130">Minor releases are backward compatible with previous releases.</span></span>
-   <span data-ttu-id="55c3e-131">la révision indique la révision DXSAS.</span><span class="sxs-lookup"><span data-stu-id="55c3e-131">revision indicates the DXSAS revision.</span></span> <span data-ttu-id="55c3e-132">Les révisions de DXSAS existent uniquement en tant que moyen de résoudre les bogues, de supprimer toute ambiguïté et d’affiner la norme.</span><span class="sxs-lookup"><span data-stu-id="55c3e-132">Revisions of DXSAS exist only as a means to fix bugs, remove ambiguity, and refine the standard.</span></span> <span data-ttu-id="55c3e-133">Les révisions du standard sont à compatibilité descendante avec les versions précédentes.</span><span class="sxs-lookup"><span data-stu-id="55c3e-133">Revisions to the standard are backward compatible with previous releases.</span></span>

<span data-ttu-id="55c3e-134">La version actuelle est 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="55c3e-134">The current version is 1.0.0.</span></span> <span data-ttu-id="55c3e-135">Il n’y a pas de valeur par défaut pour cette annotation.</span><span class="sxs-lookup"><span data-stu-id="55c3e-135">There is no default value for this annotation.</span></span>

## <a name="saseffectauthor"></a><span data-ttu-id="55c3e-136">SasEffectAuthor</span><span class="sxs-lookup"><span data-stu-id="55c3e-136">SasEffectAuthor</span></span>

<span data-ttu-id="55c3e-137">Cela déclare la personne qui a créé l’effet.</span><span class="sxs-lookup"><span data-stu-id="55c3e-137">This declares the person who created the effect.</span></span> <span data-ttu-id="55c3e-138">Elle est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="55c3e-138">It is declared like this:</span></span>


```
string SasEffectAuthor = "value";
```



<span data-ttu-id="55c3e-139">où la valeur est une chaîne qui identifie l’auteur de l’effet.</span><span class="sxs-lookup"><span data-stu-id="55c3e-139">where value is a string that identifies the effect author.</span></span> <span data-ttu-id="55c3e-140">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="55c3e-140">The default is an empty string.</span></span>

## <a name="saseffectauthoringsoftware"></a><span data-ttu-id="55c3e-141">SasEffectAuthoringSoftware</span><span class="sxs-lookup"><span data-stu-id="55c3e-141">SasEffectAuthoringSoftware</span></span>

<span data-ttu-id="55c3e-142">Cela déclare le logiciel sur lequel l’effet a été créé.</span><span class="sxs-lookup"><span data-stu-id="55c3e-142">This declares the software that the effect was authored on.</span></span> <span data-ttu-id="55c3e-143">Elle est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="55c3e-143">It is declared like this:</span></span>


```
string SasEffectAuthoringSoftware = "value";
```



<span data-ttu-id="55c3e-144">où valeur est une chaîne qui identifie le logiciel de création d’effet.</span><span class="sxs-lookup"><span data-stu-id="55c3e-144">where value is a string that identifies the effect authoring software.</span></span> <span data-ttu-id="55c3e-145">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="55c3e-145">The default is an empty string.</span></span>

## <a name="saseffectcategory"></a><span data-ttu-id="55c3e-146">SasEffectCategory</span><span class="sxs-lookup"><span data-stu-id="55c3e-146">SasEffectCategory</span></span>

<span data-ttu-id="55c3e-147">Cela déclare la catégorie d’effet.</span><span class="sxs-lookup"><span data-stu-id="55c3e-147">This declares the effect category.</span></span> <span data-ttu-id="55c3e-148">Elle est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="55c3e-148">It is declared like this:</span></span>


```
string SasEffectCategory = "value";
```



<span data-ttu-id="55c3e-149">où valeur est une chaîne qui identifie la catégorie d’effet.</span><span class="sxs-lookup"><span data-stu-id="55c3e-149">where value is a string that identifies the effect category.</span></span> <span data-ttu-id="55c3e-150">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="55c3e-150">The default is an empty string.</span></span> <span data-ttu-id="55c3e-151">La catégorie est exprimée via une valeur de type chemin d’accès utilisant la barre oblique comme séparateur.</span><span class="sxs-lookup"><span data-stu-id="55c3e-151">The category is expressed via a path-like value using the forward slash as a delimiter.</span></span> <span data-ttu-id="55c3e-152">Les effets peuvent uniquement appartenir à une catégorie, car il n’existe aucune syntaxe pour exprimer l’inclusion dans plusieurs chemins d’accès au sein d’une seule valeur SasEffectCategory.</span><span class="sxs-lookup"><span data-stu-id="55c3e-152">Effects can only belong to one category as there is no syntax for expressing inclusion in multiple paths within a single SasEffectCategory value.</span></span> <span data-ttu-id="55c3e-153">La valeur de cette annotation n’est pas traitée comme respectant la casse par l’application hôte.</span><span class="sxs-lookup"><span data-stu-id="55c3e-153">The value of this annotation is not treated as case-sensitive by the host application.</span></span>

## <a name="saseffectcompany"></a><span data-ttu-id="55c3e-154">SasEffectCompany</span><span class="sxs-lookup"><span data-stu-id="55c3e-154">SasEffectCompany</span></span>

<span data-ttu-id="55c3e-155">Cela déclare la société qui a créé l’effet.</span><span class="sxs-lookup"><span data-stu-id="55c3e-155">This declares the company that created the effect.</span></span> <span data-ttu-id="55c3e-156">Elle est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="55c3e-156">It is declared like this:</span></span>


```
string SasEffectCompany = "value";
```



<span data-ttu-id="55c3e-157">où valeur est une chaîne qui identifie le nom de la société qui possède l’effet.</span><span class="sxs-lookup"><span data-stu-id="55c3e-157">where value is a string that identifies the name of the company that owns the effect.</span></span> <span data-ttu-id="55c3e-158">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="55c3e-158">The default is an empty string.</span></span>

## <a name="saseffectdescription"></a><span data-ttu-id="55c3e-159">SasEffectDescription</span><span class="sxs-lookup"><span data-stu-id="55c3e-159">SasEffectDescription</span></span>

<span data-ttu-id="55c3e-160">Cela décrit l’effet.</span><span class="sxs-lookup"><span data-stu-id="55c3e-160">This describes the effect.</span></span> <span data-ttu-id="55c3e-161">Elle est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="55c3e-161">It is declared like this:</span></span>


```
string SasEffectDescription = "value";
```



<span data-ttu-id="55c3e-162">où la valeur est une chaîne qui décrit l’effet.</span><span class="sxs-lookup"><span data-stu-id="55c3e-162">where value is a string that describes the effect.</span></span> <span data-ttu-id="55c3e-163">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="55c3e-163">The default is an empty string.</span></span>

## <a name="saseffecthelp"></a><span data-ttu-id="55c3e-164">SasEffectHelp</span><span class="sxs-lookup"><span data-stu-id="55c3e-164">SasEffectHelp</span></span>

<span data-ttu-id="55c3e-165">Il s’agit d’une chaîne d’aide qui peut être affichée à l’utilisateur chaque fois que l’aide sur l’effet associé est demandée.</span><span class="sxs-lookup"><span data-stu-id="55c3e-165">This is a help string that can be displayed to the user whenever help on the associated effect is requested.</span></span> <span data-ttu-id="55c3e-166">Elle est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="55c3e-166">It is declared like this:</span></span>


```
string SasEffectHelp = "value";
```



<span data-ttu-id="55c3e-167">où valeur est une chaîne qui peut être affichée si l’utilisateur demande de l’aide.</span><span class="sxs-lookup"><span data-stu-id="55c3e-167">where value is a string that can be displayed if the user requests help.</span></span> <span data-ttu-id="55c3e-168">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="55c3e-168">The default is an empty string.</span></span>

## <a name="saseffectrevision"></a><span data-ttu-id="55c3e-169">SasEffectRevision</span><span class="sxs-lookup"><span data-stu-id="55c3e-169">SasEffectRevision</span></span>

<span data-ttu-id="55c3e-170">Cette annotation permet aux outils et aux utilisateurs d’enregistrer le numéro de révision du fichier d’effet associé.</span><span class="sxs-lookup"><span data-stu-id="55c3e-170">This annotation allows tools and users to record the revision number of the associated effect file.</span></span> <span data-ttu-id="55c3e-171">Par exemple, les utilisateurs peuvent insérer des mots clés appropriés dans la valeur de cette annotation pour appeler le remplacement de mot clé dans leur logiciel de contrôle de révision préféré.</span><span class="sxs-lookup"><span data-stu-id="55c3e-171">For example, users could insert appropriate keywords in the value of this annotation to invoke keyword substitution in their favorite revision control software.</span></span> <span data-ttu-id="55c3e-172">Elle est déclarée comme suit :</span><span class="sxs-lookup"><span data-stu-id="55c3e-172">It is declared like this:</span></span>


```
string SasEffectRevision = "value";
```



<span data-ttu-id="55c3e-173">où la valeur est une chaîne qui identifie la révision de l’effet.</span><span class="sxs-lookup"><span data-stu-id="55c3e-173">where value is a string that identifies the effect revision.</span></span> <span data-ttu-id="55c3e-174">La valeur par défaut est une chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="55c3e-174">The default is an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="55c3e-175">Exemples</span><span class="sxs-lookup"><span data-stu-id="55c3e-175">Examples</span></span>

<span data-ttu-id="55c3e-176">Voici un exemple qui utilise uniquement l’annotation unique obligatoire :</span><span class="sxs-lookup"><span data-stu-id="55c3e-176">Here is an example that uses only the single, required annotation:</span></span>


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
>;
```



<span data-ttu-id="55c3e-177">Voici un exemple qui utilise l’annotation requise et plusieurs annotations facultatives :</span><span class="sxs-lookup"><span data-stu-id="55c3e-177">Here is an example that uses the required annotation and several optional annotations:</span></span>


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
  string SasEffectAuthor = "Mike's Shader";
  string SasEffectAuthoringSoftware = "fxe 2.5.4";
  string SasEffectCategory = "/surface/procedural/wood";
  string SasEffectCompany = "Microsoft Corporation";
  string SasEffectDescription = "Renders an irridescent surface.";
  string SasEffectHelp = "For more information, see https://somelocation/skin.htm";    
  string SasEffectRevision = "$Revision$";  
>;
```



## <a name="related-topics"></a><span data-ttu-id="55c3e-178">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55c3e-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55c3e-179">Informations de référence sur les annotations et sémantiques DirectX standard</span><span class="sxs-lookup"><span data-stu-id="55c3e-179">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



