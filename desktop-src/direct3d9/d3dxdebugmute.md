---
description: Active ou désactive toute la sortie de débogage D3DX.
ms.assetid: e35cbfd2-401e-47ec-9f5b-e2ed63ea1fcd
title: D3DXDebugMute, fonction (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDebugMute
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9259fa43a6a64829e42cbaa661aa7223a958f22d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211767"
---
# <a name="d3dxdebugmute-function"></a><span data-ttu-id="2d382-103">D3DXDebugMute fonction)</span><span class="sxs-lookup"><span data-stu-id="2d382-103">D3DXDebugMute function</span></span>

<span data-ttu-id="2d382-104">Active ou désactive toute la sortie de débogage D3DX.</span><span class="sxs-lookup"><span data-stu-id="2d382-104">Turns on or off all D3DX debug output.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d382-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2d382-105">Syntax</span></span>


```C++
BOOL D3DXDebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a><span data-ttu-id="2d382-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2d382-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d382-107">*Muet* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2d382-107">*Mute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d382-108">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d382-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d382-109">Si la **valeur est true**, la sortie du débogueur est interrompue ; Si la **valeur est false**, la sortie de débogage est activée.</span><span class="sxs-lookup"><span data-stu-id="2d382-109">If **TRUE**, debugger output is halted; if **FALSE**, debug output is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d382-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2d382-110">Return value</span></span>

<span data-ttu-id="2d382-111">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2d382-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2d382-112">Retourne la valeur précédente de muet.</span><span class="sxs-lookup"><span data-stu-id="2d382-112">Returns the previous value of Mute.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d382-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2d382-113">Requirements</span></span>



| <span data-ttu-id="2d382-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2d382-114">Requirement</span></span> | <span data-ttu-id="2d382-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2d382-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d382-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="2d382-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2d382-117"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d382-117"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="2d382-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2d382-118">Library</span></span><br/> | <dl> <span data-ttu-id="2d382-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d382-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2d382-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2d382-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d382-121">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="2d382-121">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
