---
description: 'La méthode GetCapabilities récupère toutes les fonctionnalités de recherche du flux. Cette méthode implémente la méthode IMediaSeeking :: GetCapabilities.'
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
ms.openlocfilehash: f896adbc1015cb34e6f9063cb5ebf73e5cdb441c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530509"
---
# <a name="cpospassthrugetcapabilities-method"></a><span data-ttu-id="1c48e-104">Méthode CPosPassThru. GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="1c48e-104">CPosPassThru.GetCapabilities method</span></span>

<span data-ttu-id="1c48e-105">La méthode **GetCapabilities** récupère toutes les fonctionnalités de recherche du flux.</span><span class="sxs-lookup"><span data-stu-id="1c48e-105">The **GetCapabilities** method retrieves all the seeking capabilities of the stream.</span></span> <span data-ttu-id="1c48e-106">Cette méthode implémente la méthode [**IMediaSeeking :: GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="1c48e-106">This method implements the [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c48e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c48e-107">Syntax</span></span>


```C++
HRESULT GetCapabilities(
   DWORD *pCapabilities
);
```



## <a name="parameters"></a><span data-ttu-id="1c48e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c48e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c48e-109">*pCapabilities*</span><span class="sxs-lookup"><span data-stu-id="1c48e-109">*pCapabilities*</span></span> 
</dt> <dd>

<span data-ttu-id="1c48e-110">Pointeur vers une variable qui reçoit une combinaison d’opérations de bits des indicateurs de [**\_ \_ \_ fonctionnalités de recherche de AM**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) .</span><span class="sxs-lookup"><span data-stu-id="1c48e-110">Pointer to a variable that receives a bitwise combination of [**AM\_SEEKING\_SEEKING\_CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities) flags.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c48e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c48e-111">Return value</span></span>

<span data-ttu-id="1c48e-112">Retourne la valeur **HRESULT** de la broche connectée.</span><span class="sxs-lookup"><span data-stu-id="1c48e-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c48e-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c48e-113">Requirements</span></span>



| <span data-ttu-id="1c48e-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c48e-114">Requirement</span></span> | <span data-ttu-id="1c48e-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c48e-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c48e-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="1c48e-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1c48e-117"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1c48e-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1c48e-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1c48e-118">Library</span></span><br/> | <dl> <span data-ttu-id="1c48e-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1c48e-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c48e-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c48e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c48e-121">**CPosPassThru, classe**</span><span class="sxs-lookup"><span data-stu-id="1c48e-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




