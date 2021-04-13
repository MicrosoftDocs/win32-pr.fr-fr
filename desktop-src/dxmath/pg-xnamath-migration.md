---
description: Cette vue d’ensemble décrit les modifications requises pour migrer le code existant à l’aide de la bibliothèque Math XNA vers la bibliothèque DirectXMath.
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: Migration de code à partir de la bibliothèque XNA Math
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c446165d3d0b6b7303424959f96ddf48bc75b5fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528041"
---
# <a name="code-migration-from-the-xna-math-library"></a><span data-ttu-id="d3a29-103">Migration de code à partir de la bibliothèque XNA Math</span><span class="sxs-lookup"><span data-stu-id="d3a29-103">Code Migration from the XNA Math Library</span></span>

<span data-ttu-id="d3a29-104">Cette vue d’ensemble décrit les modifications requises pour migrer le code existant à l’aide de la bibliothèque Math XNA vers la bibliothèque DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="d3a29-104">This overview describes the changes required to migrate existing code using the XNA Math library to the DirectXMath library.</span></span>

-   [<span data-ttu-id="d3a29-105">Modifications d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d3a29-105">Header Changes</span></span>](#header-changes)
-   [<span data-ttu-id="d3a29-106">Modifications de constante</span><span class="sxs-lookup"><span data-stu-id="d3a29-106">Constant Changes</span></span>](#constant-changes)
-   [<span data-ttu-id="d3a29-107">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="d3a29-107">Namespaces</span></span>](#namespaces)
-   [<span data-ttu-id="d3a29-108">Charges partielles</span><span class="sxs-lookup"><span data-stu-id="d3a29-108">Partial Loads</span></span>](#partial-loads)
-   [<span data-ttu-id="d3a29-109">Suppression de types spécifiques de Xbox 360</span><span class="sxs-lookup"><span data-stu-id="d3a29-109">Removal of Xbox 360 Specific Types</span></span>](#removal-of-xbox-360-specific-types)
-   [<span data-ttu-id="d3a29-110">Intrinsèques ARM-néon</span><span class="sxs-lookup"><span data-stu-id="d3a29-110">ARM-NEON Intrinsics</span></span>](#arm-neon-intrinsics)
-   [<span data-ttu-id="d3a29-111">Permute</span><span class="sxs-lookup"><span data-stu-id="d3a29-111">Permute</span></span>](#permute)
-   [<span data-ttu-id="d3a29-112">Formulaires de modèle</span><span class="sxs-lookup"><span data-stu-id="d3a29-112">Template Forms</span></span>](#template-forms)
-   [<span data-ttu-id="d3a29-113">Fonctions éliminées</span><span class="sxs-lookup"><span data-stu-id="d3a29-113">Eliminated Functions</span></span>](#eliminated-functions)
-   [<span data-ttu-id="d3a29-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3a29-114">Related topics</span></span>](#related-topics)

## <a name="header-changes"></a><span data-ttu-id="d3a29-115">Modifications d’en-tête</span><span class="sxs-lookup"><span data-stu-id="d3a29-115">Header Changes</span></span>

<span data-ttu-id="d3a29-116">La bibliothèque DirectXMath utilise un nouvel ensemble d’en-têtes.</span><span class="sxs-lookup"><span data-stu-id="d3a29-116">The DirectXMath library uses a new set of headers.</span></span>

<span data-ttu-id="d3a29-117">Remplacez l’en-tête xnamath. h par DirectXMath. h et ajoutez DirectXPackedVector. h pour les types « processeurs GPU ».</span><span class="sxs-lookup"><span data-stu-id="d3a29-117">Replace the xnamath.h header with DirectXMath.h and add DirectXPackedVector.h for the “GPU packed” types.</span></span>

<span data-ttu-id="d3a29-118">Les types englobants de l’exemple de collision du kit de développement logiciel (SDK) DirectX dans xnacollision. h font désormais partie de la bibliothèque DirectXMath dans DirectXCollision. h.</span><span class="sxs-lookup"><span data-stu-id="d3a29-118">The bounding types from the DirectX SDK Collision sample in xnacollision.h is now part of the DirectXMath library in DirectXCollision.h.</span></span> <span data-ttu-id="d3a29-119">Celles-ci ont été modifiées pour utiliser des classes C++ plutôt qu’une API de style C.</span><span class="sxs-lookup"><span data-stu-id="d3a29-119">These have been modified to use C++ classes rather than a C-style API.</span></span>

## <a name="constant-changes"></a><span data-ttu-id="d3a29-120">Modifications de constante</span><span class="sxs-lookup"><span data-stu-id="d3a29-120">Constant Changes</span></span>

<span data-ttu-id="d3a29-121">La \_ version XNAMATH (200, 201, 202, 203, 204, etc.) a été remplacée par la \_ version DIRECXTMATH (300, 301, 302, 303, etc.).</span><span class="sxs-lookup"><span data-stu-id="d3a29-121">XNAMATH\_VERSION (200, 201, 202, 203, 204, and so on) has been replaced with DIRECXTMATH\_VERSION (300, 301, 302, 303, and so on).</span></span>

> [!Note]  
> <span data-ttu-id="d3a29-122">DirectXMath 3,00 et 3,02 sont livrés avec des versions préliminaires du SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="d3a29-122">DirectXMath 3.00 and 3.02 shipped with preliminary versions of the Windows SDK.</span></span> <span data-ttu-id="d3a29-123">DirectXMath 3,03 est dans la version finale du kit de développement logiciel (SDK) Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d3a29-123">DirectXMath 3.03 is in the final version of the Windows 8 SDK.</span></span>

 

## <a name="namespaces"></a><span data-ttu-id="d3a29-124">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="d3a29-124">Namespaces</span></span>

<span data-ttu-id="d3a29-125">La bibliothèque DirectXMath utilise des espaces de noms C++ pour organiser les types.</span><span class="sxs-lookup"><span data-stu-id="d3a29-125">The DirectXMath library uses C++ namespaces to organize the types.</span></span> <span data-ttu-id="d3a29-126">XNA Math a utilisé uniquement l’espace de noms global.</span><span class="sxs-lookup"><span data-stu-id="d3a29-126">XNA Math used only the global namespace.</span></span> <span data-ttu-id="d3a29-127">Les types DirectXMath en commun avec XNA Math se trouvent dans l’espace de noms « DirectX » ou « DirectX ::P ackedVector ».</span><span class="sxs-lookup"><span data-stu-id="d3a29-127">The DirectXMath types in common with XNA Math are in the “DirectX” or the “DirectX::PackedVector” namespace.</span></span>

<span data-ttu-id="d3a29-128">Dans les fichiers sources C++, une solution simple consiste à ajouter des instructions’Using' :</span><span class="sxs-lookup"><span data-stu-id="d3a29-128">In C++ source files, a simple solution is to add ‘using’ statements:</span></span>


```
#include “DirectXMath.h”
#include “DirectXPackedVector.h”

using namespace DirectX; 
using namespace DirectX::PackedVector;
```



<span data-ttu-id="d3a29-129">Pour les en-têtes, il n’est pas considéré comme « meilleure pratique » pour ajouter des instructions using.</span><span class="sxs-lookup"><span data-stu-id="d3a29-129">For headers, it is not considered ‘best practice’ to add using statements.</span></span> <span data-ttu-id="d3a29-130">Au lieu de cela, ajoutez des espaces de noms qualifiés complets :</span><span class="sxs-lookup"><span data-stu-id="d3a29-130">Instead, add fully qualified namespaces:</span></span>


```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```



## <a name="partial-loads"></a><span data-ttu-id="d3a29-131">Charges partielles</span><span class="sxs-lookup"><span data-stu-id="d3a29-131">Partial Loads</span></span>

<span data-ttu-id="d3a29-132">Pour les différentes fonctions qui chargent moins de 4 éléments d’un XMVECTOR, la bibliothèque mathématique XNA a laissé les éléments supplémentaires non définis.</span><span class="sxs-lookup"><span data-stu-id="d3a29-132">For various functions that load less than 4 elements of an XMVECTOR, the XNA Math library left the additional elements undefined.</span></span> <span data-ttu-id="d3a29-133">DirectXMath remplit toujours ces éléments supplémentaires avec 0.</span><span class="sxs-lookup"><span data-stu-id="d3a29-133">DirectXMath will always fill these additional elements with 0.</span></span>

## <a name="removal-of-xbox-360-specific-types"></a><span data-ttu-id="d3a29-134">Suppression de types spécifiques de Xbox 360</span><span class="sxs-lookup"><span data-stu-id="d3a29-134">Removal of Xbox 360 Specific Types</span></span>

<span data-ttu-id="d3a29-135">Les types, fonctions et constantes de bibliothèque mathématique XNA suivants ne sont pas disponibles dans DirectXMath.</span><span class="sxs-lookup"><span data-stu-id="d3a29-135">The following XNA Math library types, functions, and constants are not available in DirectXMath.</span></span>

-   <span data-ttu-id="d3a29-136">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span><span class="sxs-lookup"><span data-stu-id="d3a29-136">HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3</span></span>
-   <span data-ttu-id="d3a29-137">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span><span class="sxs-lookup"><span data-stu-id="d3a29-137">XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()</span></span>
-   <span data-ttu-id="d3a29-138">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span><span class="sxs-lookup"><span data-stu-id="d3a29-138">XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()</span></span>
-   <span data-ttu-id="d3a29-139">g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ XMAddDHen, g \_ XMMulHenD3, g \_ XMMulDHen3, g XMXorHenD3 \_ , g \_ XMXorDHen3</span><span class="sxs-lookup"><span data-stu-id="d3a29-139">g\_XMMaskHenD3, g\_XMMaskDHen3, g\_XMAddUHenD3, g\_XMAddHenD3, g\_XMAddDHen, g\_XMMulHenD3, g\_XMMulDHen3, g\_XMXorHenD3, g\_XMXorDHen3</span></span>
-   <span data-ttu-id="d3a29-140">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span><span class="sxs-lookup"><span data-stu-id="d3a29-140">XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4</span></span>
-   <span data-ttu-id="d3a29-141">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span><span class="sxs-lookup"><span data-stu-id="d3a29-141">XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()</span></span>
-   <span data-ttu-id="d3a29-142">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span><span class="sxs-lookup"><span data-stu-id="d3a29-142">XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()</span></span>
-   <span data-ttu-id="d3a29-143">g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g XMAddIco4 \_ , g \_ XMMulIco4</span><span class="sxs-lookup"><span data-stu-id="d3a29-143">g\_XMMaskIco4, g\_XMXorXIco4, g\_XMXorIco4, g\_XMAddXIco4, g\_XMAddUIco4, g\_XMAddIco4, g\_XMMulIco4</span></span>

<span data-ttu-id="d3a29-144">\_\_vector4i est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="d3a29-144">\_\_vector4i is deprecated.</span></span> <span data-ttu-id="d3a29-145">Utilisez [**XMVECTORI32**](xmvectori32-data-type.md) ou [**XMVECTORU32**](xmvectoru32-data-type.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="d3a29-145">Use [**XMVECTORI32**](xmvectori32-data-type.md) or [**XMVECTORU32**](xmvectoru32-data-type.md) instead.</span></span>

<span data-ttu-id="d3a29-146">Les fonctions et types suivants sont déconseillés, car il s’agit uniquement de Xbox 360 : XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span><span class="sxs-lookup"><span data-stu-id="d3a29-146">The following functions and types are deprecated as they are Xbox 360 only: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.</span></span>

## <a name="arm-neon-intrinsics"></a><span data-ttu-id="d3a29-147">Intrinsèques ARM-néon</span><span class="sxs-lookup"><span data-stu-id="d3a29-147">ARM-NEON Intrinsics</span></span>

<span data-ttu-id="d3a29-148">La déclaration d’une constante Vector avec ce code est compilée pour les mathématiques XNA pour SSE et non INTRINSÈQUEs, mais échoue pour DirectXMath à l’aide de ARM-néon.</span><span class="sxs-lookup"><span data-stu-id="d3a29-148">Declaring a vector constant with this code will compile for XNA Math for SSE and NO-INTRINSICS, but will fail for DirectXMath using ARM-NEON.</span></span>


```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```



<span data-ttu-id="d3a29-149">En général, nous ne recommandons pas cette méthode d’initialisation d’un [**XMVECTOR**](xmvector-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="d3a29-149">In general, we don't recommend this method of initialization of an [**XMVECTOR**](xmvector-data-type.md).</span></span> <span data-ttu-id="d3a29-150">Toutefois, si vous souhaitez une constante Vector, la classe [**XMVECTORF32**](xmvectorf32-data-type.md) prend en charge ce style d’initialisation et retourne le type **XMVECTOR** automatiquement afin que vous puissiez utiliser **XMVECTORF32** dans la plupart des contextes.</span><span class="sxs-lookup"><span data-stu-id="d3a29-150">However, if you want a vector constant, the [**XMVECTORF32**](xmvectorf32-data-type.md) class supports this style of initialization and returns the **XMVECTOR** type automatically so you can use **XMVECTORF32** in most of the same contexts.</span></span> <span data-ttu-id="d3a29-151">Toutes les opérations d’écriture dans une classe **XMVECTORF32** nécessitent un référencement explicite du membre **XMVECTOR** . v.</span><span class="sxs-lookup"><span data-stu-id="d3a29-151">Any write operations to an **XMVECTORF32** class require explicitly referencing the .v **XMVECTOR** member.</span></span>

## <a name="permute"></a><span data-ttu-id="d3a29-152">Permute</span><span class="sxs-lookup"><span data-stu-id="d3a29-152">Permute</span></span>

<span data-ttu-id="d3a29-153">La bibliothèque mathématique XNA a la forme suivante :</span><span class="sxs-lookup"><span data-stu-id="d3a29-153">The XNA Math library had the following form for general vector permute:</span></span>


```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```



<span data-ttu-id="d3a29-154">Pour DirectXMath, **XMVectorPermuteControl** a été éliminé et le XM \_ permute \_ 0x..</span><span class="sxs-lookup"><span data-stu-id="d3a29-154">For DirectXMath, **XMVectorPermuteControl** has been eliminated and the XM\_PERMUTE\_0X ..</span></span> <span data-ttu-id="d3a29-155">Les \_ \_ constantes de XM permute 1Z ont été redéfinies pour être des index simples de 0-7.</span><span class="sxs-lookup"><span data-stu-id="d3a29-155">XM\_PERMUTE\_1Z constants have been redefined to be simple 0-7 indices.</span></span> <span data-ttu-id="d3a29-156">Voici la nouvelle signature pour [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span><span class="sxs-lookup"><span data-stu-id="d3a29-156">Here is the new signature for [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute):</span></span>


```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```



<span data-ttu-id="d3a29-157">Au lieu d’un mot de contrôle, cette fonction accepte directement les 4 index comme paramètres, ce qui la rend également analogue à la fonction [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) à l’aide du nouveau XM \_ SWIZZLE \_ X..</span><span class="sxs-lookup"><span data-stu-id="d3a29-157">Instead of a control word, this function directly takes the 4 indices as parameters, which also makes it analogous to the [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) function using the new XM\_SWIZZLE\_X ..</span></span> <span data-ttu-id="d3a29-158">\_ \_ Les constantes XM SWIZZLE W sont définies comme des index 0-3 simples.</span><span class="sxs-lookup"><span data-stu-id="d3a29-158">XM\_SWIZZLE\_W constants defined as simple 0-3 indices.</span></span>


```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```



> [!Note]  
> <span data-ttu-id="d3a29-159">Pour les valeurs constantes, il existe un moyen bien plus efficace d’implémenter la permutation.</span><span class="sxs-lookup"><span data-stu-id="d3a29-159">For constant values, there is a much more efficient way to implement permute.</span></span> <span data-ttu-id="d3a29-160">Au lieu d’utiliser la forme de fonction de [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), utilisez le formulaire de **modèle** :</span><span class="sxs-lookup"><span data-stu-id="d3a29-160">Instead of using the function form of [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), use the **template** form:</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
> </tr>
> </tbody>
> </table>
>  
>
> ## <a name="template-forms"></a><span data-ttu-id="d3a29-161">Formulaires de modèle</span><span class="sxs-lookup"><span data-stu-id="d3a29-161">Template Forms</span></span>
>
> <span data-ttu-id="d3a29-162">En général, l’utilisation d’un formulaire de modèle sur une forme de fonction des fonctions suivantes est bien plus efficace et permet à la bibliothèque d’effectuer des optimisations spécifiques à la plateforme par le biais de la spécialisation de modèle.</span><span class="sxs-lookup"><span data-stu-id="d3a29-162">In general, using a template form over a function form of the following functions is much more efficient and allows the library to do platform specific optimizations through template specialization.</span></span>
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
>     XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
>     XMVECTOR XMVectorSwizzle(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateLeft(FXMVECTOR V)
>
> template<uint32_t Elements>
>     XMVECTOR XMVectorRotateRight(FXMVECTOR V)
>
> template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
>     XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> ## <a name="eliminated-functions"></a><span data-ttu-id="d3a29-163">Fonctions éliminées</span><span class="sxs-lookup"><span data-stu-id="d3a29-163">Eliminated Functions</span></span>
>
> 
>
> | <span data-ttu-id="d3a29-164">Fonction éliminée</span><span class="sxs-lookup"><span data-stu-id="d3a29-164">Eliminated Function</span></span>        | <span data-ttu-id="d3a29-165">Remplacement</span><span class="sxs-lookup"><span data-stu-id="d3a29-165">Replacement</span></span>                                                                                                       |
> |----------------------------|-------------------------------------------------------------------------------------------------------------------|
> | <span data-ttu-id="d3a29-166">XMStoreFloat3x3NC</span><span class="sxs-lookup"><span data-stu-id="d3a29-166">XMStoreFloat3x3NC</span></span>          | [<span data-ttu-id="d3a29-167">**XMStoreFloat3x3**</span><span class="sxs-lookup"><span data-stu-id="d3a29-167">**XMStoreFloat3x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
> | <span data-ttu-id="d3a29-168">XMStoreFloat4NC</span><span class="sxs-lookup"><span data-stu-id="d3a29-168">XMStoreFloat4NC</span></span>            | [<span data-ttu-id="d3a29-169">**XMStoreFloat4**</span><span class="sxs-lookup"><span data-stu-id="d3a29-169">**XMStoreFloat4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
> | <span data-ttu-id="d3a29-170">XMStoreFloat4x3NC</span><span class="sxs-lookup"><span data-stu-id="d3a29-170">XMStoreFloat4x3NC</span></span>          | [<span data-ttu-id="d3a29-171">**XMStoreFloat4x3**</span><span class="sxs-lookup"><span data-stu-id="d3a29-171">**XMStoreFloat4x3**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
> | <span data-ttu-id="d3a29-172">XMStoreFloat4x4NC</span><span class="sxs-lookup"><span data-stu-id="d3a29-172">XMStoreFloat4x4NC</span></span>          | [<span data-ttu-id="d3a29-173">**XMStoreFloat4x4**</span><span class="sxs-lookup"><span data-stu-id="d3a29-173">**XMStoreFloat4x4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
> | <span data-ttu-id="d3a29-174">XMStoreInt4NC</span><span class="sxs-lookup"><span data-stu-id="d3a29-174">XMStoreInt4NC</span></span>              | [<span data-ttu-id="d3a29-175">**XMStoreInt4**</span><span class="sxs-lookup"><span data-stu-id="d3a29-175">**XMStoreInt4**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
> | <span data-ttu-id="d3a29-176">XMVector2InBoundsR</span><span class="sxs-lookup"><span data-stu-id="d3a29-176">XMVector2InBoundsR</span></span>         | <span data-ttu-id="d3a29-177">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="d3a29-177">[**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ?</span></span> <span data-ttu-id="d3a29-178">[XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="d3a29-178">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="d3a29-179">XMVector2TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="d3a29-179">XMVector2TransformStreamNC</span></span> | [<span data-ttu-id="d3a29-180">**XMVector2TransformStream**</span><span class="sxs-lookup"><span data-stu-id="d3a29-180">**XMVector2TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
> | <span data-ttu-id="d3a29-181">XMVector3InBoundsR</span><span class="sxs-lookup"><span data-stu-id="d3a29-181">XMVector3InBoundsR</span></span>         | <span data-ttu-id="d3a29-182">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="d3a29-182">[**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ?</span></span> <span data-ttu-id="d3a29-183">[XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="d3a29-183">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="d3a29-184">XMVector3TransformStreamNC</span><span class="sxs-lookup"><span data-stu-id="d3a29-184">XMVector3TransformStreamNC</span></span> | [<span data-ttu-id="d3a29-185">**XMVector3TransformStream**</span><span class="sxs-lookup"><span data-stu-id="d3a29-185">**XMVector3TransformStream**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
> | <span data-ttu-id="d3a29-186">XMVector4InBoundsR</span><span class="sxs-lookup"><span data-stu-id="d3a29-186">XMVector4InBoundsR</span></span>         | <span data-ttu-id="d3a29-187">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span><span class="sxs-lookup"><span data-stu-id="d3a29-187">[**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ?</span></span> <span data-ttu-id="d3a29-188">[XM \_ CRMASK \_ CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span><span class="sxs-lookup"><span data-stu-id="d3a29-188">[XM\_CRMASK\_CR6BOUNDS](ovw-xnamath-reference-constants.md) : 0</span></span> |
> | <span data-ttu-id="d3a29-189">XMVectorCosHEst</span><span class="sxs-lookup"><span data-stu-id="d3a29-189">XMVectorCosHEst</span></span>            | [<span data-ttu-id="d3a29-190">**XMVectorCosH**</span><span class="sxs-lookup"><span data-stu-id="d3a29-190">**XMVectorCosH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
> | <span data-ttu-id="d3a29-191">XMVectorExpEst</span><span class="sxs-lookup"><span data-stu-id="d3a29-191">XMVectorExpEst</span></span>             | [<span data-ttu-id="d3a29-192">**XMVectorExp**</span><span class="sxs-lookup"><span data-stu-id="d3a29-192">**XMVectorExp**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
> | <span data-ttu-id="d3a29-193">XMVectorLogEst</span><span class="sxs-lookup"><span data-stu-id="d3a29-193">XMVectorLogEst</span></span>             | [<span data-ttu-id="d3a29-194">**XMVectorLog**</span><span class="sxs-lookup"><span data-stu-id="d3a29-194">**XMVectorLog**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
> | <span data-ttu-id="d3a29-195">XMVectorPowEst</span><span class="sxs-lookup"><span data-stu-id="d3a29-195">XMVectorPowEst</span></span>             | [<span data-ttu-id="d3a29-196">**XMVectorPow**</span><span class="sxs-lookup"><span data-stu-id="d3a29-196">**XMVectorPow**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
> | <span data-ttu-id="d3a29-197">XMVectorSinHEst</span><span class="sxs-lookup"><span data-stu-id="d3a29-197">XMVectorSinHEst</span></span>            | [<span data-ttu-id="d3a29-198">**XMVectorSinH**</span><span class="sxs-lookup"><span data-stu-id="d3a29-198">**XMVectorSinH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
> | <span data-ttu-id="d3a29-199">XMVectorTanHEst</span><span class="sxs-lookup"><span data-stu-id="d3a29-199">XMVectorTanHEst</span></span>            | [<span data-ttu-id="d3a29-200">**XMVectorTanH**</span><span class="sxs-lookup"><span data-stu-id="d3a29-200">**XMVectorTanH**</span></span>](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |
>
> 
>
>  
>
> ## <a name="related-topics"></a><span data-ttu-id="d3a29-201">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d3a29-201">Related topics</span></span>
>
> <dl> <dt>

[<span data-ttu-id="d3a29-202">Guide de programmation DirectXMath</span><span class="sxs-lookup"><span data-stu-id="d3a29-202">DirectXMath Programming Guide</span></span>](ovw-xnamath-progguide.md)
</dt> </dl>
>
>  
>
>  
>
