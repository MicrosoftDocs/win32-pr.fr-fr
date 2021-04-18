---
description: Récupérez les caractéristiques de police.
ms.assetid: ef7e0d18-492b-476b-945a-bfc0232a939a
title: 'ID3DX10Font :: GetTextMetrics, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetTextMetrics
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72decdcf0a9573f7ad8ba0f4e363df6df3599477
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530939"
---
# <a name="id3dx10fontgettextmetrics-method"></a><span data-ttu-id="f3983-103">ID3DX10Font :: GetTextMetrics, méthode</span><span class="sxs-lookup"><span data-stu-id="f3983-103">ID3DX10Font::GetTextMetrics method</span></span>

<span data-ttu-id="f3983-104">Récupérez les caractéristiques de police.</span><span class="sxs-lookup"><span data-stu-id="f3983-104">Retrieve font characteristics.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3983-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3983-105">Syntax</span></span>


```C++
BOOL GetTextMetrics(
  [in] TEXTMETRIC *pTextMetrics
);
```



## <a name="parameters"></a><span data-ttu-id="f3983-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f3983-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3983-107">*pTextMetrics* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f3983-107">*pTextMetrics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3983-108">Type : **TEXTMETRIC \***</span><span class="sxs-lookup"><span data-stu-id="f3983-108">Type: **TEXTMETRIC\***</span></span>

<span data-ttu-id="f3983-109">Pointeur vers une structure [TEXTMETRIC](/previous-versions//ms534202(v=vs.85)) , qui contient les propriétés de police.</span><span class="sxs-lookup"><span data-stu-id="f3983-109">Pointer to a [TEXTMETRIC](/previous-versions//ms534202(v=vs.85)) structure, which contains font properties.</span></span> <span data-ttu-id="f3983-110">Si Unicode est défini, la fonction retourne une structure TEXTMETRICW.</span><span class="sxs-lookup"><span data-stu-id="f3983-110">If Unicode is defined, the function returns a TEXTMETRICW structure.</span></span> <span data-ttu-id="f3983-111">Dans le cas contraire, la fonction retourne une structure TEXTMETRICA.</span><span class="sxs-lookup"><span data-stu-id="f3983-111">Otherwise, the function returns a TEXTMETRICA structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3983-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f3983-112">Return value</span></span>

<span data-ttu-id="f3983-113">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f3983-113">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f3983-114">Une valeur différente de zéro si la fonction réussit ; sinon, 0.</span><span class="sxs-lookup"><span data-stu-id="f3983-114">Nonzero if the function is successful; otherwise 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3983-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3983-115">Requirements</span></span>



| <span data-ttu-id="f3983-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3983-116">Requirement</span></span> | <span data-ttu-id="f3983-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3983-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f3983-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="f3983-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f3983-119"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3983-119"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f3983-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f3983-120">Library</span></span><br/> | <dl> <span data-ttu-id="f3983-121"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3983-121"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3983-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3983-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3983-123">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="f3983-123">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="f3983-124">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="f3983-124">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
