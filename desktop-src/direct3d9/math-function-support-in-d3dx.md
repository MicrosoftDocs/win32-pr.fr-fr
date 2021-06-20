---
description: En savoir plus sur la prise en charge des fonctions mathématiques dans D3DX. D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance. Il s’agit d’une couche au-dessus du composant Direct3D.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Prise en charge des fonctions mathématiques dans D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28c32b13d185694e4ffa41c314cf9f77cbb18b7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407522"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a><span data-ttu-id="cf250-105">Prise en charge des fonctions mathématiques dans D3DX (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cf250-105">Math Function Support in D3DX (Direct3D 9)</span></span>

<span data-ttu-id="cf250-106">D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance.</span><span class="sxs-lookup"><span data-stu-id="cf250-106">D3DX is a utility library that provides helper services.</span></span> <span data-ttu-id="cf250-107">Il s’agit d’une couche au-dessus du composant Direct3D.</span><span class="sxs-lookup"><span data-stu-id="cf250-107">It is a layer above the Direct3D component.</span></span>

## <a name="math"></a><span data-ttu-id="cf250-108">Math</span><span class="sxs-lookup"><span data-stu-id="cf250-108">Math</span></span>

<span data-ttu-id="cf250-109">La prise en charge des mathématiques, contenue dans un ensemble de fonctions, est fournie pour :</span><span class="sxs-lookup"><span data-stu-id="cf250-109">Math support, contained in a set of functions, is provided for:</span></span>

-   <span data-ttu-id="cf250-110">Calculs de couleur</span><span class="sxs-lookup"><span data-stu-id="cf250-110">Color calculations</span></span>
-   <span data-ttu-id="cf250-111">Appareils</span><span class="sxs-lookup"><span data-stu-id="cf250-111">Planes</span></span>
-   <span data-ttu-id="cf250-112">Manipulation de matrice</span><span class="sxs-lookup"><span data-stu-id="cf250-112">Matrix manipulation</span></span>
-   <span data-ttu-id="cf250-113">Quaternions</span><span class="sxs-lookup"><span data-stu-id="cf250-113">Quaternions</span></span>
-   <span data-ttu-id="cf250-114">vecteurs 2D</span><span class="sxs-lookup"><span data-stu-id="cf250-114">2D vectors</span></span>
-   <span data-ttu-id="cf250-115">vecteurs 3D</span><span class="sxs-lookup"><span data-stu-id="cf250-115">3D vectors</span></span>
-   <span data-ttu-id="cf250-116">vecteurs 4D</span><span class="sxs-lookup"><span data-stu-id="cf250-116">4D vectors</span></span>

<span data-ttu-id="cf250-117">Notez qu’en cas d’association avec les surcharges C++, la prise en charge des types mathématiques de base en 3D est complète.</span><span class="sxs-lookup"><span data-stu-id="cf250-117">Please note that when coupled with the C++ overloads, the support for basic 3D math types is extensive.</span></span>

<span data-ttu-id="cf250-118">Pour plus d’informations sur ces fonctions, consultez [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span><span class="sxs-lookup"><span data-stu-id="cf250-118">For more information about these functions, see [D3DX Functions](dx9-graphics-reference-d3dx-functions.md).</span></span> <span data-ttu-id="cf250-119">Pour vous aider à trouver la fonction dont vous avez besoin, elles sont réparties dans plusieurs dossiers.</span><span class="sxs-lookup"><span data-stu-id="cf250-119">To help find the function you need, they are broken up in several folders.</span></span>

## <a name="float16"></a><span data-ttu-id="cf250-120">FLOAT16</span><span class="sxs-lookup"><span data-stu-id="cf250-120">FLOAT16</span></span>

<span data-ttu-id="cf250-121">Lorsque vous utilisez le type de données FLOAT16, veillez à limiter les valeurs à un maximum de D3DX \_ 16F \_ Max.</span><span class="sxs-lookup"><span data-stu-id="cf250-121">When using the FLOAT16 data type, be sure to limit values to a maximum of D3DX\_16F\_MAX.</span></span> <span data-ttu-id="cf250-122">Toute valeur FLOAT16 dépassant cela entraînera un comportement indéfini dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="cf250-122">Any FLOAT16 value that exceeds this will result in undefined behavior in the pipeline.</span></span> <span data-ttu-id="cf250-123">Consultez [les autres constantes D3DX](other-d3dx-constants.md).</span><span class="sxs-lookup"><span data-stu-id="cf250-123">See [Other D3DX Constants](other-d3dx-constants.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf250-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cf250-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf250-125">D3DX</span><span class="sxs-lookup"><span data-stu-id="cf250-125">D3DX</span></span>](d3dx.md)
</dt> </dl>

 

 



