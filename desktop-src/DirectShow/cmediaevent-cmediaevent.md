---
description: Méthode constructeur CMediaEvent. CMediaEvent.
ms.assetid: 7f7a0a9f-e531-4e22-8601-b84ab088e9e7
title: Constructeur CMediaEvent. CMediaEvent (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaEvent.CMediaEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36cd82b086241012542701001c4de1fe16ac2d8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095557"
---
# <a name="cmediaeventcmediaevent-constructor"></a><span data-ttu-id="f5a6e-103">Constructeur CMediaEvent. CMediaEvent</span><span class="sxs-lookup"><span data-stu-id="f5a6e-103">CMediaEvent.CMediaEvent constructor</span></span>

<span data-ttu-id="f5a6e-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="f5a6e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a6e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f5a6e-105">Syntax</span></span>


```C++
CMediaEvent(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a><span data-ttu-id="f5a6e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5a6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5a6e-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="f5a6e-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="f5a6e-108">Pointeur vers le nom de l’objet à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="f5a6e-108">Pointer to the name of the object for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="f5a6e-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="f5a6e-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="f5a6e-110">Pointeur vers le propriétaire de cet objet.</span><span class="sxs-lookup"><span data-stu-id="f5a6e-110">Pointer to the owner of this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5a6e-111">Notes </span><span class="sxs-lookup"><span data-stu-id="f5a6e-111">Remarks</span></span>

<span data-ttu-id="f5a6e-112">Allouez le paramètre *pname* dans la mémoire statique.</span><span class="sxs-lookup"><span data-stu-id="f5a6e-112">Allocate the *pName* parameter in static memory.</span></span> <span data-ttu-id="f5a6e-113">Ce nom apparaît sur le terminal de débogage lors de la création et de la suppression de l’objet.</span><span class="sxs-lookup"><span data-stu-id="f5a6e-113">This name appears on the debugging terminal upon creation and deletion of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5a6e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f5a6e-114">Requirements</span></span>



| <span data-ttu-id="f5a6e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f5a6e-115">Requirement</span></span> | <span data-ttu-id="f5a6e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="f5a6e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a6e-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="f5a6e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="f5a6e-118"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5a6e-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f5a6e-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f5a6e-119">Library</span></span><br/> | <dl> <span data-ttu-id="f5a6e-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="f5a6e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5a6e-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5a6e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a6e-122">**CMediaEvent, classe**</span><span class="sxs-lookup"><span data-stu-id="f5a6e-122">**CMediaEvent Class**</span></span>](cmediaevent.md)
</dt> </dl>

 

 




