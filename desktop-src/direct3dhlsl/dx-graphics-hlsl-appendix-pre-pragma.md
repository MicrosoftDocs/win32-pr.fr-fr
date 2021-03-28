---
title: " pragma (directive)"
description: Directive de préprocesseur qui fournit des fonctionnalités spécifiques à l’ordinateur ou au système d’exploitation tout en conservant la compatibilité générale avec les langages C et C++.
ms.assetid: 806ddb9b-ae4b-4dd3-a2c4-39c9cb7f3820
keywords:
- Directive de pragma HLSL
topic_type:
- apiref
api_name:
- pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f843a218e39daf616fa6c59ca27f73a5511f17b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030234"
---
# <a name="pragma-directive"></a><span data-ttu-id="3af63-104">\#pragma (directive)</span><span class="sxs-lookup"><span data-stu-id="3af63-104">\#pragma Directive</span></span>

<span data-ttu-id="3af63-105">Directive de préprocesseur qui fournit des fonctionnalités spécifiques à l’ordinateur ou au système d’exploitation tout en conservant la compatibilité générale avec les langages C et C++.</span><span class="sxs-lookup"><span data-stu-id="3af63-105">Preprocessor directive that provides machine-specific or operating system-specific features while retaining overall compatibility with the C and C++ languages.</span></span>



| <span data-ttu-id="3af63-106">\#pragma *Token-String*</span><span class="sxs-lookup"><span data-stu-id="3af63-106">\#pragma *token-string*</span></span> |
|-------------------------|



 

## <a name="parameters"></a><span data-ttu-id="3af63-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3af63-107">Parameters</span></span>



| <span data-ttu-id="3af63-108">Élément</span><span class="sxs-lookup"><span data-stu-id="3af63-108">Item</span></span>                                                                                    | <span data-ttu-id="3af63-109">Description</span><span class="sxs-lookup"><span data-stu-id="3af63-109">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3af63-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*jeton-chaîne*</span><span class="sxs-lookup"><span data-stu-id="3af63-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="3af63-111">Série de caractères qui donne une instruction et des arguments spécifiques du compilateur.</span><span class="sxs-lookup"><span data-stu-id="3af63-111">Series of characters that gives a specific compiler instruction and arguments.</span></span> <span data-ttu-id="3af63-112">Ce paramètre est sujet à l’expansion macro.</span><span class="sxs-lookup"><span data-stu-id="3af63-112">This parameter is subject to macro expansion.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="3af63-113">Notes</span><span class="sxs-lookup"><span data-stu-id="3af63-113">Remarks</span></span>

<span data-ttu-id="3af63-114">Si le compilateur trouve un pragma qu’il ne reconnaît pas, il émet un avertissement, mais la compilation se poursuit.</span><span class="sxs-lookup"><span data-stu-id="3af63-114">If the compiler finds a pragma it does not recognize, it issues a warning, but compilation continues.</span></span>

<span data-ttu-id="3af63-115">Le compilateur HLSL reconnaît les pragmas suivants :</span><span class="sxs-lookup"><span data-stu-id="3af63-115">The HLSL compiler recognizes the following pragmas:</span></span>

-   [<span data-ttu-id="3af63-116">def</span><span class="sxs-lookup"><span data-stu-id="3af63-116">def</span></span>](dx-graphics-hlsl-appendix-pre-pragma-def.md)
-   [<span data-ttu-id="3af63-117">message</span><span class="sxs-lookup"><span data-stu-id="3af63-117">message</span></span>](message-pragma-directive--directx-hlsl-.md)
-   [<span data-ttu-id="3af63-118">matrice de Pack \_</span><span class="sxs-lookup"><span data-stu-id="3af63-118">pack\_matrix</span></span>](dx-graphics-hlsl-appendix-pre-pragma-pack-matrix.md)
-   [<span data-ttu-id="3af63-119">warning</span><span class="sxs-lookup"><span data-stu-id="3af63-119">warning</span></span>](dx-graphics-hlsl-appendix-pre-pragma-warning.md)

## <a name="see-also"></a><span data-ttu-id="3af63-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3af63-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3af63-121">Directives de préprocesseur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3af63-121">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





