---
description: Ces indicateurs fournissent des informations supplémentaires sur les paramètres d’effet.
ms.assetid: 7e1e4c64-56b8-4fdb-8178-50f7d61b917b
title: D3DX_PARAMETER (D3dx9effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX_PARAMETER_ANNOTATION
- D3DX_PARAMETER_LITERAL
- D3DX_PARAMETER_SHARED
api_type:
- HeaderDef
api_location:
- d3dx9effect.h
ms.openlocfilehash: 49df84c49fd1f7a0c1b4de9157a36e27d29d5e29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527114"
---
# <a name="d3dx_parameter"></a><span data-ttu-id="95983-103">\_Paramètre D3DX</span><span class="sxs-lookup"><span data-stu-id="95983-103">D3DX\_PARAMETER</span></span>

<span data-ttu-id="95983-104">Ces indicateurs fournissent des informations supplémentaires sur les paramètres d’effet.</span><span class="sxs-lookup"><span data-stu-id="95983-104">These flags provide additional information about effect parameters.</span></span>

<span data-ttu-id="95983-105">Les constantes de paramètre d’effet sont utilisées par [**D3DXPARAMETER \_ desc**](d3dxparameter-desc.md).</span><span class="sxs-lookup"><span data-stu-id="95983-105">Effect parameter constants are used by [**D3DXPARAMETER\_DESC**](d3dxparameter-desc.md).</span></span>



| <span data-ttu-id="95983-106">Constante</span><span class="sxs-lookup"><span data-stu-id="95983-106">Constant</span></span>                                                                                                                                                                                           | <span data-ttu-id="95983-107">Description</span><span class="sxs-lookup"><span data-stu-id="95983-107">Description</span></span>                                                                                                                                                                                                                                                                                                                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DX_PARAMETER_ANNOTATION"></span><span id="d3dx_parameter_annotation"></span><dl> <span data-ttu-id="95983-108"><dt>**\_Annotation de paramètre D3DX \_**</dt></span><span class="sxs-lookup"><span data-stu-id="95983-108"><dt>**D3DX\_PARAMETER\_ANNOTATION**</dt></span></span> </dl> | <span data-ttu-id="95983-109">Ce paramètre est marqué comme une annotation.</span><span class="sxs-lookup"><span data-stu-id="95983-109">This parameter is marked as an annotation.</span></span> <span data-ttu-id="95983-110">Consultez [Ajouter des informations pour appliquer des paramètres avec des annotations](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="95983-110">See [Add Information to Effect Parameters with Annotations](using-an-effect.md).</span></span><br/>                                                                                                                                                                                                 |
| <span id="D3DX_PARAMETER_LITERAL"></span><span id="d3dx_parameter_literal"></span><dl> <span data-ttu-id="95983-111"><dt>**D3DX \_ , \_ littéral de paramètre**</dt></span><span class="sxs-lookup"><span data-stu-id="95983-111"><dt>**D3DX\_PARAMETER\_LITERAL**</dt></span></span> </dl>          | <span data-ttu-id="95983-112">Ce paramètre est marqué en tant que valeur littérale.</span><span class="sxs-lookup"><span data-stu-id="95983-112">This parameter is marked as a literal value.</span></span> <span data-ttu-id="95983-113">Les paramètres Literal ne peuvent pas être modifiés après la compilation, ce qui permet au compilateur d’optimiser leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="95983-113">Literal parameters cannot change after compile, allowing the compiler to optimize their usage.</span></span> <span data-ttu-id="95983-114">Les paramètres partagés ne peuvent pas être marqués comme un littéral.</span><span class="sxs-lookup"><span data-stu-id="95983-114">Shared parameters cannot be marked as a literal.</span></span> <span data-ttu-id="95983-115">Consultez [utilisations et littéraux (Direct3D 9)](usages-and-literals.md).</span><span class="sxs-lookup"><span data-stu-id="95983-115">See [Usages and Literals (Direct3D 9)](usages-and-literals.md).</span></span> <br/>                                                               |
| <span id="D3DX_PARAMETER_SHARED"></span><span id="d3dx_parameter_shared"></span><dl> <span data-ttu-id="95983-116"><dt>**\_Paramètre D3DX \_ partagé**</dt></span><span class="sxs-lookup"><span data-stu-id="95983-116"><dt>**D3DX\_PARAMETER\_SHARED**</dt></span></span> </dl>             | <span data-ttu-id="95983-117">La valeur d’un paramètre est partagée par tous les effets dans le même espace de noms.</span><span class="sxs-lookup"><span data-stu-id="95983-117">The value of a parameter will be shared by all effects in the same namespace.</span></span> <span data-ttu-id="95983-118">La modification de la valeur dans un effet entraîne sa modification dans tous les effets partagés.</span><span class="sxs-lookup"><span data-stu-id="95983-118">Changing the value in one effect will change it in all shared effects.</span></span> <span data-ttu-id="95983-119">Consultez [partage de paramètres](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="95983-119">See [Sharing Parameters](cloning-and-sharing.md).</span></span> <span data-ttu-id="95983-120">**D3DX \_ Le paramètre \_ Shared** ne peut pas être combiné avec un **\_ \_ littéral de paramètre D3DX** ou une **\_ \_ annotation de paramètre D3DX**.</span><span class="sxs-lookup"><span data-stu-id="95983-120">**D3DX\_PARAMETER\_SHARED** cannot be combined with **D3DX\_PARAMETER\_LITERAL** or **D3DX\_PARAMETER\_ANNOTATION**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="95983-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="95983-121">Requirements</span></span>



| <span data-ttu-id="95983-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="95983-122">Requirement</span></span> | <span data-ttu-id="95983-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="95983-123">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="95983-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="95983-124">Header</span></span><br/> | <dl> <span data-ttu-id="95983-125"><dt>D3dx9effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="95983-125"><dt>D3dx9effect.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95983-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="95983-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95983-127">Constantes d’effet</span><span class="sxs-lookup"><span data-stu-id="95983-127">Effect Constants</span></span>](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 




