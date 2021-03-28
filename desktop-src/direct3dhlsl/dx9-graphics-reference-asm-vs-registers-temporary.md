---
title: Registre temporaire (référence HLSL VS)
description: Un registre temporaire de nuanceur de sommets est utilisé pour conserver les résultats intermédiaires.
ms.assetid: 186adff6-0641-4507-9adc-e02cf1cc3ea9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3dcaa5ac0c9c1531a1e1f0476d2ef13b4bac509
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104313798"
---
# <a name="temporary-register-hlsl-vs-reference"></a><span data-ttu-id="b509f-103">Registre temporaire (référence HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="b509f-103">Temporary Register (HLSL VS reference)</span></span>

<span data-ttu-id="b509f-104">Un registre temporaire de nuanceur de sommets est utilisé pour conserver les résultats intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="b509f-104">A vertex shader temporary register is used to hold intermediate results.</span></span>

<span data-ttu-id="b509f-105">Un registre temporaire doit être initialisé avant d’être utilisé.</span><span class="sxs-lookup"><span data-stu-id="b509f-105">A temporary register must be initialized before it is used.</span></span> <span data-ttu-id="b509f-106">Chaque registre temporaire dispose d’un accès en écriture unique et triple lecture.</span><span class="sxs-lookup"><span data-stu-id="b509f-106">Each temporary register has single-write and triple-read access.</span></span> <span data-ttu-id="b509f-107">Cela signifie qu’une instruction de nuanceur unique peut utiliser jusqu’à trois registres temporaires comme entrées.</span><span class="sxs-lookup"><span data-stu-id="b509f-107">This means that a single shader instruction can use as many as three temporary registers as inputs.</span></span>

<span data-ttu-id="b509f-108">Les valeurs d’un registre temporaire qui restent des appels précédents du nuanceur vertex ne peuvent pas être utilisées.</span><span class="sxs-lookup"><span data-stu-id="b509f-108">Values in a temporary register that remain from preceding invocations of the vertex shader cannot be used.</span></span>

<span data-ttu-id="b509f-109">Un registre se compose de propriétés qui déterminent le comportement de chaque registre.</span><span class="sxs-lookup"><span data-stu-id="b509f-109">A register consists of properties that determine how each register behaves.</span></span>



| <span data-ttu-id="b509f-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="b509f-110">Property</span></span>        | <span data-ttu-id="b509f-111">Description</span><span class="sxs-lookup"><span data-stu-id="b509f-111">Description</span></span>                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b509f-112">Nom</span><span class="sxs-lookup"><span data-stu-id="b509f-112">Name</span></span>            | <span data-ttu-id="b509f-113">r \[ n \] .</span><span class="sxs-lookup"><span data-stu-id="b509f-113">r\[n\].</span></span> <span data-ttu-id="b509f-114">n est un numéro de Registre facultatif.</span><span class="sxs-lookup"><span data-stu-id="b509f-114">n is an optional register number.</span></span> <span data-ttu-id="b509f-115">La valeur par défaut est 0, et est la valeur utilisée si aucune valeur n’est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b509f-115">The default is 0, and is the value used if no value is specified.</span></span>                                                                                 |
| <span data-ttu-id="b509f-116">Count</span><span class="sxs-lookup"><span data-stu-id="b509f-116">Count</span></span>           | <span data-ttu-id="b509f-117">Un maximum de 12 registres.</span><span class="sxs-lookup"><span data-stu-id="b509f-117">A maximum of 12 registers.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="b509f-118">Autorisations d’e/s</span><span class="sxs-lookup"><span data-stu-id="b509f-118">I/O permissions</span></span> | <span data-ttu-id="b509f-119">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b509f-119">Read/write.</span></span> <span data-ttu-id="b509f-120">Ce registre peut être lu ou écrit par l’API ou par le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="b509f-120">This register can be read or written by the API or by the shader.</span></span>                                                                                                               |
| <span data-ttu-id="b509f-121">Ports de lecture</span><span class="sxs-lookup"><span data-stu-id="b509f-121">Read ports</span></span>      | <span data-ttu-id="b509f-122">Le nombre de fois qu’un registre peut être lu dans une instruction unique est 3.</span><span class="sxs-lookup"><span data-stu-id="b509f-122">The number of times a register can be read within a single instruction is 3.</span></span> <span data-ttu-id="b509f-123">Un registre temporaire est le seul registre qui peut être lu et écrit plusieurs fois dans une même instruction.</span><span class="sxs-lookup"><span data-stu-id="b509f-123">A temporary register is the only register that can be read and written more than once in a single instruction.</span></span> |



 

<span data-ttu-id="b509f-124">Chaque registre temporaire dispose d’un accès en écriture unique et triple lecture.</span><span class="sxs-lookup"><span data-stu-id="b509f-124">Each temporary register has single-write and triple-read access.</span></span> <span data-ttu-id="b509f-125">Par conséquent, une instruction peut avoir jusqu’à trois registres temporaires dans son ensemble d’opérandes de source d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b509f-125">Therefore, an instruction can have as many as three temporary registers in its set of input source operands.</span></span>

<span data-ttu-id="b509f-126">Aucune valeur dans un registre temporaire qui reste des appels précédents du nuanceur vertex ne peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="b509f-126">No values in a temporary register that remain from preceding invocations of the vertex shader can be used.</span></span> <span data-ttu-id="b509f-127">Les nuanceurs de sommets qui lisent une valeur à partir d’un registre temporaire avant d’y écrire échouent à l’appel de l’API Direct3D pour créer le nuanceur de sommets.</span><span class="sxs-lookup"><span data-stu-id="b509f-127">Vertex shaders that read a value from a temporary register before writing to it will fail the Direct3D API call to create the vertex shader.</span></span>

## <a name="example"></a><span data-ttu-id="b509f-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="b509f-128">Example</span></span>

<span data-ttu-id="b509f-129">Voici un exemple d’utilisation d’un registre temporaire :</span><span class="sxs-lookup"><span data-stu-id="b509f-129">Here is an example using a temporary register:</span></span>


```
def c4, 0,0,0,1
...
// Decompress position
mov r0.x, v0.x
mov r0.y, c4.w       // 1
mov r0.z, v0.y
mov r0.w, c4.w       // 1

// Compute theta from distance and time
mov r4.xz, r0        // xz
```





| <span data-ttu-id="b509f-130">Versions de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="b509f-130">Vertex shader versions</span></span> | <span data-ttu-id="b509f-131">1\_1</span><span class="sxs-lookup"><span data-stu-id="b509f-131">1\_1</span></span> | <span data-ttu-id="b509f-132">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b509f-132">2\_0</span></span> | <span data-ttu-id="b509f-133">2 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="b509f-133">2\_sw</span></span> | <span data-ttu-id="b509f-134">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="b509f-134">2\_x</span></span> | <span data-ttu-id="b509f-135">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="b509f-135">3\_0</span></span> | <span data-ttu-id="b509f-136">3 \_ logiciels</span><span class="sxs-lookup"><span data-stu-id="b509f-136">3\_sw</span></span> |
|------------------------|------|------|-------|------|------|-------|
| <span data-ttu-id="b509f-137">Registre temporaire</span><span class="sxs-lookup"><span data-stu-id="b509f-137">Temporary Register</span></span>     | <span data-ttu-id="b509f-138">x</span><span class="sxs-lookup"><span data-stu-id="b509f-138">x</span></span>    | <span data-ttu-id="b509f-139">x</span><span class="sxs-lookup"><span data-stu-id="b509f-139">x</span></span>    | <span data-ttu-id="b509f-140">x</span><span class="sxs-lookup"><span data-stu-id="b509f-140">x</span></span>     | <span data-ttu-id="b509f-141">x</span><span class="sxs-lookup"><span data-stu-id="b509f-141">x</span></span>    | <span data-ttu-id="b509f-142">x</span><span class="sxs-lookup"><span data-stu-id="b509f-142">x</span></span>    | <span data-ttu-id="b509f-143">x</span><span class="sxs-lookup"><span data-stu-id="b509f-143">x</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="b509f-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b509f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b509f-145">Registres de nuanceur vertex</span><span class="sxs-lookup"><span data-stu-id="b509f-145">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




