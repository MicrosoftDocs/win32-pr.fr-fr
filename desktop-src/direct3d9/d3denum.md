---
description: Indicateur de fonctionnalité du pilote.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 059c2f9f1bf32275423bb9f2a9f484c12824bcda
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516777"
---
# <a name="d3denum"></a><span data-ttu-id="b2828-103">D3DENUM</span><span class="sxs-lookup"><span data-stu-id="b2828-103">D3DENUM</span></span>

<span data-ttu-id="b2828-104">Indicateur de fonctionnalité du pilote.</span><span class="sxs-lookup"><span data-stu-id="b2828-104">Driver capability flag.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b2828-105">#définition</span><span class="sxs-lookup"><span data-stu-id="b2828-105">#define</span></span></td>
<td><span data-ttu-id="b2828-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2828-106">Value</span></span></td>
<td><span data-ttu-id="b2828-107">Description</span><span class="sxs-lookup"><span data-stu-id="b2828-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2828-108">D3DENUM_WHQL_LEVEL</span><span class="sxs-lookup"><span data-stu-id="b2828-108">D3DENUM_WHQL_LEVEL</span></span></td>
<td><span data-ttu-id="b2828-109">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="b2828-109">0x00000002L</span></span></td>
<td><span data-ttu-id="b2828-110">Test des pilotes WHQL (Microsoft Windows Hardware Quality Labs).</span><span class="sxs-lookup"><span data-stu-id="b2828-110">Microsoft Windows Hardware Quality Labs (WHQL) driver testing.</span></span> <span data-ttu-id="b2828-111">Il s’agit d’un test qui prend beaucoup de temps, ce qui nécessite une pénalité d’une seconde ou de deux secondes.</span><span class="sxs-lookup"><span data-stu-id="b2828-111">This is a time-consuming test requiring a one-second or two-second time penalty.</span></span> <span data-ttu-id="b2828-112">Cette constante est utilisée par le membre WHQLLevel de <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="b2828-112">This constant is used by the WHQLLevel member of <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b2828-113">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="b2828-113">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="b2828-114">D3DENUM_WHQL_LEVEL est déconseillé pour les Direct3D9Ex s’exécutant sur Windows Vista, Windows Server 2008, Windows 7 et Windows Server 2008 R2 (ou plus le système d’exploitation actuel).</span><span class="sxs-lookup"><span data-stu-id="b2828-114">D3DENUM_WHQL_LEVEL is deprecated for Direct3D9Ex running on Windows Vista, Windows Server 2008, Windows 7, and Windows Server 2008 R2 (or more current operating system).</span></span> <span data-ttu-id="b2828-115">L’un de ces systèmes d’exploitation retourne 1 pour le niveau WHQL sans vérifier l’état du pilote.</span><span class="sxs-lookup"><span data-stu-id="b2828-115">Any of these operating systems return 1 for the WHQL level without checking the status of the driver.</span></span> <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a><span data-ttu-id="b2828-116">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="b2828-116">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="b2828-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2828-117">Header</span></span>                   | <span data-ttu-id="b2828-118">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="b2828-118">d3d9.h</span></span>     |
| <span data-ttu-id="b2828-119">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="b2828-119">Minimum operating system</span></span> | <span data-ttu-id="b2828-120">Windows 98</span><span class="sxs-lookup"><span data-stu-id="b2828-120">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b2828-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2828-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2828-122">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="b2828-122">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




