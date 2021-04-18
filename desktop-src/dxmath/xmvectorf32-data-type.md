---
description: Type portable opaque pour prendre en charge l’utilisation de la syntaxe d’initialiseur C/C++ pour charger des valeurs à virgule flottante dans une instance de type XMVECTOR.
ms.assetid: bafaa59f-fd1b-e252-cbbd-903df796fde0
title: Type de données XMVECTORF32 (DirectXMath. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e56e79ea678ede0afcac3523c09da725ede00d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533106"
---
# <a name="xmvectorf32-data-type"></a><span data-ttu-id="349c3-103">Type de données XMVECTORF32</span><span class="sxs-lookup"><span data-stu-id="349c3-103">XMVECTORF32 Data Type</span></span>

<span data-ttu-id="349c3-104">Type portable opaque pour prendre en charge l’utilisation de la syntaxe d’initialiseur C/C++ pour charger des valeurs à virgule flottante dans une instance de type [**XMVECTOR**](xmvector-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="349c3-104">An opaque, portable type to support the use of C/C++ initializer syntax to load floating-point values into an instance of [**XMVECTOR**](xmvector-data-type.md) type.</span></span>


```C++
typedef XMVECTORF32 vectorf32;
```



## <a name="remarks"></a><span data-ttu-id="349c3-105">Notes</span><span class="sxs-lookup"><span data-stu-id="349c3-105">Remarks</span></span>

<span data-ttu-id="349c3-106">Pour obtenir la liste des fonctionnalités supplémentaires, telles que les constructeurs et les opérateurs, disponibles à l’aide `XMVECTORF32` de lors de la programmation en C++, consultez [Extensions XMVECTORF32](ovw-xmvectorf32-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="349c3-106">For a list of additional functionality, such as constructors and operators, available using `XMVECTORF32` when programming in C++, see [XMVECTORF32 Extensions](ovw-xmvectorf32-extensions.md).</span></span>

<span data-ttu-id="349c3-107">Les structures **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md)et [**XMVECTORU8**](xmvectoru8-data-type.md) sont fournies en tant que mécanisme pour créer des [**XMVECTOR**](xmvector-data-type.md) à partir de différents types de données constantes (virgule flottante, entier non signé, entier et octet) à l’aide d’initialiseurs.</span><span class="sxs-lookup"><span data-stu-id="349c3-107">The **XMVECTORF32**, [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORI32**](xmvectori32-data-type.md), and [**XMVECTORU8**](xmvectoru8-data-type.md) structures are provided as a mechanism for creating [**XMVECTOR**](xmvector-data-type.md) from different constant data types (floating point, unsigned integer, integer, and byte) using initializers.</span></span>

<span data-ttu-id="349c3-108">Cela est nécessaire pour prendre en charge [**XMVECTOR**](xmvector-data-type.md), car il ne prend pas en charge les initialiseurs, pour des raisons de portabilité et d’optimisation.</span><span class="sxs-lookup"><span data-stu-id="349c3-108">This is necessary to support [**XMVECTOR**](xmvector-data-type.md), as it does not itself support initializers, for portability and optimization reasons.</span></span>

<span data-ttu-id="349c3-109">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="349c3-109">For example:</span></span>


```
XMVECTOR data;
XMVECTORF32 floatingVector = { 0.f, 0.f, 0.1f, 1.f };
data = floatingVector;
```



<span data-ttu-id="349c3-110">**Espace de noms**: utiliser DirectX</span><span class="sxs-lookup"><span data-stu-id="349c3-110">**Namespace**: Use DirectX</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="349c3-111">Conditions requises par la plateforme</span><span class="sxs-lookup"><span data-stu-id="349c3-111">Platform Requirements</span></span>

<span data-ttu-id="349c3-112">Microsoft Visual Studio 2010 ou Microsoft Visual Studio 2012 avec le SDK Windows pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="349c3-112">Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8.</span></span> <span data-ttu-id="349c3-113">Pris en charge pour les applications de bureau Win32, les applications du Windows Store et les applications Windows Phone 8.</span><span class="sxs-lookup"><span data-stu-id="349c3-113">Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.</span></span>

## <a name="requirements"></a><span data-ttu-id="349c3-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="349c3-114">Requirements</span></span>



| <span data-ttu-id="349c3-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="349c3-115">Requirement</span></span> | <span data-ttu-id="349c3-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="349c3-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="349c3-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="349c3-117">Header</span></span><br/> | <dl> <span data-ttu-id="349c3-118"><dt>DirectXMath. h</dt></span><span class="sxs-lookup"><span data-stu-id="349c3-118"><dt>DirectXMath.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="349c3-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="349c3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="349c3-120">Types de bibliothèque DirectXMath</span><span class="sxs-lookup"><span data-stu-id="349c3-120">DirectXMath Library Types</span></span>](ovw-xnamath-reference-types.md)
</dt> <dt>

[<span data-ttu-id="349c3-121">**Type de données XMVECTORI32**</span><span class="sxs-lookup"><span data-stu-id="349c3-121">**XMVECTORI32 Data Type**</span></span>](xmvectori32-data-type.md)
</dt> <dt>

[<span data-ttu-id="349c3-122">**Type de données XMVECTOR**</span><span class="sxs-lookup"><span data-stu-id="349c3-122">**XMVECTOR Data Type**</span></span>](xmvector-data-type.md)
</dt> <dt>

[<span data-ttu-id="349c3-123">**Type de données XMVECTORU32**</span><span class="sxs-lookup"><span data-stu-id="349c3-123">**XMVECTORU32 Data Type**</span></span>](xmvectoru32-data-type.md)
</dt> <dt>

[<span data-ttu-id="349c3-124">**Type de données XMVECTORU8**</span><span class="sxs-lookup"><span data-stu-id="349c3-124">**XMVECTORU8 Data Type**</span></span>](xmvectoru8-data-type.md)
</dt> <dt>

[<span data-ttu-id="349c3-125">**Type de données XMVECTORF32**</span><span class="sxs-lookup"><span data-stu-id="349c3-125">**XMVECTORF32 Data Type**</span></span>](xmvectorf32-data-type.md)
</dt> </dl>

 

 




