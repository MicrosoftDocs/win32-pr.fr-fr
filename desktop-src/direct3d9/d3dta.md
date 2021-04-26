---
description: 'Les constantes d’argument de texture sont utilisées comme valeurs pour les membres suivants du type énuméré D3DTEXTURESTAGESTATETYPE :'
ms.assetid: 36b2b715-5ced-4246-840e-8ea343521ef4
title: D3DTA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 898e1bb66f74a1087a9da186599469bb195734ce
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995286"
---
# <a name="d3dta"></a><span data-ttu-id="c0adf-103">D3DTA</span><span class="sxs-lookup"><span data-stu-id="c0adf-103">D3DTA</span></span>

<span data-ttu-id="c0adf-104">Les constantes d’argument de texture sont utilisées comme valeurs pour les membres suivants du type énuméré [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) :</span><span class="sxs-lookup"><span data-stu-id="c0adf-104">Texture argument constants are used as values for the following members of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type:</span></span>

-   <span data-ttu-id="c0adf-105">D3DTSS \_ ALPHAARG0</span><span class="sxs-lookup"><span data-stu-id="c0adf-105">D3DTSS\_ALPHAARG0</span></span>
-   <span data-ttu-id="c0adf-106">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="c0adf-106">D3DTSS\_ALPHAARG1</span></span>
-   <span data-ttu-id="c0adf-107">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="c0adf-107">D3DTSS\_ALPHAARG2</span></span>
-   <span data-ttu-id="c0adf-108">D3DTSS \_ COLORARG0</span><span class="sxs-lookup"><span data-stu-id="c0adf-108">D3DTSS\_COLORARG0</span></span>
-   <span data-ttu-id="c0adf-109">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="c0adf-109">D3DTSS\_COLORARG1</span></span>
-   <span data-ttu-id="c0adf-110">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="c0adf-110">D3DTSS\_COLORARG2</span></span>
-   <span data-ttu-id="c0adf-111">D3DTSS \_ RESULTARG</span><span class="sxs-lookup"><span data-stu-id="c0adf-111">D3DTSS\_RESULTARG</span></span>

<span data-ttu-id="c0adf-112">Définissez et récupérez des arguments de texture en appelant les méthodes [**SetTextureStageState**](/windows/desktop/api) et [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="c0adf-112">Set and retrieve texture arguments by calling the [**SetTextureStageState**](/windows/desktop/api) and [**GetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) methods.</span></span>

<span data-ttu-id="c0adf-113">Indicateurs d’argument</span><span class="sxs-lookup"><span data-stu-id="c0adf-113">Argument flags</span></span>

<span data-ttu-id="c0adf-114">Vous pouvez combiner un indicateur d’argument avec un modificateur, mais deux indicateurs d’arguments ne peuvent pas être combinés.</span><span class="sxs-lookup"><span data-stu-id="c0adf-114">You can combine an argument flag with a modifier, but two argument flags cannot be combined.</span></span>



| <span data-ttu-id="c0adf-115">\#définition</span><span class="sxs-lookup"><span data-stu-id="c0adf-115">\#define</span></span>          | <span data-ttu-id="c0adf-116">Description</span><span class="sxs-lookup"><span data-stu-id="c0adf-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0adf-117">D3DTA \_ constante)</span><span class="sxs-lookup"><span data-stu-id="c0adf-117">D3DTA\_CONSTANT</span></span>   | <span data-ttu-id="c0adf-118">Sélectionnez une constante dans une étape de texture.</span><span class="sxs-lookup"><span data-stu-id="c0adf-118">Select a constant from a texture stage.</span></span> <span data-ttu-id="c0adf-119">La valeur par défaut est 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="c0adf-119">The default value is 0xffffffff.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="c0adf-120">D3DTA \_ actuel</span><span class="sxs-lookup"><span data-stu-id="c0adf-120">D3DTA\_CURRENT</span></span>    | <span data-ttu-id="c0adf-121">L’argument texture est le résultat de l’étape de fusion précédente.</span><span class="sxs-lookup"><span data-stu-id="c0adf-121">The texture argument is the result of the previous blending stage.</span></span> <span data-ttu-id="c0adf-122">Dans la première étape de texture (étape 0), cet argument est équivalent à D3DTA \_ diffus.</span><span class="sxs-lookup"><span data-stu-id="c0adf-122">In the first texture stage (stage 0), this argument is equivalent to D3DTA\_DIFFUSE.</span></span> <span data-ttu-id="c0adf-123">Si la phase de fusion précédente utilise une texture de la carte de bosselage ( \_ opération D3DTOP BUMPENVMAP), le système choisit la texture à partir de l’étape avant la texture de la carte de bosselage.</span><span class="sxs-lookup"><span data-stu-id="c0adf-123">If the previous blending stage uses a bump-map texture (the D3DTOP\_BUMPENVMAP operation), the system chooses the texture from the stage before the bump-map texture.</span></span> <span data-ttu-id="c0adf-124">Si s représente l’étape de texture actuelle et que s-1 contient une texture de carte de bosselage, cet argument devient la sortie de résultat par l’étape de texture s-2.</span><span class="sxs-lookup"><span data-stu-id="c0adf-124">If s represents the current texture stage and s - 1 contains a bump-map texture, this argument becomes the result output by texture stage s - 2.</span></span> <span data-ttu-id="c0adf-125">Les autorisations sont en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c0adf-125">Permissions are read/write.</span></span> |
| <span data-ttu-id="c0adf-126">\_Diffusion D3DTA</span><span class="sxs-lookup"><span data-stu-id="c0adf-126">D3DTA\_DIFFUSE</span></span>    | <span data-ttu-id="c0adf-127">L’argument texture est la couleur diffuse interpolée à partir des composants de vertex pendant l’ombrage Gouraud.</span><span class="sxs-lookup"><span data-stu-id="c0adf-127">The texture argument is the diffuse color interpolated from vertex components during Gouraud shading.</span></span> <span data-ttu-id="c0adf-128">Si le vertex ne contient pas de couleur diffuse, la couleur par défaut est 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="c0adf-128">If the vertex does not contain a diffuse color, the default color is 0xffffffff.</span></span> <span data-ttu-id="c0adf-129">Les autorisations sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c0adf-129">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="c0adf-130">D3DTA \_ SELECTMASK</span><span class="sxs-lookup"><span data-stu-id="c0adf-130">D3DTA\_SELECTMASK</span></span> | <span data-ttu-id="c0adf-131">Valeur de masque pour tous les arguments ; non utilisé lors de la définition des arguments de texture.</span><span class="sxs-lookup"><span data-stu-id="c0adf-131">Mask value for all arguments; not used when setting texture arguments.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="c0adf-132">D3DTA \_ spéculaire</span><span class="sxs-lookup"><span data-stu-id="c0adf-132">D3DTA\_SPECULAR</span></span>   | <span data-ttu-id="c0adf-133">L’argument texture est la couleur spéculaire interpolée à partir des composants de vertex pendant l’ombrage Gouraud.</span><span class="sxs-lookup"><span data-stu-id="c0adf-133">The texture argument is the specular color interpolated from vertex components during Gouraud shading.</span></span> <span data-ttu-id="c0adf-134">Si le vertex ne contient pas de couleur spéculaire, la couleur par défaut est 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="c0adf-134">If the vertex does not contain a specular color, the default color is 0xffffffff.</span></span> <span data-ttu-id="c0adf-135">Les autorisations sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c0adf-135">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="c0adf-136">D3DTA \_ temp</span><span class="sxs-lookup"><span data-stu-id="c0adf-136">D3DTA\_TEMP</span></span>       | <span data-ttu-id="c0adf-137">L’argument texture est une couleur de registre temporaire pour la lecture ou l’écriture.</span><span class="sxs-lookup"><span data-stu-id="c0adf-137">The texture argument is a temporary register color for read or write.</span></span> <span data-ttu-id="c0adf-138">D3DTA \_ temp est pris en charge si la fonctionnalité de l’appareil [D3DPMISCCAPS \_ TSSARGTEMP](d3dpmisccaps.md) est présente.</span><span class="sxs-lookup"><span data-stu-id="c0adf-138">D3DTA\_TEMP is supported if the [D3DPMISCCAPS\_TSSARGTEMP](d3dpmisccaps.md) device capability is present.</span></span> <span data-ttu-id="c0adf-139">La valeur par défaut du Registre est (0,0, 0,0, 0,0, 0,0).</span><span class="sxs-lookup"><span data-stu-id="c0adf-139">The default value for the register is (0.0, 0.0, 0.0, 0.0).</span></span> <span data-ttu-id="c0adf-140">Les autorisations sont en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c0adf-140">Permissions are read/write.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="c0adf-141">\_Texture D3DTA</span><span class="sxs-lookup"><span data-stu-id="c0adf-141">D3DTA\_TEXTURE</span></span>    | <span data-ttu-id="c0adf-142">L’argument texture est la couleur de texture pour cette étape de texture.</span><span class="sxs-lookup"><span data-stu-id="c0adf-142">The texture argument is the texture color for this texture stage.</span></span> <span data-ttu-id="c0adf-143">Les autorisations sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c0adf-143">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="c0adf-144">D3DTA \_ TFACTOR</span><span class="sxs-lookup"><span data-stu-id="c0adf-144">D3DTA\_TFACTOR</span></span>    | <span data-ttu-id="c0adf-145">L’argument texture est le facteur de texture défini dans un appel précédent à [**SetRenderState**](/windows/desktop/api) avec la valeur [**D3DRS \_ TEXTUREFACTOR**](./d3drenderstatetype.md) Render-State.</span><span class="sxs-lookup"><span data-stu-id="c0adf-145">The texture argument is the texture factor set in a previous call to the [**SetRenderState**](/windows/desktop/api) with the [**D3DRS\_TEXTUREFACTOR**](./d3drenderstatetype.md) render-state value.</span></span> <span data-ttu-id="c0adf-146">Les autorisations sont en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c0adf-146">Permissions are read-only.</span></span>                                                                                                                                                                                                                                                       |



 

<span data-ttu-id="c0adf-147">Indicateurs de modificateur</span><span class="sxs-lookup"><span data-stu-id="c0adf-147">Modifier flags</span></span>

<span data-ttu-id="c0adf-148">Un indicateur d’argument peut être combiné avec l’un des indicateurs de modificateur suivants.</span><span class="sxs-lookup"><span data-stu-id="c0adf-148">An argument flag may be combined with one of the following modifier flags.</span></span>



| <span data-ttu-id="c0adf-149">\#définition</span><span class="sxs-lookup"><span data-stu-id="c0adf-149">\#define</span></span>              | <span data-ttu-id="c0adf-150">Description</span><span class="sxs-lookup"><span data-stu-id="c0adf-150">Description</span></span>                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0adf-151">D3DTA \_ ALPHAREPLICATE</span><span class="sxs-lookup"><span data-stu-id="c0adf-151">D3DTA\_ALPHAREPLICATE</span></span> | <span data-ttu-id="c0adf-152">Répliquez les informations alpha sur tous les canaux de couleur avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="c0adf-152">Replicate the alpha information to all color channels before the operation completes.</span></span> <span data-ttu-id="c0adf-153">Il s’agit d’un modificateur de lecture.</span><span class="sxs-lookup"><span data-stu-id="c0adf-153">This is a read modifier.</span></span> |
| <span data-ttu-id="c0adf-154">\_Complément D3DTA</span><span class="sxs-lookup"><span data-stu-id="c0adf-154">D3DTA\_COMPLEMENT</span></span>     | <span data-ttu-id="c0adf-155">Prenez le complément de l’argument x, (1,0-x).</span><span class="sxs-lookup"><span data-stu-id="c0adf-155">Take the complement of the argument x, (1.0 - x).</span></span> <span data-ttu-id="c0adf-156">Il s’agit d’un modificateur de lecture.</span><span class="sxs-lookup"><span data-stu-id="c0adf-156">This is a read modifier.</span></span>                                     |



 

## <a name="constant-information"></a><span data-ttu-id="c0adf-157">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="c0adf-157">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="c0adf-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0adf-158">Header</span></span>                   | <span data-ttu-id="c0adf-159">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="c0adf-159">d3d9types.h</span></span> |
| <span data-ttu-id="c0adf-160">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="c0adf-160">Minimum operating system</span></span> | <span data-ttu-id="c0adf-161">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c0adf-161">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="c0adf-162">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c0adf-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0adf-163">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="c0adf-163">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
