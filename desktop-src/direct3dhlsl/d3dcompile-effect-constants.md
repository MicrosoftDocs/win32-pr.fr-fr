---
title: Constantes D3DCOMPILE_EFFECT (D3DCompiler. h)
description: Ces constantes indiquent comment le compilateur compile un fichier Effect ou comment le runtime traite le fichier Effect.
ms.assetid: AA46E5ED-92DD-4327-B852-8DD23A878562
topic_type:
- apiref
api_name:
- D3DCOMPILE_EFFECT_CHILD_EFFECT
- D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS
api_location:
- D3DCompiler.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69f0597341a331af82ed279a6030126d222b70f7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974458"
---
# <a name="d3dcompile_effect-constants"></a><span data-ttu-id="0b411-103">\_Constantes d’effet D3DCOMPILE</span><span class="sxs-lookup"><span data-stu-id="0b411-103">D3DCOMPILE\_EFFECT Constants</span></span>

<span data-ttu-id="0b411-104">Ces constantes indiquent comment le compilateur compile un fichier Effect ou comment le runtime traite le fichier Effect.</span><span class="sxs-lookup"><span data-stu-id="0b411-104">These constants direct how the compiler compiles an effect file or how the runtime processes the effect file.</span></span>

<dl> <dt>

<span data-ttu-id="0b411-105"><span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**Effet \_ \_ enfant D3DCOMPILE \_**</span><span class="sxs-lookup"><span data-stu-id="0b411-105"><span id="D3DCOMPILE_EFFECT_CHILD_EFFECT"></span><span id="d3dcompile_effect_child_effect"></span>**D3DCOMPILE\_EFFECT\_CHILD\_EFFECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b411-106">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="0b411-106">(1 << 0)</span></span>
</dt> <dt>



<span data-ttu-id="0b411-107">Compilez le fichier Effects (. FX) en un effet enfant.</span><span class="sxs-lookup"><span data-stu-id="0b411-107">Compile the effects (.fx) file to a child effect.</span></span> <span data-ttu-id="0b411-108">Les effets enfants n’ont aucun initialiseur pour les valeurs partagées, car ces effets enfants sont initialisés dans l’effet principal (le pool d’effets).</span><span class="sxs-lookup"><span data-stu-id="0b411-108">Child effects have no initializers for any shared values because these child effects are initialized in the master effect (the effect pool).</span></span>

> [!Note]  
> <span data-ttu-id="0b411-109">Les pools d’effets sont pris en charge par les effets 10 (FX10), mais pas par les effets 11 (FX11).</span><span class="sxs-lookup"><span data-stu-id="0b411-109">Effect pools are supported by Effects 10 (FX10) but not by Effects 11 (FX11).</span></span> <span data-ttu-id="0b411-110">Pour plus d’informations sur les différences entre les pools d’effets dans Direct3D 10 et les groupes d’effets dans Direct3D 11, consultez [pools et groupes](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences)d’effets.</span><span class="sxs-lookup"><span data-stu-id="0b411-110">For more info about differences between effect pools in Direct3D 10 and effect groups in Direct3D 11, see [Effect Pools and Groups](/windows/desktop/direct3d11/d3d11-graphics-programming-guide-effects-differences).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="0b411-111"><span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**L' \_ effet D3DCOMPILE \_ autorise les \_ opérations lentes \_**</span><span class="sxs-lookup"><span data-stu-id="0b411-111"><span id="D3DCOMPILE_EFFECT_ALLOW_SLOW_OPS"></span><span id="d3dcompile_effect_allow_slow_ops"></span>**D3DCOMPILE\_EFFECT\_ALLOW\_SLOW\_OPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b411-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="0b411-112">(1 << 1)</span></span>
</dt> <dt>



<span data-ttu-id="0b411-113">Désactive le mode de performance et autorise les objets d’État mutable.</span><span class="sxs-lookup"><span data-stu-id="0b411-113">Disables performance mode and allows for mutable state objects.</span></span>

<span data-ttu-id="0b411-114">Par défaut, le mode de performance est activé.</span><span class="sxs-lookup"><span data-stu-id="0b411-114">By default, performance mode is enabled.</span></span> <span data-ttu-id="0b411-115">Le mode de performance interdit les objets d’État mutable en empêchant les expressions non littérales d’apparaître dans les définitions d’objets d’État.</span><span class="sxs-lookup"><span data-stu-id="0b411-115">Performance mode disallows mutable state objects by preventing non-literal expressions from appearing in state object definitions.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b411-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="0b411-116">Requirements</span></span>



| <span data-ttu-id="0b411-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b411-117">Requirement</span></span> | <span data-ttu-id="0b411-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b411-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b411-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b411-119">Header</span></span><br/> | <dl> <span data-ttu-id="0b411-120"><dt>D3DCompiler. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b411-120"><dt>D3DCompiler.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b411-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b411-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b411-122">Constantes D3DCompiler</span><span class="sxs-lookup"><span data-stu-id="0b411-122">D3DCompiler Constants</span></span>](dx-graphics-d3dcompiler-reference-constants.md)
</dt> </dl>

 

