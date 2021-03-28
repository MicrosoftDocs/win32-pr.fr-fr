---
title: Masquage du registre de destination
description: Le masquage spécifie les composants du registre de destination qui seront mis à jour avec le résultat d’une instruction. Les registres de texture ont un ensemble de règles et les registres de la même façon ont un autre ensemble de règles.
ms.assetid: 989ebe55-1f80-4063-b116-4284520f52cc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7ce15f75f424cb7796ef7db7a8b89bd5bcbfa9cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380153"
---
# <a name="destination-register-masking"></a><span data-ttu-id="fad13-104">Masquage du registre de destination</span><span class="sxs-lookup"><span data-stu-id="fad13-104">Destination Register Masking</span></span>

<span data-ttu-id="fad13-105">Le masquage spécifie les composants du registre de destination qui seront mis à jour avec le résultat d’une instruction.</span><span class="sxs-lookup"><span data-stu-id="fad13-105">Masking specifies which components of the destination register will be updated with the result of an instruction.</span></span> <span data-ttu-id="fad13-106">Les registres de texture ont un ensemble de règles et les registres de la même façon ont un autre ensemble de règles.</span><span class="sxs-lookup"><span data-stu-id="fad13-106">Texture registers have one set of rules and nontexture registers have another set of rules.</span></span>

-   <span data-ttu-id="fad13-107">virtuel DX9 \_ Graphics \_ Reference \_ ASM \_ vs \_ enregistreurs \_ modificateurs \_ Masking-cette section contient des règles pour l’application de masques aux registres de destination.</span><span class="sxs-lookup"><span data-stu-id="fad13-107">dx9\_graphics\_reference\_asm\_vs\_registers\_modifiers\_masking - This section contains rules for applying masks to destination registers.</span></span>
-   <span data-ttu-id="fad13-108">\_ \_ Masques de registre de texture-les registres de texture présentent des règles uniques.</span><span class="sxs-lookup"><span data-stu-id="fad13-108">Texture\_Register\_Masks - Texture registers have some unique rules.</span></span>

## <a name="destination-register-masking"></a><span data-ttu-id="fad13-109">Masquage du registre de destination</span><span class="sxs-lookup"><span data-stu-id="fad13-109">Destination Register Masking</span></span>

<span data-ttu-id="fad13-110">Comme indiqué dans le tableau suivant, le masquage (où est l’un des [registres de nuanceur](dx9-graphics-reference-asm-vs-registers.md)vertex nuanceur de sommets valides) peut être appliqué aux composants individuels des données vectorielles.</span><span class="sxs-lookup"><span data-stu-id="fad13-110">As shown in the following table, masking (where r is one of the valid vertex shader [Vertex Shader Registers](dx9-graphics-reference-asm-vs-registers.md)) can be applied to the individual components of the vector data.</span></span>



| <span data-ttu-id="fad13-111">Modificateur de composant</span><span class="sxs-lookup"><span data-stu-id="fad13-111">Component modifier</span></span> | <span data-ttu-id="fad13-112">Description</span><span class="sxs-lookup"><span data-stu-id="fad13-112">Description</span></span>      |
|--------------------|------------------|
| <span data-ttu-id="fad13-113">r. {x} {y} {z} {w}</span><span class="sxs-lookup"><span data-stu-id="fad13-113">r.{x}{y}{z}{w}</span></span>     | <span data-ttu-id="fad13-114">Masque de destination</span><span class="sxs-lookup"><span data-stu-id="fad13-114">Destination mask</span></span> |



 

-   <span data-ttu-id="fad13-115">En général, la spécification de masques d’écriture de registre de destination est un bon style de codage.</span><span class="sxs-lookup"><span data-stu-id="fad13-115">In general, specifying destination register write masks is good coding style.</span></span> <span data-ttu-id="fad13-116">Cela rend le code plus facile à lire et à gérer.</span><span class="sxs-lookup"><span data-stu-id="fad13-116">It makes code easier to read and maintain.</span></span>
-   <span data-ttu-id="fad13-117">Vous pouvez spécifier n’importe quelle combinaison de composants (y compris aucun) tant que x précède y, y précède z et z précède w.</span><span class="sxs-lookup"><span data-stu-id="fad13-117">Any combination of components may be specified (including none) as long as x precedes y, y precedes z, and z precedes w.</span></span>
-   <span data-ttu-id="fad13-118">Les registres de sortie oPts et oFog doivent utiliser un seul masque.</span><span class="sxs-lookup"><span data-stu-id="fad13-118">The oPts and oFog output registers must use only one mask.</span></span>
-   <span data-ttu-id="fad13-119">Certaines instructions requièrent que le registre de destination utilise un masque d’écriture unique : exp, expp, log, logP, Pow, RCP et rsq.</span><span class="sxs-lookup"><span data-stu-id="fad13-119">Certain instructions require the destination register to use a single write mask: exp, expp, log, logp, pow, rcp, and rsq.</span></span>
-   <span data-ttu-id="fad13-120">Dans la version 1,0, l’instruction FRC nécessitait l’une des combinaisons de masques suivantes :. x ou. y ou. XY.</span><span class="sxs-lookup"><span data-stu-id="fad13-120">In version 1.0, the frc instruction required one of the following mask combinations: .x or .y or .xy.</span></span> <span data-ttu-id="fad13-121">La version 2,0 n’a aucune restriction de masque.</span><span class="sxs-lookup"><span data-stu-id="fad13-121">Version 2.0 has no mask restriction.</span></span>
-   <span data-ttu-id="fad13-122">SinCos, requiert l’une des combinaisons de masques suivantes :. x ou. y ou. xyz.</span><span class="sxs-lookup"><span data-stu-id="fad13-122">sincos requires one of the following mask combinations: .x or .y or .xyz.</span></span>
-   <span data-ttu-id="fad13-123">M3X2 requiert le masque d’écriture. XY.</span><span class="sxs-lookup"><span data-stu-id="fad13-123">m3x2 requires the .xy write mask.</span></span>
-   <span data-ttu-id="fad13-124">M3x3 et m4x3 requièrent le masque d’écriture. xyz.</span><span class="sxs-lookup"><span data-stu-id="fad13-124">m3x3 and m4x3 require the .xyz write mask.</span></span>
-   <span data-ttu-id="fad13-125">M3x4 et M4X4 requièrent le masque d’écriture. xyz ou le masque d’écriture par défaut (XYZW).</span><span class="sxs-lookup"><span data-stu-id="fad13-125">m3x4 and m4x4 require either the .xyz write mask or the default write mask (xyzw).</span></span>

## <a name="texture-register-masks"></a><span data-ttu-id="fad13-126">Masques de registre de texture</span><span class="sxs-lookup"><span data-stu-id="fad13-126">Texture Register Masks</span></span>

<span data-ttu-id="fad13-127">Les règles de validation pour l’utilisation de modificateurs sur les registres de coordonnées de texture sont plus strictes que les règles de validation pour les autres registres.</span><span class="sxs-lookup"><span data-stu-id="fad13-127">The validation rules for using modifiers on texture coordinate registers are tighter than the validation rules for other registers.</span></span>

-   <span data-ttu-id="fad13-128">Si oTn est écrit, tous les registres précédents (oTn-1 ~ oT0) doivent également être écrits.</span><span class="sxs-lookup"><span data-stu-id="fad13-128">If oTn is written, all previous registers (oTn-1 ~ oT0) have to be written as well.</span></span>
-   <span data-ttu-id="fad13-129">Le masque d’écriture « combiné » pour tout \# Registre OT doit être exactement l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="fad13-129">The "combined" write mask for any oT\# register must be exactly one of the following:</span></span>
    -   <span data-ttu-id="fad13-130">.x</span><span class="sxs-lookup"><span data-stu-id="fad13-130">.x</span></span>
    -   <span data-ttu-id="fad13-131">. XY</span><span class="sxs-lookup"><span data-stu-id="fad13-131">.xy</span></span>
    -   <span data-ttu-id="fad13-132">. xyz</span><span class="sxs-lookup"><span data-stu-id="fad13-132">.xyz</span></span>
    -   <span data-ttu-id="fad13-133">. XYZW (ce qui équivaut à ne pas utiliser de modificateurs de composant)</span><span class="sxs-lookup"><span data-stu-id="fad13-133">.xyzw (which is equivalent to not using any component modifiers)</span></span>

<span data-ttu-id="fad13-134">Par exemple, un nuanceur de sommets peut sortir des registres de texture dans des instructions distinctes.</span><span class="sxs-lookup"><span data-stu-id="fad13-134">For example, a vertex shader can output to texture registers in separate instructions.</span></span>


```
    oT1.y  
    oT0.y  
    oT2  
    oT0.xz  
    oT1.x
```



<span data-ttu-id="fad13-135">Ou, les instructions peuvent être combinées.</span><span class="sxs-lookup"><span data-stu-id="fad13-135">Or, the instructions can be combined.</span></span>


```
    oT0.xyz  
    oT1.xy  
    oT2.xyzw    
```



<span data-ttu-id="fad13-136">Ces restrictions s’appliquent uniquement aux registres de coordonnées de texture.</span><span class="sxs-lookup"><span data-stu-id="fad13-136">These restrictions apply only to the texture coordinate registers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fad13-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fad13-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fad13-138">Modificateurs de registre de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="fad13-138">Vertex Shader Register Modifiers</span></span>](dx9-graphics-reference-asm-vs-registers-modifiers.md)
</dt> </dl>

 

 




