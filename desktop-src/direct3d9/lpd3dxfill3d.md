---
description: 'LPD3DXFILL3D : type de fonction utilisé par les fonctions de remplissage de texture.'
ms.assetid: ab2f3005-150f-46e1-b75b-75c39e7feed1
title: LPD3DXFILL3D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6c711459cffa3430b31ba7c91d77cc9519e6a43
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114307"
---
# <a name="lpd3dxfill3d"></a><span data-ttu-id="5a508-103">LPD3DXFILL3D</span><span class="sxs-lookup"><span data-stu-id="5a508-103">LPD3DXFILL3D</span></span>

<span data-ttu-id="5a508-104">Type de fonction utilisé par les fonctions de remplissage de texture.</span><span class="sxs-lookup"><span data-stu-id="5a508-104">Function type used by the texture fill functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a508-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a508-105">Syntax</span></span>


```
typedef VOID (WINAPI *LPD3DXFILL2D)(
    D3DXVECTOR4* pOut, 
    CONST D3DXVECTOR3* pTexCoord, 
    CONST D3DXVECTOR3* pTexelSize, 
    LPVOID pData,  
);
```



## <a name="parameters"></a><span data-ttu-id="5a508-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a508-106">Parameters</span></span>

<span data-ttu-id="5a508-107">Moue-pointeur vers un vecteur, que la fonction utilise pour retourner son résultat.</span><span class="sxs-lookup"><span data-stu-id="5a508-107">pOut - Pointer to a vector, which the function uses to return its result.</span></span> <span data-ttu-id="5a508-108">X, Y, Z et W sont mappés respectivement à R, G, B et A.</span><span class="sxs-lookup"><span data-stu-id="5a508-108">X, Y, Z, and W will be mapped to R, G, B, and A, respectively.</span></span>

<span data-ttu-id="5a508-109">pTexCoord-pointeur vers un vecteur contenant les coordonnées du Texel en cours d’évaluation.</span><span class="sxs-lookup"><span data-stu-id="5a508-109">pTexCoord - Pointer to a vector containing the coordinates of the texel currently being evaluated.</span></span> <span data-ttu-id="5a508-110">Les composants de coordonnée de texture des textures et volumes sont compris entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="5a508-110">Texture coordinate components for texture and volume textures range from 0 to 1.</span></span> <span data-ttu-id="5a508-111">Les composants de coordonnée de texture pour les textures de cube sont compris entre-1 et 1.</span><span class="sxs-lookup"><span data-stu-id="5a508-111">Texture coordinate components for cube textures range from -1 to 1.</span></span>

<span data-ttu-id="5a508-112">pTexelSize-pointeur vers un vecteur contenant les dimensions du Texel actuel.</span><span class="sxs-lookup"><span data-stu-id="5a508-112">pTexelSize - Pointer to a vector containing the dimensions of the current texel.</span></span>

<span data-ttu-id="5a508-113">pData-pointeur vers les données utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5a508-113">pData - Pointer to user data.</span></span>

## <a name="return-value"></a><span data-ttu-id="5a508-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5a508-114">Return Value</span></span>

<span data-ttu-id="5a508-115">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="5a508-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a508-116">Notes </span><span class="sxs-lookup"><span data-stu-id="5a508-116">Remarks</span></span>

<span data-ttu-id="5a508-117">Veillez à spécifier la Convention d’appel des [**types de données Windows**](../winprog/windows-data-types.md) lors de la déclaration de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="5a508-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="5a508-118">Sinon, les dépassements de capacité de la pile peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="5a508-118">Otherwise, stack overflows can occur.</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="5a508-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a508-119">Header</span></span>                   | <span data-ttu-id="5a508-120">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="5a508-120">d3dx9tex.h</span></span> |
| <span data-ttu-id="5a508-121">Bibliothèque d'importation</span><span class="sxs-lookup"><span data-stu-id="5a508-121">Import Library</span></span>           | <span data-ttu-id="5a508-122">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="5a508-122">d3dx9.lib</span></span>  |
| <span data-ttu-id="5a508-123">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="5a508-123">Minimum Operating System</span></span> | <span data-ttu-id="5a508-124">Windows 98</span><span class="sxs-lookup"><span data-stu-id="5a508-124">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5a508-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a508-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a508-126">Fonctions de rappel</span><span class="sxs-lookup"><span data-stu-id="5a508-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> <dt>

[<span data-ttu-id="5a508-127">LPD3DXFILL2D</span><span class="sxs-lookup"><span data-stu-id="5a508-127">LPD3DXFILL2D</span></span>](lpd3dxfill2d.md)
</dt> </dl>

 

 
