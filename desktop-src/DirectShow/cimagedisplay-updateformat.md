---
description: La méthode UpdateFormat remplit certains membres facultatifs de la structure VIDEOINFO.
ms.assetid: 5ca34fa0-eef4-44f5-bbcc-e686e5181d86
title: Méthode CImageDisplay. UpdateFormat (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.UpdateFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c6966da171e37e1cc285afc1872d221ca7aad99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524025"
---
# <a name="cimagedisplayupdateformat-method"></a><span data-ttu-id="4e6da-103">Méthode CImageDisplay. UpdateFormat</span><span class="sxs-lookup"><span data-stu-id="4e6da-103">CImageDisplay.UpdateFormat method</span></span>

<span data-ttu-id="4e6da-104">La `UpdateFormat` méthode remplit certains membres facultatifs de la structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="4e6da-104">The `UpdateFormat` method fills in some optional members of the [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e6da-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e6da-105">Syntax</span></span>


```C++
HRESULT UpdateFormat(
   VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a><span data-ttu-id="4e6da-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e6da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e6da-107">*pVideoInfo*</span><span class="sxs-lookup"><span data-stu-id="4e6da-107">*pVideoInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="4e6da-108">Pointeur vers une structure **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="4e6da-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e6da-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4e6da-109">Return value</span></span>

<span data-ttu-id="4e6da-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4e6da-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e6da-111">Notes</span><span class="sxs-lookup"><span data-stu-id="4e6da-111">Remarks</span></span>

<span data-ttu-id="4e6da-112">Cette méthode définit les membres **biClrUsed**, **biClrImportant** et **biSizeImage** sur les valeurs correctes, et efface les rectangles source et cible.</span><span class="sxs-lookup"><span data-stu-id="4e6da-112">This method sets the **biClrUsed**, **biClrImportant**, and **biSizeImage** members to the correct values, and clears the source and target rectangles.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e6da-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4e6da-113">Requirements</span></span>



| <span data-ttu-id="4e6da-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4e6da-114">Requirement</span></span> | <span data-ttu-id="4e6da-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="4e6da-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e6da-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="4e6da-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4e6da-117"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4e6da-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4e6da-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4e6da-118">Library</span></span><br/> | <dl> <span data-ttu-id="4e6da-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="4e6da-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e6da-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e6da-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e6da-121">**CImageDisplay, classe**</span><span class="sxs-lookup"><span data-stu-id="4e6da-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




