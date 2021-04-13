---
description: Définit les opérations de fusion de texture par étape.
ms.assetid: 7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3
title: Énumération D3DTEXTUREOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d35e2d4b65cd41a49d8ed8edb3252295ca3baef3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322782"
---
# <a name="d3dtextureop-enumeration"></a><span data-ttu-id="b3ea8-103">Énumération D3DTEXTUREOP</span><span class="sxs-lookup"><span data-stu-id="b3ea8-103">D3DTEXTUREOP enumeration</span></span>

<span data-ttu-id="b3ea8-104">Définit les opérations de fusion de texture par étape.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-104">Defines per-stage texture-blending operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3ea8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3ea8-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREOP { 
  D3DTOP_DISABLE                    = 1,
  D3DTOP_SELECTARG1                 = 2,
  D3DTOP_SELECTARG2                 = 3,
  D3DTOP_MODULATE                   = 4,
  D3DTOP_MODULATE2X                 = 5,
  D3DTOP_MODULATE4X                 = 6,
  D3DTOP_ADD                        = 7,
  D3DTOP_ADDSIGNED                  = 8,
  D3DTOP_ADDSIGNED2X                = 9,
  D3DTOP_SUBTRACT                   = 10,
  D3DTOP_ADDSMOOTH                  = 11,
  D3DTOP_BLENDDIFFUSEALPHA          = 12,
  D3DTOP_BLENDTEXTUREALPHA          = 13,
  D3DTOP_BLENDFACTORALPHA           = 14,
  D3DTOP_BLENDTEXTUREALPHAPM        = 15,
  D3DTOP_BLENDCURRENTALPHA          = 16,
  D3DTOP_PREMODULATE                = 17,
  D3DTOP_MODULATEALPHA_ADDCOLOR     = 18,
  D3DTOP_MODULATECOLOR_ADDALPHA     = 19,
  D3DTOP_MODULATEINVALPHA_ADDCOLOR  = 20,
  D3DTOP_MODULATEINVCOLOR_ADDALPHA  = 21,
  D3DTOP_BUMPENVMAP                 = 22,
  D3DTOP_BUMPENVMAPLUMINANCE        = 23,
  D3DTOP_DOTPRODUCT3                = 24,
  D3DTOP_MULTIPLYADD                = 25,
  D3DTOP_LERP                       = 26,
  D3DTOP_FORCE_DWORD                = 0x7fffffff
} D3DTEXTUREOP, *LPD3DTEXTUREOP;
```



## <a name="constants"></a><span data-ttu-id="b3ea8-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b3ea8-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b3ea8-107"><span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**Désactivation de D3DTOP \_**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-107"><span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**D3DTOP\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-108">Désactive la sortie de cette étape de texture et toutes les étapes avec un index plus élevé.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-108">Disables output from this texture stage and all stages with a higher index.</span></span> <span data-ttu-id="b3ea8-109">Pour désactiver le mappage de texture, définissez-le en tant qu’opération de couleur pour la première étape de texture (étape 0).</span><span class="sxs-lookup"><span data-stu-id="b3ea8-109">To disable texture mapping, set this as the color operation for the first texture stage (stage 0).</span></span> <span data-ttu-id="b3ea8-110">Les opérations alpha ne peuvent pas être désactivées lorsque les opérations de couleur sont activées.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-110">Alpha operations cannot be disabled when color operations are enabled.</span></span> <span data-ttu-id="b3ea8-111">La définition de l’opération alpha sur D3DTOP \_ désactive lorsque la fusion de couleurs est activée entraîne un comportement indéfini.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-111">Setting the alpha operation to D3DTOP\_DISABLE when color blending is enabled causes undefined behavior.</span></span>

</dd> <dt>

<span data-ttu-id="b3ea8-112"><span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP \_ SELECTARG1**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-112"><span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP\_SELECTARG1**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-113">Utilisez la première couleur ou l’argument alpha de cette étape de texture, non modifié, comme sortie.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-113">Use this texture stage's first color or alpha argument, unmodified, as the output.</span></span> <span data-ttu-id="b3ea8-114">Cette opération affecte l’argument Color lorsqu’il est utilisé avec l' \_ État D3DTSS COLOROP texture-stage et l’argument alpha en cas d’utilisation avec D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-114">This operation affects the color argument when used with the D3DTSS\_COLOROP texture-stage state, and the alpha argument when used with D3DTSS\_ALPHAOP.</span></span>

![équation de cet argument (s (RVBA) = Arg1)](images/topfrm1.png)

</dd> <dt>

<span data-ttu-id="b3ea8-116"><span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP \_ SELECTARG2**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-116"><span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP\_SELECTARG2**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-117">Utilisez la deuxième couleur de cette étape de texture ou l’argument alpha, non modifié, comme sortie.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-117">Use this texture stage's second color or alpha argument, unmodified, as the output.</span></span> <span data-ttu-id="b3ea8-118">Cette opération affecte l’argument de couleur lorsqu’il est utilisé avec l’état de l' \_ étape de texture D3DTSS COLOROP, et l’argument alpha lorsqu’il est utilisé avec D3DTSS \_ ALPHAOP.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-118">This operation affects the color argument when used with the D3DTSS\_COLOROP texture stage state, and the alpha argument when used with D3DTSS\_ALPHAOP.</span></span>

![équation de cet argument (s (RVBA) = Arg2)](images/topfrm2.png)

</dd> <dt>

<span data-ttu-id="b3ea8-120"><span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**\_Modulation D3DTOP**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-120"><span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**D3DTOP\_MODULATE**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-121">Multipliez les composants des arguments.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-121">Multiply the components of the arguments.</span></span>

![équation de l’opération de modulation (s (RVBA) = Arg1 x ARG 2)](images/topfrm3.png)

</dd> <dt>

<span data-ttu-id="b3ea8-123"><span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP \_ MODULATE2X**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-123"><span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP\_MODULATE2X**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-124">Multipliez les composants des arguments et décalez les produits vers le bit de gauche 1 (en les multipliant par 2) pour l’éclaircissement.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-124">Multiply the components of the arguments, and shift the products to the left 1 bit (effectively multiplying them by 2) for brightening.</span></span>

![équation de l’opération Modulate2X (s (RVBA) = (Arg1 x ARG 2) puis décalée vers la gauche 1)](images/topfrm4.png)

</dd> <dt>

<span data-ttu-id="b3ea8-126"><span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP \_ MODULATE4X**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-126"><span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP\_MODULATE4X**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-127">Multipliez les composants des arguments et décalez les produits vers les 2 bits de gauche (en les multipliant par 4) pour l’éclaircissement.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-127">Multiply the components of the arguments, and shift the products to the left 2 bits (effectively multiplying them by 4) for brightening.</span></span>

![équation de l’opération Modulate4X (s (RVBA) = (Arg1 x ARG 2) puis décalée vers la gauche 2)](images/topfrm5.png)

</dd> <dt>

<span data-ttu-id="b3ea8-129"><span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP \_ Ajouter**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-129"><span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP\_ADD**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-130">Ajoutez les composants des arguments.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-130">Add the components of the arguments.</span></span>

![équation de l’opération d’ajout (s (RVBA) = Arg1 + ARG 2)](images/topfrm6.png)

</dd> <dt>

<span data-ttu-id="b3ea8-132"><span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP \_ ADDSIGNED**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-132"><span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP\_ADDSIGNED**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-133">Ajoutez les composants des arguments avec un décalage-0,5, ce qui rend la plage effective des valeurs comprises entre-0,5 et 0,5.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-133">Add the components of the arguments with a - 0.5 bias, making the effective range of values from - 0.5 through 0.5.</span></span>

![équation de l’ajout d’une ou de plusieurs opérations signées (RVBA) = Arg1 + ARG 2 – 0,5)](images/topfrm7.png)

</dd> <dt>

<span data-ttu-id="b3ea8-135"><span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP \_ ADDSIGNED2X**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-135"><span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP\_ADDSIGNED2X**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-136">Ajoutez les composants des arguments avec un décalage-0,5, puis décalez les produits vers la gauche 1 bit.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-136">Add the components of the arguments with a - 0.5 bias, and shift the products to the left 1 bit.</span></span>

![équation de l’opération Add signed 2x ((s (RVBA) = Arg1 + ARG 2-0,5), puis décalée vers la gauche 1)](images/topfrm8.png)

</dd> <dt>

<span data-ttu-id="b3ea8-138"><span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**D3DTOP \_ soustraire**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-138"><span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**D3DTOP\_SUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-139">Soustraire les composants du deuxième argument de ceux du premier argument.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-139">Subtract the components of the second argument from those of the first argument.</span></span>

![équation de l’opération de soustraction (s (RVBA) = Arg1-ARG 2)](images/topfrm9.png)

</dd> <dt>

<span data-ttu-id="b3ea8-141"><span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP \_ ADDSMOOTH**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-141"><span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP\_ADDSMOOTH**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-142">Ajoutez le premier et le deuxième arguments ; soustrayez ensuite le produit de la somme.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-142">Add the first and second arguments; then subtract their product from the sum.</span></span>

![équation de l’ajout d’opérations lisses (s (RVBA) = Arg1 + ARG 2 x (1-Arg1))](images/topfrm10.png)

</dd> <dt>

<span data-ttu-id="b3ea8-144"><span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP \_ BLENDDIFFUSEALPHA**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-144"><span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP\_BLENDDIFFUSEALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-145">Mélanger de manière linéaire cette étape de texture à l’aide de l’alpha interpolé à partir de chaque vertex.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-145">Linearly blend this texture stage, using the interpolated alpha from each vertex.</span></span>

![équation de l’opération Blend diffuse alpha (s (RVBA) = Arg1 x alpha + ARG 2 x (1-alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="b3ea8-147"><span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP \_ BLENDTEXTUREALPHA**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-147"><span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP\_BLENDTEXTUREALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-148">Fusionne de manière linéaire cette étape de texture à l’aide de l’alpha de la texture de cette étape.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-148">Linearly blend this texture stage, using the alpha from this stage's texture.</span></span>

![équation de l’opération alpha de texture de fusion (s (RVBA) = Arg1 x alpha + ARG 2 x (1-alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="b3ea8-150"><span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP \_ BLENDFACTORALPHA**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-150"><span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP\_BLENDFACTORALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-151">Mélangez de manière linéaire cette étape de texture à l’aide d’un alpha scalaire défini avec l' \_ État de rendu D3DRS TEXTUREFACTOR.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-151">Linearly blend this texture stage, using a scalar alpha set with the D3DRS\_TEXTUREFACTOR render state.</span></span>

![équation du facteur de fusion alpha Operation (s (RVBA) = Arg1 x alpha + ARG 2 x (1-alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="b3ea8-153"><span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP \_ BLENDTEXTUREALPHAPM**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-153"><span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP\_BLENDTEXTUREALPHAPM**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-154">Fusionne de manière linéaire une étape de texture qui utilise une alpha prémultipliée.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-154">Linearly blend a texture stage that uses a premultiplied alpha.</span></span>

![équation de la texture de fusion alpha PM (s (RVBA) = Arg1 + ARG 2 x (1-alpha))](images/topfrm12.png)

</dd> <dt>

<span data-ttu-id="b3ea8-156"><span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP \_ BLENDCURRENTALPHA**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-156"><span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP\_BLENDCURRENTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-157">Mélangez de manière linéaire cette étape de texture à l’aide de l’alpha prélevé à partir de l’étape de texture précédente.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-157">Linearly blend this texture stage, using the alpha taken from the previous texture stage.</span></span>

![équation de l’opération alpha actuelle de fusion (s (RVBA) = Arg1 x alpha + Arg2 x (1-alpha))](images/topfrm11.png)

</dd> <dt>

<span data-ttu-id="b3ea8-159"><span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**Prémodulation D3DTOP \_**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-159"><span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOP\_PREMODULATE**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-160">Le \_ PRÉMODULATION D3DTOP est défini à l’étape n.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-160">D3DTOP\_PREMODULATE is set in stage n.</span></span> <span data-ttu-id="b3ea8-161">La sortie de la phase n est Arg1.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-161">The output of stage n is arg1.</span></span> <span data-ttu-id="b3ea8-162">En outre, s’il y a une texture à la phase n + 1, tout D3DTA \_ actuel à la phase n + 1 est prémultiplié par la texture à l’étape n + 1.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-162">Additionally, if there is a texture in stage n + 1, any D3DTA\_CURRENT in stage n + 1 is premultiplied by texture in stage n + 1.</span></span>

</dd> <dt>

<span data-ttu-id="b3ea8-163"><span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP \_ MODULATEALPHA \_ ADDCOLOR**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-163"><span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP\_MODULATEALPHA\_ADDCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-164">Moduler la couleur du deuxième argument, à l’aide de l’alpha du premier argument ; Ajoutez ensuite le résultat à l’argument 1.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-164">Modulate the color of the second argument, using the alpha of the first argument; then add the result to argument one.</span></span> <span data-ttu-id="b3ea8-165">Cette opération est prise en charge uniquement pour les opérations de couleur (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="b3ea8-165">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![équation de l’opération d’ajout de couleurs module alpha (s (RVBA) = Arg1 (RVB) + Arg1 (a) x Arg2 (RVB))](images/topfrm13.png)

</dd> <dt>

<span data-ttu-id="b3ea8-167"><span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP \_ MODULATECOLOR \_ ADDALPHA**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-167"><span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP\_MODULATECOLOR\_ADDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-168">Moduler les arguments ; Ajoutez ensuite le alpha du premier argument.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-168">Modulate the arguments; then add the alpha of the first argument.</span></span> <span data-ttu-id="b3ea8-169">Cette opération est prise en charge uniquement pour les opérations de couleur (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="b3ea8-169">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![équation de l’opération de couleur ajouter un module alpha (s (RVBA) = Arg1 (RVB) x Arg2 (RVB) + Arg1 (a))](images/topfrm14.png)

</dd> <dt>

<span data-ttu-id="b3ea8-171"><span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP \_ MODULATEINVALPHA \_ ADDCOLOR**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-171"><span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP\_MODULATEINVALPHA\_ADDCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-172">Semblable à D3DTOP \_ MODULATEALPHA \_ ADDCOLOR, mais utilise l’inverse de l’alpha du premier argument.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-172">Similar to D3DTOP\_MODULATEALPHA\_ADDCOLOR, but use the inverse of the alpha of the first argument.</span></span> <span data-ttu-id="b3ea8-173">Cette opération est prise en charge uniquement pour les opérations de couleur (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="b3ea8-173">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![équation de l’ajout de couleur module de l’opération alpha inverse (s (RVBA) = (1-Arg1 (a)) x Arg2 (RVB) + Arg1 (RVB))](images/topfrm15.png)

</dd> <dt>

<span data-ttu-id="b3ea8-175"><span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP \_ MODULATEINVCOLOR \_ ADDALPHA**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-175"><span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP\_MODULATEINVCOLOR\_ADDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-176">Semblable à D3DTOP \_ MODULATECOLOR \_ ADDALPHA, mais utilise l’inverse de la couleur du premier argument.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-176">Similar to D3DTOP\_MODULATECOLOR\_ADDALPHA, but use the inverse of the color of the first argument.</span></span> <span data-ttu-id="b3ea8-177">Cette opération est prise en charge uniquement pour les opérations de couleur (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="b3ea8-177">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

![équation de l’opération ajouter une couleur d’inversion de module alpha (RVBA) = (1-Arg1 (RVB)) x Arg2 (RVB) + Arg1 (a))](images/topfrm16.png)

</dd> <dt>

<span data-ttu-id="b3ea8-179"><span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP \_ BUMPENVMAP**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-179"><span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP\_BUMPENVMAP**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-180">Effectuez un mappage de bosselage par pixel à l’aide de la carte d’environnement dans l’étape de texture suivante, sans luminance.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-180">Perform per-pixel bump mapping, using the environment map in the next texture stage, without luminance.</span></span> <span data-ttu-id="b3ea8-181">Cette opération est prise en charge uniquement pour les opérations de couleur (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="b3ea8-181">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

</dd> <dt>

<span data-ttu-id="b3ea8-182"><span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP \_ BUMPENVMAPLUMINANCE**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-182"><span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP\_BUMPENVMAPLUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-183">Effectuez un mappage de bosselage par pixel, à l’aide de la carte d’environnement dans l’étape de texture suivante, avec la luminance.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-183">Perform per-pixel bump mapping, using the environment map in the next texture stage, with luminance.</span></span> <span data-ttu-id="b3ea8-184">Cette opération est prise en charge uniquement pour les opérations de couleur (D3DTSS \_ COLOROP).</span><span class="sxs-lookup"><span data-stu-id="b3ea8-184">This operation is supported only for color operations (D3DTSS\_COLOROP).</span></span>

</dd> <dt>

<span data-ttu-id="b3ea8-185"><span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP \_ DOTPRODUCT3**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-185"><span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP\_DOTPRODUCT3**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-186">Moduler les composants de chaque argument en tant que composants signés, ajouter leurs produits ; Ensuite, répliquez la somme sur tous les canaux de couleurs, y compris alpha.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-186">Modulate the components of each argument as signed components, add their products; then replicate the sum to all color channels, including alpha.</span></span> <span data-ttu-id="b3ea8-187">Cette opération est prise en charge pour les opérations de couleur et alpha.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-187">This operation is supported for color and alpha operations.</span></span>

![équation du point produit 3 Operations (s (RVBA) = Arg1 (r) x Arg2 (r) + Arg1 (g) x Arg2 (g) + Arg1 (b) x Arg2 (b))](images/topfrm17.png)

<span data-ttu-id="b3ea8-189">Dans DirectX 6 et DirectX 7, les opérations de multitextures, les entrées ci-dessus sont toutes décalées de moitié (y = x-0,5) avant d’être utilisées pour simuler des données signées, et le résultat scalaire est automatiquement ancré aux valeurs positives et répliqué sur les trois canaux de sortie.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-189">In DirectX 6 and DirectX 7, multitexture operations the above inputs are all shifted down by half (y = x - 0.5) before use to simulate signed data, and the scalar result is automatically clamped to positive values and replicated to all three output channels.</span></span> <span data-ttu-id="b3ea8-190">Notez également qu’en tant qu’opération de couleur, cela ne met pas à jour le alpha, il met simplement à jour les composants RGB.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-190">Also, note that as a color operation this does not updated the alpha it just updates the RGB components.</span></span>

<span data-ttu-id="b3ea8-191">Toutefois, dans les nuanceurs DirectX 8,1, vous pouvez spécifier que la sortie doit être acheminée vers les composants. RGB ou. a ou les deux (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="b3ea8-191">However, in DirectX 8.1 shaders you can specify that the output be routed to the .rgb or the .a components or both (the default).</span></span> <span data-ttu-id="b3ea8-192">Vous pouvez également spécifier une opération scalaire distincte sur le canal alpha.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-192">You can also specify a separate scalar operation on the alpha channel.</span></span>

</dd> <dt>

<span data-ttu-id="b3ea8-193"><span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP \_ MULTIPLYADD**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-193"><span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP\_MULTIPLYADD**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-194">Effectue une opération de multiplication cumulée.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-194">Performs a multiply-accumulate operation.</span></span> <span data-ttu-id="b3ea8-195">Elle prend les deux derniers arguments, les multiplie et les ajoute à l’argument d’entrée/source restant, et les place dans le résultat.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-195">It takes the last two arguments, multiplies them together, and adds them to the remaining input/source argument, and places that into the result.</span></span>

<span data-ttu-id="b3ea8-196">S<sub>RVBA</sub> = Arg1 + Arg2 \* Arg3</span><span class="sxs-lookup"><span data-stu-id="b3ea8-196">S<sub>RGBA</sub> = Arg1 + Arg2 \* Arg3</span></span>

</dd> <dt>

<span data-ttu-id="b3ea8-197"><span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP \_ LERP**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-197"><span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP\_LERP**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-198">Interpole de manière linéaire entre le deuxième et le troisième argument source en fonction d’une proportion spécifiée dans le premier argument source.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-198">Linearly interpolates between the second and third source arguments by a proportion specified in the first source argument.</span></span>

<span data-ttu-id="b3ea8-199">S<sub>RVBA</sub> = (Arg1) \* Arg2 + (1-Arg1) \* Arg3.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-199">S<sub>RGBA</sub> = (Arg1) \* Arg2 + (1- Arg1) \* Arg3.</span></span>

</dd> <dt>

<span data-ttu-id="b3ea8-200"><span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-200"><span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="b3ea8-201">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-201">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="b3ea8-202">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-202">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="b3ea8-203">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-203">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3ea8-204">Notes</span><span class="sxs-lookup"><span data-stu-id="b3ea8-204">Remarks</span></span>

<span data-ttu-id="b3ea8-205">Les membres de ce type sont utilisés lors de la définition d’opérations de couleur ou alpha à l’aide des \_ valeurs D3DTSS COLOROP ou D3DTSS \_ ALPHAOP avec la méthode [**IDirect3DDevice9 :: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="b3ea8-205">The members of this type are used when setting color or alpha operations by using the D3DTSS\_COLOROP or D3DTSS\_ALPHAOP values with the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span>

<span data-ttu-id="b3ea8-206">Dans les formules ci-dessus, S<sub>RVBA</sub> est la couleur RVBA produite par une opération de texture, et Arg1, Arg2 et Arg3 représentent la couleur RVBA complète des arguments de texture.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-206">In the above formulas, S<sub>RGBA</sub> is the RGBA color produced by a texture operation, and Arg1, Arg2, and Arg3 represent the complete RGBA color of the texture arguments.</span></span> <span data-ttu-id="b3ea8-207">Les composants individuels d’un argument sont affichés avec des indices.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-207">Individual components of an argument are shown with subscripts.</span></span> <span data-ttu-id="b3ea8-208">Par exemple, le composant alpha pour l’argument 1 s’affiche comme Arg1<sub>A</sub>.</span><span class="sxs-lookup"><span data-stu-id="b3ea8-208">For example, the alpha component for argument 1 would be shown as Arg1<sub>A</sub>.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3ea8-209">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3ea8-209">Requirements</span></span>



| <span data-ttu-id="b3ea8-210">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3ea8-210">Requirement</span></span> | <span data-ttu-id="b3ea8-211">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3ea8-211">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3ea8-212">En-tête</span><span class="sxs-lookup"><span data-stu-id="b3ea8-212">Header</span></span><br/> | <dl> <span data-ttu-id="b3ea8-213"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3ea8-213"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3ea8-214">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3ea8-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3ea8-215">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="b3ea8-215">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="b3ea8-216">**D3DTEXTURESTAGESTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="b3ea8-216">**D3DTEXTURESTAGESTATETYPE**</span></span>](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
