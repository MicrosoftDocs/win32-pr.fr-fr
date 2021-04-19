---
description: Obsolète. Utilisez AMovieSetupRegisterFilter2 à la place.
ms.assetid: 42278829-d09e-46c7-8f1a-fa4572f7cc00
title: AMovieSetupRegisterFilter, fonction (DLLSETUP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AMovieSetupRegisterFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 398d2d727e26feaca23d6bddbdcbc8a578d096eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528804"
---
# <a name="amoviesetupregisterfilter-function"></a><span data-ttu-id="a113a-104">AMovieSetupRegisterFilter fonction)</span><span class="sxs-lookup"><span data-stu-id="a113a-104">AMovieSetupRegisterFilter function</span></span>

<span data-ttu-id="a113a-105">Obsolète.</span><span class="sxs-lookup"><span data-stu-id="a113a-105">Obsolete.</span></span> <span data-ttu-id="a113a-106">Utilisez [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="a113a-106">Use [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="a113a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a113a-107">Syntax</span></span>


```C++
HRESULT AMovieSetupRegisterFilter(
   const AMOVIESETUP_FILTER const * psetupdata,
         IFilterMapper              *pIFM,
         BOOL                       bRegister
);
```



## <a name="parameters"></a><span data-ttu-id="a113a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a113a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a113a-109">*psetupdata*</span><span class="sxs-lookup"><span data-stu-id="a113a-109">*psetupdata*</span></span> 
</dt> <dd>

<span data-ttu-id="a113a-110">Réservé.</span><span class="sxs-lookup"><span data-stu-id="a113a-110">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a113a-111">*pIFM*</span><span class="sxs-lookup"><span data-stu-id="a113a-111">*pIFM*</span></span> 
</dt> <dd>

<span data-ttu-id="a113a-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="a113a-112">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="a113a-113">*bRegister*</span><span class="sxs-lookup"><span data-stu-id="a113a-113">*bRegister*</span></span> 
</dt> <dd>

<span data-ttu-id="a113a-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="a113a-114">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a113a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a113a-115">Return value</span></span>

<span data-ttu-id="a113a-116">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a113a-116">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a113a-117">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a113a-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a113a-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a113a-118">Requirements</span></span>



| <span data-ttu-id="a113a-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a113a-119">Requirement</span></span> | <span data-ttu-id="a113a-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="a113a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a113a-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a113a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a113a-122"><dt>DLLSETUP. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a113a-122"><dt>Dllsetup.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a113a-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a113a-123">Library</span></span><br/> | <dl> <span data-ttu-id="a113a-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="a113a-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a113a-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a113a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a113a-126">**Fonctions de configuration des DLL**</span><span class="sxs-lookup"><span data-stu-id="a113a-126">**DLL Setup Functions**</span></span>](dll-setup-functions.md)
</dt> </dl>

 

 




