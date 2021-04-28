---
description: Méthode constructeur CSeekingPassThru. CSeekingPassThru.
ms.assetid: e31253fc-b365-4414-9dee-906d4c41d16e
title: Constructeur CSeekingPassThru. CSeekingPassThru (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cab9d6329f5175c96a3bfc5962ca5a555fe62b5d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085377"
---
# <a name="cseekingpassthrucseekingpassthru-constructor"></a><span data-ttu-id="ccfac-103">Constructeur CSeekingPassThru. CSeekingPassThru</span><span class="sxs-lookup"><span data-stu-id="ccfac-103">CSeekingPassThru.CSeekingPassThru constructor</span></span>

<span data-ttu-id="ccfac-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="ccfac-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccfac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ccfac-105">Syntax</span></span>


```C++
CSeekingPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="ccfac-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ccfac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccfac-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="ccfac-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="ccfac-108">Chaîne contenant le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ccfac-108">String containing the name of the object.</span></span> <span data-ttu-id="ccfac-109">Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md) .</span><span class="sxs-lookup"><span data-stu-id="ccfac-109">See [**CBaseObject**](cbaseobject.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="ccfac-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="ccfac-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="ccfac-111">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="ccfac-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="ccfac-112">Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="ccfac-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="ccfac-113">Sinon, affectez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="ccfac-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ccfac-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="ccfac-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="ccfac-115">Pointeur vers une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ccfac-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="ccfac-116">Ignoré.</span><span class="sxs-lookup"><span data-stu-id="ccfac-116">Ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ccfac-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ccfac-117">Requirements</span></span>



| <span data-ttu-id="ccfac-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ccfac-118">Requirement</span></span> | <span data-ttu-id="ccfac-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ccfac-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccfac-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="ccfac-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ccfac-121"><dt>Seekpt. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ccfac-121"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="ccfac-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ccfac-122">Library</span></span><br/> | <dl> <span data-ttu-id="ccfac-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ccfac-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccfac-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccfac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccfac-125">**CSeekingPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="ccfac-125">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




