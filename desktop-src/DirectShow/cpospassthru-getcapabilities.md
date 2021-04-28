---
description: 'Méthode CPosPassThru. GetCapabilities : la méthode GetCapabilities récupère toutes les fonctionnalités de recherche du flux. Cette méthode implémente la méthode IMediaSeeking :: GetCapabilities.'
ms.assetid: c60c4f47-48de-47d0-9b87-589b84df842c
title: Méthode CPosPassThru. GetCapabilities (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetCapabilities
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c21838d3df72d52255d0a2e35dd0b7d34ef55411
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085567"
---
# <a name="cpospassthrugetcapabilities-method"></a><span data-ttu-id="dd896-104">Méthode CPosPassThru. GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="dd896-104">CPosPassThru.GetCapabilities method</span></span>

<span data-ttu-id="dd896-105">La méthode **GetCapabilities** récupère toutes les fonctionnalités de recherche du flux.</span><span class="sxs-lookup"><span data-stu-id="dd896-105">The **GetCapabilities** method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="dd896-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="dd896-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd896-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd896-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="dd896-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd896-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd896-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="dd896-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="dd896-110">Pointeur vers une variable qui reçoit une combinaison d’opérations de bits des indicateurs de [**\_ \_ \_ fonctionnalités de recherche de AM**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="dd896-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd896-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dd896-111">Return value</span></span>

<span data-ttu-id="dd896-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="dd896-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd896-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd896-113">Requirements</span></span>



| <span data-ttu-id="dd896-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd896-114">Requirement</span></span> | <span data-ttu-id="dd896-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd896-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd896-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd896-116">Header</span></span><br/>  | <dl> <span data-ttu-id="dd896-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dd896-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dd896-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dd896-118">Library</span></span><br/> | <dl> <span data-ttu-id="dd896-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="dd896-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd896-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd896-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd896-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="dd896-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




