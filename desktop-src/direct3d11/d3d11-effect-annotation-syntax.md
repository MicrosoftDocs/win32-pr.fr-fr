---
title: Syntaxe d’annotation (Direct3D 11)
description: Une annotation est une information définie par l’utilisateur, déclarée avec la syntaxe décrite dans cette section.
ms.assetid: a81198d2-c4d7-47b5-b3b8-2de11a9ee9a3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9583dafd3e1fb314ae6ac9e53d609bebc74a030
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941019"
---
# <a name="annotation-syntax-direct3d-11"></a><span data-ttu-id="2f73b-103">Syntaxe d’annotation (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="2f73b-103">Annotation Syntax (Direct3D 11)</span></span>

<span data-ttu-id="2f73b-104">Une annotation est une information définie par l’utilisateur, déclarée avec la syntaxe décrite dans cette section.</span><span class="sxs-lookup"><span data-stu-id="2f73b-104">An annotation is a user-defined piece of information, declared with the syntax described in this section.</span></span>



| <span data-ttu-id="2f73b-105"><Valeur du *nom* de *type de données*  =  ; *...* ; ></span><span class="sxs-lookup"><span data-stu-id="2f73b-105"><*DataType* *Name* = *Value*; *...* ;></span></span> |
|----------------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="2f73b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f73b-106">Parameters</span></span>



| <span data-ttu-id="2f73b-107">Élément</span><span class="sxs-lookup"><span data-stu-id="2f73b-107">Item</span></span>                                                                                                   | <span data-ttu-id="2f73b-108">Description</span><span class="sxs-lookup"><span data-stu-id="2f73b-108">Description</span></span>                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f73b-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Décimal*</span><span class="sxs-lookup"><span data-stu-id="2f73b-109"><span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*DataType*</span></span><br/> | <span data-ttu-id="2f73b-110">\[dans \] le type de données, qui comprend tout type [HLSL scalaire](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) , ainsi que le [type chaîne](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).</span><span class="sxs-lookup"><span data-stu-id="2f73b-110">\[in\] The data type, which includes any [scalar HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) type as well as the [string type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar).</span></span><br/> |
| <span data-ttu-id="2f73b-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomme*</span><span class="sxs-lookup"><span data-stu-id="2f73b-111"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span><br/>                 | <span data-ttu-id="2f73b-112">\[dans \] une chaîne ASCII, qui représente le nom de l’annotation.</span><span class="sxs-lookup"><span data-stu-id="2f73b-112">\[in\] An ASCII string, that represents the annotation name.</span></span><br/>                                                                                                          |
| <span data-ttu-id="2f73b-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Ajoutée*</span><span class="sxs-lookup"><span data-stu-id="2f73b-113"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Value*</span></span><br/>             | <span data-ttu-id="2f73b-114">\[dans \] la valeur initiale de l’annotation.</span><span class="sxs-lookup"><span data-stu-id="2f73b-114">\[in\] The initial value of the annotation.</span></span><br/>                                                                                                                           |
| <span data-ttu-id="2f73b-115"><span id="..."></span>*...*</span><span class="sxs-lookup"><span data-stu-id="2f73b-115"><span id="..."></span>*...*</span></span><br/>                                                                 | <span data-ttu-id="2f73b-116">\[dans \] les annotations supplémentaires (paires nom-valeur).</span><span class="sxs-lookup"><span data-stu-id="2f73b-116">\[in\] Additional annotations (name-value pairs).</span></span><br/>                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="2f73b-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2f73b-117">Remarks</span></span>

<span data-ttu-id="2f73b-118">Vous pouvez ajouter plusieurs annotations entre crochets pointus, chacune d’elles étant séparées par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="2f73b-118">You may add more than one annotation within the angle brackets, each one separated by a semicolon.</span></span> <span data-ttu-id="2f73b-119">Les API d’infrastructure d’effet reconnaissent les annotations sur les variables globales ; toutes les autres annotations sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="2f73b-119">The effect framework APIs recognize annotations on global variables; all other annotations are ignored.</span></span>

## <a name="example"></a><span data-ttu-id="2f73b-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="2f73b-120">Example</span></span>

<span data-ttu-id="2f73b-121">Voici quelques exemples.</span><span class="sxs-lookup"><span data-stu-id="2f73b-121">Here are some examples.</span></span>


```
       
int i <int blabla=27; string blacksheep="Hello There";>;

int j <int bambam=30; string blacksheep="Goodbye There";> = 5 ;

float y <float y=2.3;> = 2.3, z <float y=1.3;> = 1.3 ;

half w <half GlobalW = 3.62;>;

float4 main(float4 pos : SV_POSITION ) : SV_POSITION
{
    pos.y = pos.x > 0 ? pos.w * 1.3 : pos.z * .032;
    for (int x = i; x < j ; x++) 
    {
        pos.w = pos.w * pos.y + x + j - y * w;
    } 

return pos;
}
```



## <a name="related-topics"></a><span data-ttu-id="2f73b-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2f73b-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f73b-123">Format d’effet</span><span class="sxs-lookup"><span data-stu-id="2f73b-123">Effect Format</span></span>](d3d11-effect-format.md)
</dt> <dt>

[<span data-ttu-id="2f73b-124">Syntaxe de la variable Effect</span><span class="sxs-lookup"><span data-stu-id="2f73b-124">Effect Variable Syntax</span></span>](d3d11-effect-variable-syntax.md)
</dt> </dl>

 

