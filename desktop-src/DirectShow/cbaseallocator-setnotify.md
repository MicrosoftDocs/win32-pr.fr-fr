---
description: 'La méthode SetNotify définit ou supprime un rappel sur l’allocateur. L’allocateur appelle la méthode de rappel chaque fois que la méthode IMemAllocator :: ReleaseBuffer de l’allocateur est appelée.'
ms.assetid: ef9a6c66-d392-4130-b4fc-9eb6aecb6cbf
title: Méthode CBaseAllocator. SetNotify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetNotify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8269112325d470cae59cff6e615f04fbdfab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528965"
---
# <a name="cbaseallocatorsetnotify-method"></a><span data-ttu-id="c0e6c-104">Méthode CBaseAllocator. SetNotify</span><span class="sxs-lookup"><span data-stu-id="c0e6c-104">CBaseAllocator.SetNotify method</span></span>

<span data-ttu-id="c0e6c-105">\[Les [**SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) peuvent être modifiés ou non disponibles dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="c0e6c-105">\[[**SetNotify**](/previous-versions/windows/desktop/api/Dshowasf/nf-dshowasf-iamwmbufferpass-setnotify) may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="c0e6c-106">La `SetNotify` méthode définit ou supprime un rappel sur l’allocateur.</span><span class="sxs-lookup"><span data-stu-id="c0e6c-106">The `SetNotify` method sets or removes a callback on the allocator.</span></span> <span data-ttu-id="c0e6c-107">L’allocateur appelle la méthode de rappel chaque fois que la méthode [**IMemAllocator :: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) de l’allocateur est appelée.</span><span class="sxs-lookup"><span data-stu-id="c0e6c-107">The allocator calls the callback method whenever the allocator's [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0e6c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0e6c-108">Syntax</span></span>


```C++
HRESULT SetNotify(
   IMemAllocatorNotifyCallbackTemp *pNotify
);
```



## <a name="parameters"></a><span data-ttu-id="c0e6c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0e6c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0e6c-110">*pNotify*</span><span class="sxs-lookup"><span data-stu-id="c0e6c-110">*pNotify*</span></span> 
</dt> <dd>

<span data-ttu-id="c0e6c-111">Pointeur vers l’interface [**IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) qui sera utilisée pour le rappel.</span><span class="sxs-lookup"><span data-stu-id="c0e6c-111">Pointer to the [**IMemAllocatorNotifyCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatornotifycallbacktemp) interface that will be used for the callback.</span></span> <span data-ttu-id="c0e6c-112">L’appelant doit implémenter l’interface.</span><span class="sxs-lookup"><span data-stu-id="c0e6c-112">The caller must implement the interface.</span></span> <span data-ttu-id="c0e6c-113">Utilisez la valeur **null** pour supprimer le rappel.</span><span class="sxs-lookup"><span data-stu-id="c0e6c-113">Use the value **NULL** to remove the callback.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0e6c-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c0e6c-114">Return value</span></span>

<span data-ttu-id="c0e6c-115">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c0e6c-115">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0e6c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c0e6c-116">Remarks</span></span>

<span data-ttu-id="c0e6c-117">Cette méthode implémente la méthode [**IMemAllocatorCallbackTemp :: SetNotify**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) .</span><span class="sxs-lookup"><span data-stu-id="c0e6c-117">This method implements the [**IMemAllocatorCallbackTemp::SetNotify**](/windows/desktop/api/Strmif/nf-strmif-imemallocatorcallbacktemp-setnotify) method.</span></span> <span data-ttu-id="c0e6c-118">L’Allocator n’expose pas l’interface [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) , sauf si l’indicateur *fEnableReleaseCallback* a la valeur **true** dans le constructeur [**CBaseAllocator**](cbaseallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="c0e6c-118">The allocator does not expose the [**IMemAllocatorCallbackTemp**](/windows/desktop/api/Strmif/nn-strmif-imemallocatorcallbacktemp) interface unless the *fEnableReleaseCallback* flag is set to **TRUE** in the [**CBaseAllocator**](cbaseallocator.md) constructor.</span></span>

<span data-ttu-id="c0e6c-119">Cette méthode définit la variable de membre [**CBaseAllocator :: m \_ pNotify**](cbaseallocator-m-pnotify.md) sur la valeur *pNotify* et incrémente le décompte de références sur l’interface.</span><span class="sxs-lookup"><span data-stu-id="c0e6c-119">This method sets the [**CBaseAllocator::m\_pNotify**](cbaseallocator-m-pnotify.md) member variable equal to *pNotify* and increments the reference count on the interface.</span></span> <span data-ttu-id="c0e6c-120">Si *m \_ pNotify* n’est pas **null**, la méthode **ReleaseBuffer** de l’allocateur appelle [**IMemAllocatorNotifyCallbackTemp :: NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease).</span><span class="sxs-lookup"><span data-stu-id="c0e6c-120">If *m\_pNotify* is non-**NULL**, the allocator's **ReleaseBuffer** method calls [**IMemAllocatorNotifyCallbackTemp::NotifyRelease**](/windows/desktop/api/Strmif/nf-strmif-imemallocatornotifycallbacktemp-notifyrelease).</span></span> <span data-ttu-id="c0e6c-121">Consultez la section Notes dans cette méthode pour plus d’informations sur l’implémentation du rappel.</span><span class="sxs-lookup"><span data-stu-id="c0e6c-121">See the Remarks section in that method for information about implementing the callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0e6c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0e6c-122">Requirements</span></span>



| <span data-ttu-id="c0e6c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0e6c-123">Requirement</span></span> | <span data-ttu-id="c0e6c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0e6c-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0e6c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0e6c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c0e6c-126"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0e6c-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c0e6c-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c0e6c-127">Library</span></span><br/> | <dl> <span data-ttu-id="c0e6c-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c0e6c-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0e6c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0e6c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0e6c-130">**CBaseAllocator, classe**</span><span class="sxs-lookup"><span data-stu-id="c0e6c-130">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




