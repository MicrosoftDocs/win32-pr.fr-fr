---
description: Création d’applications DirectShow
ms.assetid: 2fbdbe49-0d4d-4dce-afc3-7049c793ace0
title: Création d’applications DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c6ab8a0731e93eece734abd4380b092414ff5f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106519174"
---
# <a name="building-directshow-applications"></a><span data-ttu-id="1f432-103">Création d’applications DirectShow</span><span class="sxs-lookup"><span data-stu-id="1f432-103">Building DirectShow Applications</span></span>

<span data-ttu-id="1f432-104">Cette rubrique décrit les en-têtes et les bibliothèques nécessaires pour créer des applications DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1f432-104">This topic describes the headers and libraries needed to build DirectShow applications.</span></span>

<span data-ttu-id="1f432-105">Les derniers en-têtes et bibliothèques DirectShow sont disponibles dans le [SDK Windows](https://msdn.microsoft.com/windows/aa904949.aspx).</span><span class="sxs-lookup"><span data-stu-id="1f432-105">The latest DirectShow headers and libraries are available in the [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx).</span></span>

## <a name="header-files"></a><span data-ttu-id="1f432-106">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1f432-106">Header Files</span></span>

<span data-ttu-id="1f432-107">Toutes les applications DirectShow utilisent le fichier d’en-tête indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1f432-107">All DirectShow applications use the header file shown in the following table.</span></span>



| <span data-ttu-id="1f432-108">Fichier d'en-tête</span><span class="sxs-lookup"><span data-stu-id="1f432-108">Header File</span></span> | <span data-ttu-id="1f432-109">Requis pour</span><span class="sxs-lookup"><span data-stu-id="1f432-109">Required For</span></span>                 |
|-------------|------------------------------|
| <span data-ttu-id="1f432-110">DShow. h</span><span class="sxs-lookup"><span data-stu-id="1f432-110">Dshow.h</span></span>     | <span data-ttu-id="1f432-111">Toutes les applications DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1f432-111">All DirectShow applications.</span></span> |



 

<span data-ttu-id="1f432-112">Certaines interfaces DirectShow requièrent des fichiers d’en-tête supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="1f432-112">Some DirectShow interfaces require additional header files.</span></span> <span data-ttu-id="1f432-113">Ces exigences sont indiquées dans la référence de l’interface.</span><span class="sxs-lookup"><span data-stu-id="1f432-113">These requirements are noted in the interface reference.</span></span>

## <a name="library-files"></a><span data-ttu-id="1f432-114">Fichiers de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1f432-114">Library Files</span></span>

<span data-ttu-id="1f432-115">DirectShow utilise les fichiers de bibliothèque statique indiqués dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="1f432-115">DirectShow uses the static library files shown in the following table.</span></span>



| <span data-ttu-id="1f432-116">Fichier bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1f432-116">Library File</span></span> | <span data-ttu-id="1f432-117">Description</span><span class="sxs-lookup"><span data-stu-id="1f432-117">Description</span></span>                                                                                                                    |
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f432-118">Strmiids. lib</span><span class="sxs-lookup"><span data-stu-id="1f432-118">Strmiids.lib</span></span> | <span data-ttu-id="1f432-119">Exporte les identificateurs de classe (CLSID) et les identificateurs d’interface (IID).</span><span class="sxs-lookup"><span data-stu-id="1f432-119">Exports class identifiers (CLSIDs) and interface identifiers (IIDs).</span></span>                                                           |
| <span data-ttu-id="1f432-120">Quartz. lib</span><span class="sxs-lookup"><span data-stu-id="1f432-120">Quartz.lib</span></span>   | <span data-ttu-id="1f432-121">Exporte la fonction [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) .</span><span class="sxs-lookup"><span data-stu-id="1f432-121">Exports the [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) function.</span></span> <span data-ttu-id="1f432-122">Si vous n’appelez pas cette fonction, cette bibliothèque n’est pas requise.</span><span class="sxs-lookup"><span data-stu-id="1f432-122">If you do not call this function, this library is not required.</span></span> |



 

<span data-ttu-id="1f432-123">Utilisez les mêmes fichiers. lib pour les versions Debug et Release.</span><span class="sxs-lookup"><span data-stu-id="1f432-123">Use the same .lib files for debug and release builds.</span></span>

## <a name="filter-base-classes"></a><span data-ttu-id="1f432-124">Filtrer les classes de base</span><span class="sxs-lookup"><span data-stu-id="1f432-124">Filter Base Classes</span></span>

<span data-ttu-id="1f432-125">L’SDK Windows fournit un ensemble de classes C++ recommandées si vous écrivez un filtre DirectShow personnalisé.</span><span class="sxs-lookup"><span data-stu-id="1f432-125">The Windows SDK provides a set of C++ classes that are recommended if you are writing a custom DirectShow filter.</span></span> <span data-ttu-id="1f432-126">Ces classes sont fournies en tant qu’exemple de code, que vous pouvez compiler dans une bibliothèque statique.</span><span class="sxs-lookup"><span data-stu-id="1f432-126">These classes are provided as sample code, which you can compile to a static library.</span></span> <span data-ttu-id="1f432-127">Pour plus d’informations, consultez [classes de base DirectShow](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="1f432-127">For more information, see [DirectShow Base Classes](directshow-base-classes.md).</span></span>

## <a name="redistributable-dlls"></a><span data-ttu-id="1f432-128">Dll redistribuables</span><span class="sxs-lookup"><span data-stu-id="1f432-128">Redistributable DLLs</span></span>

<span data-ttu-id="1f432-129">Les applications DirectShow écrites pour Windows XP avec Service Pack 2 (SP2) et versions ultérieures n’ont pas besoin de redistribuer les dll DirectShow.</span><span class="sxs-lookup"><span data-stu-id="1f432-129">DirectShow applications written for Windows XP with Service Pack 2 (SP2) and later do not need to redistribute any DirectShow DLLs.</span></span>

<span data-ttu-id="1f432-130">Pour Windows XP avec Service Pack 1 (SP1) et versions antérieures, les dll DirectShow redistribuables sont disponibles dans le kit de développement logiciel (SDK) Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="1f432-130">For Windows XP with Service Pack 1 (SP1) and earlier, redistributable DirectShow DLLs are available from the Microsoft DirectX SDK.</span></span> <span data-ttu-id="1f432-131">La version la plus récente de ces dll est la version 9.0 c.</span><span class="sxs-lookup"><span data-stu-id="1f432-131">The latest version of these DLLs is version 9.0c.</span></span> <span data-ttu-id="1f432-132">Aucun développement supplémentaire de ces dll redistribuables n’est prévu.</span><span class="sxs-lookup"><span data-stu-id="1f432-132">No further development of these redistributable DLLs is planned.</span></span> <span data-ttu-id="1f432-133">Windows XP avec Service Pack 2 (SP2) contient les dll c version 9.0.</span><span class="sxs-lookup"><span data-stu-id="1f432-133">Windows XP with Service Pack 2 (SP2) contains the version 9.0c DLLs.</span></span>

<span data-ttu-id="1f432-134">Les packages redstributable contiennent les dll suivantes :</span><span class="sxs-lookup"><span data-stu-id="1f432-134">The redstributable packages contain the following DLLs:</span></span>

-   <span data-ttu-id="1f432-135">dxnt.cab</span><span class="sxs-lookup"><span data-stu-id="1f432-135">dxnt.cab</span></span>
    -   <span data-ttu-id="1f432-136">amstream.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-136">amstream.dll</span></span>
    -   <span data-ttu-id="1f432-137">devenum.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-137">devenum.dll</span></span>
    -   <span data-ttu-id="1f432-138">encapi.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-138">encapi.dll</span></span>
    -   <span data-ttu-id="1f432-139">ks.sys</span><span class="sxs-lookup"><span data-stu-id="1f432-139">ks.sys</span></span>
    -   <span data-ttu-id="1f432-140">ksolay.ax</span><span class="sxs-lookup"><span data-stu-id="1f432-140">ksolay.ax</span></span>
    -   <span data-ttu-id="1f432-141">ksproxy.ax</span><span class="sxs-lookup"><span data-stu-id="1f432-141">ksproxy.ax</span></span>
    -   <span data-ttu-id="1f432-142">ksuser.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-142">ksuser.dll</span></span>
    -   <span data-ttu-id="1f432-143">l3codecx.ax</span><span class="sxs-lookup"><span data-stu-id="1f432-143">l3codecx.ax</span></span>
    -   <span data-ttu-id="1f432-144">mciqtz32.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-144">mciqtz32.dll</span></span>
    -   <span data-ttu-id="1f432-145">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="1f432-145">mpg2splt.ax</span></span>
    -   <span data-ttu-id="1f432-146">msdmo.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-146">msdmo.dll</span></span>
    -   <span data-ttu-id="1f432-147">mskssrv.sys</span><span class="sxs-lookup"><span data-stu-id="1f432-147">mskssrv.sys</span></span>
    -   <span data-ttu-id="1f432-148">mspclock.sys</span><span class="sxs-lookup"><span data-stu-id="1f432-148">mspclock.sys</span></span>
    -   <span data-ttu-id="1f432-149">mspqm.sys</span><span class="sxs-lookup"><span data-stu-id="1f432-149">mspqm.sys</span></span>
    -   <span data-ttu-id="1f432-150">mstee.sys</span><span class="sxs-lookup"><span data-stu-id="1f432-150">mstee.sys</span></span>
    -   <span data-ttu-id="1f432-151">mswebdvd.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-151">mswebdvd.dll</span></span>
    -   <span data-ttu-id="1f432-152">qasf.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-152">qasf.dll</span></span>
    -   <span data-ttu-id="1f432-153">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-153">qcap.dll</span></span>
    -   <span data-ttu-id="1f432-154">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-154">qdv.dll</span></span>
    -   <span data-ttu-id="1f432-155">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-155">qdvd.dll</span></span>
    -   <span data-ttu-id="1f432-156">qedit.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-156">qedit.dll</span></span>
    -   <span data-ttu-id="1f432-157">qedwipes.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-157">qedwipes.dll</span></span>
    -   <span data-ttu-id="1f432-158">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-158">quartz.dll</span></span>
    -   <span data-ttu-id="1f432-159">stream.sys</span><span class="sxs-lookup"><span data-stu-id="1f432-159">stream.sys</span></span>
    -   <span data-ttu-id="1f432-160">swenum.sys</span><span class="sxs-lookup"><span data-stu-id="1f432-160">swenum.sys</span></span>
-   <span data-ttu-id="1f432-161">bda.cab</span><span class="sxs-lookup"><span data-stu-id="1f432-161">bda.cab</span></span>
    -   <span data-ttu-id="1f432-162">bdaplgin.ax</span><span class="sxs-lookup"><span data-stu-id="1f432-162">bdaplgin.ax</span></span>
    -   <span data-ttu-id="1f432-163">bdasup.sys</span><span class="sxs-lookup"><span data-stu-id="1f432-163">bdasup.sys</span></span>
    -   <span data-ttu-id="1f432-164">ccdecode.sys</span><span class="sxs-lookup"><span data-stu-id="1f432-164">ccdecode.sys</span></span>
    -   <span data-ttu-id="1f432-165">ipsink.ax</span><span class="sxs-lookup"><span data-stu-id="1f432-165">ipsink.ax</span></span>
    -   <span data-ttu-id="1f432-166">kstvtune.ax</span><span class="sxs-lookup"><span data-stu-id="1f432-166">kstvtune.ax</span></span>
    -   <span data-ttu-id="1f432-167">kswdmcap.ax</span><span class="sxs-lookup"><span data-stu-id="1f432-167">kswdmcap.ax</span></span>
    -   <span data-ttu-id="1f432-168">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="1f432-168">ksxbar.ax</span></span>
    -   <span data-ttu-id="1f432-169">mpe.sys</span><span class="sxs-lookup"><span data-stu-id="1f432-169">mpe.sys</span></span>
    -   <span data-ttu-id="1f432-170">mpeg2data.ax</span><span class="sxs-lookup"><span data-stu-id="1f432-170">mpeg2data.ax</span></span>
    -   <span data-ttu-id="1f432-171">msdv.sys</span><span class="sxs-lookup"><span data-stu-id="1f432-171">msdv.sys</span></span>
    -   <span data-ttu-id="1f432-172">msdvbnp.ax</span><span class="sxs-lookup"><span data-stu-id="1f432-172">msdvbnp.ax</span></span>
    -   <span data-ttu-id="1f432-173">msvidctl.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-173">msvidctl.dll</span></span>
    -   <span data-ttu-id="1f432-174">msyuv.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-174">msyuv.dll</span></span>
    -   <span data-ttu-id="1f432-175">nabtsfec.sys</span><span class="sxs-lookup"><span data-stu-id="1f432-175">nabtsfec.sys</span></span>
    -   <span data-ttu-id="1f432-176">ndisip.sys</span><span class="sxs-lookup"><span data-stu-id="1f432-176">ndisip.sys</span></span>
    -   <span data-ttu-id="1f432-177">psisdecd.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-177">psisdecd.dll</span></span>
    -   <span data-ttu-id="1f432-178">psisrndr.ax</span><span class="sxs-lookup"><span data-stu-id="1f432-178">psisrndr.ax</span></span>
    -   <span data-ttu-id="1f432-179">slip.sys</span><span class="sxs-lookup"><span data-stu-id="1f432-179">slip.sys</span></span>
    -   <span data-ttu-id="1f432-180">streamip.sys</span><span class="sxs-lookup"><span data-stu-id="1f432-180">streamip.sys</span></span>
    -   <span data-ttu-id="1f432-181">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="1f432-181">vbisurf.ax</span></span>
    -   <span data-ttu-id="1f432-182">wstcodec.sys</span><span class="sxs-lookup"><span data-stu-id="1f432-182">wstcodec.sys</span></span>
    -   <span data-ttu-id="1f432-183">wstdecod.dll</span><span class="sxs-lookup"><span data-stu-id="1f432-183">wstdecod.dll</span></span>

## <a name="related-topics"></a><span data-ttu-id="1f432-184">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1f432-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f432-185">Génération de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="1f432-185">Building DirectShow Filters</span></span>](building-directshow-filters.md)
</dt> </dl>

 

 
