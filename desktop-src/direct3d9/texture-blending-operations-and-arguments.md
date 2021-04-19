---
description: Les applications associent une phase de fusion à chaque texture dans le jeu de textures actuelles. Direct3D évalue chaque étape de fusion dans l’ordre, en commençant par la première texture du jeu et en finissant par le huitième.
ms.assetid: 3b7faefd-30be-4f74-b0f7-621d65130286
title: Opérations et arguments de fusion de texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae65386e01bfff7d4bfc2ebc0cafd242e25c4265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106544557"
---
# <a name="texture-blending-operations-and-arguments-direct3d-9"></a><span data-ttu-id="83158-104">Opérations et arguments de fusion de texture (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="83158-104">Texture Blending Operations and Arguments (Direct3D 9)</span></span>

<span data-ttu-id="83158-105">Les applications associent une phase de fusion à chaque texture dans le jeu de textures actuelles.</span><span class="sxs-lookup"><span data-stu-id="83158-105">Applications associate a blending stage with each texture in the set of current textures.</span></span> <span data-ttu-id="83158-106">Direct3D évalue chaque étape de fusion dans l’ordre, en commençant par la première texture du jeu et en finissant par le huitième.</span><span class="sxs-lookup"><span data-stu-id="83158-106">Direct3D evaluates each blending stage in order, beginning with the first texture in the set and ending with the eighth.</span></span>

<span data-ttu-id="83158-107">Direct3D applique les informations de chaque texture de l’ensemble des textures actuelles à la phase de fusion qui lui est associée.</span><span class="sxs-lookup"><span data-stu-id="83158-107">Direct3D applies the information from each texture in the set of current textures to the blending stage that is associated with it.</span></span> <span data-ttu-id="83158-108">Les applications contrôlent les informations d’une étape de texture qui sont utilisées en appelant [**IDirect3DDevice9 :: SetTextureStageState**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="83158-108">Applications control what information from a texture stage is used by calling [**IDirect3DDevice9::SetTextureStageState**](/windows/desktop/api).</span></span> <span data-ttu-id="83158-109">Vous pouvez définir des opérations distinctes pour la couleur et les canaux alpha, et chaque opération utilise deux arguments.</span><span class="sxs-lookup"><span data-stu-id="83158-109">You can set separate operations for the color and alpha channels, and each operation uses two arguments.</span></span> <span data-ttu-id="83158-110">Spécifiez les opérations de canal de couleur à l’aide de l' \_ État D3DTSS COLOROP stage. spécifiez des opérations alpha à l’aide de D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="83158-110">Specify color channel operations by using the D3DTSS\_COLOROP stage state; specify alpha operations by using D3DTSS\_ALPHAOP.</span></span> <span data-ttu-id="83158-111">Les deux États d’étape utilisent des valeurs du type énuméré [**D3DTEXTUREOP**](./d3dtextureop.md) .</span><span class="sxs-lookup"><span data-stu-id="83158-111">Both stage states use values from the [**D3DTEXTUREOP**](./d3dtextureop.md) enumerated type.</span></span>

<span data-ttu-id="83158-112">Les arguments de fusion de texture utilisent les \_ membres D3DTSS COLORARG1, D3DTSS \_ COLORARG2, D3DTSS \_ ALPHARG1 et D3DTSS ALPHARG2 \_ du type énuméré [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) .</span><span class="sxs-lookup"><span data-stu-id="83158-112">Texture blending arguments use the D3DTSS\_COLORARG1, D3DTSS\_COLORARG2, D3DTSS\_ALPHARG1, and D3DTSS\_ALPHARG2 members of the [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) enumerated type.</span></span> <span data-ttu-id="83158-113">Les valeurs d’argument correspondantes sont identifiées à l’aide de [D3DTA](d3dta.md).</span><span class="sxs-lookup"><span data-stu-id="83158-113">The corresponding argument values are identified using [D3DTA](d3dta.md).</span></span>

> [!Note]  
> <span data-ttu-id="83158-114">Vous pouvez désactiver une étape de texture, ainsi que toutes les étapes suivantes de fusion de texture dans le cascade, en définissant l’opération de couleur pour cette étape sur D3DTOP \_ Désactiver.</span><span class="sxs-lookup"><span data-stu-id="83158-114">You can disable a texture stage - and any subsequent texture blending stages in the cascade - by setting the color operation for that stage to D3DTOP\_DISABLE.</span></span> <span data-ttu-id="83158-115">La désactivation de l’opération de couleur désactive efficacement également l’opération alpha.</span><span class="sxs-lookup"><span data-stu-id="83158-115">Disabling the color operation effectively disables the alpha operation as well.</span></span> <span data-ttu-id="83158-116">Les opérations alpha ne peuvent pas être désactivées lorsque les opérations de couleur sont activées.</span><span class="sxs-lookup"><span data-stu-id="83158-116">Alpha operations cannot be disabled when color operations are enabled.</span></span> <span data-ttu-id="83158-117">La définition de l’opération alpha sur D3DTOP \_ désactive lorsque la fusion de couleurs est activée entraîne un comportement indéfini.</span><span class="sxs-lookup"><span data-stu-id="83158-117">Setting the alpha operation to D3DTOP\_DISABLE when color blending is enabled causes undefined behavior.</span></span>

 

<span data-ttu-id="83158-118">Pour déterminer les opérations de fusion de texture prises en charge d’un appareil, interrogez le membre TextureCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="83158-118">To determine the supported texture blending operations of a device, query the TextureCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="83158-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="83158-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83158-120">Fusion de texture</span><span class="sxs-lookup"><span data-stu-id="83158-120">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
