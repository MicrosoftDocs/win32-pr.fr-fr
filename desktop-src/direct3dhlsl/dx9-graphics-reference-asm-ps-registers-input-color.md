---
title: Registre des couleurs d’entrée
description: Registre d’entrée de nuanceur de pixels contenant la couleur du vertex.
ms.assetid: d2e21f87-000e-410a-aaba-172000ed1c5f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73ea16c5aa6b49bce59fe51905734344e4e1cffb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380426"
---
# <a name="input-color-register"></a><span data-ttu-id="80de6-103">Registre des couleurs d’entrée</span><span class="sxs-lookup"><span data-stu-id="80de6-103">Input Color Register</span></span>

<span data-ttu-id="80de6-104">Registre d’entrée de nuanceur de pixels contenant la couleur du vertex.</span><span class="sxs-lookup"><span data-stu-id="80de6-104">Pixel shader input register containing vertex color.</span></span>

## <a name="syntax"></a><span data-ttu-id="80de6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80de6-105">Syntax</span></span>


```
dcl v#.writeMask
```



<span data-ttu-id="80de6-106">où :</span><span class="sxs-lookup"><span data-stu-id="80de6-106">where:</span></span>

-   <span data-ttu-id="80de6-107">[DCL-(SM2, SM3-PS ASM)](dcl---ps.md) est une instruction de déclaration de registre.</span><span class="sxs-lookup"><span data-stu-id="80de6-107">[dcl - (sm2, sm3 - ps asm)](dcl---ps.md) is a register declaration instruction.</span></span>
-   <span data-ttu-id="80de6-108">v est un registre d’entrée et \# est le numéro du Registre.</span><span class="sxs-lookup"><span data-stu-id="80de6-108">v is an input register and \# is the register number.</span></span> <span data-ttu-id="80de6-109">Le nombre de registres autorisés est déterminé par la version du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="80de6-109">The number of registers allowed is determined by the shader version.</span></span>
-   <span data-ttu-id="80de6-110">writeMask détermine les composants (jusqu’à quatre) qui sont écrits.</span><span class="sxs-lookup"><span data-stu-id="80de6-110">writeMask determines which components (up to four) are written.</span></span> <span data-ttu-id="80de6-111">Les composants valides sont : (x, y, z, w) ou (r, g, b, a).</span><span class="sxs-lookup"><span data-stu-id="80de6-111">Valid components are: (x,y,z,w) or (r,g,b,a).</span></span>

## <a name="remarks"></a><span data-ttu-id="80de6-112">Notes</span><span class="sxs-lookup"><span data-stu-id="80de6-112">Remarks</span></span>

<span data-ttu-id="80de6-113">Les registres de couleurs sont des registres en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="80de6-113">Color registers are read-only registers.</span></span> <span data-ttu-id="80de6-114">Chaque registre contient des valeurs RVBA à quatre composants itérées à partir des vertex d’entrée.</span><span class="sxs-lookup"><span data-stu-id="80de6-114">Each register contains four-component RGBA values iterated from input vertices.</span></span> <span data-ttu-id="80de6-115">Ils ont une précision inférieure à la plupart des registres, garanti qu’ils disposent de 8 bits de données non signées dans la plage (0, + 1).</span><span class="sxs-lookup"><span data-stu-id="80de6-115">They have lower precision than most registers, guaranteed to have 8 bits of unsigned data in the range (0, +1).</span></span> <span data-ttu-id="80de6-116">Vous ne pouvez pas en utiliser plusieurs dans une seule instruction.</span><span class="sxs-lookup"><span data-stu-id="80de6-116">You cannot use more than one in a single instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80de6-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80de6-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80de6-118">Inscrit</span><span class="sxs-lookup"><span data-stu-id="80de6-118">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> <dt>

[<span data-ttu-id="80de6-119">registres PS 1 \_ \_ 1 PS 1 2 PS 1 \_ \_ \_ \_ \_ \_ \_ \_ 3 PS 1 \_ \_ \_ \_ 4</span><span class="sxs-lookup"><span data-stu-id="80de6-119">ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)
</dt> <dt>

[<span data-ttu-id="80de6-120">\_registres PS 2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="80de6-120">ps\_2\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-0.md)
</dt> <dt>

[<span data-ttu-id="80de6-121">\_registres PS 2 \_ x</span><span class="sxs-lookup"><span data-stu-id="80de6-121">ps\_2\_x Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-2-x.md)
</dt> <dt>

[<span data-ttu-id="80de6-122">\_registres PS 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="80de6-122">ps\_3\_0 Registers</span></span>](dx9-graphics-reference-asm-ps-registers-ps-3-0.md)
</dt> </dl>

 

 




