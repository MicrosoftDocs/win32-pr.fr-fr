---
description: Méthode constructeur CBaseControlVideo. CBaseControlVideo.
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: Constructeur CBaseControlVideo. CBaseControlVideo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CBaseControlVideo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 389c05b5254326d2966799b857107e79792610e9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096347"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a><span data-ttu-id="3cd5b-103">Constructeur CBaseControlVideo. CBaseControlVideo</span><span class="sxs-lookup"><span data-stu-id="3cd5b-103">CBaseControlVideo.CBaseControlVideo constructor</span></span>

<span data-ttu-id="3cd5b-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cd5b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3cd5b-105">Syntax</span></span>


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="3cd5b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3cd5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cd5b-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="3cd5b-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="3cd5b-108">Pointeur vers l’objet de filtre de média propriétaire.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="3cd5b-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="3cd5b-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="3cd5b-110">Pointeur vers la section critique à utiliser pour le verrouillage.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="3cd5b-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="3cd5b-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="3cd5b-112">Pointeur vers la description de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="3cd5b-113">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="3cd5b-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="3cd5b-114">Pointeur vers l’interface de contrôle **IUnknown** , si l’objet fait partie d’un agrégat ; dans le cas contraire, doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3cd5b-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="3cd5b-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="3cd5b-116">Pointeur vers une variable qui reçoit une valeur HRESULT indiquant la réussite ou l’échec de la méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3cd5b-117">Notes </span><span class="sxs-lookup"><span data-stu-id="3cd5b-117">Remarks</span></span>

<span data-ttu-id="3cd5b-118">L’objet implémente l’interface de contrôle [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .</span><span class="sxs-lookup"><span data-stu-id="3cd5b-118">The object implements the [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) control interface.</span></span>

<span data-ttu-id="3cd5b-119">Toutes les méthodes d’interface de [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) implémentées par cette classe requièrent que le filtre soit correctement connecté.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-119">All the interface methods from [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) that this class implements require that the filter be connected correctly.</span></span> <span data-ttu-id="3cd5b-120">Pour cette raison, la classe reçoit un code confidentiel avec lequel elle doit se synchroniser.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-120">For this reason, the class is passed a pin with which it should synchronize with.</span></span> <span data-ttu-id="3cd5b-121">Chaque fois qu’une méthode d’interface est appelée, l’objet détermine que le pin est toujours connecté.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-121">Whenever an interface method is called, the object determines that the pin is still connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cd5b-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3cd5b-122">Requirements</span></span>



| <span data-ttu-id="3cd5b-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3cd5b-123">Requirement</span></span> | <span data-ttu-id="3cd5b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="3cd5b-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cd5b-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="3cd5b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3cd5b-126"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3cd5b-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3cd5b-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3cd5b-127">Library</span></span><br/> | <dl> <span data-ttu-id="3cd5b-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3cd5b-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cd5b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3cd5b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cd5b-130">**CBaseControlVideo, classe**</span><span class="sxs-lookup"><span data-stu-id="3cd5b-130">**CBaseControlVideo Class**</span></span>](cbasecontrolvideo.md)
</dt> </dl>

 

 




