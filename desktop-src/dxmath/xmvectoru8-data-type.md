---
description: Type portable opaque pour prendre en charge l’utilisation de la syntaxe d’initialiseur C/C++ pour charger les valeurs de UInt8 \_ t dans une instance de type XMVECTOR.
ms.assetid: ab73ac2c-f178-1bb9-910d-9eef5fc6f5df
title: Type de données XMVECTORU8 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4428cdd78206bfa17c295a9578653bb0a66f0c6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523023"
---
# <a name="xmvectoru8-data-type"></a><span data-ttu-id="e945a-103">Type de données XMVECTORU8</span><span class="sxs-lookup"><span data-stu-id="e945a-103">XMVECTORU8 Data Type</span></span>

<span data-ttu-id="e945a-104">Type portable opaque pour prendre en charge l’utilisation de la syntaxe d’initialiseur C/C++ pour charger les valeurs de UInt8 \_ t dans une instance de type [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="e945a-104">An opaque, portable type to support the use of C/C++ initializer syntax to load uint8\_t values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORU8 vectoru8;
```



## <a name="remarks"></a><span data-ttu-id="e945a-105">Notes</span><span class="sxs-lookup"><span data-stu-id="e945a-105">Remarks</span></span>

<span data-ttu-id="e945a-106">Pour obtenir la liste des fonctionnalités supplémentaires, telles que les constructeurs et les opérateurs, disponibles à l’aide de XMVECTORU8 lors de la programmation en C++, consultez [Extensions XMVECTORU8](ovw-xmvectoru8-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="e945a-106">For a list of additional functionality, such as constructors and operators, available using XMVECTORU8 when programming in C++, see [XMVECTORU8 Extensions](ovw-xmvectoru8-extensions.md).</span></span>

<span data-ttu-id="e945a-107">Les structures [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)et **XMVECTORU8** sont fournies en tant que mécanisme pour créer des [**XMVECTOR**](xmvector-data-type.md) à partir de différents types de données constantes (virgule flottante, entier non signé, entier et octet) à l’aide d’initialiseurs.</span><span class="sxs-lookup"><span data-stu-id="e945a-107">The [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md), and **XMVECTORU8** structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="e945a-108">Cela est nécessaire pour prendre en charge [**XMVECTOR**](xmvector-data-type.md), car il ne prend pas en charge les initialiseurs, pour des raisons de portabilité et d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="e945a-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="e945a-109">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="e945a-109">For example:</span></span>

``` syntax
XMVECTOR data;
XMVECTORU8  byteVector = { (uint8_t)  1,(uint8_t) 16,(uint8_t)101,(uint8_t) 62,
                           (uint8_t)  4,(uint8_t)  0,(uint8_t)  2,(uint8_t) 99,
                           (uint8_t)  9,(uint8_t) 18,(uint8_t)  0,(uint8_t)  0,
                           (uint8_t)100,(uint8_t) 51,(uint8_t) 23,(uint8_t)117};

data = floatingVector;
```

<span data-ttu-id="e945a-110">**Espace de noms**: utiliser DirectX</span><span class="sxs-lookup"><span data-stu-id="e945a-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="e945a-111">Conditions requises par la plateforme</span><span class="sxs-lookup"><span data-stu-id="e945a-111">Platform Requirements</span></span>

<span data-ttu-id="e945a-112">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e945a-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="e945a-113">Pris en charge pour les applications de bureau Win32, les applications du Windows Store et les applications Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="e945a-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="e945a-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e945a-114">Requirements</span></span>



| <span data-ttu-id="e945a-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e945a-115">Requirement</span></span> | <span data-ttu-id="e945a-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e945a-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e945a-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="e945a-117">Header</span></span><br/> | <dl> <span data-ttu-id="e945a-118"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="e945a-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e945a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e945a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e945a-120">Types de bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="e945a-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="e945a-121">**Type de données XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="e945a-121">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="e945a-122">**Type de données XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="e945a-122">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> <dt>

[<span data-ttu-id="e945a-123">**Type de données XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="e945a-123">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="e945a-124">**Type de données XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="e945a-124">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="e945a-125">Extensions XMVECTORU8</span><span class="sxs-lookup"><span data-stu-id="e945a-125">XMVECTORU8 Extensions</span></span>](ovw-xmvectoru8-extensions.md)
</dt> </dl>

 

 




