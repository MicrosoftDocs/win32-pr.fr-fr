---
description: Prototype de fonction utilisé par D3DXComputeIMTFromSignal pour décrire un signal défini par l’utilisateur dans l’espace u, v d’un maillage d’entrée. La fonction évalue un signal procédural de la dimension uSignalDimension à la coordonnée u, v fournie.
ms.assetid: 97b07dbc-6b84-46d2-acc7-db81d94538f7
title: LPD3DXIMTSIGNALCALLBACK
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dbf75bf1a3fc05b217feef8446636efaae55b3b
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342834"
---
# <a name="lpd3dximtsignalcallback"></a><span data-ttu-id="5b4b6-104">LPD3DXIMTSIGNALCALLBACK</span><span class="sxs-lookup"><span data-stu-id="5b4b6-104">LPD3DXIMTSIGNALCALLBACK</span></span>

<span data-ttu-id="5b4b6-105">Prototype de fonction utilisé par [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) pour décrire un signal défini par l’utilisateur dans l’espace u, v d’un maillage d’entrée.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-105">Function prototype used by [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md) to describe a user-defined signal in an input mesh's u,v space.</span></span> <span data-ttu-id="5b4b6-106">La fonction évalue un signal procédural de la dimension uSignalDimension à la coordonnée u, v fournie.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-106">The function evaluates a procedural signal of dimension uSignalDimension at the provided u,v coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b4b6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b4b6-107">Syntax</span></span>


```
typedef HRESULT (WINAPI* LPD3DXIMTSIGNALCALLBACK)
     (CONST D3DXVECTOR2 *uv,
      UINT uPrimitiveID,
      UINT uSignalDimension,
      VOID *pUserData,
      FLOAT *pfSignalOut);
```



## <a name="parameters"></a><span data-ttu-id="5b4b6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b4b6-108">Parameters</span></span>

<span data-ttu-id="5b4b6-109">\[dans \] UV-A, pointeur vers un vecteur qui contient la coordonnée de texture de vertex.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-109">\[in\] uv - A pointer to a vector that contains the vertex texture coordinate.</span></span>

<span data-ttu-id="5b4b6-110">\[dans \] uPrimitiveId, index du triangle d’entrée sur la maille pour laquelle le signal doit être calculé.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-110">\[in\] uPrimitiveId - The index of the input triangle on the mesh for which the signal should be calculated.</span></span>

<span data-ttu-id="5b4b6-111">\[en \] uSignalDimension-nombre de valeurs float à stocker dans le tableau de données de signal (pfSignalOut).</span><span class="sxs-lookup"><span data-stu-id="5b4b6-111">\[in\] uSignalDimension - The number of floats to store in the array of signal data (pfSignalOut).</span></span>

<span data-ttu-id="5b4b6-112">\[dans \] pUserData, le pointeur pUserData est passé à [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span><span class="sxs-lookup"><span data-stu-id="5b4b6-112">\[in\] pUserData - The pUserData pointer passed in to [**D3DXComputeIMTFromSignal**](d3dxcomputeimtfromsignal.md).</span></span>

<span data-ttu-id="5b4b6-113">\[out \] pfSignalOut : tableau de valeurs float qui contient les données de signal.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-113">\[out\] pfSignalOut - An array of floats, that contains the signal data.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b4b6-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5b4b6-114">Return Value</span></span>

<span data-ttu-id="5b4b6-115">Cette fonction doit être implémentée pour retourner S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-115">This function must be implemented to return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b4b6-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="5b4b6-116">Remarks</span></span>

<span data-ttu-id="5b4b6-117">Veillez à spécifier la Convention d’appel des [**types de données Windows**](../winprog/windows-data-types.md) lors de la déclaration de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-117">Be sure to specify the [**Windows Data Types**](../winprog/windows-data-types.md) calling convention when declaring the callback function.</span></span> <span data-ttu-id="5b4b6-118">Sinon, les dépassements de capacité de la pile peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="5b4b6-118">Otherwise, stack overflows can occur.</span></span>



| <span data-ttu-id="5b4b6-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b4b6-119">Requirement</span></span>               | <span data-ttu-id="5b4b6-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b4b6-120">Value</span></span>            |
|----------------|-------------|
| <span data-ttu-id="5b4b6-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b4b6-121">Header</span></span>         | <span data-ttu-id="5b4b6-122">d3dx9mesh. h</span><span class="sxs-lookup"><span data-stu-id="5b4b6-122">d3dx9mesh.h</span></span> |
| <span data-ttu-id="5b4b6-123">Bibliothèque d'importation</span><span class="sxs-lookup"><span data-stu-id="5b4b6-123">Import Library</span></span> | <span data-ttu-id="5b4b6-124">d3dx9. lib</span><span class="sxs-lookup"><span data-stu-id="5b4b6-124">d3dx9.lib</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="5b4b6-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5b4b6-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b4b6-126">Fonctions de rappel</span><span class="sxs-lookup"><span data-stu-id="5b4b6-126">Callback Functions</span></span>](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
