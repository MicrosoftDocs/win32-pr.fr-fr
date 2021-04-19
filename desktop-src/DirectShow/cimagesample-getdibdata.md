---
description: La méthode GetDIBData récupère des informations sur la bitmap indépendante du périphérique (DIB) GDI que cet objet gère.
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: Méthode CImageSample. GetDIBData (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.GetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd198152e7c0042a6d48cf942a48745540960d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535868"
---
# <a name="cimagesamplegetdibdata-method"></a><span data-ttu-id="03768-103">Méthode CImageSample. GetDIBData</span><span class="sxs-lookup"><span data-stu-id="03768-103">CImageSample.GetDIBData method</span></span>

<span data-ttu-id="03768-104">La `GetDIBData` méthode récupère des informations sur la bitmap indépendante du périphérique (DIB) GDI que cet objet gère.</span><span class="sxs-lookup"><span data-stu-id="03768-104">The `GetDIBData` method retrieves information about the GDI device-independent bitmap (DIB) that this object is managing.</span></span>

## <a name="syntax"></a><span data-ttu-id="03768-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="03768-105">Syntax</span></span>


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a><span data-ttu-id="03768-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03768-106">Parameters</span></span>

<span data-ttu-id="03768-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="03768-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03768-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="03768-108">Return value</span></span>

<span data-ttu-id="03768-109">Retourne un pointeur vers une structure [**DIBDATA**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="03768-109">Returns a pointer to a [**DIBDATA**](dibdata.md) structure.</span></span>

## <a name="remarks"></a><span data-ttu-id="03768-110">Notes</span><span class="sxs-lookup"><span data-stu-id="03768-110">Remarks</span></span>

<span data-ttu-id="03768-111">L’appelant doit initialiser la structure **DIBDATA** avant d’appeler cette méthode. Vérifiez la valeur de **CImageSample :: m \_ bInit**.</span><span class="sxs-lookup"><span data-stu-id="03768-111">The caller must initialize the **DIBDATA** structure before calling this method; check the value of **CImageSample::m\_bInit**.</span></span> <span data-ttu-id="03768-112">Pour initialiser la structure, appelez la méthode [**CImageSample :: SetDIBData**](cimagesample-setdibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="03768-112">To initialize the structure, call the [**CImageSample::SetDIBData**](cimagesample-setdibdata.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="03768-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="03768-113">Requirements</span></span>



| <span data-ttu-id="03768-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="03768-114">Requirement</span></span> | <span data-ttu-id="03768-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="03768-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03768-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="03768-116">Header</span></span><br/>  | <dl> <span data-ttu-id="03768-117"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="03768-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="03768-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="03768-118">Library</span></span><br/> | <dl> <span data-ttu-id="03768-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="03768-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03768-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03768-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03768-121">**CImageSample, classe**</span><span class="sxs-lookup"><span data-stu-id="03768-121">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




