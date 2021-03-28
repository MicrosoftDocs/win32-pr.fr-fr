---
title: " Error (directive)"
description: Directive de préprocesseur qui génère des messages d’erreur au moment du compilateur.
ms.assetid: e32bcd6f-f2c1-43f7-a0bb-2c384b056492
keywords:
- Directive d’erreur (HLSL)
topic_type:
- apiref
api_name:
- error Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 362150e494398abbc708416e6bfca6aa83756c52
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104380786"
---
# <a name="error-directive"></a><span data-ttu-id="7d040-104">\#Error (directive)</span><span class="sxs-lookup"><span data-stu-id="7d040-104">\#error Directive</span></span>

<span data-ttu-id="7d040-105">Directive de préprocesseur qui génère des messages d’erreur au moment du compilateur.</span><span class="sxs-lookup"><span data-stu-id="7d040-105">Preprocessor directive that produces compiler-time error messages.</span></span>



| <span data-ttu-id="7d040-106">\#jeton d’erreur *-chaîne*</span><span class="sxs-lookup"><span data-stu-id="7d040-106">\#error *token-string*</span></span> |
|------------------------|



 

## <a name="parameters"></a><span data-ttu-id="7d040-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7d040-107">Parameters</span></span>



| <span data-ttu-id="7d040-108">Élément</span><span class="sxs-lookup"><span data-stu-id="7d040-108">Item</span></span>                                                                                    | <span data-ttu-id="7d040-109">Description</span><span class="sxs-lookup"><span data-stu-id="7d040-109">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d040-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*jeton-chaîne*</span><span class="sxs-lookup"><span data-stu-id="7d040-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="7d040-111">Message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7d040-111">Error message.</span></span> <span data-ttu-id="7d040-112">Ce paramètre se compose d’une série de jetons, tels que les mots clés, les constantes ou les instructions complètes.</span><span class="sxs-lookup"><span data-stu-id="7d040-112">This parameter consists of a series of tokens, such as keywords, constants, or complete statements.</span></span> <span data-ttu-id="7d040-113">La chaîne de jeton est sujette à l’expansion macro.</span><span class="sxs-lookup"><span data-stu-id="7d040-113">The token string is subject to macro expansion.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="7d040-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7d040-114">Remarks</span></span>

<span data-ttu-id="7d040-115">\#les directives d’erreur sont particulièrement utiles pour détecter les incohérences du programmeur et la violation des contraintes lors du prétraitement.</span><span class="sxs-lookup"><span data-stu-id="7d040-115">\#error directives are most useful for detecting programmer inconsistencies and violation of constraints during preprocessing.</span></span> <span data-ttu-id="7d040-116">Lorsqu’une \# directive d’erreur est rencontrée, la compilation se termine.</span><span class="sxs-lookup"><span data-stu-id="7d040-116">When an \#error directive is encountered, compilation terminates.</span></span>

## <a name="examples"></a><span data-ttu-id="7d040-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="7d040-117">Examples</span></span>

<span data-ttu-id="7d040-118">L’exemple suivant illustre le traitement des erreurs pendant le prétraitement.</span><span class="sxs-lookup"><span data-stu-id="7d040-118">The following example demonstrates error processing during preprocessing.</span></span>


```
#if !defined(__cplusplus)
  #error C++ compiler required.
#endif
```



## <a name="see-also"></a><span data-ttu-id="7d040-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d040-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d040-120">Directives de préprocesseur (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="7d040-120">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> </dl>

 

 





