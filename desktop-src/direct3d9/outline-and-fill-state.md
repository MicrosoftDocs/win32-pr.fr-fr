---
description: Les primitives qui n’ont pas de textures sont rendues avec la couleur spécifiée par leur matériau, ou avec les couleurs spécifiées pour les vertex, le cas échéant.
ms.assetid: 8a7ed4b1-25a1-4984-baea-6e176f0545ea
title: État du contour et du remplissage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65092fb2e4bfe29ac5e9f9291250a0c78b80626d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517368"
---
# <a name="outline-and-fill-state-direct3d-9"></a><span data-ttu-id="bbe7e-103">État du contour et du remplissage (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="bbe7e-103">Outline and Fill State (Direct3D 9)</span></span>

<span data-ttu-id="bbe7e-104">Les primitives qui n’ont pas de textures sont rendues avec la couleur spécifiée par leur matériau, ou avec les couleurs spécifiées pour les vertex, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="bbe7e-104">Primitives that have no textures are rendered with the color specified by their material, or with the colors specified for the vertices, if any.</span></span> <span data-ttu-id="bbe7e-105">Vous pouvez sélectionner la méthode pour les remplir en spécifiant une valeur définie par le type énuméré [**D3DFILLMODE**](./d3dfillmode.md) pour l' \_ État de rendu D3DRS FillMode.</span><span class="sxs-lookup"><span data-stu-id="bbe7e-105">You can select the method to fill them by specifying a value defined by the [**D3DFILLMODE**](./d3dfillmode.md) enumerated type for the D3DRS\_FILLMODE render state.</span></span>

<span data-ttu-id="bbe7e-106">Pour activer le tramage, votre application doit passer la \_ valeur énumérée D3DRS DITHERENABLE en tant que premier paramètre à [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span><span class="sxs-lookup"><span data-stu-id="bbe7e-106">To enable dithering, your application must pass the D3DRS\_DITHERENABLE enumerated value as the first parameter to [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span> <span data-ttu-id="bbe7e-107">Il doit affecter la **valeur true** au deuxième paramètre pour activer le tramage et la **valeur false** pour le désactiver.</span><span class="sxs-lookup"><span data-stu-id="bbe7e-107">It must set the second parameter to **TRUE** to enable dithering, and **FALSE** to disable it.</span></span>

<span data-ttu-id="bbe7e-108">À des moments, le fait de dessiner le dernier pixel d’une ligne peut entraîner un chevauchement des primitives environnantes.</span><span class="sxs-lookup"><span data-stu-id="bbe7e-108">At times, drawing the last pixel in a line can cause unsightly overlap with surrounding primitives.</span></span> <span data-ttu-id="bbe7e-109">Vous pouvez contrôler cela à l’aide de la \_ valeur énumérée D3DRS LASTPIXEL.</span><span class="sxs-lookup"><span data-stu-id="bbe7e-109">You can control this using the D3DRS\_LASTPIXEL enumerated value.</span></span> <span data-ttu-id="bbe7e-110">Toutefois, ne modifiez pas ce paramètre sans une réflexion.</span><span class="sxs-lookup"><span data-stu-id="bbe7e-110">However, do not alter this setting without some forethought.</span></span> <span data-ttu-id="bbe7e-111">Dans certaines conditions, la suppression du rendu du dernier Pixel peut entraîner des écarts imesthétiques entre les primitives.</span><span class="sxs-lookup"><span data-stu-id="bbe7e-111">Under some conditions, suppressing the rendering of the last pixel can cause unsightly gaps between primitives.</span></span>

<span data-ttu-id="bbe7e-112">Les contours d’objets peuvent être dessinés en définissant le modèle de dessin de ligne approprié.</span><span class="sxs-lookup"><span data-stu-id="bbe7e-112">Object outlines can be drawn by setting the appropriate line drawing pattern.</span></span> <span data-ttu-id="bbe7e-113">L’état de dessin par défaut consiste à dessiner des lignes pleines.</span><span class="sxs-lookup"><span data-stu-id="bbe7e-113">The default line drawing state is to draw solid lines.</span></span> <span data-ttu-id="bbe7e-114">Pour plus d’informations, consultez [prise en charge du dessin en ligne dans l’état de rendu D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) .</span><span class="sxs-lookup"><span data-stu-id="bbe7e-114">For more information, see [Line Drawing Support in D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) render state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bbe7e-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bbe7e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbe7e-116">États de rendu</span><span class="sxs-lookup"><span data-stu-id="bbe7e-116">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
