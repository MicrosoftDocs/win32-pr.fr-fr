---
description: La méthode SetDIBData spécifie des informations sur la bitmap indépendante du périphérique (DIB) GDI que cet objet gère. Appelez cette méthode pour initialiser l’objet CImageSample.
ms.assetid: 850fa16b-d4b9-4fe6-b202-7b54c49a4589
title: Méthode CImageSample. SetDIBData (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.SetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 418263da0416b325b1b080713dd6289f3bcc688e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525366"
---
# <a name="cimagesamplesetdibdata-method"></a><span data-ttu-id="619df-104">Méthode CImageSample. SetDIBData</span><span class="sxs-lookup"><span data-stu-id="619df-104">CImageSample.SetDIBData method</span></span>

<span data-ttu-id="619df-105">La `SetDIBData` méthode spécifie des informations sur la bitmap indépendante du périphérique (DIB) GDI que cet objet gère.</span><span class="sxs-lookup"><span data-stu-id="619df-105">The `SetDIBData` method specifies information about the GDI device-independent bitmap (DIB) that this object is managing.</span></span> <span data-ttu-id="619df-106">Appelez cette méthode pour initialiser l’objet **CImageSample** .</span><span class="sxs-lookup"><span data-stu-id="619df-106">Call this method to initialize the **CImageSample** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="619df-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="619df-107">Syntax</span></span>


```C++
void SetDIBData(
   DIBDATA *pDibData
);
```



## <a name="parameters"></a><span data-ttu-id="619df-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="619df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="619df-109">*pDibData*</span><span class="sxs-lookup"><span data-stu-id="619df-109">*pDibData*</span></span> 
</dt> <dd>

<span data-ttu-id="619df-110">Pointeur vers une structure [**DIBDATA**](dibdata.md) .</span><span class="sxs-lookup"><span data-stu-id="619df-110">Pointer to a [**DIBDATA**](dibdata.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="619df-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="619df-111">Return value</span></span>

<span data-ttu-id="619df-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="619df-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="619df-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="619df-113">Requirements</span></span>



| <span data-ttu-id="619df-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="619df-114">Requirement</span></span> | <span data-ttu-id="619df-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="619df-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="619df-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="619df-116">Header</span></span><br/>  | <dl> <span data-ttu-id="619df-117"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="619df-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="619df-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="619df-118">Library</span></span><br/> | <dl> <span data-ttu-id="619df-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="619df-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="619df-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="619df-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="619df-121">**CImageSample, classe**</span><span class="sxs-lookup"><span data-stu-id="619df-121">**CImageSample Class**</span></span>](cimagesample.md)
</dt> </dl>

 

 




