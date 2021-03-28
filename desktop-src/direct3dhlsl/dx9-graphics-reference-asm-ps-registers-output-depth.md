---
title: Registre de profondeur de sortie
description: Le registre de profondeur de sortie du nuanceur de pixels (oDepth) est un registre scalaire en écriture seule avec la plage \ 0.. 1 \ qui retourne une nouvelle valeur de profondeur pour un test de profondeur par rapport à la mémoire tampon du stencil de profondeur.
ms.assetid: 47b9afd9-4520-480d-b4a2-3d9a5569defb
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9be825d6117cf1cc14464973146dbe176d696d25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311482"
---
# <a name="output-depth-register"></a><span data-ttu-id="23f60-103">Registre de profondeur de sortie</span><span class="sxs-lookup"><span data-stu-id="23f60-103">Output Depth Register</span></span>

<span data-ttu-id="23f60-104">Le registre de profondeur de sortie du nuanceur de pixels (oDepth) est un registre scalaire en écriture seule avec la plage \[ 0.. 1 \] qui retourne une nouvelle valeur de profondeur pour un test de profondeur par rapport à la mémoire tampon du stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="23f60-104">The pixel shader output depth register (oDepth) is a write-only scalar register with the range \[0..1\] that returns a new depth value for a depth test against the depth-stencil buffer.</span></span>

<span data-ttu-id="23f60-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23f60-105">Syntax</span></span>



| <span data-ttu-id="23f60-106">oDepth</span><span class="sxs-lookup"><span data-stu-id="23f60-106">oDepth</span></span> |
|--------|



 

<span data-ttu-id="23f60-107">Où :</span><span class="sxs-lookup"><span data-stu-id="23f60-107">Where:</span></span>



| <span data-ttu-id="23f60-108">Nom</span><span class="sxs-lookup"><span data-stu-id="23f60-108">Name</span></span>   | <span data-ttu-id="23f60-109">Description</span><span class="sxs-lookup"><span data-stu-id="23f60-109">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="23f60-110">oDepth</span><span class="sxs-lookup"><span data-stu-id="23f60-110">oDepth</span></span> | <span data-ttu-id="23f60-111">Nouvelle valeur de profondeur pour un test de profondeur par rapport à la mémoire tampon du stencil de profondeur</span><span class="sxs-lookup"><span data-stu-id="23f60-111">New depth value for a depth test against the depth-stencil buffer</span></span> |



 

<span data-ttu-id="23f60-112">Il est important de savoir que l’écriture dans oDepth provoque la perte des algorithmes d’optimisation de la mémoire tampon de profondeur matérielle (Z) qui accélèrent les performances des tests de profondeur.</span><span class="sxs-lookup"><span data-stu-id="23f60-112">It is important to be aware that writing to oDepth causes the loss of any hardware-specific depth buffer optimization algorithms (i.e. hierarchical Z) which accelerate depth test performance.</span></span>

<span data-ttu-id="23f60-113">REPLICATE source Swizzle (. x.y. \| \| z. z \| ) est requis lors de l’écriture dans oDepth.</span><span class="sxs-lookup"><span data-stu-id="23f60-113">Replicate source swizzle (.x \| .y \| .z \| .w) is required when writing to oDepth.</span></span> <span data-ttu-id="23f60-114">Les masques d’écriture explicites ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="23f60-114">Explicit write masks are not allowed.</span></span>

<span data-ttu-id="23f60-115">L’écriture dans le registre oDepth remplace la valeur de profondeur interpolée (et ignore tous les décalages de profondeur/slopescale renderstates).</span><span class="sxs-lookup"><span data-stu-id="23f60-115">Writing to the oDepth register replaces the interpolated depth value (and ignores any depth bias/slopescale renderstates).</span></span> <span data-ttu-id="23f60-116">Si aucune mémoire tampon de profondeur n’a été créée ou attachée à l’appareil, l’écriture dans oDepth est ignorée.</span><span class="sxs-lookup"><span data-stu-id="23f60-116">If no depth buffer has been created or attached to the device, then write to oDepth is ignored.</span></span>

<span data-ttu-id="23f60-117">Si vous effectuez un échantillonnage multiple et écrivez dans oDepth, étant donné que le nuanceur de pixels ne s’exécute qu’une seule fois par pixel, la valeur de votre profondeur est répliquée pour tous les emplacements sous-échantillons couverts.</span><span class="sxs-lookup"><span data-stu-id="23f60-117">If you are multisampling and write to oDepth, since the pixel shader only runs once per pixel, your depth value is replicated for all covered sub-sample locations.</span></span> <span data-ttu-id="23f60-118">Le test de profondeur se produit toujours par échantillon, mais vous n’avez pas de valeur de profondeur par exemple dans la comparaison du nuanceur de pixels comme vous le feriez si vous n’aviez pas écrit de oDepth.</span><span class="sxs-lookup"><span data-stu-id="23f60-118">The depth test still happens per-sample, but you don't have a per-sample depth value going into the comparison from the pixel shader like you would have if you didn't write oDepth.</span></span>

<span data-ttu-id="23f60-119">Si une application a une mémoire tampon w définie en tant que tampon de profondeur, elle doit en tenir compte lors de l’écriture dans oDepth.</span><span class="sxs-lookup"><span data-stu-id="23f60-119">If an application has a w-buffer set as its depth buffer, then it needs to take that into account while writing to oDepth.</span></span> <span data-ttu-id="23f60-120">Il doit éventuellement envoyer des informations w-Range au nuanceur de pixels et calculer la plage w pour mettre à l’échelle les valeurs w écrites sur oDepth.</span><span class="sxs-lookup"><span data-stu-id="23f60-120">It potentially needs to send w-range information to the pixel shader and compute the w-range to scale the w-values written out to oDepth.</span></span>

### <a name="ps_2_0-and-ps_2_x-restrictions"></a><span data-ttu-id="23f60-121">\_restrictions PS 2 \_ 0 et PS \_ 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="23f60-121">ps\_2\_0 and ps\_2\_x Restrictions</span></span>

-   <span data-ttu-id="23f60-122">oDepth peut uniquement être écrit avec l’instruction [MOV-PS](mov---ps.md) et ne peut être fait qu’une seule fois.</span><span class="sxs-lookup"><span data-stu-id="23f60-122">oDepth can only be written with the [mov - ps](mov---ps.md) instruction and can only be done once.</span></span>
-   <span data-ttu-id="23f60-123">Aucun modificateur source n’est autorisé lors de l’écriture dans oDepth.</span><span class="sxs-lookup"><span data-stu-id="23f60-123">No source modifier is allowed when writing to oDepth.</span></span>
-   <span data-ttu-id="23f60-124">Aucun modificateur d’instruction n’est autorisé lors de l’écriture dans oDepth.</span><span class="sxs-lookup"><span data-stu-id="23f60-124">No instruction modifier is allowed when writing to oDepth.</span></span>
-   <span data-ttu-id="23f60-125">Aucune écriture dans oDepth à partir d’une construction de contrôle de Flow, ou lors de l’utilisation d’un prédicat.</span><span class="sxs-lookup"><span data-stu-id="23f60-125">No writing to oDepth from within a flow control construct, or when using predication.</span></span>

### <a name="ps_3_0-restrictions"></a><span data-ttu-id="23f60-126">\_restrictions PS 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="23f60-126">ps\_3\_0 Restrictions</span></span>

-   <span data-ttu-id="23f60-127">Pour PS \_ 3 \_ 0, les registres de sortie OC # et OD \# peuvent être écrits un nombre quelconque de fois.</span><span class="sxs-lookup"><span data-stu-id="23f60-127">For ps\_3\_0, output registers oC# and oD\# can be written any number of times.</span></span> <span data-ttu-id="23f60-128">La sortie du nuanceur de pixels provient du contenu des registres de sortie à la fin de l’exécution du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="23f60-128">The output of the pixel shader comes from the contents of the output registers at the end of shader execution.</span></span> <span data-ttu-id="23f60-129">Si une écriture dans un registre de sortie ne se produit pas, peut-être en raison du contrôle de flow ou si le nuanceur ne l’a pas écrit, la cible de rendu correspondante n’est pas non plus mise à jour.</span><span class="sxs-lookup"><span data-stu-id="23f60-129">If a write to an output register does not happen, perhaps due to flow control or if the shader just did not write it, the corresponding render target is also not updated.</span></span> <span data-ttu-id="23f60-130">Si un sous-ensemble des canaux d’un registre de sortie est écrit, les valeurs non définies sont écrites sur les autres canaux.</span><span class="sxs-lookup"><span data-stu-id="23f60-130">If a subset of the channels in an output register are written, then undefined values will be written to the remaining channels.</span></span>
-   <span data-ttu-id="23f60-131">Vous pouvez écrire dans oDepth dans un contrôle de flow ou un prédicat, à condition que tous les chemins d’accès possibles écrivent dans le registre.</span><span class="sxs-lookup"><span data-stu-id="23f60-131">You can write to oDepth within flow control or predication as long as all possible paths eventually write into the register.</span></span>
-   <span data-ttu-id="23f60-132">Vous n’êtes pas autorisé à effectuer des calculs de dégradés (ou des opérations qui appellent implicitement des calculs de gradient tels que [texld-PS \_ 2 \_ 0 et up](texld---ps-2-0.md), [texldb-PS](texldb---ps.md), [texldp-PS](texldp---ps.md)) à l’intérieur d’instructions de contrôle de Flow dont les conditions de création de branche varient en fonction de la primitive (c’est-à-dire : instructions de contrôle de workflow dynamique).</span><span class="sxs-lookup"><span data-stu-id="23f60-132">You may not perform any gradient calculations (or operations that implicitly invoke gradient calculations such as [texld - ps\_2\_0 and up](texld---ps-2-0.md), [texldb - ps](texldb---ps.md), [texldp - ps](texldp---ps.md)) inside of flow control statements whose branching conditions vary on a per-primitive basis (ie: dynamic flow control instructions).</span></span> <span data-ttu-id="23f60-133">La prédicat d’instruction n’est pas considéré comme un contrôle de workflow dynamique.</span><span class="sxs-lookup"><span data-stu-id="23f60-133">Instruction predication is not considered dynamic flow control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="23f60-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="23f60-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23f60-135">Inscrit</span><span class="sxs-lookup"><span data-stu-id="23f60-135">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




