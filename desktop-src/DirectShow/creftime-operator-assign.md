---
description: L’opérateur = assigne une nouvelle heure de référence.
ms.assetid: 0b11e2ea-23dc-4c75-88c6-94215a4b14b6
title: CRefTime. Operator =, méthode (reftime. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b87e6517946c64cb2a60e95912aba423a1880215
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540014"
---
# <a name="creftimeoperator-method-reftimeh"></a><span data-ttu-id="7de06-103">CRefTime. Operator =, méthode (reftime. h)</span><span class="sxs-lookup"><span data-stu-id="7de06-103">CRefTime.operator= method (Reftime.h)</span></span>

<span data-ttu-id="7de06-104">L’opérateur = assigne une nouvelle heure de référence.</span><span class="sxs-lookup"><span data-stu-id="7de06-104">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="7de06-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7de06-105">Syntax</span></span>


```C++
CRefTime& operator=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="7de06-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7de06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7de06-107">*RT* \[ Réf\]</span><span class="sxs-lookup"><span data-stu-id="7de06-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="7de06-108">Référence à un objet **CRefTime** qui spécifie la nouvelle heure de référence.</span><span class="sxs-lookup"><span data-stu-id="7de06-108">Reference to a **CRefTime** object that specifies the new reference time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7de06-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7de06-109">Return value</span></span>

<span data-ttu-id="7de06-110">Retourne une référence à l’objet.</span><span class="sxs-lookup"><span data-stu-id="7de06-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="7de06-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7de06-111">Requirements</span></span>



| <span data-ttu-id="7de06-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7de06-112">Requirement</span></span> | <span data-ttu-id="7de06-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="7de06-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7de06-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="7de06-114">Header</span></span><br/>  | <dl> <span data-ttu-id="7de06-115"><dt>Reftime. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7de06-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7de06-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7de06-116">Library</span></span><br/> | <dl> <span data-ttu-id="7de06-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="7de06-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




