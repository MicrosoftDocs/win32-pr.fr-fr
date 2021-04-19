---
description: Msitran.exe utilise MsiDatabaseGenerateTransform, MsiCreateTransformSummaryInfo et MsiDatabaseApplyTransform pour générer ou appliquer un fichier de transformation. Cet outil est disponible uniquement dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: cfc7b907-78d7-4a78-bab4-ede9012d5a36
title: Msitran.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69936155fb3880f43e0f7563bc6aabd59f53703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529365"
---
# <a name="msitranexe"></a><span data-ttu-id="5b3cd-103">Msitran.exe</span><span class="sxs-lookup"><span data-stu-id="5b3cd-103">Msitran.exe</span></span>

<span data-ttu-id="5b3cd-104">Msitran.exe utilise [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)et [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) pour générer ou appliquer un fichier de transformation.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-104">Msitran.exe uses [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa), and [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) to generate or apply a transform file.</span></span>

<span data-ttu-id="5b3cd-105">Cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="5b3cd-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b3cd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b3cd-106">Syntax</span></span>

<span data-ttu-id="5b3cd-107">Pour générer une transformation, utilisez la syntaxe ci-après.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-107">Use the following syntax to generate a transform.</span></span>

<span data-ttu-id="5b3cd-108">**msitran-g** *{base dB} {ref DB} {nom du fichier de transformation} \[ {conditions d’erreur/ \] conditions de validation}*</span><span class="sxs-lookup"><span data-stu-id="5b3cd-108">**msitran -g** *{base db}{ref db}{transform file name}\[{error conditions / validation conditions}\]*</span></span>

<span data-ttu-id="5b3cd-109">Pour appliquer une transformation, utilisez la syntaxe ci-après.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-109">Use the following syntax to apply a transform</span></span>

<span data-ttu-id="5b3cd-110">**msitran-a** *{transformer} {base de données} \[ {conditions \] d’erreur}*</span><span class="sxs-lookup"><span data-stu-id="5b3cd-110">**msitran -a** *{transform}{database}\[{error conditions}\]*</span></span>

## <a name="command-line-options"></a><span data-ttu-id="5b3cd-111">Options de la ligne de commande</span><span class="sxs-lookup"><span data-stu-id="5b3cd-111">Command Line Options</span></span>

<span data-ttu-id="5b3cd-112">Msitran.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-112">Msitran.exe uses the following case-insensitive command line options.</span></span> <span data-ttu-id="5b3cd-113">Un séparateur de barre oblique peut également être utilisé à la place d’un tiret.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-113">A slash delimiter may also be used in place of a dash.</span></span>



| <span data-ttu-id="5b3cd-114">Option</span><span class="sxs-lookup"><span data-stu-id="5b3cd-114">Option</span></span> | <span data-ttu-id="5b3cd-115">Description</span><span class="sxs-lookup"><span data-stu-id="5b3cd-115">Description</span></span>            |
|--------|------------------------|
| <span data-ttu-id="5b3cd-116">-g</span><span class="sxs-lookup"><span data-stu-id="5b3cd-116">-g</span></span>     | <span data-ttu-id="5b3cd-117">Génération de transformation.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-117">Transform generation.</span></span>  |
| <span data-ttu-id="5b3cd-118">-a</span><span class="sxs-lookup"><span data-stu-id="5b3cd-118">-a</span></span>     | <span data-ttu-id="5b3cd-119">Transformation de l’application.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-119">Transform application.</span></span> |



 

<span data-ttu-id="5b3cd-120">Les erreurs suivantes peuvent être supprimées lors de l’application d’une transformation.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-120">The following errors may be suppressed when applying a transform.</span></span> <span data-ttu-id="5b3cd-121">Pour supprimer une erreur, incluez le caractère approprié dans l’argument {condition d’erreur}.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-121">To suppress an error, include the appropriate character in the {error conditions} argument.</span></span> <span data-ttu-id="5b3cd-122">Les conditions spécifiées avec-g sont placées dans les informations récapitulatives de la transformation, mais ne sont pas utilisées lors de l’application d’une transformation avec-a.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-122">Conditions specified with -g are placed in the summary information of the transform, but are not used when applying a transform with -a.</span></span> <span data-ttu-id="5b3cd-123">Pour plus d’informations, consultez [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).</span><span class="sxs-lookup"><span data-stu-id="5b3cd-123">For information, see [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).</span></span>



| <span data-ttu-id="5b3cd-124">Option</span><span class="sxs-lookup"><span data-stu-id="5b3cd-124">Option</span></span> | <span data-ttu-id="5b3cd-125">Erreur supprimée</span><span class="sxs-lookup"><span data-stu-id="5b3cd-125">Suppressed error</span></span>           |
|--------|----------------------------|
| <span data-ttu-id="5b3cd-126">a</span><span class="sxs-lookup"><span data-stu-id="5b3cd-126">a</span></span>      | <span data-ttu-id="5b3cd-127">Ajoutez une ligne existante.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-127">Add existing row.</span></span>          |
| <span data-ttu-id="5b3cd-128">b</span><span class="sxs-lookup"><span data-stu-id="5b3cd-128">b</span></span>      | <span data-ttu-id="5b3cd-129">Supprimer une ligne non existante.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-129">Delete non-existing row.</span></span>   |
| <span data-ttu-id="5b3cd-130">c</span><span class="sxs-lookup"><span data-stu-id="5b3cd-130">c</span></span>      | <span data-ttu-id="5b3cd-131">Ajoutez une table existante.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-131">Add existing table.</span></span>        |
| <span data-ttu-id="5b3cd-132">d</span><span class="sxs-lookup"><span data-stu-id="5b3cd-132">d</span></span>      | <span data-ttu-id="5b3cd-133">Supprime une table non existante.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-133">Delete non-existing table.</span></span> |
| <span data-ttu-id="5b3cd-134">e</span><span class="sxs-lookup"><span data-stu-id="5b3cd-134">e</span></span>      | <span data-ttu-id="5b3cd-135">Modifiez la ligne existante.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-135">Modify existing row.</span></span>       |
| <span data-ttu-id="5b3cd-136">f</span><span class="sxs-lookup"><span data-stu-id="5b3cd-136">f</span></span>      | <span data-ttu-id="5b3cd-137">Modifiez la page de codes.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-137">Change codepage.</span></span>           |



 

<span data-ttu-id="5b3cd-138">Les conditions de validation suivantes peuvent être utilisées pour indiquer qu’une transformation peut être appliquée à un package.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-138">The following validation conditions may be used to indicate when a transform may be applied to a package.</span></span> <span data-ttu-id="5b3cd-139">Ces conditions peuvent être spécifiées avec-g, mais pas-a.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-139">These conditions may be specified with -g, but not -a.</span></span>



| <span data-ttu-id="5b3cd-140">Option</span><span class="sxs-lookup"><span data-stu-id="5b3cd-140">Option</span></span> | <span data-ttu-id="5b3cd-141">Condition de validation</span><span class="sxs-lookup"><span data-stu-id="5b3cd-141">Validation condition</span></span>                                  |
|--------|-------------------------------------------------------|
| <span data-ttu-id="5b3cd-142">g</span><span class="sxs-lookup"><span data-stu-id="5b3cd-142">g</span></span>      | <span data-ttu-id="5b3cd-143">Vérifiez le code de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-143">Check upgrade code.</span></span>                                   |
| <span data-ttu-id="5b3cd-144">l</span><span class="sxs-lookup"><span data-stu-id="5b3cd-144">l</span></span>      | <span data-ttu-id="5b3cd-145">Vérifiez la langue.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-145">Check language.</span></span>                                       |
| <span data-ttu-id="5b3cd-146">p</span><span class="sxs-lookup"><span data-stu-id="5b3cd-146">p</span></span>      | <span data-ttu-id="5b3cd-147">Vérifiez la plateforme.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-147">Check platform.</span></span>                                       |
| <span data-ttu-id="5b3cd-148">r</span><span class="sxs-lookup"><span data-stu-id="5b3cd-148">r</span></span>      | <span data-ttu-id="5b3cd-149">Vérifiez le produit.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-149">Check product.</span></span>                                        |
| <span data-ttu-id="5b3cd-150">s</span><span class="sxs-lookup"><span data-stu-id="5b3cd-150">s</span></span>      | <span data-ttu-id="5b3cd-151">Vérifiez uniquement la version principale.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-151">Check major version only.</span></span>                             |
| <span data-ttu-id="5b3cd-152">t</span><span class="sxs-lookup"><span data-stu-id="5b3cd-152">t</span></span>      | <span data-ttu-id="5b3cd-153">Vérifiez uniquement les versions majeures et mineures.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-153">Check major and minor versions only.</span></span>                  |
| <span data-ttu-id="5b3cd-154">u</span><span class="sxs-lookup"><span data-stu-id="5b3cd-154">u</span></span>      | <span data-ttu-id="5b3cd-155">Vérifiez les versions majeure, mineure et de mise à niveau.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-155">Check major, minor, and upgrade versions.</span></span>             |
| <span data-ttu-id="5b3cd-156">v</span><span class="sxs-lookup"><span data-stu-id="5b3cd-156">v</span></span>      | <span data-ttu-id="5b3cd-157">Version de base de données appliquée < version de base de données de base.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-157">Applied database version < Base database version.</span></span>  |
| <span data-ttu-id="5b3cd-158">w</span><span class="sxs-lookup"><span data-stu-id="5b3cd-158">w</span></span>      | <span data-ttu-id="5b3cd-159">Version de base de données appliquée <= version de base de données de base.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-159">Applied database version <= Base database version.</span></span> |
| <span data-ttu-id="5b3cd-160">x</span><span class="sxs-lookup"><span data-stu-id="5b3cd-160">x</span></span>      | <span data-ttu-id="5b3cd-161">Version de base de données appliquée = version de base de la base de données.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-161">Applied database version = Base database version.</span></span>     |
| <span data-ttu-id="5b3cd-162">y</span><span class="sxs-lookup"><span data-stu-id="5b3cd-162">y</span></span>      | <span data-ttu-id="5b3cd-163">Version de base de données appliquée >= version de base de données de base.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-163">Applied database version >= Base database version.</span></span> |
| <span data-ttu-id="5b3cd-164">z</span><span class="sxs-lookup"><span data-stu-id="5b3cd-164">z</span></span>      | <span data-ttu-id="5b3cd-165">Version de base de données appliquée > version de base de données de base.</span><span class="sxs-lookup"><span data-stu-id="5b3cd-165">Applied database version > Base database version.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="5b3cd-166">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b3cd-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b3cd-167">Outils de développement Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5b3cd-167">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="5b3cd-168">Transformations de base de données</span><span class="sxs-lookup"><span data-stu-id="5b3cd-168">Database Transforms</span></span>](database-transforms.md)
</dt> <dt>

[<span data-ttu-id="5b3cd-169">Exemple de transformation de personnalisation</span><span class="sxs-lookup"><span data-stu-id="5b3cd-169">A Customization Transform Example</span></span>](a-customization-transform-example.md)
</dt> <dt>

[<span data-ttu-id="5b3cd-170">Versions, outils et redistribuables publiés</span><span class="sxs-lookup"><span data-stu-id="5b3cd-170">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



