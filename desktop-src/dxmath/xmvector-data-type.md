---
description: Type portable utilisé pour représenter un vecteur de composants à virgule flottante ou entier 4 32 bits, chacun étant aligné de manière optimale et mappé à un registre de vecteur matériel.
ms.assetid: 1a044094-444d-e787-fa6a-76e88531aef1
title: Type de données XMVECTOR (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c62cab01098cd95f904ac2e2ee33d420309e8e99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545898"
---
# <a name="xmvector-data-type"></a><span data-ttu-id="e6790-103">Type de données XMVECTOR</span><span class="sxs-lookup"><span data-stu-id="e6790-103">XMVECTOR Data Type</span></span>

<span data-ttu-id="e6790-104">Type portable utilisé pour représenter un vecteur de composants à virgule flottante ou entier 4 32 bits, chacun étant aligné de manière optimale et mappé à un registre de vecteur matériel.</span><span class="sxs-lookup"><span data-stu-id="e6790-104">A portable type used to represent a vector of four 32-bit floating-point or integer components, each aligned optimally and mapped to a hardware vector register.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6790-105">Notes</span><span class="sxs-lookup"><span data-stu-id="e6790-105">Remarks</span></span>

<span data-ttu-id="e6790-106">Pour obtenir la liste des fonctionnalités supplémentaires, telles que les constructeurs et les opérateurs, disponibles à l’aide `XMVECTOR` de lors de la programmation en C++, consultez [Extensions XMVECTOR](ovw-xmvector-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="e6790-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTOR` when programming in C++, see [XMVECTOR Extensions](ovw-xmvector-extensions.md).</span></span>

<span data-ttu-id="e6790-107">Dans la bibliothèque DirectXMath, pour prendre entièrement en charge la portabilité et l’optimisation, `XMVECTOR` est, par conception, un type opaque.</span><span class="sxs-lookup"><span data-stu-id="e6790-107">In the DirectXMath Library, to fully support portability and optimization, `XMVECTOR` is, by design, an opaque type.</span></span> <span data-ttu-id="e6790-108">L’implémentation réelle de dépend de la `XMVECTOR` plateforme.</span><span class="sxs-lookup"><span data-stu-id="e6790-108">The actual implementation of `XMVECTOR` is platform dependent.</span></span>

<span data-ttu-id="e6790-109">En général, le code ne doit pas reposer sur les caractéristiques de toute implémentation spécifique à une plateforme donnée de `XMVECTOR` .</span><span class="sxs-lookup"><span data-stu-id="e6790-109">In general, code should not rely on the specifics of any given platform specific implementation of `XMVECTOR`.</span></span> <span data-ttu-id="e6790-110">Les implémentations spécifiques à la plateforme présentent les caractéristiques suivantes :</span><span class="sxs-lookup"><span data-stu-id="e6790-110">Platform-specific implementations have these characteristics:</span></span>

-   <span data-ttu-id="e6790-111">Ils ne sont pas portables.</span><span class="sxs-lookup"><span data-stu-id="e6790-111">They are not portable.</span></span>
-   <span data-ttu-id="e6790-112">Ils peuvent changer d’une version à l’autre.</span><span class="sxs-lookup"><span data-stu-id="e6790-112">They may change between releases.</span></span>
-   <span data-ttu-id="e6790-113">L’utilisation inopportune des détails d’implémentation peut être non optimale.</span><span class="sxs-lookup"><span data-stu-id="e6790-113">Injudicious use of implementation details may be suboptimal.</span></span>

<span data-ttu-id="e6790-114">Les développeurs doivent utiliser les fonctions d' [accesseur](ovw-xnamath-reference-functions-accessors.md), de [chargement](ovw-xnamath-reference-functions-load.md)et de [stockage](ovw-xnamath-reference-functions-storage.md) de la bibliothèque DirectXMath pour récupérer et définir les vecteurs, ainsi que les fonctions de Vector 4D de la [bibliothèque DirectXMath](ovw-xnamath-reference-functions-vector4.md) pour les manipuler.</span><span class="sxs-lookup"><span data-stu-id="e6790-114">Developers should use DirectXMath Library's [accessor](ovw-xnamath-reference-functions-accessors.md), [load](ovw-xnamath-reference-functions-load.md), and [store](ovw-xnamath-reference-functions-storage.md) functions to get and set the vectors, and the [DirectXMath Library 4D Vector Functions](ovw-xnamath-reference-functions-vector4.md) to manipulate them.</span></span>

<span data-ttu-id="e6790-115">Pour les projets qui requièrent des informations détaillées sur la façon d’implémenter `XMVECTOR` sur différentes plateformes, consultez [bibliothèques internes](pg-xnamath-internals.md).</span><span class="sxs-lookup"><span data-stu-id="e6790-115">For projects that need detailed information about how to implement `XMVECTOR` on different platforms, see [Library Internals](pg-xnamath-internals.md).</span></span>

### <a name="compiler-aliases"></a><span data-ttu-id="e6790-116">Alias de compilateur</span><span class="sxs-lookup"><span data-stu-id="e6790-116">Compiler Aliases</span></span>

<span data-ttu-id="e6790-117">Le fichier d’en-tête DirectXMath. h utilise des alias pour l' `XMVECTOR` objet, notamment **CXMVECTOR** et **FXMVECTOR**.</span><span class="sxs-lookup"><span data-stu-id="e6790-117">The DirectXMath.h header file uses aliases to the `XMVECTOR` object, specifically **CXMVECTOR** and **FXMVECTOR**.</span></span> <span data-ttu-id="e6790-118">L’en-tête utilise ces alias pour se conformer aux conventions d’appel optimales en ligne de différents compilateurs.</span><span class="sxs-lookup"><span data-stu-id="e6790-118">The header uses these aliases to comply with the optimal in-line calling conventions of different compilers.</span></span> <span data-ttu-id="e6790-119">Pour la plupart des projets qui utilisent DirectXMath, il suffit de traiter ces types comme un alias exact de `XMVECTOR` .</span><span class="sxs-lookup"><span data-stu-id="e6790-119">For most projects that use DirectXMath it is sufficient to treat these types as an exact alias to `XMVECTOR`.</span></span>

<span data-ttu-id="e6790-120">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e6790-120">For example:</span></span>


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



<span data-ttu-id="e6790-121">Pour les projets qui requièrent des informations détaillées sur la façon dont les différentes plateformes gèrent leurs conventions d’appel, consultez [bibliothèques internes](pg-xnamath-internals.md).</span><span class="sxs-lookup"><span data-stu-id="e6790-121">For projects that need detailed information about how different platforms handle their calling conventions, see [Library Internals](pg-xnamath-internals.md).</span></span>

<span data-ttu-id="e6790-122">Pour XNAMATH 2. x, le `XMVECTOR` type de données contient des membres d’élément. x,. y,. z,. et. w, ce qui entraîne généralement une baisse des performances.</span><span class="sxs-lookup"><span data-stu-id="e6790-122">For XNAMATH 2.x, the `XMVECTOR` data type has .x, .y, .z, .and .w element members, which generally cause poor performance.</span></span> <span data-ttu-id="e6790-123">L’utilisation du \_ \_ type strict VECTOR4 fournit un abonnement à la définition DirectXMath d’un type de données opaque.</span><span class="sxs-lookup"><span data-stu-id="e6790-123">The use of the XM\_STRICT\_VECTOR4 type provides an opt-in of the DirectXMath definition of an opaque data type.</span></span>

<span data-ttu-id="e6790-124">**Espace de noms**: utiliser DirectX</span><span class="sxs-lookup"><span data-stu-id="e6790-124">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="e6790-125">Conditions requises par la plateforme</span><span class="sxs-lookup"><span data-stu-id="e6790-125">Platform Requirements</span></span>

<span data-ttu-id="e6790-126">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e6790-126">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="e6790-127">Pris en charge pour les applications de bureau Win32, les applications du Windows Store et les applications Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="e6790-127">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6790-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6790-128">Requirements</span></span>



| <span data-ttu-id="e6790-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6790-129">Requirement</span></span> | <span data-ttu-id="e6790-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6790-130">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6790-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6790-131">Header</span></span><br/> | <dl> <span data-ttu-id="e6790-132"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6790-132"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6790-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6790-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6790-134">Types de bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="e6790-134">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="e6790-135">**Type de données XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="e6790-135">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="e6790-136">**Type de données XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="e6790-136">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="e6790-137">**Type de données XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="e6790-137">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="e6790-138">**Type de données XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="e6790-138">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="e6790-139">**Type de données XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="e6790-139">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> </dl>

 

 




