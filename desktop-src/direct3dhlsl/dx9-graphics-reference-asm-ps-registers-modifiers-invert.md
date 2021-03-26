---
title: Registre source inversé
description: Effectue un calcul (1 valeur) pour chaque canal du Registre spécifié.
ms.assetid: 387e409f-d76d-4d70-be0f-fb563f542482
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce65960474816a91eb64ece7b754b97090903d46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971455"
---
# <a name="source-register-invert"></a><span data-ttu-id="a3ccb-103">Registre source inversé</span><span class="sxs-lookup"><span data-stu-id="a3ccb-103">Source Register Invert</span></span>

<span data-ttu-id="a3ccb-104">Effectue un calcul (1 valeur) pour chaque canal du Registre spécifié.</span><span class="sxs-lookup"><span data-stu-id="a3ccb-104">Performs a (1 - value) calculation for each channel of the specified register.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3ccb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3ccb-105">Syntax</span></span>


```
1 - register
```



## <a name="registers"></a><span data-ttu-id="a3ccb-106">Registres</span><span class="sxs-lookup"><span data-stu-id="a3ccb-106">Registers</span></span>

<span data-ttu-id="a3ccb-107">Registre source.</span><span class="sxs-lookup"><span data-stu-id="a3ccb-107">Source Register.</span></span> <span data-ttu-id="a3ccb-108">Pour plus d’informations sur les types de registres, consultez les [registres PS 1 \_ \_ 1 \_ \_ PS 1 \_ \_ 2 \_ \_ \_ \_ \_ \_ \_ \_ ](dx9-graphics-reference-asm-ps-registers-ps-1-x.md)PS 1 3 PS 1 4.</span><span class="sxs-lookup"><span data-stu-id="a3ccb-108">For more about register types, see [ps\_1\_1\_\_ps\_1\_2\_\_ps\_1\_3\_\_ps\_1\_4 Registers](dx9-graphics-reference-asm-ps-registers-ps-1-x.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="a3ccb-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a3ccb-109">Remarks</span></span>

<span data-ttu-id="a3ccb-110">Le contenu du Registre n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="a3ccb-110">The contents of the register are not changed.</span></span> <span data-ttu-id="a3ccb-111">Le modificateur est appliqué uniquement aux données lues à partir du Registre.</span><span class="sxs-lookup"><span data-stu-id="a3ccb-111">The modifier is applied only to the data read from the register.</span></span> <span data-ttu-id="a3ccb-112">L’opération inversée est appliquée aux quatre canaux de couleurs (RVBA).</span><span class="sxs-lookup"><span data-stu-id="a3ccb-112">The invert operation is applied to all four color channels (RGBA).</span></span>

<span data-ttu-id="a3ccb-113">Ce modificateur ne peut être utilisé qu’avec des instructions arithmétiques.</span><span class="sxs-lookup"><span data-stu-id="a3ccb-113">This modifier can be used only with arithmetic instructions.</span></span> <span data-ttu-id="a3ccb-114">En outre, ce modificateur ne peut pas être combiné avec l’autre [masque d’écriture de registre de destination](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span><span class="sxs-lookup"><span data-stu-id="a3ccb-114">In addition, this modifier cannot be combined with the other [Destination Register Write Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).</span></span>

## <a name="example"></a><span data-ttu-id="a3ccb-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="a3ccb-115">Example</span></span>

<span data-ttu-id="a3ccb-116">Cet exemple utilise inversion pour générer le complément du Registre R1.</span><span class="sxs-lookup"><span data-stu-id="a3ccb-116">This example uses inversion to generate the complement of register r1.</span></span>


```
mul r0, r0, 1-r1;
```



## <a name="related-topics"></a><span data-ttu-id="a3ccb-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a3ccb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3ccb-118">Modificateurs de Registre source du nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="a3ccb-118">Pixel Shader Source Register Modifiers</span></span>](dx9-graphics-reference-asm-ps-registers-modifiers-source.md)
</dt> </dl>

 

 




