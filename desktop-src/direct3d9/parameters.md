---
description: Les paramètres sont des variables d’effet.
ms.assetid: vs|directx_sdk|~\parameters.htm
title: Paramètres (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5c78a4f6c0518c99b61be10b721d98b17630ab
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109890"
---
# <a name="parameters-direct3d-9"></a><span data-ttu-id="10708-103">Paramètres (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="10708-103">Parameters (Direct3D 9)</span></span>

<span data-ttu-id="10708-104">Les paramètres sont des variables d’effet.</span><span class="sxs-lookup"><span data-stu-id="10708-104">Parameters are effect variables.</span></span>

## <a name="syntax"></a><span data-ttu-id="10708-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10708-105">Syntax</span></span>

<span data-ttu-id="10708-106">*ID du type d’utilisation* \[ : expression *sémantique* \] \[ < *(s) d’annotation* > \] \[ =   \] ;</span><span class="sxs-lookup"><span data-stu-id="10708-106">*usage type ID* \[: *semantic*\] \[<*annotation(s)*>\] \[= *expression*\];</span></span>

<span data-ttu-id="10708-107">Les paramètres peuvent être lus et écrits par l’application avec [**ID3DXEffect**](id3dxeffect.md) ou [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span><span class="sxs-lookup"><span data-stu-id="10708-107">Parameters can be read from and written to by the application with [**ID3DXEffect**](id3dxeffect.md) or [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).</span></span>

<span data-ttu-id="10708-108">Les paramètres peuvent être référencés dans des fonctions et dans des techniques (plus précisément, dans la partie droite des affectations d’État).</span><span class="sxs-lookup"><span data-stu-id="10708-108">Parameters can be referenced in functions and in techniques (specifically, in the right side of state assignments).</span></span>



| <span data-ttu-id="10708-109">Élément</span><span class="sxs-lookup"><span data-stu-id="10708-109">Item</span></span>                                                                                 | <span data-ttu-id="10708-110">Description</span><span class="sxs-lookup"><span data-stu-id="10708-110">Description</span></span>                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10708-111"><span id="usage"></span><span id="USAGE"></span>*syntaxe*</span><span class="sxs-lookup"><span data-stu-id="10708-111"><span id="usage"></span><span id="USAGE"></span>*usage*</span></span><br/>                   | <span data-ttu-id="10708-112">Étendue du paramètre.</span><span class="sxs-lookup"><span data-stu-id="10708-112">Scope of the parameter.</span></span> <span data-ttu-id="10708-113">Consultez [utilisations et littéraux (Direct3D 9)](usages-and-literals.md).</span><span class="sxs-lookup"><span data-stu-id="10708-113">See [Usages and Literals (Direct3D 9)](usages-and-literals.md).</span></span><br/>                                                             |
| <span data-ttu-id="10708-114"><span id="type"></span><span id="TYPE"></span>*entrer*</span><span class="sxs-lookup"><span data-stu-id="10708-114"><span id="type"></span><span id="TYPE"></span>*type*</span></span><br/>                      | <span data-ttu-id="10708-115">Toute [référence valide pour](../direct3dhlsl/dx-graphics-hlsl-reference.md) le type HLSL.</span><span class="sxs-lookup"><span data-stu-id="10708-115">Any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) type.</span></span><br/>                                                                        |
| <span data-ttu-id="10708-116"><span id="ID"></span><span id="id"></span>*IDENTIFI*</span><span class="sxs-lookup"><span data-stu-id="10708-116"><span id="ID"></span><span id="id"></span>*ID*</span></span><br/>                            | <span data-ttu-id="10708-117">Nom unique.</span><span class="sxs-lookup"><span data-stu-id="10708-117">A unique name.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="10708-118"><span id="semantic"></span><span id="SEMANTIC"></span>*équivalent*</span><span class="sxs-lookup"><span data-stu-id="10708-118"><span id="semantic"></span><span id="SEMANTIC"></span>*semantic*</span></span><br/>          | <span data-ttu-id="10708-119">Étiquette qui suit les règles d’identificateur qui indiquent généralement l’utilisation du paramètre.</span><span class="sxs-lookup"><span data-stu-id="10708-119">A tag following identifier rules that typically indicates the usage of the parameter.</span></span> <span data-ttu-id="10708-120">Doit être un type particulier.</span><span class="sxs-lookup"><span data-stu-id="10708-120">Must be a particular type.</span></span><br/>                                     |
| <span data-ttu-id="10708-121"><span id="annotations"></span><span id="ANNOTATIONS"></span>*annotations*</span><span class="sxs-lookup"><span data-stu-id="10708-121"><span id="annotations"></span><span id="ANNOTATIONS"></span>*annotations*</span></span><br/> | <span data-ttu-id="10708-122">Zéro, un ou plusieurs éléments d’informations spécifiques à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="10708-122">Zero or more pieces of user-specific information.</span></span> <span data-ttu-id="10708-123">Peut être de n’importe quel type.</span><span class="sxs-lookup"><span data-stu-id="10708-123">May be any type.</span></span> <span data-ttu-id="10708-124">Consultez [Ajouter des informations pour appliquer des paramètres avec des annotations](using-an-effect.md).</span><span class="sxs-lookup"><span data-stu-id="10708-124">See [Add Information to Effect Parameters with Annotations](using-an-effect.md).</span></span><br/> |
| <span data-ttu-id="10708-125"><span id="expression"></span><span id="EXPRESSION"></span>*formule*</span><span class="sxs-lookup"><span data-stu-id="10708-125"><span id="expression"></span><span id="EXPRESSION"></span>*expression*</span></span><br/>    | <span data-ttu-id="10708-126">Initialise la valeur du paramètre.</span><span class="sxs-lookup"><span data-stu-id="10708-126">Initializes the parameter's value.</span></span> <span data-ttu-id="10708-127">Consultez [expressions (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="10708-127">See [Expressions (Direct3D 9)](expressions.md).</span></span><br/>                                                                  |



 

<span data-ttu-id="10708-128">Les paramètres peuvent être initialisés à toute [référence valide pour](../direct3dhlsl/dx-graphics-hlsl-reference.md) l’expression HLSL qui réduit à une valeur littérale.</span><span class="sxs-lookup"><span data-stu-id="10708-128">Parameters can be initialized to any valid [Reference for HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) expression that reduces to a literal value.</span></span>

<span data-ttu-id="10708-129">Les valeurs de paramètre ne sont pas modifiées par l’exécution d’une assignation d’État ou d’appels de fonction.</span><span class="sxs-lookup"><span data-stu-id="10708-129">Parameter values are not changed by the execution of state assignment or function calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10708-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="10708-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10708-131">Format d’effet</span><span class="sxs-lookup"><span data-stu-id="10708-131">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
