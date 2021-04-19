---
title: Référence HLSL Direct3D 12 Raytracing
description: Cette section fournit des informations sur les constructions HLSL qui prennent en charge le pipeline Raytracing Direct3D 12.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7522d26eef8d3c9865a456a94fbd7eafdf99604f
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106535753"
---
# <a name="raytracing-hlsl-reference"></a><span data-ttu-id="0f82d-103">Référence HLSL Raytracing</span><span class="sxs-lookup"><span data-stu-id="0f82d-103">Raytracing HLSL reference</span></span>

<span data-ttu-id="0f82d-104">Cette section fournit des informations sur les constructions HLSL qui prennent en charge le pipeline Raytracing Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="0f82d-104">This section provides information on the HLSL constructs that support the Direct3D 12 raytracing pipeline.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0f82d-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="0f82d-105">In this section</span></span>

| <span data-ttu-id="0f82d-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="0f82d-106">Topic</span></span> | <span data-ttu-id="0f82d-107">Description</span><span class="sxs-lookup"><span data-stu-id="0f82d-107">Description</span></span> |
|-|-|
| [<span data-ttu-id="0f82d-108">Énumérations HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="0f82d-108">Direct3D 12 raytracing HLSL enumerations</span></span>](direct3d-12-raytracing-hlsl-enumerations.md) | <span data-ttu-id="0f82d-109">Décrit les énumérations HLSL qui prennent en charge le pipeline Raytracing Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="0f82d-109">Describes the HLSL enumerations that support the Direct3D 12 raytracing pipeline.</span></span>  |
| [<span data-ttu-id="0f82d-110">Intrinsèques de langage HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="0f82d-110">Direct3D 12 raytracing HLSL intrinsics</span></span>](direct3d-12-raytracing-hlsl-intrinsics.md) | <span data-ttu-id="0f82d-111">Décrit le Instrinsics HLSL qui prend en charge le pipeline Direct3D 12 Raytracing.</span><span class="sxs-lookup"><span data-stu-id="0f82d-111">Describes the HLSL instrinsics that support the Direct3D 12 raytracing pipeline.</span></span> |
| [<span data-ttu-id="0f82d-112">Types de ressources HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="0f82d-112">Direct3D 12 raytracing HLSL resource types</span></span>](direct3d-12-raytracing-hlsl-resource-types.md) | <span data-ttu-id="0f82d-113">Décrit les types de ressources HLSL qui prennent en charge le pipeline Direct3D 12 Raytracing.</span><span class="sxs-lookup"><span data-stu-id="0f82d-113">Describes the HLSL resource types that support the Direct3D 12 raytracing pipeline.</span></span> |
| [<span data-ttu-id="0f82d-114">Nuanceurs HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="0f82d-114">Direct3D 12 raytracing HLSL shaders</span></span>](direct3d-12-raytracing-hlsl-shaders.md) | <span data-ttu-id="0f82d-115">Décrit les nuanceurs HLSL qui prennent en charge le pipeline Raytracing Direct3D 12.</span><span class="sxs-lookup"><span data-stu-id="0f82d-115">Describes the HLSL shaders that support the Direct3D 12 raytracing pipeline.</span></span> |
| [<span data-ttu-id="0f82d-116">Structures HLSL Direct3D 12 Raytracing</span><span class="sxs-lookup"><span data-stu-id="0f82d-116">Direct3D 12 raytracing HLSL structures</span></span>](direct3d-12-raytracing-hlsl-structures.md) | <span data-ttu-id="0f82d-117">Décrit les structures HLSL qui prennent en charge le pipeline Direct3D 12 Raytracing.</span><span class="sxs-lookup"><span data-stu-id="0f82d-117">Describes the HLSL structures that support the Direct3D 12 raytracing pipeline.</span></span> |

<span data-ttu-id="0f82d-118">En outre, consultez la rubrique [objets d’État](../direct3dhlsl/dx-graphics-hlsl-state-object.md) pour plus d’informations sur la syntaxe utilisée pour la définition des objets d’État Direct3D 12 Raytracing en langage HLSL.</span><span class="sxs-lookup"><span data-stu-id="0f82d-118">Additionally, see the topic [State objects](../direct3dhlsl/dx-graphics-hlsl-state-object.md) for information about the syntax used for defining Direct3D 12 raytracing state objects in HLSL.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f82d-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0f82d-119">Related topics</span></span>

* [<span data-ttu-id="0f82d-120">Informations de référence sur Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="0f82d-120">Direct3D 12 reference</span></span>](direct3d-12-reference.md)