---
description: D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance. Il s’agit d’une couche au-dessus du composant Direct3D.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Prise en charge des fonctions mathématiques dans D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac69e0385919b015d1f8d3e7d47e221c06a04fbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109151"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a><span data-ttu-id="3d3b1-104">Prise en charge des fonctions mathématiques dans D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3d3b1-104">Math Function Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="3d3b1-105">D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance.</span><span class="sxs-lookup"><span data-stu-id="3d3b1-105">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="3d3b1-106">Il s’agit d’une couche au-dessus du composant Direct3D.</span><span class="sxs-lookup"><span data-stu-id="3d3b1-106">It is a layer above the Direct3D component.</span></span>

## <a name="math"></a><span data-ttu-id="3d3b1-107">Math</span><span class="sxs-lookup"><span data-stu-id="3d3b1-107">Math</span></span>

<span data-ttu-id="3d3b1-108">La prise en charge des mathématiques, contenue dans un ensemble de fonctions, est fournie pour :</span><span class="sxs-lookup"><span data-stu-id="3d3b1-108">Math support, contained in a set of functions, is provided for:</span></span>

-   <span data-ttu-id="3d3b1-109">Calculs de couleur</span><span class="sxs-lookup"><span data-stu-id="3d3b1-109">Color calculations</span></span>
-   <span data-ttu-id="3d3b1-110">Appareils</span><span class="sxs-lookup"><span data-stu-id="3d3b1-110">Planes</span></span>
-   <span data-ttu-id="3d3b1-111">Manipulation de matrice</span><span class="sxs-lookup"><span data-stu-id="3d3b1-111">Matrix manipulation</span></span>
-   <span data-ttu-id="3d3b1-112">Quaternions</span><span class="sxs-lookup"><span data-stu-id="3d3b1-112">Quaternions</span></span>
-   <span data-ttu-id="3d3b1-113">vecteurs 2D</span><span class="sxs-lookup"><span data-stu-id="3d3b1-113">2D vectors</span></span>
-   <span data-ttu-id="3d3b1-114">vecteurs 3D</span><span class="sxs-lookup"><span data-stu-id="3d3b1-114">3D vectors</span></span>
-   <span data-ttu-id="3d3b1-115">vecteurs 4D</span><span class="sxs-lookup"><span data-stu-id="3d3b1-115">4D vectors</span></span>

<span data-ttu-id="3d3b1-116">Notez qu’en cas d’association avec les surcharges C++, la prise en charge des types mathématiques de base en 3D est complète.</span><span class="sxs-lookup"><span data-stu-id="3d3b1-116">Please note that when coupled with the C++ overloads, the support for basic 3D math types is extensive.</span></span>

<span data-ttu-id="3d3b1-117">Pour plus d’informations sur ces fonctions, consultez [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span><span class="sxs-lookup"><span data-stu-id="3d3b1-117">For more information about these functions, see [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span></span> <span data-ttu-id="3d3b1-118">Pour vous aider à trouver la fonction dont vous avez besoin, elles sont réparties dans plusieurs dossiers.</span><span class="sxs-lookup"><span data-stu-id="3d3b1-118">To help find the function you need, they are broken up in several folders.</span></span>

## <a name="float16"></a><span data-ttu-id="3d3b1-119">FLOAT16</span><span class="sxs-lookup"><span data-stu-id="3d3b1-119">FLOAT16</span></span>

<span data-ttu-id="3d3b1-120">Lorsque vous utilisez le type de données FLOAT16, veillez à limiter les valeurs à un maximum de D3DX \_ 16F \_ Max.</span><span class="sxs-lookup"><span data-stu-id="3d3b1-120">When using the FLOAT16 data type, be sure to limit values to a maximum of D3DX\_16F\_MAX.</span></span> <span data-ttu-id="3d3b1-121">Toute valeur FLOAT16 dépassant cela entraînera un comportement indéfini dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="3d3b1-121">Any FLOAT16 value that exceeds this will result in undefined behavior in the pipeline.</span></span> <span data-ttu-id="3d3b1-122">Consultez [les autres constantes D3DX](other-d3dx-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3d3b1-122">See [Other D3DX Constants](other-d3dx-constants.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3d3b1-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d3b1-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d3b1-124">D3DX</span><span class="sxs-lookup"><span data-stu-id="3d3b1-124">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



