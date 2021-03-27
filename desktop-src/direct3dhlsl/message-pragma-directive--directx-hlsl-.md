---
title: message (directive de pragma)
description: Directive pragma qui produit des messages au moment du compilateur.
ms.assetid: dc3ece10-9730-4ab1-acc8-f95abc92de7d
keywords:
- Directive de pragma de message (HLSL)
topic_type:
- apiref
api_name:
- message pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f342f4a139320e4beb821f32662da72785ab751c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678817"
---
# <a name="message-pragma-directive"></a><span data-ttu-id="4fc04-104">message (directive de pragma)</span><span class="sxs-lookup"><span data-stu-id="4fc04-104">message pragma Directive</span></span>

<span data-ttu-id="4fc04-105">Directive pragma qui produit des messages au moment du compilateur.</span><span class="sxs-lookup"><span data-stu-id="4fc04-105">Pragma directive that produces compiler-time messages.</span></span>



| <span data-ttu-id="4fc04-106">\#message du pragma «*Token-String*»</span><span class="sxs-lookup"><span data-stu-id="4fc04-106">\#pragma message "*token-string*"</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="4fc04-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4fc04-107">Parameters</span></span>



| <span data-ttu-id="4fc04-108">Élément</span><span class="sxs-lookup"><span data-stu-id="4fc04-108">Item</span></span>                                                                                    | <span data-ttu-id="4fc04-109">Description</span><span class="sxs-lookup"><span data-stu-id="4fc04-109">Description</span></span>                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="4fc04-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*jeton-chaîne*</span><span class="sxs-lookup"><span data-stu-id="4fc04-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="4fc04-111">Message du compilateur.</span><span class="sxs-lookup"><span data-stu-id="4fc04-111">Compiler message.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="4fc04-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="4fc04-112">Examples</span></span>

<span data-ttu-id="4fc04-113">L’exemple suivant illustre le traitement des messages pendant le prétraitement.</span><span class="sxs-lookup"><span data-stu-id="4fc04-113">The following example demonstrates message processing during preprocessing.</span></span>


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a><span data-ttu-id="4fc04-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4fc04-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc04-115">Directives de préprocesseur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4fc04-115">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="4fc04-116">\#Directive pragma (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4fc04-116">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





