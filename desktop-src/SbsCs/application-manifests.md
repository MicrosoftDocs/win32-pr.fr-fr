---
description: Un manifeste d'application est un fichier XML qui décrit et identifie les assemblys côte à côte partagés et privés auxquels une application doit se lier au moment de l'exécution.
ms.assetid: c5016251-db7a-4edc-9be9-3acb03d495f8
title: Manifestes d’application
ms.topic: article
ms.date: 10/08/2020
ms.custom: 19H1
ms.openlocfilehash: 2fb7297310102134dfcacf0e5f0d907fbf3a3e0b
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230234"
---
# <a name="application-manifests"></a><span data-ttu-id="d001c-103">Manifestes d’application</span><span class="sxs-lookup"><span data-stu-id="d001c-103">Application Manifests</span></span>

<span data-ttu-id="d001c-104">Un manifeste d'application est un fichier XML qui décrit et identifie les assemblys côte à côte partagés et privés auxquels une application doit se lier au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="d001c-104">An application manifest is an XML file that describes and identifies the shared and private side-by-side assemblies that an application should bind to at run time.</span></span> <span data-ttu-id="d001c-105">Il doit s'agir des mêmes versions d'assembly qui ont été utilisées pour tester l'application.</span><span class="sxs-lookup"><span data-stu-id="d001c-105">These should be the same assembly versions that were used to test the application.</span></span> <span data-ttu-id="d001c-106">Les manifestes d'application peuvent également décrire les métadonnées de fichiers privés pour l'application.</span><span class="sxs-lookup"><span data-stu-id="d001c-106">Application manifests may also describe metadata for files that are private to the application.</span></span>

<span data-ttu-id="d001c-107">Pour obtenir une liste complète du schéma XML, consultez [schéma de fichier manifeste](manifest-file-schema.md).</span><span class="sxs-lookup"><span data-stu-id="d001c-107">For a complete listing of the XML schema, see [Manifest File Schema](manifest-file-schema.md).</span></span>

<span data-ttu-id="d001c-108">Les manifestes d’application comportent les éléments et les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="d001c-108">Application manifests have the following elements and attributes.</span></span>

| <span data-ttu-id="d001c-109">Élément</span><span class="sxs-lookup"><span data-stu-id="d001c-109">Element</span></span>                               | <span data-ttu-id="d001c-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="d001c-110">Attributes</span></span>                | <span data-ttu-id="d001c-111">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d001c-111">Required</span></span> |
|---------------------------------------|---------------------------|----------|
| <span data-ttu-id="d001c-112">**chargeur**</span><span class="sxs-lookup"><span data-stu-id="d001c-112">**assembly**</span></span>                          |                           | <span data-ttu-id="d001c-113">Oui</span><span class="sxs-lookup"><span data-stu-id="d001c-113">Yes</span></span>      |
|                                       | <span data-ttu-id="d001c-114">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="d001c-114">**manifestVersion**</span></span>       | <span data-ttu-id="d001c-115">Oui</span><span class="sxs-lookup"><span data-stu-id="d001c-115">Yes</span></span>      |
| <span data-ttu-id="d001c-116">**noInherit**</span><span class="sxs-lookup"><span data-stu-id="d001c-116">**noInherit**</span></span>                         |                           | <span data-ttu-id="d001c-117">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-117">No</span></span>       |
| <span data-ttu-id="d001c-118">**assemblyIdentity**</span><span class="sxs-lookup"><span data-stu-id="d001c-118">**assemblyIdentity**</span></span>                  |                           | <span data-ttu-id="d001c-119">Oui</span><span class="sxs-lookup"><span data-stu-id="d001c-119">Yes</span></span>      |
|                                       | <span data-ttu-id="d001c-120">**type**</span><span class="sxs-lookup"><span data-stu-id="d001c-120">**type**</span></span>                  | <span data-ttu-id="d001c-121">Oui</span><span class="sxs-lookup"><span data-stu-id="d001c-121">Yes</span></span>      |
|                                       | <span data-ttu-id="d001c-122">**name**</span><span class="sxs-lookup"><span data-stu-id="d001c-122">**name**</span></span>                  | <span data-ttu-id="d001c-123">Oui</span><span class="sxs-lookup"><span data-stu-id="d001c-123">Yes</span></span>      |
|                                       | <span data-ttu-id="d001c-124">**language**</span><span class="sxs-lookup"><span data-stu-id="d001c-124">**language**</span></span>              | <span data-ttu-id="d001c-125">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-125">No</span></span>       |
|                                       | <span data-ttu-id="d001c-126">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="d001c-126">**processorArchitecture**</span></span> | <span data-ttu-id="d001c-127">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-127">No</span></span>       |
|                                       | <span data-ttu-id="d001c-128">**version**</span><span class="sxs-lookup"><span data-stu-id="d001c-128">**version**</span></span>               | <span data-ttu-id="d001c-129">Oui</span><span class="sxs-lookup"><span data-stu-id="d001c-129">Yes</span></span>      |
|                                       | <span data-ttu-id="d001c-130">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="d001c-130">**publicKeyToken**</span></span>        | <span data-ttu-id="d001c-131">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-131">No</span></span>       |
| <span data-ttu-id="d001c-132">**compatibilité**</span><span class="sxs-lookup"><span data-stu-id="d001c-132">**compatibility**</span></span>                     |                           | <span data-ttu-id="d001c-133">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-133">No</span></span>       |
| <span data-ttu-id="d001c-134">**application**</span><span class="sxs-lookup"><span data-stu-id="d001c-134">**application**</span></span>                       |                           | <span data-ttu-id="d001c-135">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-135">No</span></span>       |
| <span data-ttu-id="d001c-136">**pris en charge**</span><span class="sxs-lookup"><span data-stu-id="d001c-136">**supportedOS**</span></span>                       | <span data-ttu-id="d001c-137">**Id**</span><span class="sxs-lookup"><span data-stu-id="d001c-137">**Id**</span></span>                    | <span data-ttu-id="d001c-138">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-138">No</span></span>       |
| <span data-ttu-id="d001c-139">**maxversiontested**</span><span class="sxs-lookup"><span data-stu-id="d001c-139">**maxversiontested**</span></span>                  | <span data-ttu-id="d001c-140">**Id**</span><span class="sxs-lookup"><span data-stu-id="d001c-140">**Id**</span></span>                    | <span data-ttu-id="d001c-141">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-141">No</span></span>       |
| <span data-ttu-id="d001c-142">**dépendance**</span><span class="sxs-lookup"><span data-stu-id="d001c-142">**dependency**</span></span>                        |                           | <span data-ttu-id="d001c-143">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-143">No</span></span>       |
| <span data-ttu-id="d001c-144">**dependentAssembly**</span><span class="sxs-lookup"><span data-stu-id="d001c-144">**dependentAssembly**</span></span>                 |                           | <span data-ttu-id="d001c-145">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-145">No</span></span>       |
| <span data-ttu-id="d001c-146">**file**</span><span class="sxs-lookup"><span data-stu-id="d001c-146">**file**</span></span>                              |                           | <span data-ttu-id="d001c-147">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-147">No</span></span>       |
|                                       | <span data-ttu-id="d001c-148">**name**</span><span class="sxs-lookup"><span data-stu-id="d001c-148">**name**</span></span>                  | <span data-ttu-id="d001c-149">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-149">No</span></span>       |
|                                       | <span data-ttu-id="d001c-150">**hashAlg**</span><span class="sxs-lookup"><span data-stu-id="d001c-150">**hashalg**</span></span>               | <span data-ttu-id="d001c-151">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-151">No</span></span>       |
|                                       | <span data-ttu-id="d001c-152">**hash**</span><span class="sxs-lookup"><span data-stu-id="d001c-152">**hash**</span></span>                  | <span data-ttu-id="d001c-153">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-153">No</span></span>       |
| <span data-ttu-id="d001c-154">**activeCodePage**</span><span class="sxs-lookup"><span data-stu-id="d001c-154">**activeCodePage**</span></span>                    |                           | <span data-ttu-id="d001c-155">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-155">No</span></span>       |
| <span data-ttu-id="d001c-156">**Élever**</span><span class="sxs-lookup"><span data-stu-id="d001c-156">**autoElevate**</span></span>                       |                           | <span data-ttu-id="d001c-157">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-157">No</span></span>       |
| <span data-ttu-id="d001c-158">**disableTheming**</span><span class="sxs-lookup"><span data-stu-id="d001c-158">**disableTheming**</span></span>                    |                           | <span data-ttu-id="d001c-159">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-159">No</span></span>       |
| <span data-ttu-id="d001c-160">**disableWindowFiltering**</span><span class="sxs-lookup"><span data-stu-id="d001c-160">**disableWindowFiltering**</span></span>            |                           | <span data-ttu-id="d001c-161">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-161">No</span></span>       |
| <span data-ttu-id="d001c-162">**dpiAware**</span><span class="sxs-lookup"><span data-stu-id="d001c-162">**dpiAware**</span></span>                          |                           | <span data-ttu-id="d001c-163">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-163">No</span></span>       |
| <span data-ttu-id="d001c-164">**dpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="d001c-164">**dpiAwareness**</span></span>                      |                           | <span data-ttu-id="d001c-165">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-165">No</span></span>       |
| <span data-ttu-id="d001c-166">**gdiScaling**</span><span class="sxs-lookup"><span data-stu-id="d001c-166">**gdiScaling**</span></span>                        |                           | <span data-ttu-id="d001c-167">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-167">No</span></span>       |
| <span data-ttu-id="d001c-168">**highResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="d001c-168">**highResolutionScrollingAware**</span></span>      |                           | <span data-ttu-id="d001c-169">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-169">No</span></span>       |
| <span data-ttu-id="d001c-170">**longPathAware**</span><span class="sxs-lookup"><span data-stu-id="d001c-170">**longPathAware**</span></span>                     |                           | <span data-ttu-id="d001c-171">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-171">No</span></span>       |
| <span data-ttu-id="d001c-172">**printerDriverIsolation**</span><span class="sxs-lookup"><span data-stu-id="d001c-172">**printerDriverIsolation**</span></span>            |                           | <span data-ttu-id="d001c-173">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-173">No</span></span>       |
| <span data-ttu-id="d001c-174">**ultraHighResolutionScrollingAware**</span><span class="sxs-lookup"><span data-stu-id="d001c-174">**ultraHighResolutionScrollingAware**</span></span> |                           | <span data-ttu-id="d001c-175">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-175">No</span></span>       |
| <span data-ttu-id="d001c-176">**msix**</span><span class="sxs-lookup"><span data-stu-id="d001c-176">**msix**</span></span>                              |                           | <span data-ttu-id="d001c-177">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-177">No</span></span>       |
| <span data-ttu-id="d001c-178">**heapType**</span><span class="sxs-lookup"><span data-stu-id="d001c-178">**heapType**</span></span>                          |                           | <span data-ttu-id="d001c-179">Non</span><span class="sxs-lookup"><span data-stu-id="d001c-179">No</span></span>       |

## <a name="file-location"></a><span data-ttu-id="d001c-180">Emplacement du fichier</span><span class="sxs-lookup"><span data-stu-id="d001c-180">File Location</span></span>

<span data-ttu-id="d001c-181">Les manifestes d’application doivent être inclus en tant que ressource dans le fichier EXE ou la DLL de l’application.</span><span class="sxs-lookup"><span data-stu-id="d001c-181">Application manifests should be included as a resource in the application's EXE file or DLL.</span></span>

<span data-ttu-id="d001c-182">Pour plus d’informations, consultez [installation d’assemblys côte à côte](installing-side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="d001c-182">For more information, see [Installing Side-by-side Assemblies](installing-side-by-side-assemblies.md).</span></span>

## <a name="file-name-syntax"></a><span data-ttu-id="d001c-183">Syntaxe du nom de fichier</span><span class="sxs-lookup"><span data-stu-id="d001c-183">File Name Syntax</span></span>

<span data-ttu-id="d001c-184">Le nom d’un fichier manifeste d’application est le nom de l’exécutable de l’application suivi de. manifest.</span><span class="sxs-lookup"><span data-stu-id="d001c-184">The name of an application manifest file is the name of the application's executable followed by .manifest.</span></span>

<span data-ttu-id="d001c-185">Par exemple, un manifeste d’application qui fait référence à example.exe ou example.dll utiliserait la syntaxe de nom de fichier suivante.</span><span class="sxs-lookup"><span data-stu-id="d001c-185">For example, an application manifest that refers to example.exe or example.dll would use the following file name syntax.</span></span> <span data-ttu-id="d001c-186">Vous pouvez omettre le champ *ID de ressource* <> si l’ID de ressource est 1.</span><span class="sxs-lookup"><span data-stu-id="d001c-186">You can omit the <*resource ID*> field if resource ID is 1.</span></span>

<span data-ttu-id="d001c-187">***ID de ressource* example.exe. <>. manifest**</span><span class="sxs-lookup"><span data-stu-id="d001c-187">**example.exe.<*resource ID*>.manifest**</span></span>

<span data-ttu-id="d001c-188">***ID de ressource* example.dll. <>. manifest**</span><span class="sxs-lookup"><span data-stu-id="d001c-188">**example.dll.<*resource ID*>.manifest**</span></span>

## <a name="elements"></a><span data-ttu-id="d001c-189">Éléments</span><span class="sxs-lookup"><span data-stu-id="d001c-189">Elements</span></span>

<span data-ttu-id="d001c-190">Les noms des éléments et des attributs respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="d001c-190">Names of elements and attributes are case-sensitive.</span></span> <span data-ttu-id="d001c-191">Les valeurs des éléments et des attributs ne respectent pas la casse, à l’exception de la valeur de l’attribut type.</span><span class="sxs-lookup"><span data-stu-id="d001c-191">The values of elements and attributes are case-insensitive, except for the value of the type attribute.</span></span>

<span id="assembly"></span><span id="ASSEMBLY"></span>

### <a name="assembly"></a><span data-ttu-id="d001c-192">assembly</span><span class="sxs-lookup"><span data-stu-id="d001c-192">assembly</span></span>

<span data-ttu-id="d001c-193">Élément conteneur.</span><span class="sxs-lookup"><span data-stu-id="d001c-193">A container element.</span></span> <span data-ttu-id="d001c-194">Son premier sous-élément doit être un élément **NoInherit** ou **assemblyIdentity** .</span><span class="sxs-lookup"><span data-stu-id="d001c-194">Its first subelement must be a **noInherit** or **assemblyIdentity** element.</span></span> <span data-ttu-id="d001c-195">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d001c-195">Required.</span></span>

<span data-ttu-id="d001c-196">L’élément **assembly** doit figurer dans l’espace de noms « urn : schemas-microsoft-com : ASM. v1 ».</span><span class="sxs-lookup"><span data-stu-id="d001c-196">The **assembly** element must be in the namespace "urn:schemas-microsoft-com:asm.v1".</span></span> <span data-ttu-id="d001c-197">Les éléments enfants de l’assembly doivent également être dans cet espace de noms, par héritage ou par balisage.</span><span class="sxs-lookup"><span data-stu-id="d001c-197">Child elements of the assembly must also be in this namespace, by inheritance or by tagging.</span></span>

<span data-ttu-id="d001c-198">L’élément **assembly** a les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="d001c-198">The **assembly** element has the following attributes.</span></span>



| <span data-ttu-id="d001c-199">Attribut</span><span class="sxs-lookup"><span data-stu-id="d001c-199">Attribute</span></span>           | <span data-ttu-id="d001c-200">Description</span><span class="sxs-lookup"><span data-stu-id="d001c-200">Description</span></span>                                           |
|---------------------|-------------------------------------------------------|
| <span data-ttu-id="d001c-201">**manifestVersion**</span><span class="sxs-lookup"><span data-stu-id="d001c-201">**manifestVersion**</span></span> | <span data-ttu-id="d001c-202">L’attribut **manifestVersion** doit avoir la valeur 1,0.</span><span class="sxs-lookup"><span data-stu-id="d001c-202">The **manifestVersion** attribute must be set to 1.0.</span></span> |


<span id="noInherit"></span><span id="noinherit"></span><span id="NOINHERIT"></span>

### <a name="noinherit"></a><span data-ttu-id="d001c-203">noInherit</span><span class="sxs-lookup"><span data-stu-id="d001c-203">noInherit</span></span>

<span data-ttu-id="d001c-204">Incluez cet élément dans un manifeste d’application pour définir les [contextes d’activation](activation-contexts.md) générés à partir du manifeste avec l’indicateur « no Inherit ».</span><span class="sxs-lookup"><span data-stu-id="d001c-204">Include this element in an application manifest to set the [activation contexts](activation-contexts.md) generated from the manifest with the "no inherit" flag.</span></span> <span data-ttu-id="d001c-205">Lorsque cet indicateur n’est pas défini dans un contexte d’activation et que le contexte d’activation est actif, il est hérité par les nouveaux threads dans les mêmes processus, fenêtres, procédures de fenêtre et [appels de procédure asynchrone](/windows/desktop/Sync/asynchronous-procedure-calls).</span><span class="sxs-lookup"><span data-stu-id="d001c-205">When this flag is not set in an activation context, and the activation context is active, it is inherited by new threads in the same process, windows, window procedures, and [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span> <span data-ttu-id="d001c-206">La définition de cet indicateur empêche le nouvel objet d’hériter du contexte actif.</span><span class="sxs-lookup"><span data-stu-id="d001c-206">Setting this flag prevents the new object from inheriting the active context.</span></span>

<span data-ttu-id="d001c-207">L’élément **NoInherit** est facultatif et généralement omis.</span><span class="sxs-lookup"><span data-stu-id="d001c-207">The **noInherit** element is optional and typically omitted.</span></span> <span data-ttu-id="d001c-208">La plupart des assemblys ne fonctionnent pas correctement à l’aide d’un contexte d’activation sans héritage, car l’assembly doit être conçu explicitement pour gérer la propagation de son propre contexte d’activation.</span><span class="sxs-lookup"><span data-stu-id="d001c-208">Most assemblies do not work correctly using a no-inherit activation context because the assembly must be explicitly designed to manage the propagation of their own activation context.</span></span> <span data-ttu-id="d001c-209">L’utilisation de l’élément **NoInherit** requiert que tous les assemblys dépendants référencés par le manifeste d’application aient un élément **noinherits** dans leur [manifeste d’assembly](assembly-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="d001c-209">The use of the **noInherit** element requires that any dependent assemblies referenced by the application manifest have a **noInherit** element in their [assembly manifest](assembly-manifests.md).</span></span>

<span data-ttu-id="d001c-210">Si **NoInherit** est utilisé dans un manifeste, il doit s’agir du premier sous-élément de l’élément **assembly** .</span><span class="sxs-lookup"><span data-stu-id="d001c-210">If **noInherit** is used in a manifest, it must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="d001c-211">L’élément **assemblyIdentity** doit être placé immédiatement après l’élément **NoInherit** .</span><span class="sxs-lookup"><span data-stu-id="d001c-211">The **assemblyIdentity** element should come immediately after the **noInherit** element.</span></span> <span data-ttu-id="d001c-212">Si **NoInherit** n’est pas utilisé, **assemblyIdentity** doit être le premier sous-élément de l’élément **assembly** .</span><span class="sxs-lookup"><span data-stu-id="d001c-212">If **noInherit** is not used, **assemblyIdentity** must be the first subelement of the **assembly** element.</span></span> <span data-ttu-id="d001c-213">L’élément **NoInherit** n’a pas d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="d001c-213">The **noInherit** element has no child elements.</span></span> <span data-ttu-id="d001c-214">Il ne s’agit pas d’un élément valide dans les [manifestes d’assembly](assembly-manifests.md).</span><span class="sxs-lookup"><span data-stu-id="d001c-214">It is not a valid element in [assembly manifests](assembly-manifests.md).</span></span>

<span id="assemblyIdentity"></span><span id="assemblyidentity"></span><span id="ASSEMBLYIDENTITY"></span>

### <a name="assemblyidentity"></a><span data-ttu-id="d001c-215">assemblyIdentity</span><span class="sxs-lookup"><span data-stu-id="d001c-215">assemblyIdentity</span></span>

<span data-ttu-id="d001c-216">En tant que premier sous-élément d’un élément **assembly** , **assemblyIdentity** décrit et identifie de façon unique l’application qui possède ce manifeste d’application.</span><span class="sxs-lookup"><span data-stu-id="d001c-216">As the first subelement of an **assembly** element, **assemblyIdentity** describes and uniquely identifies the application owning this application manifest.</span></span> <span data-ttu-id="d001c-217">En tant que premier sous-élément d’un élément **dependentAssembly** , **assemblyIdentity** décrit un assembly côte à côte requis par l’application.</span><span class="sxs-lookup"><span data-stu-id="d001c-217">As the first subelement of a **dependentAssembly** element, **assemblyIdentity** describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="d001c-218">Notez que chaque assembly référencé dans le manifeste de l’application nécessite un **assemblyIdentity** qui correspond exactement à l’expression **assemblyIdentity** dans le manifeste de l’assembly de l’assembly référencé.</span><span class="sxs-lookup"><span data-stu-id="d001c-218">Note that every assembly referenced in the application manifest requires an **assemblyIdentity** that exactly matches the **assemblyIdentity** in the referenced assembly's own assembly manifest.</span></span>

<span data-ttu-id="d001c-219">L’élément **assemblyIdentity** a les attributs suivants.</span><span class="sxs-lookup"><span data-stu-id="d001c-219">The **assemblyIdentity** element has the following attributes.</span></span> <span data-ttu-id="d001c-220">Il n’a pas de sous-éléments.</span><span class="sxs-lookup"><span data-stu-id="d001c-220">It has no subelements.</span></span>

| <span data-ttu-id="d001c-221">Attribut</span><span class="sxs-lookup"><span data-stu-id="d001c-221">Attribute</span></span>                 | <span data-ttu-id="d001c-222">Description</span><span class="sxs-lookup"><span data-stu-id="d001c-222">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d001c-223">**type**</span><span class="sxs-lookup"><span data-stu-id="d001c-223">**type**</span></span>                  | <span data-ttu-id="d001c-224">Spécifie l’application ou le type d’assembly.</span><span class="sxs-lookup"><span data-stu-id="d001c-224">Specifies the application or assembly type.</span></span> <span data-ttu-id="d001c-225">La valeur doit être Win32 et tout en minuscules.</span><span class="sxs-lookup"><span data-stu-id="d001c-225">The value must be Win32 and all in lower case.</span></span> <span data-ttu-id="d001c-226">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d001c-226">Required.</span></span>                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d001c-227">**name**</span><span class="sxs-lookup"><span data-stu-id="d001c-227">**name**</span></span>                  | <span data-ttu-id="d001c-228">Nomme l’application ou l’assembly de manière unique.</span><span class="sxs-lookup"><span data-stu-id="d001c-228">Uniquely names the application or assembly.</span></span> <span data-ttu-id="d001c-229">Utilisez le format suivant pour le nom : Organization.Division.Name.</span><span class="sxs-lookup"><span data-stu-id="d001c-229">Use the following format for the name: Organization.Division.Name.</span></span> <span data-ttu-id="d001c-230">Par exemple, Microsoft. Windows. mysampleApp.</span><span class="sxs-lookup"><span data-stu-id="d001c-230">For example Microsoft.Windows.mysampleApp.</span></span> <span data-ttu-id="d001c-231">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d001c-231">Required.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="d001c-232">**language**</span><span class="sxs-lookup"><span data-stu-id="d001c-232">**language**</span></span>              | <span data-ttu-id="d001c-233">Identifie la langue de l’application ou de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="d001c-233">Identifies the language of the application or assembly.</span></span> <span data-ttu-id="d001c-234">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d001c-234">Optional.</span></span> <span data-ttu-id="d001c-235">Si l’application ou l’assembly est spécifique à une langue, spécifiez le code de langue DHTML.</span><span class="sxs-lookup"><span data-stu-id="d001c-235">If the application or assembly is language-specific, specify the DHTML language code.</span></span> <span data-ttu-id="d001c-236">Dans le champ **assemblyIdentity** d’une application destinée à une utilisation mondiale (indépendant de la langue), omettez l’attribut Language.</span><span class="sxs-lookup"><span data-stu-id="d001c-236">In the **assemblyIdentity** of an application intended for worldwide use (language neutral) omit the language attribute.</span></span><br/> <span data-ttu-id="d001c-237">Dans un **assemblyIdentity** d’un assembly destiné à une utilisation dans le monde entier (indépendant de la langue), définissez la valeur de Language sur « \* ».</span><span class="sxs-lookup"><span data-stu-id="d001c-237">In an **assemblyIdentity** of an assembly intended for worldwide use (language neutral) set the value of language to "\*".</span></span><br/> |
| <span data-ttu-id="d001c-238">**processorArchitecture**</span><span class="sxs-lookup"><span data-stu-id="d001c-238">**processorArchitecture**</span></span> | <span data-ttu-id="d001c-239">Spécifie le processeur.</span><span class="sxs-lookup"><span data-stu-id="d001c-239">Specifies the processor.</span></span> <span data-ttu-id="d001c-240">Les valeurs autorisées sont `x86`, `amd64`, `arm` et `arm64`.</span><span class="sxs-lookup"><span data-stu-id="d001c-240">Valid values include `x86`, `amd64`, `arm` and `arm64`.</span></span> <span data-ttu-id="d001c-241">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d001c-241">Optional.</span></span>                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d001c-242">**version**</span><span class="sxs-lookup"><span data-stu-id="d001c-242">**version**</span></span>               | <span data-ttu-id="d001c-243">Spécifie la version de l’application ou de l’assembly.</span><span class="sxs-lookup"><span data-stu-id="d001c-243">Specifies the application or assembly version.</span></span> <span data-ttu-id="d001c-244">Utilisez le format de version en quatre parties : MMMM. nnnnn. ooooo. ppppp.</span><span class="sxs-lookup"><span data-stu-id="d001c-244">Use the four-part version format: mmmmm.nnnnn.ooooo.ppppp.</span></span> <span data-ttu-id="d001c-245">Chacun des composants séparés par des points peut être de 0-65535 inclus.</span><span class="sxs-lookup"><span data-stu-id="d001c-245">Each of the parts separated by periods can be 0-65535 inclusive.</span></span> <span data-ttu-id="d001c-246">Pour plus d’informations, consultez [versions d’assembly](assembly-versions.md).</span><span class="sxs-lookup"><span data-stu-id="d001c-246">For more information, see [Assembly Versions](assembly-versions.md).</span></span> <span data-ttu-id="d001c-247">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d001c-247">Required.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="d001c-248">**publicKeyToken**</span><span class="sxs-lookup"><span data-stu-id="d001c-248">**publicKeyToken**</span></span>        | <span data-ttu-id="d001c-249">Chaîne hexadécimale de 16 caractères représentant les 8 derniers octets du hachage SHA-1 de la clé publique sous laquelle l’application ou l’assembly est signé.</span><span class="sxs-lookup"><span data-stu-id="d001c-249">A 16-character hexadecimal string representing the last 8 bytes of the SHA-1 hash of the public key under which the application or assembly is signed.</span></span> <span data-ttu-id="d001c-250">La clé publique utilisée pour signer le catalogue doit être supérieure ou égale à 2048 bits.</span><span class="sxs-lookup"><span data-stu-id="d001c-250">The public key used to sign the catalog must be 2048 bits or greater.</span></span> <span data-ttu-id="d001c-251">Obligatoire pour tous les assemblys côte à côte partagés.</span><span class="sxs-lookup"><span data-stu-id="d001c-251">Required for all shared side-by-side assemblies.</span></span>                                                                                                                                                     |

<span id="compatibility"></span><span id="COMPATIBILITY"></span>

### <a name="compatibility"></a><span data-ttu-id="d001c-252">compatibilité</span><span class="sxs-lookup"><span data-stu-id="d001c-252">compatibility</span></span>

<span data-ttu-id="d001c-253">Contient au moins une **application**.</span><span class="sxs-lookup"><span data-stu-id="d001c-253">Contains at least one **application**.</span></span> <span data-ttu-id="d001c-254">Elle n’a pas d’attribut.</span><span class="sxs-lookup"><span data-stu-id="d001c-254">It has no attributes.</span></span> <span data-ttu-id="d001c-255">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d001c-255">Optional.</span></span> <span data-ttu-id="d001c-256">Les manifestes d’application sans élément de compatibilité ont par défaut la compatibilité avec Windows Vista sur Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d001c-256">Application manifests without a compatibility element default to Windows Vista compatibility on Windows 7.</span></span>

<span id="application"></span><span id="APPLICATION"></span>

### <a name="application"></a><span data-ttu-id="d001c-257">application</span><span class="sxs-lookup"><span data-stu-id="d001c-257">application</span></span>

<span data-ttu-id="d001c-258">Contient au moins un élémentos **pris en charge** .</span><span class="sxs-lookup"><span data-stu-id="d001c-258">Contains at least one **supportedOS** element.</span></span> <span data-ttu-id="d001c-259">À compter de Windows 10, la version 1903, elle peut également contenir un élément **maxversiontested** facultatif.</span><span class="sxs-lookup"><span data-stu-id="d001c-259">Starting in Windows 10, version 1903, it can also contain one optional **maxversiontested** element.</span></span> <span data-ttu-id="d001c-260">Elle n’a pas d’attribut.</span><span class="sxs-lookup"><span data-stu-id="d001c-260">It has no attributes.</span></span> <span data-ttu-id="d001c-261">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d001c-261">Optional.</span></span>

<span id="supportedOS"></span><span id="supportedos"></span><span id="SUPPORTEDOS"></span>

### <a name="supportedos"></a><span data-ttu-id="d001c-262">pris en charge</span><span class="sxs-lookup"><span data-stu-id="d001c-262">supportedOS</span></span>

<span data-ttu-id="d001c-263">L’élément **pris en charge** a l’attribut suivant.</span><span class="sxs-lookup"><span data-stu-id="d001c-263">The **supportedOS** element has the following attribute.</span></span> <span data-ttu-id="d001c-264">Il n’a pas de sous-éléments.</span><span class="sxs-lookup"><span data-stu-id="d001c-264">It has no subelements.</span></span>

| <span data-ttu-id="d001c-265">Attribut</span><span class="sxs-lookup"><span data-stu-id="d001c-265">Attribute</span></span> | <span data-ttu-id="d001c-266">Description</span><span class="sxs-lookup"><span data-stu-id="d001c-266">Description</span></span>   |
|-----------|-----------------------|
| <span data-ttu-id="d001c-267">**Id**</span><span class="sxs-lookup"><span data-stu-id="d001c-267">**Id**</span></span>    | <span data-ttu-id="d001c-268">Affectez à l’attribut ID la valeur **{e2011457-1546-43C5-a5fe-008deee3d3f0}** pour exécuter l’application à l’aide de la fonctionnalité Vista.</span><span class="sxs-lookup"><span data-stu-id="d001c-268">Set the Id attribute to **{e2011457-1546-43c5-a5fe-008deee3d3f0}** to run the application using Vista functionality.</span></span> <span data-ttu-id="d001c-269">Cela peut permettre à une application conçue pour Windows Vista de s’exécuter sur un système d’exploitation ultérieur.</span><span class="sxs-lookup"><span data-stu-id="d001c-269">This can enable an application designed for Windows Vista to run on a later operating system.</span></span> <br/> <span data-ttu-id="d001c-270">Affectez à l’attribut ID la valeur **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** pour exécuter l’application à l’aide de la fonctionnalité Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d001c-270">Set the Id attribute to **{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** to run the application using Windows 7 functionality.</span></span><br/> <span data-ttu-id="d001c-271">Les applications qui prennent en charge les fonctionnalités Windows Vista, Windows 7 et Windows 8 ne nécessitent pas de manifestes distincts.</span><span class="sxs-lookup"><span data-stu-id="d001c-271">Applications that support Windows Vista, Windows 7, and Windows 8 functionality do not require separate manifests.</span></span> <span data-ttu-id="d001c-272">Dans ce cas, ajoutez les GUID pour tous les systèmes d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="d001c-272">In this case, add the GUIDs for all the Windows operating systems.</span></span><br/> <span data-ttu-id="d001c-273">Pour plus d’informations sur le comportement de l’attribut **ID** dans Windows, consultez le livre de recettes sur la [compatibilité avec Windows 8 et Windows Server 2012](https://www.microsoft.com/download/details.aspx?id=27416).</span><span class="sxs-lookup"><span data-stu-id="d001c-273">For info about the **Id** attribute behavior in Windows, see the [Windows 8 and Windows Server 2012 Compatibility Cookbook](https://www.microsoft.com/download/details.aspx?id=27416).</span></span><br/> <span data-ttu-id="d001c-274">Les GUID suivants correspondent aux systèmes d’exploitation indiqués :</span><span class="sxs-lookup"><span data-stu-id="d001c-274">The following GUIDs correspond with the indicated operating systems:</span></span><br/> <span data-ttu-id="d001c-275">**{8e0f7a12-bfb3-4FE8-B9A5-48fd50a15a9a}** -> Windows 10, windows server 2016 et windows server 2019</span><span class="sxs-lookup"><span data-stu-id="d001c-275">**{8e0f7a12-bfb3-4fe8-b9a5-48fd50a15a9a}** -> Windows 10, Windows Server 2016 and Windows Server 2019</span></span><br/> <span data-ttu-id="d001c-276">**{1f676c76-80E1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 et Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d001c-276">**{1f676c76-80e1-4239-95bb-83d0f6d0da78}** -> Windows 8.1 and Windows Server 2012 R2</span></span><br/> <span data-ttu-id="d001c-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 et windows server 2012</span><span class="sxs-lookup"><span data-stu-id="d001c-277">**{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}** -> Windows 8 and Windows Server 2012</span></span><br/> <span data-ttu-id="d001c-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 et windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d001c-278">**{35138b9a-5d96-4fbd-8e2d-a2440225f93a}** -> Windows 7 and Windows Server 2008 R2</span></span><br/> <span data-ttu-id="d001c-279">**{e2011457-1546-43C5-a5fe-008deee3d3f0}** -> Windows Vista et windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d001c-279">**{e2011457-1546-43c5-a5fe-008deee3d3f0}** -> Windows Vista and Windows Server 2008</span></span><br/> <span data-ttu-id="d001c-280">Vous pouvez tester cela sur Windows 7 ou Windows 8. x en exécutant moniteur de ressource (resmon), en accédant à l’onglet UC, en cliquant avec le bouton droit sur les étiquettes de colonne, « sélectionner une colonne... » et en cochant « contexte du système d’exploitation ».</span><span class="sxs-lookup"><span data-stu-id="d001c-280">You can test this on Windows 7 or Windows 8.x by running Resource Monitor (resmon), going to the CPU tab, right-clicking on the column labels, "Select Column...", and check "Operating System Context".</span></span> <span data-ttu-id="d001c-281">Sur Windows 8. x, vous trouverez également cette colonne disponible dans le gestionnaire des tâches (taskmgr).</span><span class="sxs-lookup"><span data-stu-id="d001c-281">On Windows 8.x, you can also find this column available in the Task Manager (taskmgr).</span></span> <span data-ttu-id="d001c-282">Le contenu de la colonne indique la valeur la plus élevée trouvée ou « Windows Vista » comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d001c-282">The content of the column shows the highest value found or "Windows Vista" as the default.</span></span> <br/> |

<span id="maxVersionTested"></span><span id="maxversiontested"></span><span id="MAXVERSIONTESTED"></span>

### <a name="maxversiontested"></a><span data-ttu-id="d001c-283">maxversiontested</span><span class="sxs-lookup"><span data-stu-id="d001c-283">maxversiontested</span></span>

<span data-ttu-id="d001c-284">L’élément **maxversiontested** spécifie les versions de Windows sur lesquelles l’application a été testée, en commençant par la version minimale du système d’exploitation que l’application prend en charge jusqu’à la version maximale.</span><span class="sxs-lookup"><span data-stu-id="d001c-284">The **maxversiontested** element specifies the versions of Windows that the application was tested against starting with the minimum OS version the application supports up to the maximum version.</span></span> <span data-ttu-id="d001c-285">L’ensemble complet des versions est disponible [ici](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span><span class="sxs-lookup"><span data-stu-id="d001c-285">The complete set of versions can be found [here](https://developer.microsoft.com/windows/downloads/sdk-archive/).</span></span> <span data-ttu-id="d001c-286">Elle est destinée à être utilisée par les applications de bureau qui utilisent des [îlots XAML](/windows/apps/desktop/modernize/xaml-islands) et qui ne sont pas déployées dans un package MSIX.</span><span class="sxs-lookup"><span data-stu-id="d001c-286">This is intended to be used by desktop applications that use [XAML Islands](/windows/apps/desktop/modernize/xaml-islands) and that are not deployed in an MSIX package.</span></span> <span data-ttu-id="d001c-287">Cet élément est pris en charge dans Windows 10, version 1903 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d001c-287">This element is supported in Windows 10, version 1903, and later versions.</span></span>

<span data-ttu-id="d001c-288">L’élément **maxversiontested** a l’attribut suivant.</span><span class="sxs-lookup"><span data-stu-id="d001c-288">The **maxversiontested** element has the following attribute.</span></span> <span data-ttu-id="d001c-289">Il n’a pas de sous-éléments.</span><span class="sxs-lookup"><span data-stu-id="d001c-289">It has no subelements.</span></span>

| <span data-ttu-id="d001c-290">Attribut</span><span class="sxs-lookup"><span data-stu-id="d001c-290">Attribute</span></span> | <span data-ttu-id="d001c-291">Description</span><span class="sxs-lookup"><span data-stu-id="d001c-291">Description</span></span>    |
|-----------|----------------|
| <span data-ttu-id="d001c-292">**Id**</span><span class="sxs-lookup"><span data-stu-id="d001c-292">**Id**</span></span>    | <span data-ttu-id="d001c-293">Définissez l’attribut ID sur une chaîne de version en 4 parties qui spécifie la version maximale des fenêtres pour lesquelles l’application a été testée.</span><span class="sxs-lookup"><span data-stu-id="d001c-293">Set the Id attribute to a 4-part version string that specifies the maximum version of Windows that the application was tested against.</span></span> <span data-ttu-id="d001c-294">Par exemple, « 10.0.18226.0 ».</span><span class="sxs-lookup"><span data-stu-id="d001c-294">For example, "10.0.18226.0".</span></span> |

<span id="dependency"></span><span id="DEPENDENCY"></span>

### <a name="dependency"></a><span data-ttu-id="d001c-295">dependency</span><span class="sxs-lookup"><span data-stu-id="d001c-295">dependency</span></span>

<span data-ttu-id="d001c-296">Contient au moins un **dependentAssembly**.</span><span class="sxs-lookup"><span data-stu-id="d001c-296">Contains at least one **dependentAssembly**.</span></span> <span data-ttu-id="d001c-297">Elle n’a pas d’attribut.</span><span class="sxs-lookup"><span data-stu-id="d001c-297">It has no attributes.</span></span> <span data-ttu-id="d001c-298">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d001c-298">Optional.</span></span>

<span id="dependentAssembly"></span><span id="dependentassembly"></span><span id="DEPENDENTASSEMBLY"></span>

### <a name="dependentassembly"></a><span data-ttu-id="d001c-299">dependentAssembly</span><span class="sxs-lookup"><span data-stu-id="d001c-299">dependentAssembly</span></span>

<span data-ttu-id="d001c-300">Le premier sous-élément de **dependentAssembly** doit être un élément **assemblyIdentity** qui décrit un assembly côte à côte requis par l’application.</span><span class="sxs-lookup"><span data-stu-id="d001c-300">The first subelement of **dependentAssembly** must be an **assemblyIdentity** element that describes a side-by-side assembly required by the application.</span></span> <span data-ttu-id="d001c-301">Chaque **dependentAssembly** doit se trouver à l’intérieur d’une seule **dépendance**.</span><span class="sxs-lookup"><span data-stu-id="d001c-301">Every **dependentAssembly** must be inside exactly one **dependency**.</span></span> <span data-ttu-id="d001c-302">Elle n’a pas d’attribut.</span><span class="sxs-lookup"><span data-stu-id="d001c-302">It has no attributes.</span></span>

<span id="file"></span><span id="FILE"></span>

### <a name="file"></a><span data-ttu-id="d001c-303">fichier</span><span class="sxs-lookup"><span data-stu-id="d001c-303">file</span></span>

<span data-ttu-id="d001c-304">Spécifie les fichiers qui sont privés pour l’application.</span><span class="sxs-lookup"><span data-stu-id="d001c-304">Specifies files that are private to the application.</span></span> <span data-ttu-id="d001c-305">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d001c-305">Optional.</span></span>

<span data-ttu-id="d001c-306">L’élément **file** a les attributs indiqués dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d001c-306">The **file** element has the attributes shown in the following table.</span></span>



| <span data-ttu-id="d001c-307">Attribut</span><span class="sxs-lookup"><span data-stu-id="d001c-307">Attribute</span></span>   | <span data-ttu-id="d001c-308">Description</span><span class="sxs-lookup"><span data-stu-id="d001c-308">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d001c-309">**name**</span><span class="sxs-lookup"><span data-stu-id="d001c-309">**name**</span></span>    | <span data-ttu-id="d001c-310">Nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="d001c-310">Name of the file.</span></span> <span data-ttu-id="d001c-311">Par exemple, Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="d001c-311">For example, Comctl32.dll.</span></span>                                                            |
| <span data-ttu-id="d001c-312">**hashAlg**</span><span class="sxs-lookup"><span data-stu-id="d001c-312">**hashalg**</span></span> | <span data-ttu-id="d001c-313">Algorithme utilisé pour créer un hachage du fichier.</span><span class="sxs-lookup"><span data-stu-id="d001c-313">Algorithm used to create a hash of the file.</span></span> <span data-ttu-id="d001c-314">Cette valeur doit être SHA1.</span><span class="sxs-lookup"><span data-stu-id="d001c-314">This value should be SHA1.</span></span>                                 |
| <span data-ttu-id="d001c-315">**hash**</span><span class="sxs-lookup"><span data-stu-id="d001c-315">**hash**</span></span>    | <span data-ttu-id="d001c-316">Hachage du fichier référencé par nom.</span><span class="sxs-lookup"><span data-stu-id="d001c-316">A hash of the file referred to by name.</span></span> <span data-ttu-id="d001c-317">Chaîne hexadécimale de longueur selon l’algorithme de hachage.</span><span class="sxs-lookup"><span data-stu-id="d001c-317">A hexadecimal string of length depending on the hash algorithm.</span></span> |

<span id="activeCodePage"></span><span id="activecodepage"></span><span id="ACTIVECODEPAGE"></span>

### <a name="activecodepage"></a><span data-ttu-id="d001c-318">activeCodePage</span><span class="sxs-lookup"><span data-stu-id="d001c-318">activeCodePage</span></span>

<span data-ttu-id="d001c-319">Forcez un processus à utiliser UTF-8 comme page de code de processus.</span><span class="sxs-lookup"><span data-stu-id="d001c-319">Force a process to use UTF-8 as the process code page.</span></span>

<span data-ttu-id="d001c-320">**activeCodePage** a été ajouté dans Windows version 1903 (mise à jour de mai 2019).</span><span class="sxs-lookup"><span data-stu-id="d001c-320">**activeCodePage** was added in Windows Version 1903 (May 2019 Update).</span></span> <span data-ttu-id="d001c-321">Vous pouvez déclarer cette propriété et la cible/exécuter sur des versions précédentes de Windows, mais vous devez gérer la détection et la conversion de pages de codes héritées comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="d001c-321">You can declare this property and target/run on earlier Windows builds, but you must handle legacy code page detection and conversion as usual.</span></span> <span data-ttu-id="d001c-322">Pour plus d’informations, consultez [utiliser la page de codes UTF-8](/windows/uwp/design/globalizing/use-utf8-code-page) .</span><span class="sxs-lookup"><span data-stu-id="d001c-322">See [Use the UTF-8 code page](/windows/uwp/design/globalizing/use-utf8-code-page) for details.</span></span>

<span data-ttu-id="d001c-323">Cet élément n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="d001c-323">This element has no attributes.</span></span> <span data-ttu-id="d001c-324">**UTF-8 est une** valeur valide uniquement pour l’élément **activeCodePage** .</span><span class="sxs-lookup"><span data-stu-id="d001c-324">**UTF-8** is only valid value for **activeCodePage** element.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2019/WindowsSettings"> 
      <activeCodePage>UTF-8</activeCodePage> 
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="autoElevate"></span><span id="autoelevate"></span><span id="AUTOELEVATE"></span>

### <a name="autoelevate"></a><span data-ttu-id="d001c-325">Élever</span><span class="sxs-lookup"><span data-stu-id="d001c-325">autoElevate</span></span>

<span data-ttu-id="d001c-326">Spécifie si l’élévation automatique est activée.</span><span class="sxs-lookup"><span data-stu-id="d001c-326">Specifies whether auto elevate is enabled.</span></span> <span data-ttu-id="d001c-327">La **valeur true** indique qu’elle est activée.</span><span class="sxs-lookup"><span data-stu-id="d001c-327">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="d001c-328">Elle n’a pas d’attribut.</span><span class="sxs-lookup"><span data-stu-id="d001c-328">It has no attributes.</span></span>

<span id="disableTheming"></span><span id="disabletheming"></span><span id="DISABLETHEMING"></span>

### <a name="disabletheming"></a><span data-ttu-id="d001c-329">disableTheming</span><span class="sxs-lookup"><span data-stu-id="d001c-329">disableTheming</span></span>

<span data-ttu-id="d001c-330">Spécifie si les éléments d’interface utilisateur d’un thème sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="d001c-330">Specifies whether giving UI elements a theme is disabled.</span></span> <span data-ttu-id="d001c-331">**True** indique que l’activation est désactivée.</span><span class="sxs-lookup"><span data-stu-id="d001c-331">**TRUE** indicates disabled.</span></span> <span data-ttu-id="d001c-332">Elle n’a pas d’attribut.</span><span class="sxs-lookup"><span data-stu-id="d001c-332">It has no attributes.</span></span>

<span id="disableWindowFiltering"></span><span id="disablewindowfiltering"></span><span id="DISABLEWINDOWFILTERING"></span>

### <a name="disablewindowfiltering"></a><span data-ttu-id="d001c-333">disableWindowFiltering</span><span class="sxs-lookup"><span data-stu-id="d001c-333">disableWindowFiltering</span></span>

<span data-ttu-id="d001c-334">Spécifie s’il faut désactiver le filtrage de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d001c-334">Specifies whether to disable window filtering.</span></span> <span data-ttu-id="d001c-335">**True** désactive le filtrage de fenêtre pour vous permettre d’énumérer les fenêtres immersives à partir du bureau.</span><span class="sxs-lookup"><span data-stu-id="d001c-335">**TRUE** disables window filtering so you can enumerate immersive windows from the desktop.</span></span> <span data-ttu-id="d001c-336">**disableWindowFiltering** a été ajouté dans Windows 8 et n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="d001c-336">**disableWindowFiltering** was added in Windows 8 and has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <disableWindowFiltering>true</disableWindowFiltering>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAware"></span><span id="dpiaware"></span><span id="DPIAWARE"></span>

### <a name="dpiaware"></a><span data-ttu-id="d001c-337">dpiAware</span><span class="sxs-lookup"><span data-stu-id="d001c-337">dpiAware</span></span>

<span data-ttu-id="d001c-338">Spécifie si le processus actuel prend en charge la résolution en points par pouce (dpi).</span><span class="sxs-lookup"><span data-stu-id="d001c-338">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="d001c-339">**Windows 10, version 1607 :** L’élément **dpiAware** est ignoré si l’élément **dpiAwareness** est présent.</span><span class="sxs-lookup"><span data-stu-id="d001c-339">**Windows 10, version 1607:** The **dpiAware** element is ignored if the **dpiAwareness** element is present.</span></span> <span data-ttu-id="d001c-340">Vous pouvez inclure les deux éléments dans un manifeste si vous souhaitez spécifier un comportement différent pour Windows 10, version 1607 que pour une version antérieure du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d001c-340">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="d001c-341">Le tableau suivant décrit le comportement qui se produit en fonction de la présence de l’élément **dpiAware** et du texte qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="d001c-341">The following table describes the behavior that results based upon the presence of the **dpiAware** element and the text that it contains.</span></span> <span data-ttu-id="d001c-342">Le texte contenu dans l’élément n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="d001c-342">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="d001c-343">État de l’élément **dpiAware**</span><span class="sxs-lookup"><span data-stu-id="d001c-343">State of the **dpiAware** element</span></span> | <span data-ttu-id="d001c-344">Description</span><span class="sxs-lookup"><span data-stu-id="d001c-344">Description</span></span>     |
|-----------------------------------|---------|
| <span data-ttu-id="d001c-345">Absent</span><span class="sxs-lookup"><span data-stu-id="d001c-345">Absent</span></span>                            | <span data-ttu-id="d001c-346">Le processus actuel ne prend pas en charge DPI par défaut.</span><span class="sxs-lookup"><span data-stu-id="d001c-346">The current process is dpi unaware by default.</span></span> <span data-ttu-id="d001c-347">Vous pouvez modifier ce paramètre par programmation en appelant la fonction [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="d001c-347">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>                                                                                                                                                            |
| <span data-ttu-id="d001c-348">Contient « true »</span><span class="sxs-lookup"><span data-stu-id="d001c-348">Contains "true"</span></span>                   | <span data-ttu-id="d001c-349">Le processus actuel prend en charge la résolution du système.</span><span class="sxs-lookup"><span data-stu-id="d001c-349">The current process is system dpi aware.</span></span>                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d001c-350">Contient « false »</span><span class="sxs-lookup"><span data-stu-id="d001c-350">Contains "false"</span></span>                  | <span data-ttu-id="d001c-351">**Windows Vista, Windows 7 et Windows 8 :** Le comportement est le même que lorsque le **dpiAware** est absent.</span><span class="sxs-lookup"><span data-stu-id="d001c-351">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="d001c-352">**Windows 8.1 et Windows 10 :** Le processus actuel ne prend pas en charge dpi, et vous ne pouvez pas modifier ce paramètre par programmation en appelant la fonction [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="d001c-352">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |
| <span data-ttu-id="d001c-353">Contient « true/PM »</span><span class="sxs-lookup"><span data-stu-id="d001c-353">Contains "true/pm"</span></span>                | <span data-ttu-id="d001c-354">**Windows Vista, Windows 7 et Windows 8 :** Le processus actuel prend en charge la résolution du système.</span><span class="sxs-lookup"><span data-stu-id="d001c-354">**Windows Vista, Windows 7 and Windows 8:** The current process is system dpi aware.</span></span><br/> <span data-ttu-id="d001c-355">**Windows 8.1 et Windows 10 :** Le processus actuel prend en charge la résolution par moniteur.</span><span class="sxs-lookup"><span data-stu-id="d001c-355">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="d001c-356">Contient « par moniteur »</span><span class="sxs-lookup"><span data-stu-id="d001c-356">Contains "per monitor"</span></span>            | <span data-ttu-id="d001c-357">**Windows Vista, Windows 7 et Windows 8 :** Le comportement est le même que lorsque le **dpiAware** est absent.</span><span class="sxs-lookup"><span data-stu-id="d001c-357">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="d001c-358">**Windows 8.1 et Windows 10 :** Le processus actuel prend en charge la résolution par moniteur.</span><span class="sxs-lookup"><span data-stu-id="d001c-358">**Windows 8.1 and Windows 10:** The current process is per-monitor dpi aware.</span></span><br/>                                                                                                                                                                                      |
| <span data-ttu-id="d001c-359">Contient une autre chaîne</span><span class="sxs-lookup"><span data-stu-id="d001c-359">Contains any other string</span></span>         | <span data-ttu-id="d001c-360">**Windows Vista, Windows 7 et Windows 8 :** Le comportement est le même que lorsque le **dpiAware** est absent.</span><span class="sxs-lookup"><span data-stu-id="d001c-360">**Windows Vista, Windows 7 and Windows 8:** The behavior is the same as when the **dpiAware** is absent.</span></span><br/> <span data-ttu-id="d001c-361">**Windows 8.1 et Windows 10 :** Le processus actuel ne prend pas en charge dpi, et vous ne pouvez pas modifier ce paramètre par programmation en appelant la fonction [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="d001c-361">**Windows 8.1 and Windows 10:** The current process is dpi unaware, and you cannot programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span><br/> |

<span data-ttu-id="d001c-362">Pour plus d’informations sur les paramètres de reconnaissance dpi, consultez [comparaison des niveaux de détection PPP](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="d001c-362">For more information about dpi awareness settings, see [Comparison of DPI Awareness Levels](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

<span data-ttu-id="d001c-363">**dpiAware** n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="d001c-363">**dpiAware** has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
      <dpiAware>true</dpiAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="dpiAwareness"></span><span id="dpiawareness"></span><span id="DPIAWARENESS"></span>

### <a name="dpiawareness"></a><span data-ttu-id="d001c-364">dpiAwareness</span><span class="sxs-lookup"><span data-stu-id="d001c-364">dpiAwareness</span></span>

<span data-ttu-id="d001c-365">Spécifie si le processus actuel prend en charge la résolution en points par pouce (dpi).</span><span class="sxs-lookup"><span data-stu-id="d001c-365">Specifies whether the current process is dots per inch (dpi) aware.</span></span>

<span data-ttu-id="d001c-366">La version minimale du système d’exploitation qui prend en charge l’élément **dpiAwareness** est Windows 10, version 1607.</span><span class="sxs-lookup"><span data-stu-id="d001c-366">The minimum version of the operating system that supports the **dpiAwareness** element is Windows 10, version 1607.</span></span> <span data-ttu-id="d001c-367">Pour les versions qui prennent en charge l’élément **dpiAwareness** , **dpiAwareness** remplace l’élément **dpiAware** .</span><span class="sxs-lookup"><span data-stu-id="d001c-367">For versions that support the **dpiAwareness** element, the **dpiAwareness** overrides the **dpiAware** element.</span></span> <span data-ttu-id="d001c-368">Vous pouvez inclure les deux éléments dans un manifeste si vous souhaitez spécifier un comportement différent pour Windows 10, version 1607 que pour une version antérieure du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d001c-368">You can include both elements in a manifest if you want to specify a different behavior for Windows 10, version 1607 than for an earlier version of the operating system.</span></span>

<span data-ttu-id="d001c-369">L’élément **dpiAwareness** peut contenir un seul élément ou une liste d’éléments séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="d001c-369">The **dpiAwareness** element can contain a single item or a list of comma-separated items.</span></span> <span data-ttu-id="d001c-370">Dans ce dernier cas, le premier élément (le plus à gauche) dans la liste reconnue par le système d’exploitation est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d001c-370">In the latter case, the first (leftmost) item in the list recognized by the operating system is used.</span></span> <span data-ttu-id="d001c-371">De cette façon, vous pouvez spécifier des comportements différents pris en charge dans les versions ultérieures du système d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="d001c-371">In this way, you can specify different behaviors supported in future Windows operating system versions.</span></span>

<span data-ttu-id="d001c-372">Le tableau suivant décrit le comportement qui se produit en fonction de la présence de l’élément **dpiAwareness** et du texte qu’il contient dans son élément reconnu le plus à gauche.</span><span class="sxs-lookup"><span data-stu-id="d001c-372">The following table describes the behavior that results based upon the presence of the **dpiAwareness** element and the text that it contains in its leftmost recognized item.</span></span> <span data-ttu-id="d001c-373">Le texte contenu dans l’élément n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="d001c-373">The text within the element is not case-sensitive.</span></span>

| <span data-ttu-id="d001c-374">État de l’élément **dpiAwareness** :</span><span class="sxs-lookup"><span data-stu-id="d001c-374">**dpiAwareness** element status:</span></span>        | <span data-ttu-id="d001c-375">Description</span><span class="sxs-lookup"><span data-stu-id="d001c-375">Description</span></span>                          |
|-----------------------------------------|-------------------------------------------|
| <span data-ttu-id="d001c-376">L’élément est absent</span><span class="sxs-lookup"><span data-stu-id="d001c-376">Element is absent</span></span>                       | <span data-ttu-id="d001c-377">L’élément **dpiAware** spécifie si le processus prend en charge dpi.</span><span class="sxs-lookup"><span data-stu-id="d001c-377">The **dpiAware** element specifies whether the process is dpi aware.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="d001c-378">Ne contient aucun élément reconnu</span><span class="sxs-lookup"><span data-stu-id="d001c-378">Contains no recognized items</span></span>            | <span data-ttu-id="d001c-379">Le processus actuel ne prend pas en charge DPI par défaut.</span><span class="sxs-lookup"><span data-stu-id="d001c-379">The current process is dpi unaware by default.</span></span> <span data-ttu-id="d001c-380">Vous pouvez modifier ce paramètre par programmation en appelant la fonction [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="d001c-380">You can programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span> |
| <span data-ttu-id="d001c-381">Le premier élément reconnu est « système »</span><span class="sxs-lookup"><span data-stu-id="d001c-381">First recognized item is "system"</span></span>       | <span data-ttu-id="d001c-382">Le processus actuel prend en charge la résolution du système.</span><span class="sxs-lookup"><span data-stu-id="d001c-382">The current process is system dpi aware.</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="d001c-383">Le premier élément reconnu est « permonitor »</span><span class="sxs-lookup"><span data-stu-id="d001c-383">First recognized item is "permonitor"</span></span>   | <span data-ttu-id="d001c-384">Le processus actuel prend en charge la résolution par moniteur.</span><span class="sxs-lookup"><span data-stu-id="d001c-384">The current process is per-monitor dpi aware.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="d001c-385">Le premier élément reconnu est « permonitorv2 »</span><span class="sxs-lookup"><span data-stu-id="d001c-385">First recognized item is "permonitorv2"</span></span> | <span data-ttu-id="d001c-386">Le processus en cours utilise le contexte de détection par moniteur-v2 PPP.</span><span class="sxs-lookup"><span data-stu-id="d001c-386">The current process uses the per-monitor-v2 dpi awareness context.</span></span> <span data-ttu-id="d001c-387">Cet élément sera uniquement reconnu sur Windows 10 version 1703 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="d001c-387">This item will only be recognized on Windows 10 version 1703 or later.</span></span>                                                                                              |
| <span data-ttu-id="d001c-388">Le premier élément reconnu est « non pris en charge »</span><span class="sxs-lookup"><span data-stu-id="d001c-388">First recognized item is "unaware"</span></span>      | <span data-ttu-id="d001c-389">Le processus actuel ne prend pas en charge dpi.</span><span class="sxs-lookup"><span data-stu-id="d001c-389">The current process is dpi unaware.</span></span> <span data-ttu-id="d001c-390">Vous **ne pouvez pas** modifier ce paramètre par programmation en appelant la fonction [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) ou [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) .</span><span class="sxs-lookup"><span data-stu-id="d001c-390">You **cannot** programmatically change this setting by calling the [**SetProcessDpiAwareness**](/windows/desktop/api/shellscalingapi/nf-shellscalingapi-setprocessdpiawareness) or [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) function.</span></span>      |

<span data-ttu-id="d001c-391">Pour plus d’informations sur les paramètres de reconnaissance dpi pris en charge par cet élément, consultez prise en charge des [dpi \_ ](/windows/desktop/api/windef/ne-windef-dpi_awareness) et du [ \_ \_ contexte de détection dpi](/windows/desktop/hidpi/dpi-awareness-context).</span><span class="sxs-lookup"><span data-stu-id="d001c-391">For more information about dpi awareness settings supported by this element, see [DPI\_AWARENESS](/windows/desktop/api/windef/ne-windef-dpi_awareness) and [DPI\_AWARENESS\_CONTEXT](/windows/desktop/hidpi/dpi-awareness-context).</span></span>

<span data-ttu-id="d001c-392">**dpiAwareness** n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="d001c-392">**dpiAwareness** has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <dpiAwareness>PerMonitorV2, unaware</dpiAwareness>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="gdiScaling"></span><span id="gdiscaling"></span><span id="GDISCALING"></span>

### <a name="gdiscaling"></a><span data-ttu-id="d001c-393">gdiScaling</span><span class="sxs-lookup"><span data-stu-id="d001c-393">gdiScaling</span></span>

<span data-ttu-id="d001c-394">Spécifie si la mise à l’échelle GDI est activée.</span><span class="sxs-lookup"><span data-stu-id="d001c-394">Specifies whether GDI scaling is enabled.</span></span> <span data-ttu-id="d001c-395">La version minimale du système d’exploitation qui prend en charge l’élément **gdiScaling** est Windows 10 version 1703.</span><span class="sxs-lookup"><span data-stu-id="d001c-395">The minimum version of the operating system that supports the **gdiScaling** element is Windows 10 version 1703.</span></span>

<span data-ttu-id="d001c-396">L’infrastructure GDI (Graphics Device Interface) peut appliquer la mise à l’échelle DPI aux primitives et au texte en fonction de chaque moniteur sans mettre à jour l’application elle-même.</span><span class="sxs-lookup"><span data-stu-id="d001c-396">The GDI (graphics device interface) framework can apply DPI scaling to primitives and text on a per-monitor basis without updates to the application itself.</span></span> <span data-ttu-id="d001c-397">Cela peut être utile pour les applications GDI qui ne sont plus mises à jour activement.</span><span class="sxs-lookup"><span data-stu-id="d001c-397">This can be useful for GDI applications no longer being actively updated.</span></span>

<span data-ttu-id="d001c-398">Les graphiques non vectoriels (tels que les bitmaps, les icônes ou les barres d’outils) ne peuvent pas être mis à l’échelle par cet élément.</span><span class="sxs-lookup"><span data-stu-id="d001c-398">Non-vector graphics (such as bitmaps, icons, or toolbars) cannot be scaled by this element.</span></span> <span data-ttu-id="d001c-399">En outre, les graphiques et le texte figurant dans les bitmaps construits dynamiquement par les applications ne peuvent pas non plus être mis à l’échelle par cet élément.</span><span class="sxs-lookup"><span data-stu-id="d001c-399">In addition, graphics and text appearing within bitmaps dynamically constructed by applications also cannot be scaled by this element.</span></span>

<span data-ttu-id="d001c-400">**True** indique que cet élément est activé.</span><span class="sxs-lookup"><span data-stu-id="d001c-400">**TRUE** indicates that this element is enabled.</span></span> <span data-ttu-id="d001c-401">Elle n’a pas d’attribut.</span><span class="sxs-lookup"><span data-stu-id="d001c-401">It has no attributes.</span></span>


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2017/WindowsSettings">
      <gdiScaling>true</gdiScaling>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="highResolutionScrollingAware"></span><span id="highresolutionscrollingaware"></span><span id="HIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="highresolutionscrollingaware"></a><span data-ttu-id="d001c-402">highResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="d001c-402">highResolutionScrollingAware</span></span>

<span data-ttu-id="d001c-403">Spécifie si la prise en charge du défilement haute résolution est activée.</span><span class="sxs-lookup"><span data-stu-id="d001c-403">Specifies whether high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="d001c-404">La **valeur true** indique qu’elle est activée.</span><span class="sxs-lookup"><span data-stu-id="d001c-404">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="d001c-405">Elle n’a pas d’attribut.</span><span class="sxs-lookup"><span data-stu-id="d001c-405">It has no attributes.</span></span>

<span id="longPathAware"></span><span id="longpathaware"></span><span id="LONGPATHAWARE"></span>

### <a name="longpathaware"></a><span data-ttu-id="d001c-406">longPathAware</span><span class="sxs-lookup"><span data-stu-id="d001c-406">longPathAware</span></span>

<span data-ttu-id="d001c-407">Active les chemins longs qui dépassent **MAX_PATH** de longueur.</span><span class="sxs-lookup"><span data-stu-id="d001c-407">Enables long paths that exceed **MAX_PATH** in length.</span></span> <span data-ttu-id="d001c-408">Cet élément est pris en charge dans Windows 10, version 1607 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d001c-408">This element is supported in Windows 10, version 1607, and later.</span></span> <span data-ttu-id="d001c-409">Pour plus d’informations, consultez [cet article](../fileio/maximum-file-path-limitation.md).</span><span class="sxs-lookup"><span data-stu-id="d001c-409">For more information, see [this article](../fileio/maximum-file-path-limitation.md).</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns:ws2="http://schemas.microsoft.com/SMI/2016/WindowsSettings">
      <ws2:longPathAware>true</ws2:longPathAware>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="printerDriverIsolation"></span><span id="printerdriverisolation"></span><span id="PRINTERDRIVERISOLATION"></span>

### <a name="printerdriverisolation"></a><span data-ttu-id="d001c-410">printerDriverIsolation</span><span class="sxs-lookup"><span data-stu-id="d001c-410">printerDriverIsolation</span></span>

<span data-ttu-id="d001c-411">Spécifie si l’isolation du pilote d’imprimante est activée.</span><span class="sxs-lookup"><span data-stu-id="d001c-411">Specifies whether printer driver isolation is enabled.</span></span> <span data-ttu-id="d001c-412">La **valeur true** indique qu’elle est activée.</span><span class="sxs-lookup"><span data-stu-id="d001c-412">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="d001c-413">Elle n’a pas d’attribut.</span><span class="sxs-lookup"><span data-stu-id="d001c-413">It has no attributes.</span></span> <span data-ttu-id="d001c-414">L’isolation du pilote d’imprimante améliore la fiabilité du service d’impression Windows en permettant aux pilotes d’imprimante de s’exécuter dans des processus distincts du processus dans lequel le spouleur d’impression s’exécute.</span><span class="sxs-lookup"><span data-stu-id="d001c-414">Printer driver isolation improves the reliability of the Windows print service by enabling printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="d001c-415">La prise en charge de l’isolation du pilote d’imprimante a démarré dans Windows 7 et Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="d001c-415">Support for printer driver isolation started in Windows 7 and Windows Server 2008 R2.</span></span> <span data-ttu-id="d001c-416">Une application peut déclarer l’isolement du pilote d’imprimante dans son manifeste d’application pour s’isoler du pilote d’imprimante et améliorer sa fiabilité.</span><span class="sxs-lookup"><span data-stu-id="d001c-416">An app can declare printer driver isolation in its app manifest to isolate itself from the printer driver and improve its reliability.</span></span> <span data-ttu-id="d001c-417">Autrement dit, l’application ne se bloquera pas si le pilote d’imprimante rencontre une erreur.</span><span class="sxs-lookup"><span data-stu-id="d001c-417">That is, the app won't crash if the printer driver has an error.</span></span>


```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">
      <printerDriverIsolation>true</printerDriverIsolation>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

<span id="ultraHighResolutionScrollingAware"></span><span id="ultrahighresolutionscrollingaware"></span><span id="ULTRAHIGHRESOLUTIONSCROLLINGAWARE"></span>

### <a name="ultrahighresolutionscrollingaware"></a><span data-ttu-id="d001c-418">ultraHighResolutionScrollingAware</span><span class="sxs-lookup"><span data-stu-id="d001c-418">ultraHighResolutionScrollingAware</span></span>

<span data-ttu-id="d001c-419">Spécifie si la prise en charge du défilement ultra-haute résolution est activée.</span><span class="sxs-lookup"><span data-stu-id="d001c-419">Specifies whether ultra-high-resolution-scrolling aware is enabled.</span></span> <span data-ttu-id="d001c-420">La **valeur true** indique qu’elle est activée.</span><span class="sxs-lookup"><span data-stu-id="d001c-420">**TRUE** indicates that it is enabled.</span></span> <span data-ttu-id="d001c-421">Elle n’a pas d’attribut.</span><span class="sxs-lookup"><span data-stu-id="d001c-421">It has no attributes.</span></span>

<span id="msix"></span><span id="MSIX"></span>

### <a name="msix"></a><span data-ttu-id="d001c-422">msix</span><span class="sxs-lookup"><span data-stu-id="d001c-422">msix</span></span>

<span data-ttu-id="d001c-423">Spécifie les informations d’identité d’un [package MSIX fragmenté](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) pour l’application actuelle.</span><span class="sxs-lookup"><span data-stu-id="d001c-423">Specifies the identity info of a [sparse MSIX package](/windows/apps/desktop/modernize/grant-identity-to-nonpackaged-apps) for the current application.</span></span> <span data-ttu-id="d001c-424">Cet élément est pris en charge dans Windows 10, version 2004 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d001c-424">This element is supported in Windows 10, version 2004, and later versions.</span></span>

<span data-ttu-id="d001c-425">L’élément **msix** doit se trouver dans l’espace de noms `urn:schemas-microsoft-com:msix.v1` .</span><span class="sxs-lookup"><span data-stu-id="d001c-425">The **msix** element must be in the namespace `urn:schemas-microsoft-com:msix.v1`.</span></span> <span data-ttu-id="d001c-426">Il possède les attributs répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d001c-426">It has the attributes shown in the following table.</span></span>

| <span data-ttu-id="d001c-427">Attribut</span><span class="sxs-lookup"><span data-stu-id="d001c-427">Attribute</span></span>   | <span data-ttu-id="d001c-428">Description</span><span class="sxs-lookup"><span data-stu-id="d001c-428">Description</span></span>                                                                                             |
|-------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d001c-429">**publisher**</span><span class="sxs-lookup"><span data-stu-id="d001c-429">**publisher**</span></span>    | <span data-ttu-id="d001c-430">Décrit les informations sur le serveur de publication.</span><span class="sxs-lookup"><span data-stu-id="d001c-430">Describes the publisher information.</span></span> <span data-ttu-id="d001c-431">Cette valeur doit correspondre à l’attribut **Publisher** de l’élément [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) dans votre manifeste de package fragmenté.</span><span class="sxs-lookup"><span data-stu-id="d001c-431">This value must match the **Publisher** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span> |
| <span data-ttu-id="d001c-432">**packageName**</span><span class="sxs-lookup"><span data-stu-id="d001c-432">**packageName**</span></span> | <span data-ttu-id="d001c-433">Décrit le contenu du package.</span><span class="sxs-lookup"><span data-stu-id="d001c-433">Describes the contents of the package.</span></span> <span data-ttu-id="d001c-434">Cette valeur doit correspondre à l’attribut **Name** de l’élément [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) dans votre manifeste de package fragmenté.</span><span class="sxs-lookup"><span data-stu-id="d001c-434">This value must match the **Name** attribute in the [Identity](/uwp/schemas/appxpackage/uapmanifestschema/element-identity) element in your sparse package manifest.</span></span>    |
| <span data-ttu-id="d001c-435">**applicationId**</span><span class="sxs-lookup"><span data-stu-id="d001c-435">**applicationId**</span></span>    | <span data-ttu-id="d001c-436">Identificateur unique de l’application.</span><span class="sxs-lookup"><span data-stu-id="d001c-436">The unique identifier of the application.</span></span> <span data-ttu-id="d001c-437">Cette valeur doit correspondre à l’attribut **ID** de l’élément [application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) dans le manifeste de votre package épars.</span><span class="sxs-lookup"><span data-stu-id="d001c-437">This value must match the **Id** attribute in the [Application](/uwp/schemas/appxpackage/uapmanifestschema/element-application) element in your sparse package manifest.</span></span>  |

```xml
<?xml version="1.0" encoding="utf-8"?>
<assembly manifestVersion="1.0" xmlns="urn:schemas-microsoft-com:asm.v1">
  <assemblyIdentity version="1.0.0.0" name="Contoso.PhotoStoreApp"/>
  <msix xmlns="urn:schemas-microsoft-com:msix.v1"
          publisher="CN=Contoso"
          packageName="ContosoPhotoStore"
          applicationId="ContosoPhotoStore"
        />
</assembly>
```

### <a name="heaptype"></a><span data-ttu-id="d001c-438">heapType</span><span class="sxs-lookup"><span data-stu-id="d001c-438">heapType</span></span>

<span data-ttu-id="d001c-439">Substitue l’implémentation du tas par défaut pour les [API de tas Win32](../Memory/heap-functions.md) à utiliser.</span><span class="sxs-lookup"><span data-stu-id="d001c-439">Overrides the default heap implementation for the [Win32 heap APIs](../Memory/heap-functions.md) to use.</span></span>

* <span data-ttu-id="d001c-440">La valeur **SegmentHeap** indique que le segment de mémoire est utilisé.</span><span class="sxs-lookup"><span data-stu-id="d001c-440">The value **SegmentHeap** indicates that segment heap will be used.</span></span> <span data-ttu-id="d001c-441">Segment Heap est une implémentation de tas moderne qui réduit généralement l’utilisation globale de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="d001c-441">Segment heap is a modern heap implementation that will generally reduce your overall memory usage.</span></span> <span data-ttu-id="d001c-442">Cet élément est pris en charge dans Windows 10, version 2004 (Build 19041) et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="d001c-442">This element is supported in Windows 10, version 2004 (build 19041) and later.</span></span>
* <span data-ttu-id="d001c-443">Toutes les autres valeurs sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="d001c-443">All other values are ignored.</span></span>

<span data-ttu-id="d001c-444">Cet élément n’a pas d’attributs.</span><span class="sxs-lookup"><span data-stu-id="d001c-444">This element has no attributes.</span></span>

```XML
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
 ...
  <asmv3:application>
    <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2020/WindowsSettings">
      <heapType>SegmentHeap</heapType>
    </asmv3:windowsSettings>
  </asmv3:application>
 ...
</assembly>
```

## <a name="example"></a><span data-ttu-id="d001c-445">Exemple</span><span class="sxs-lookup"><span data-stu-id="d001c-445">Example</span></span>

<span data-ttu-id="d001c-446">Voici un exemple de manifeste d’application pour une application nommée MySampleApp.exe.</span><span class="sxs-lookup"><span data-stu-id="d001c-446">The following is an example of an application manifest for an application named MySampleApp.exe.</span></span> <span data-ttu-id="d001c-447">L’application consomme l’assembly côte à côte SampleAssembly.</span><span class="sxs-lookup"><span data-stu-id="d001c-447">The application consumes the SampleAssembly side-by-side assembly.</span></span>

``` syntax
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">

  <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--This Id value indicates the application supports Windows Vista functionality -->
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--This Id value indicates the application supports Windows 7 functionality-->
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--This Id value indicates the application supports Windows 8 functionality-->
          <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
        <!--This Id value indicates the application supports Windows 8.1 functionality-->
          <supportedOS Id="{1f676c76-80e1-4239-95bb-83d0f6d0da78}"/>
      </application> 
  </compatibility>

  <assemblyIdentity type="win32" 
                    name="myOrganization.myDivision.mySampleApp" 
                    version="6.0.0.0" 
                    processorArchitecture="x86" 
                    publicKeyToken="0000000000000000"
  />
  <dependency>
    <dependentAssembly>
      <assemblyIdentity type="win32" 
                        name="Proseware.Research.SampleAssembly" 
                        version="6.0.0.0" 
                        processorArchitecture="X86" 
                        publicKeyToken="0000000000000000" 
                        language="*"
      />
    </dependentAssembly>
  </dependency>
</assembly>
```
