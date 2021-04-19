---
description: L’opérateur + = ajoute deux heures de référence.
ms.assetid: 016d3dac-4d7c-490a-83aa-1d88a2080748
title: CRefTime. Operator + =, méthode (reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b5e0d9a5a16a963b67643823e5e3b547a1076fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542620"
---
# <a name="creftimeoperator-method"></a><span data-ttu-id="115c4-103">CRefTime. Operator + =, méthode</span><span class="sxs-lookup"><span data-stu-id="115c4-103">CRefTime.operator+= method</span></span>

<span data-ttu-id="115c4-104">L’opérateur + = ajoute deux heures de référence.</span><span class="sxs-lookup"><span data-stu-id="115c4-104">The += operator adds two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="115c4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="115c4-105">Syntax</span></span>


```C++
CRefTime& operator+=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="115c4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="115c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="115c4-107">*RT* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="115c4-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="115c4-108">Référence à un objet **CRefTime** .</span><span class="sxs-lookup"><span data-stu-id="115c4-108">Reference to a **CRefTime** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="115c4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="115c4-109">Return value</span></span>

<span data-ttu-id="115c4-110">Retourne une référence à l’objet.</span><span class="sxs-lookup"><span data-stu-id="115c4-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="115c4-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="115c4-111">Requirements</span></span>



| <span data-ttu-id="115c4-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="115c4-112">Requirement</span></span> | <span data-ttu-id="115c4-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="115c4-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="115c4-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="115c4-114">Header</span></span><br/>  | <dl> <span data-ttu-id="115c4-115"><dt>Reftime. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="115c4-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="115c4-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="115c4-116">Library</span></span><br/> | <dl> <span data-ttu-id="115c4-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="115c4-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




