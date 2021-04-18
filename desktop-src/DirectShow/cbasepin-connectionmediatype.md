---
description: 'La méthode ConnectionMediaType récupère le type de média pour la connexion de code confidentiel actuelle, le cas échéant. Cette méthode implémente la méthode IPin :: ConnectionMediaType.'
ms.assetid: 57d100ba-4171-4caa-ab98-66a0a327a53b
title: Méthode CBasePin. ConnectionMediaType (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ConnectionMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62bd211b6c93e44c571d822ccc86104a5a6fdcab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525951"
---
# <a name="cbasepinconnectionmediatype-method"></a><span data-ttu-id="98e47-104">Méthode CBasePin. ConnectionMediaType</span><span class="sxs-lookup"><span data-stu-id="98e47-104">CBasePin.ConnectionMediaType method</span></span>

<span data-ttu-id="98e47-105">La méthode **ConnectionMediaType** récupère le type de média pour la connexion de code confidentiel actuelle, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="98e47-105">The **ConnectionMediaType** method retrieves the media type for the current pin connection, if any.</span></span> <span data-ttu-id="98e47-106">Cette méthode implémente la méthode [**IPIN :: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) .</span><span class="sxs-lookup"><span data-stu-id="98e47-106">This method implements the [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="98e47-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="98e47-107">Syntax</span></span>


```C++
HRESULT ConnectionMediaType(
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a><span data-ttu-id="98e47-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98e47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98e47-109">*crédit*</span><span class="sxs-lookup"><span data-stu-id="98e47-109">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="98e47-110">Pointeur vers une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui reçoit le type de média.</span><span class="sxs-lookup"><span data-stu-id="98e47-110">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that receives the media type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98e47-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="98e47-111">Return value</span></span>

<span data-ttu-id="98e47-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="98e47-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="98e47-113">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="98e47-113">Possible values include those in the following table.</span></span>



| <span data-ttu-id="98e47-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="98e47-114">Return code</span></span>                                                                                           | <span data-ttu-id="98e47-115">Description</span><span class="sxs-lookup"><span data-stu-id="98e47-115">Description</span></span>                           |
|-------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="98e47-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="98e47-116"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="98e47-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="98e47-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="98e47-118"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="98e47-118"><dt>**E\_POINTER**</dt></span></span> </dl>             | <span data-ttu-id="98e47-119">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="98e47-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="98e47-120"><dt>**VFW \_ E \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="98e47-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="98e47-121">Le pin n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="98e47-121">Pin is not connected.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="98e47-122">Notes</span><span class="sxs-lookup"><span data-stu-id="98e47-122">Remarks</span></span>

<span data-ttu-id="98e47-123">Si le code PIN est connecté, cette méthode copie le type de média dans la structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) spécifiée par *VPM*. L’appelant doit libérer le bloc de format du type de média.</span><span class="sxs-lookup"><span data-stu-id="98e47-123">If the pin is connected, this method copies the media type into the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure specified by *pmt*. The caller must free the media type's format block.</span></span> <span data-ttu-id="98e47-124">Vous pouvez utiliser la fonction [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ou la fonction d’assistance [**FreeMediaType**](freemediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="98e47-124">You can use the [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) function, or the [**FreeMediaType**](freemediatype.md) helper function.</span></span>

<span data-ttu-id="98e47-125">Si le code pin n’est pas connecté, cette méthode zéro le bloc de mémoire spécifié par *VPM* et retourne un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="98e47-125">If the pin is not connected, this method zeroes the memory block specified by *pmt* and returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="98e47-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="98e47-126">Requirements</span></span>



| <span data-ttu-id="98e47-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="98e47-127">Requirement</span></span> | <span data-ttu-id="98e47-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="98e47-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98e47-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="98e47-129">Header</span></span><br/>  | <dl> <span data-ttu-id="98e47-130"><dt>Amfilter. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98e47-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="98e47-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="98e47-131">Library</span></span><br/> | <dl> <span data-ttu-id="98e47-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="98e47-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98e47-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="98e47-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98e47-134">**CBasePin, classe**</span><span class="sxs-lookup"><span data-stu-id="98e47-134">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

