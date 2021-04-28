---
description: 'Méthode CSourceSeeking. GetCapabilities : la méthode GetCapabilities récupère toutes les fonctionnalités de recherche du flux. Cette méthode implémente la méthode IMediaSeeking :: GetCapabilities.'
ms.assetid: a2ff7ea2-09bd-49a7-8e1b-d6360939036e
title: Méthode CSourceSeeking. GetCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f1f354381c4c99cf880c75cbbc4b13355e386030
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098777"
---
# <a name="csourceseekinggetcapabilities-method"></a><span data-ttu-id="b8975-104">Méthode CSourceSeeking. GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="b8975-104">CSourceSeeking.GetCapabilities method</span></span>

<span data-ttu-id="b8975-105">La `GetCapabilities` méthode récupère toutes les fonctionnalités de recherche du flux.</span><span class="sxs-lookup"><span data-stu-id="b8975-105">The `GetCapabilities` method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="b8975-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="b8975-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8975-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8975-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="b8975-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8975-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8975-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="b8975-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="b8975-110">Pointeur vers une variable qui reçoit une combinaison d’opérations de bits des indicateurs de [**\_ \_ \_ fonctionnalités de recherche de AM**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="b8975-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8975-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b8975-111">Return value</span></span>

<span data-ttu-id="b8975-112">Retourne l’une des valeurs **HRESULT** listées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b8975-112">Returns one of the **HRESULT** values listed in the following table.</span></span>



| <span data-ttu-id="b8975-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b8975-113">Return code</span></span>                                                                               | <span data-ttu-id="b8975-114">Description</span><span class="sxs-lookup"><span data-stu-id="b8975-114">Description</span></span>                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <span data-ttu-id="b8975-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b8975-115"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="b8975-116">Opération réussie</span><span class="sxs-lookup"><span data-stu-id="b8975-116">Success</span></span><br/>                |
| <dl> <span data-ttu-id="b8975-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="b8975-117"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="b8975-118">Valeur de pointeur **null**</span><span class="sxs-lookup"><span data-stu-id="b8975-118">**NULL** pointer value</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b8975-119">Notes </span><span class="sxs-lookup"><span data-stu-id="b8975-119">Remarks</span></span>

<span data-ttu-id="b8975-120">Les fonctionnalités de recherche sont spécifiées par la variable membre [**CSourceSeeking :: m \_ dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="b8975-120">The seeking capabilities are specified by the [**CSourceSeeking::m\_dwSeekingCaps**](csourceseeking-m-dwseekingcaps.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8975-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8975-121">Requirements</span></span>



| <span data-ttu-id="b8975-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8975-122">Requirement</span></span> | <span data-ttu-id="b8975-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8975-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8975-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b8975-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b8975-125"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8975-125"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b8975-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b8975-126">Library</span></span><br/> | <dl> <span data-ttu-id="b8975-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="b8975-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8975-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8975-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8975-129">**CSourceSeeking, classe**</span><span class="sxs-lookup"><span data-stu-id="b8975-129">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




