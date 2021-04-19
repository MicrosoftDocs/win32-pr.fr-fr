---
description: Constantes utilisées par les \_ paramètres D3DPRESENT.
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3b7fe950a6fe09425aa47a79ce8f803eb81298
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513935"
---
# <a name="d3dpresentflag"></a><span data-ttu-id="c4358-103">D3DPRESENTFLAG</span><span class="sxs-lookup"><span data-stu-id="c4358-103">D3DPRESENTFLAG</span></span>

<span data-ttu-id="c4358-104">Constantes utilisées par [**les \_ paramètres D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c4358-104">Constants used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4358-105">#définition</span><span class="sxs-lookup"><span data-stu-id="c4358-105">#define</span></span></td>
<td><span data-ttu-id="c4358-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4358-106">Value</span></span></td>
<td><span data-ttu-id="c4358-107">Description</span><span class="sxs-lookup"><span data-stu-id="c4358-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4358-108">D3DPRESENTFLAG_DEVICECLIP</span><span class="sxs-lookup"><span data-stu-id="c4358-108">D3DPRESENTFLAG_DEVICECLIP</span></span></td>
<td><span data-ttu-id="c4358-109">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c4358-109">0x00000004</span></span></td>
<td><span data-ttu-id="c4358-110">Découpez un blit <a href="/windows/desktop/api"><strong>présent</strong></a> dans la zone cliente de la fenêtre, dans la zone de l’écran moniteur de la carte vidéo qui a créé l’appareil Direct3D.</span><span class="sxs-lookup"><span data-stu-id="c4358-110">Clip a windowed <a href="/windows/desktop/api"><strong>Present</strong></a> blit into the window client area, within the monitor screen area of the video adapter that created the Direct3D device.</span></span> <span data-ttu-id="c4358-111">D3DPRESENTFLAG_DEVICECLIP n’est pas valide avec D3DSWAPEFFECT_FLIPEX.</span><span class="sxs-lookup"><span data-stu-id="c4358-111">D3DPRESENTFLAG_DEVICECLIP is not valid with D3DSWAPEFFECT_FLIPEX.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4358-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span><span class="sxs-lookup"><span data-stu-id="c4358-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span></span></td>
<td><span data-ttu-id="c4358-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c4358-113">0x00000002</span></span></td>
<td><span data-ttu-id="c4358-114">Définissez cet indicateur lors de la création de l’appareil ou de la chaîne de permutation pour activer l’abandon de la mémoire tampon z.</span><span class="sxs-lookup"><span data-stu-id="c4358-114">Set this flag when the device or swap chain is created to enable z-buffer discarding.</span></span> <span data-ttu-id="c4358-115">Si cet indicateur est défini, le contenu de la mémoire tampon du stencil de profondeur n’est pas valide <a href="/windows/desktop/api"><strong>après l’appel de, ou</strong></a> <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> avec une surface de profondeur différente.</span><span class="sxs-lookup"><span data-stu-id="c4358-115">If this flag is set, the contents of the depth stencil buffer will be invalid after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span> <span data-ttu-id="c4358-116">L’abandon des données de la mémoire tampon z peut améliorer les performances et dépend du pilote.</span><span class="sxs-lookup"><span data-stu-id="c4358-116">Discarding z-buffer data can increase performance and is driver dependent.</span></span> <span data-ttu-id="c4358-117">Le runtime de débogage applique l’élimination en effaçant la mémoire tampon z pour une valeur constante après l’appel de la <a href="/windows/desktop/api"><strong>présente</strong></a>ou <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> avec une surface de profondeur différente.</span><span class="sxs-lookup"><span data-stu-id="c4358-117">The debug runtime will enforce discarding by clearing the z-buffer to some constant value after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span><br/> <span data-ttu-id="c4358-118">La suppression des données de la mémoire tampon z est illégale pour tous les formats verrouillables, D3DFMT_D16_LOCKABLE et D3DFMT_D32F_LOCKABLE.</span><span class="sxs-lookup"><span data-stu-id="c4358-118">Discarding z-buffer data is illegal for all lockable formats, D3DFMT_D16_LOCKABLE and D3DFMT_D32F_LOCKABLE.</span></span> <span data-ttu-id="c4358-119">Toute utilisation de <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> qui spécifie un format verrouillable et l’abandon de la mémoire tampon z échoue.</span><span class="sxs-lookup"><span data-stu-id="c4358-119">Any use of <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> specifying a lockable format and z-buffer discarding will fail.</span></span> <span data-ttu-id="c4358-120">Pour plus d’informations sur les formats, consultez <a href="d3dformat.md">D3DFORMAT</a>.</span><span class="sxs-lookup"><span data-stu-id="c4358-120">For more information about formats, see <a href="d3dformat.md">D3DFORMAT</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4358-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span><span class="sxs-lookup"><span data-stu-id="c4358-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span></span></td>
<td><span data-ttu-id="c4358-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c4358-122">0x00000001</span></span></td>
<td><span data-ttu-id="c4358-123">Définissez cet indicateur si l’application a besoin de pouvoir verrouiller directement la mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="c4358-123">Set this flag if the application requires the ability to lock the back buffer directly.</span></span> <span data-ttu-id="c4358-124">Notez que les mémoires tampons d’arrière-plan ne sont pas verrouillables, sauf si l’application spécifie D3DPRESENTFLAG_LOCKABLE_BACKBUFFER lors de l’appel de <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> ou <a href="/windows/desktop/api"><strong>Reset</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c4358-124">Note that back buffers are not lockable unless the application specifies D3DPRESENTFLAG_LOCKABLE_BACKBUFFER when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> or <a href="/windows/desktop/api"><strong>Reset</strong></a>.</span></span> <span data-ttu-id="c4358-125">Les mémoires tampons d’arrière-plan verrouillables entraînent des coûts de performances sur certaines configurations matérielles graphiques.</span><span class="sxs-lookup"><span data-stu-id="c4358-125">Lockable back buffers incur a performance cost on some graphics hardware configurations.</span></span> <span data-ttu-id="c4358-126">L’exécution d’une opération de verrouillage (ou l’utilisation de <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> pour écrire) sur la mémoire tampon d’arrière-plan verrouillable diminue les performances sur de nombreuses cartes.</span><span class="sxs-lookup"><span data-stu-id="c4358-126">Performing a lock operation (or using <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> to write) on the lockable back buffer decreases performance on many cards.</span></span> <span data-ttu-id="c4358-127">Dans ce cas, envisagez d’utiliser des triangles texturés pour déplacer des données vers la mémoire tampon d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="c4358-127">In this case, consider using textured triangles to move data to the back buffer.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4358-128">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="c4358-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c4358-129">Dans Direct3D9Ex, cet indicateur ne peut pas être défini si le D3DSWAPEFFECT est D3DSWAPEFFECT_FLIPEX, car le modèle de retournement permet au Gestionnaire de fenêtrage d’accéder à la mémoire tampon d’arrière-plan d’une application.</span><span class="sxs-lookup"><span data-stu-id="c4358-129">In Direct3D9Ex this flag cannot be set if the D3DSWAPEFFECT is D3DSWAPEFFECT_FLIPEX, since the flip model enables the Desktop Window Manager to access an application's back buffer.</span></span> <span data-ttu-id="c4358-130">Une surface partagée inter-processus ne doit pas être verrouillée.</span><span class="sxs-lookup"><span data-stu-id="c4358-130">A cross-process shared-surface should not be locked.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4358-131">D3DPRESENTFLAG_NOAUTOROTATE</span><span class="sxs-lookup"><span data-stu-id="c4358-131">D3DPRESENTFLAG_NOAUTOROTATE</span></span></td>
<td><span data-ttu-id="c4358-132">0x00000020</span><span class="sxs-lookup"><span data-stu-id="c4358-132">0x00000020</span></span></td>
<td><span data-ttu-id="c4358-133">Les analyses pivotées sont gérées automatiquement avec une copie en rotation au cours de la présentation, ce qui n’est pas très efficace.</span><span class="sxs-lookup"><span data-stu-id="c4358-133">Rotated monitors are handled automatically with a rotating copy during presentation, which is not very efficient.</span></span> <span data-ttu-id="c4358-134">Cet indicateur signifie que l’application effectuera sa propre rotation d’affichage.</span><span class="sxs-lookup"><span data-stu-id="c4358-134">This flag means the application will perform it's own display rotation.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4358-135">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="c4358-135">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c4358-136">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c4358-136">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="c4358-137">Les applications peuvent obtenir leur propre rotation éventuellement à l’aide d’une matrice de vue pivotée.</span><span class="sxs-lookup"><span data-stu-id="c4358-137">Applications can achieve their own rotation possibly by using a rotated view matrix.</span></span> <span data-ttu-id="c4358-138">Les méthodes <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> et <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> doivent être utilisées pour rechercher le paramètre de rotation actuel.</span><span class="sxs-lookup"><span data-stu-id="c4358-138">The methods <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> should be used to to find the current rotation setting.</span></span> <span data-ttu-id="c4358-139">Les paramètres de largeur et de hauteur de la mémoire tampon dans <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> et <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> doivent utiliser l’orientation paysage, tandis que la structure du mode plein écran doit être identique à ce qui est retourné par <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (par exemple, la largeur et la hauteur sont échangées lors d’une rotation de 90 et de 270 degrés).</span><span class="sxs-lookup"><span data-stu-id="c4358-139">The backbuffer Width and Height parameters in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> must be use landscape orientation, while the fullscreen display mode structure should be the same as what is returned from <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (i.e. Width and Height are swapped when rotated 90 and 270 degrees).</span></span></p>
<p><span data-ttu-id="c4358-140">Lors de l’utilisation du verrou sur les cibles de rendu pivotées, les hypothèses d’angle supérieur gauche ne sont plus vraies, la cible de rendu SURFACE_DESC reste paysage (comme impliqué par les paramètres de création) et la fenêtre GDI, les coordonnées de la souris, et doivent être traduites correctement quand elles sont utilisées avec la cible de rendu Direct3D et la scène.</span><span class="sxs-lookup"><span data-stu-id="c4358-140">When using Lock on rotated render targets, upper-left corner assumptions no longer hold true, the render target SURFACE_DESC will remain landscape (as implied by the creation parameters), and GDI window, mouse coordinates, and such need to be properly translated when used with the Direct3D render target and scene.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4358-141">D3DPRESENTFLAG_UNPRUNEDMODE</span><span class="sxs-lookup"><span data-stu-id="c4358-141">D3DPRESENTFLAG_UNPRUNEDMODE</span></span></td>
<td><span data-ttu-id="c4358-142">0x00000040</span><span class="sxs-lookup"><span data-stu-id="c4358-142">0x00000040</span></span></td>
<td><span data-ttu-id="c4358-143">Utilisez cet indicateur pour spécifier un mode d’affichage brut énuméré par l’adaptateur d’affichage même si Direct3D peut avoir indiqué que le mode n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c4358-143">Use this flag to specify any RAW display mode enumerated by the display adapter even though Direct3D may have indicated the mode is invalid.</span></span> <span data-ttu-id="c4358-144">L’application doit implémenter cela de manière fiable si le mode souhaité n’est pas vraiment valide.</span><span class="sxs-lookup"><span data-stu-id="c4358-144">The application should implement this in a robust manner in case the desired mode really is invalid.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4358-145">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="c4358-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c4358-146">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c4358-146">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4358-147">D3DPRESENTFLAG_VIDEO</span><span class="sxs-lookup"><span data-stu-id="c4358-147">D3DPRESENTFLAG_VIDEO</span></span></td>
<td><span data-ttu-id="c4358-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c4358-148">0x00000010</span></span></td>
<td><span data-ttu-id="c4358-149">Il s’agit d’un indicateur pour le pilote que les mémoires tampons d’arrière-plan contiendront des données vidéo.</span><span class="sxs-lookup"><span data-stu-id="c4358-149">This is a hint to the driver that the back buffers will contain video data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4358-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span><span class="sxs-lookup"><span data-stu-id="c4358-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span></span></td>
<td><span data-ttu-id="c4358-151">0x00000080</span><span class="sxs-lookup"><span data-stu-id="c4358-151">0x00000080</span></span></td>
<td><span data-ttu-id="c4358-152">Spécifie si la superposition est une plage pleine RVB ou une plage de valeurs RVB limitée.</span><span class="sxs-lookup"><span data-stu-id="c4358-152">Specifies whether the overlay is full range RGB or limited range RGB.</span></span> <span data-ttu-id="c4358-153">La définition de cet indicateur indique une plage limitée RVB.</span><span class="sxs-lookup"><span data-stu-id="c4358-153">Setting this flag indicates limited range RGB.</span></span> <span data-ttu-id="c4358-154">Dans une plage limitée, la plage RVB est compressée, de sorte que 16:16:16 est noir et 235:235:235 est blanc.</span><span class="sxs-lookup"><span data-stu-id="c4358-154">In limited range RGB, the RGB range is compressed such that 16:16:16 is black and 235:235:235 is white.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4358-155">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="c4358-155">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c4358-156">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c4358-156">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4358-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span><span class="sxs-lookup"><span data-stu-id="c4358-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span></span></td>
<td><span data-ttu-id="c4358-158">0x00000100</span><span class="sxs-lookup"><span data-stu-id="c4358-158">0x00000100</span></span></td>
<td><span data-ttu-id="c4358-159">Spécifie si la superposition est BT. 601 ou BT. 709.</span><span class="sxs-lookup"><span data-stu-id="c4358-159">Specifies whether the overlay is BT.601 or BT.709.</span></span> <span data-ttu-id="c4358-160">La définition de cet indicateur indique BT. 709, pour la télévision haute définition (HDTV).</span><span class="sxs-lookup"><span data-stu-id="c4358-160">Setting this flag indicates BT.709, for high-definition TV (HDTV).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4358-161">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="c4358-161">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c4358-162">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c4358-162">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4358-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span><span class="sxs-lookup"><span data-stu-id="c4358-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span></span></td>
<td><span data-ttu-id="c4358-164">0x00000200</span><span class="sxs-lookup"><span data-stu-id="c4358-164">0x00000200</span></span></td>
<td><span data-ttu-id="c4358-165">Spécifie si la superposition est conventionnelle YCbCr ou YCbCr étendu (xvYCC).</span><span class="sxs-lookup"><span data-stu-id="c4358-165">Specifies whether the overlay is conventional YCbCr or extended YCbCr (xvYCC).</span></span> <span data-ttu-id="c4358-166">La définition de cet indicateur indique une extension YCbCr étendue (xvYCC).</span><span class="sxs-lookup"><span data-stu-id="c4358-166">Setting this flag indicates extended YCbCr (xvYCC).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4358-167">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="c4358-167">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c4358-168">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c4358-168">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c4358-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span><span class="sxs-lookup"><span data-stu-id="c4358-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span></span></td>
<td><span data-ttu-id="c4358-170">0x00000400</span><span class="sxs-lookup"><span data-stu-id="c4358-170">0x00000400</span></span></td>
<td><span data-ttu-id="c4358-171">La définition de cet indicateur indique que le utilise permutation contient du contenu protégé et contraint automatiquement le runtime à limiter l’accès au utilise permutation afin que seul le gestionnaire Windows Desktop (DWM) puisse utiliser le utilise permutation.</span><span class="sxs-lookup"><span data-stu-id="c4358-171">Setting this flag indicates that the swapchain contains protected content and automatically causes the runtime to restrict access to the swapchain so that only the Desktop Windows Manager (DWM) can use the swapchain.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4358-172">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="c4358-172">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c4358-173">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c4358-173">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c4358-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span><span class="sxs-lookup"><span data-stu-id="c4358-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span></span></td>
<td><span data-ttu-id="c4358-175">0x00000800</span><span class="sxs-lookup"><span data-stu-id="c4358-175">0x00000800</span></span></td>
<td><span data-ttu-id="c4358-176">La définition de cet indicateur indique que le pilote doit restreindre l’accès à toutes les ressources partagées créées pour l’interaction DWM.</span><span class="sxs-lookup"><span data-stu-id="c4358-176">Setting this flag indicates that the driver should restrict access to any shared resources that are created for DWM interaction.</span></span> <span data-ttu-id="c4358-177">L’appelant doit créer un canal authentifié avec le pilote.</span><span class="sxs-lookup"><span data-stu-id="c4358-177">The caller must create an authenticated channel with the driver.</span></span> <span data-ttu-id="c4358-178">Le pilote doit ensuite autoriser l’accès aux processus qui tentent d’ouvrir ces ressources partagées.</span><span class="sxs-lookup"><span data-stu-id="c4358-178">The driver should then allow access to processes that attempt to open those shared resources.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c4358-179">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="c4358-179">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c4358-180">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c4358-180">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c4358-181">Ces constantes sont utilisées par [**les \_ paramètres D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c4358-181">These constants are used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="c4358-182">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="c4358-182">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="c4358-183">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4358-183">Header</span></span>                   | <span data-ttu-id="c4358-184">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="c4358-184">d3d9types.h</span></span> |
| <span data-ttu-id="c4358-185">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="c4358-185">Minimum operating system</span></span> | <span data-ttu-id="c4358-186">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c4358-186">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="c4358-187">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c4358-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4358-188">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="c4358-188">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




