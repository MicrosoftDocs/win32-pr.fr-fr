---
description: Type portable opaque pour prendre en charge l’utilisation de la syntaxe d’initialiseur C/C++ pour charger des valeurs entières dans une instance de type XMVECTOR.
ms.assetid: 6564030e-b6e9-0c4f-4e2a-4132e4264c94
title: Type de données XMVECTORI32 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ac36caf97a62037223840e9220876f1c7a1f09a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540688"
---
# <a name="xmvectori32-data-type"></a><span data-ttu-id="94e17-103">Type de données XMVECTORI32</span><span class="sxs-lookup"><span data-stu-id="94e17-103">XMVECTORI32 Data Type</span></span>

<span data-ttu-id="94e17-104">Type portable opaque pour prendre en charge l’utilisation de la syntaxe d’initialiseur C/C++ pour charger des valeurs entières dans une instance de type [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="94e17-104">An opaque, portable type to support the use of C/C++ initializer syntax to load integer values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORI32 vectori32;
```



## <a name="remarks"></a><span data-ttu-id="94e17-105">Notes</span><span class="sxs-lookup"><span data-stu-id="94e17-105">Remarks</span></span>

<span data-ttu-id="94e17-106">Pour obtenir la liste des fonctionnalités supplémentaires, telles que les constructeurs et les opérateurs, disponibles à l’aide `XMVECTORI32` de lors de la programmation en C++, consultez [Extensions XMVECTORI32](ovw-xmvectori32-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="94e17-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTORI32` when programming in C++, see [XMVECTORI32 Extensions](ovw-xmvectori32-extensions.md).</span></span>

<span data-ttu-id="94e17-107">Les structures [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32** et [**XMVECTORU8**](xmvectoru8-data-type.md) sont fournies en tant que mécanisme pour créer des [**XMVECTOR**](xmvector-data-type.md) à partir de différents types de données constantes (virgule flottante, entier non signé, entier et octet) à l’aide d’initialiseurs.</span><span class="sxs-lookup"><span data-stu-id="94e17-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32**, and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="94e17-108">Cela est nécessaire pour prendre en charge [**XMVECTOR**](xmvector-data-type.md), car il ne prend pas en charge les initialiseurs, pour des raisons de portabilité et d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="94e17-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="94e17-109">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="94e17-109">For example:</span></span>


```
XMVECTOR data;
XMVECTORI32 intVector = { -1, 5, 33, 0 };
data = intVector;
```



<span data-ttu-id="94e17-110">**Espace de noms**: utiliser DirectX</span><span class="sxs-lookup"><span data-stu-id="94e17-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="94e17-111">Conditions requises par la plateforme</span><span class="sxs-lookup"><span data-stu-id="94e17-111">Platform Requirements</span></span>

<span data-ttu-id="94e17-112">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="94e17-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="94e17-113">Pris en charge pour les applications de bureau Win32, les applications du Windows Store et les applications Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="94e17-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="94e17-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94e17-114">Requirements</span></span>



| <span data-ttu-id="94e17-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="94e17-115">Requirement</span></span> | <span data-ttu-id="94e17-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="94e17-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="94e17-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="94e17-117">Header</span></span><br/> | <dl> <span data-ttu-id="94e17-118"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="94e17-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94e17-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94e17-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94e17-120">Types de bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="94e17-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="94e17-121">**Type de données XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="94e17-121">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="94e17-122">**Type de données XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="94e17-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="94e17-123">**Type de données XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="94e17-123">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="94e17-124">**Type de données XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="94e17-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="94e17-125">**Type de données XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="94e17-125">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> </dl>

 

 




