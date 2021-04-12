---
description: .
ms.assetid: 719954bf-0d7d-f647-2d3f-a77d87df204e
title: DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f316939514d9a186fcd5ef36372f31709b69a7a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "104321777"
---
# <a name="directxmath"></a><span data-ttu-id="0ec09-103">DirectXMath</span><span class="sxs-lookup"><span data-stu-id="0ec09-103">DirectXMath</span></span>

## <a name="purpose"></a><span data-ttu-id="0ec09-104">Objectif</span><span class="sxs-lookup"><span data-stu-id="0ec09-104">Purpose</span></span>

<span data-ttu-id="0ec09-105">L’API DirectXMath fournit des fonctions et des types C++ compatibles SIMD pour les opérations mathématiques de graphiques algébriques et mathématiques courantes communes aux applications DirectX.</span><span class="sxs-lookup"><span data-stu-id="0ec09-105">The DirectXMath API provides SIMD-friendly C++ types and functions for common linear algebra and graphics math operations common to DirectX applications.</span></span> <span data-ttu-id="0ec09-106">La bibliothèque fournit des versions optimisées pour Windows 32 bits (x86), Windows 64 bits (x64) et Windows sur ARM/ARM64 via la prise en charge des intrinsèques SSE, AVX et ARM-néon dans le compilateur de Visual C++.</span><span class="sxs-lookup"><span data-stu-id="0ec09-106">The library provides optimized versions for Windows 32-bit (x86), Windows 64-bit (x64), and Windows on ARM/ARM64 through SSE, AVX, and ARM-NEON intrinsics support in the Visual C++ compiler.</span></span>

<span data-ttu-id="0ec09-107">Pour les développeurs qui débutent avec DirectXMath, vous pouvez envisager d’utiliser le wrapper SimpleMath dans le *Kit d’outils DirectX* pour [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929)  /  [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) comme point de départ.</span><span class="sxs-lookup"><span data-stu-id="0ec09-107">For developers new to DirectXMath, you may want to consider using the SimpleMath wrapper in the *DirectX Tool Kit* for [DirectX 11](https://go.microsoft.com/fwlink/?LinkId=248929) / [DirectX12](https://go.microsoft.com/fwlink/?LinkID=615561) as a starting point.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0ec09-108">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="0ec09-108">In this section</span></span>



| <span data-ttu-id="0ec09-109">Rubrique</span><span class="sxs-lookup"><span data-stu-id="0ec09-109">Topic</span></span>                                                                     | <span data-ttu-id="0ec09-110">Description</span><span class="sxs-lookup"><span data-stu-id="0ec09-110">Description</span></span>                                                                      |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="0ec09-111">Guide de programmation DirectXMath</span><span class="sxs-lookup"><span data-stu-id="0ec09-111">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)<br/>     | <span data-ttu-id="0ec09-112">DirectXMath fournit une solution mathématique optimisée pour Windows.</span><span class="sxs-lookup"><span data-stu-id="0ec09-112">DirectXMath provides a math solution optimized for Windows.</span></span><br/>           |
| [<span data-ttu-id="0ec09-113">Informations de référence sur la programmation DirectXMath</span><span class="sxs-lookup"><span data-stu-id="0ec09-113">DirectXMath Programming Reference</span></span>](ovw-xnamath-reference.md)<br/> | <span data-ttu-id="0ec09-114">Cette section contient des documents de référence pour la bibliothèque DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="0ec09-114">This section contains reference material for the DirectXMath Library.</span></span><br/> |



 

## <a name="developer-audience"></a><span data-ttu-id="0ec09-115">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="0ec09-115">Developer audience</span></span>

<span data-ttu-id="0ec09-116">La bibliothèque DirectXMath est conçue pour les développeurs C++ qui travaillent sur les jeux et les graphiques DirectX dans les applications du Windows Store, les jeux Xbox et les applications de bureau traditionnelles pour Windows.</span><span class="sxs-lookup"><span data-stu-id="0ec09-116">The DirectXMath library is designed for C++ developers working on games and DirectX graphics in Windows Store apps, Xbox games, and traditional desktop apps for Windows.</span></span>

## <a name="obtaining-directxmath"></a><span data-ttu-id="0ec09-117">Obtention de DirectXMath</span><span class="sxs-lookup"><span data-stu-id="0ec09-117">Obtaining DirectXMath</span></span>
 
<span data-ttu-id="0ec09-118">Les en-têtes DirectXMath sont fournis dans le SDK Windows fourni avec Visual Studio 2012 ou version ultérieure, et en tant qu’en-tête en ligne, il n’y a aucune DLL ou bibliothèque statique à lier.</span><span class="sxs-lookup"><span data-stu-id="0ec09-118">The DirectXMath headers ship in the Windows SDK that comes with Visual Studio 2012 or later, and as an all inline header there is no DLL or static library to link against.</span></span> <span data-ttu-id="0ec09-119">Il est également disponible sous la forme d’un package sur [NuGet](https://www.nuget.org/packages/directxmath/).</span><span class="sxs-lookup"><span data-stu-id="0ec09-119">It is also available as a package on [NuGet](https://www.nuget.org/packages/directxmath/).</span></span>

<span data-ttu-id="0ec09-120">DirectXMath est open source sous la [licence MIT](https://opensource.org/licenses/MIT) hébergée sur [GitHub](https://github.com/Microsoft/DirectXMath).</span><span class="sxs-lookup"><span data-stu-id="0ec09-120">DirectXMath is open source under the [MIT license](https://opensource.org/licenses/MIT) hosted on [GitHub](https://github.com/Microsoft/DirectXMath).</span></span>




