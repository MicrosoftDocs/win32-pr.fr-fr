---
description: Type portable opaque pour prendre en charge l’utilisation de la syntaxe d’initialiseur C/C++ pour charger les \_ valeurs UInt32 t dans une instance de type XMVECTOR.
ms.assetid: 1ac1f48a-cd7f-7741-933f-c341fc42a21c
title: Type de données XMVECTORU32 (Directxmath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c7a64d42bc4638573b987642c0cd77c37cc12d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542406"
---
# <a name="xmvectoru32-data-type"></a><span data-ttu-id="ae82d-103">Type de données XMVECTORU32</span><span class="sxs-lookup"><span data-stu-id="ae82d-103">XMVECTORU32 Data Type</span></span>

<span data-ttu-id="ae82d-104">Type portable opaque pour prendre en charge l’utilisation de la syntaxe d’initialiseur C/C++ pour charger les \_ valeurs UInt32 t dans une instance de type [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="ae82d-104">An opaque, portable type to support the use of C/C++ initializer syntax to load uint32\_t values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTOR32 vectoru32;
```



## <a name="remarks"></a><span data-ttu-id="ae82d-105">Notes</span><span class="sxs-lookup"><span data-stu-id="ae82d-105">Remarks</span></span>

<span data-ttu-id="ae82d-106">Pour obtenir la liste des fonctionnalités supplémentaires, telles que les constructeurs et les opérateurs, disponibles à l’aide de XMVECTORU32 lors de la programmation en C++, consultez [Extensions XMVECTORU32](ovw-xmvectoru32-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="ae82d-106">For a list of additional functionality, such as constructors and operators, available using XMVECTORU32 when programming in C++, see [XMVECTORU32 Extensions](ovw-xmvectoru32-extensions.md).</span></span>

<span data-ttu-id="ae82d-107">Les structures [**XMVECTORF32**](xmvectorf32-data-type.md), **XMVECTORU32**, [**XMVECTORI32**](xmvectori32-data-type.md)et [**XMVECTORU8**](xmvectoru8-data-type.md) sont fournies en tant que mécanisme pour créer des [**XMVECTOR**](xmvector-data-type.md) à partir de différents types de données constantes (virgule flottante, entier non signé, entier et octet) à l’aide d’initialiseurs.</span><span class="sxs-lookup"><span data-stu-id="ae82d-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), **XMVECTORU32**, [**XMVECTORI32**](xmvectori32-data-type.md), and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="ae82d-108">Cela est nécessaire pour prendre en charge [**XMVECTOR**](xmvector-data-type.md), car il ne prend pas en charge les initialiseurs, pour des raisons de portabilité et d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="ae82d-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="ae82d-109">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="ae82d-109">For example:</span></span>

``` syntax
XMVECTOR data;
XMVECTORU32 uintVector = { 0xf7000000, 0x8310000, 0x1000000, 0 };
data = uintVector;
```

<span data-ttu-id="ae82d-110">**Espace de noms**: utiliser DirectX</span><span class="sxs-lookup"><span data-stu-id="ae82d-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="ae82d-111">Conditions requises par la plateforme</span><span class="sxs-lookup"><span data-stu-id="ae82d-111">Platform Requirements</span></span>

<span data-ttu-id="ae82d-112">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ae82d-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="ae82d-113">Pris en charge pour les applications de bureau Win32, les applications du Windows Store et les applications Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="ae82d-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae82d-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae82d-114">Requirements</span></span>



| <span data-ttu-id="ae82d-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae82d-115">Requirement</span></span> | <span data-ttu-id="ae82d-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae82d-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae82d-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae82d-117">Header</span></span><br/> | <dl> <span data-ttu-id="ae82d-118"><dt>Directxmath. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae82d-118"><dt>Directxmath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae82d-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae82d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae82d-120">Types de bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="ae82d-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="ae82d-121">**Type de données XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="ae82d-121">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="ae82d-122">**Type de données XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="ae82d-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="ae82d-123">**Type de données XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="ae82d-123">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="ae82d-124">**Type de données XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="ae82d-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="ae82d-125">Extensions XMVECTORU32</span><span class="sxs-lookup"><span data-stu-id="ae82d-125">XMVECTORU32 Extensions</span></span>](ovw-xmvectoru32-extensions.md)
</dt> </dl>

 

 




