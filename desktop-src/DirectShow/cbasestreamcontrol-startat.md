---
description: 'La méthode Started indique au code confidentiel quand commencer à transmettre des données. Cette méthode implémente la méthode IAMStreamControl :: startat.'
ms.assetid: fd2943e8-8d35-4122-a99e-96d12459b335
title: CBaseStreamControl. StartAt, méthode (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.StartAt
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7adcf7cbd435992333bb8ae59d5ab1674056223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542216"
---
# <a name="cbasestreamcontrolstartat-method"></a><span data-ttu-id="07540-104">CBaseStreamControl. StartAt, méthode</span><span class="sxs-lookup"><span data-stu-id="07540-104">CBaseStreamControl.StartAt method</span></span>

<span data-ttu-id="07540-105">La `StartAt` méthode informe le code confidentiel quand il faut commencer à transmettre des données.</span><span class="sxs-lookup"><span data-stu-id="07540-105">The `StartAt` method informs the pin when to start delivering data.</span></span> <span data-ttu-id="07540-106">Cette méthode implémente la méthode [**IAMStreamControl :: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .</span><span class="sxs-lookup"><span data-stu-id="07540-106">This method implements the [**IAMStreamControl::StartAt**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="07540-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07540-107">Syntax</span></span>


```C++
HRESULT StartAt(
   const REFERENCE_TIME *ptStart = NULL,
         DWORD          dwCookie = 0
);
```



## <a name="parameters"></a><span data-ttu-id="07540-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07540-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07540-109">*ptStart*</span><span class="sxs-lookup"><span data-stu-id="07540-109">*ptStart*</span></span> 
</dt> <dd>

<span data-ttu-id="07540-110">Pointeur vers une valeur de [**\_ temps de référence**](reference-time.md) qui spécifie quand le code confidentiel doit commencer à transmettre des données.</span><span class="sxs-lookup"><span data-stu-id="07540-110">Pointer to a [**REFERENCE\_TIME**](reference-time.md) value that specifies when the pin should start delivering data.</span></span>

</dd> <dt>

<span data-ttu-id="07540-111">*dwCookie*</span><span class="sxs-lookup"><span data-stu-id="07540-111">*dwCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="07540-112">Spécifie une valeur à envoyer avec la notification de démarrage.</span><span class="sxs-lookup"><span data-stu-id="07540-112">Specifies a value to send along with the start notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07540-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="07540-113">Return value</span></span>

<span data-ttu-id="07540-114">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="07540-114">Returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="07540-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07540-115">Requirements</span></span>



| <span data-ttu-id="07540-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="07540-116">Requirement</span></span> | <span data-ttu-id="07540-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="07540-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07540-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="07540-118">Header</span></span><br/>  | <dl> <span data-ttu-id="07540-119"><dt>Strmctl. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07540-119"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="07540-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="07540-120">Library</span></span><br/> | <dl> <span data-ttu-id="07540-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="07540-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07540-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07540-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07540-123">**CBaseStreamControl, classe**</span><span class="sxs-lookup"><span data-stu-id="07540-123">**CBaseStreamControl Class**</span></span>](cbasestreamcontrol.md)
</dt> </dl>

 

 




