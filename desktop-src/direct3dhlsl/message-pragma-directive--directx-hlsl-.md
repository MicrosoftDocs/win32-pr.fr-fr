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
ms.openlocfilehash: 813483efb161a06db5ef7e40da99c391f53565bc
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153482"
---
# <a name="message-pragma-directive"></a><span data-ttu-id="9badc-104">message (directive de pragma)</span><span class="sxs-lookup"><span data-stu-id="9badc-104">message pragma Directive</span></span>

<span data-ttu-id="9badc-105">Directive pragma qui produit des messages au moment du compilateur.</span><span class="sxs-lookup"><span data-stu-id="9badc-105">Pragma directive that produces compiler-time messages.</span></span>



| <span data-ttu-id="9badc-106">\#message du pragma («*Token-String*»)</span><span class="sxs-lookup"><span data-stu-id="9badc-106">\#pragma message("*token-string*")</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="9badc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9badc-107">Parameters</span></span>



| <span data-ttu-id="9badc-108">Élément</span><span class="sxs-lookup"><span data-stu-id="9badc-108">Item</span></span>                                                                                    | <span data-ttu-id="9badc-109">Description</span><span class="sxs-lookup"><span data-stu-id="9badc-109">Description</span></span>                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="9badc-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*jeton-chaîne*</span><span class="sxs-lookup"><span data-stu-id="9badc-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="9badc-111">Message du compilateur.</span><span class="sxs-lookup"><span data-stu-id="9badc-111">Compiler message.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="9badc-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="9badc-112">Examples</span></span>

<span data-ttu-id="9badc-113">L’exemple suivant illustre le traitement des messages pendant le prétraitement.</span><span class="sxs-lookup"><span data-stu-id="9badc-113">The following example demonstrates message processing during preprocessing.</span></span>


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a><span data-ttu-id="9badc-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9badc-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9badc-115">Directives de préprocesseur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9badc-115">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="9badc-116">\#Directive pragma (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9badc-116">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





