---
description: La méthode CheckVideoType vérifie si un format VIDEOINFO spécifié est compatible avec le format d’affichage.
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: Méthode CImageDisplay. CheckVideoType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckVideoType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7db198270804053993352c4969b924fa7edc891f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535337"
---
# <a name="cimagedisplaycheckvideotype-method"></a><span data-ttu-id="3465b-103">Méthode CImageDisplay. CheckVideoType</span><span class="sxs-lookup"><span data-stu-id="3465b-103">CImageDisplay.CheckVideoType method</span></span>

<span data-ttu-id="3465b-104">La `CheckVideoType` méthode vérifie si un format [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) spécifié est compatible avec le format d’affichage.</span><span class="sxs-lookup"><span data-stu-id="3465b-104">The `CheckVideoType` method checks whether a specified [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) format is compatible with the display format.</span></span>

## <a name="syntax"></a><span data-ttu-id="3465b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3465b-105">Syntax</span></span>


```C++
HRESULT CheckVideoType(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a><span data-ttu-id="3465b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3465b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3465b-107">*pInput*</span><span class="sxs-lookup"><span data-stu-id="3465b-107">*pInput*</span></span> 
</dt> <dd>

<span data-ttu-id="3465b-108">Pointeur vers une structure **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="3465b-108">Pointer to a **VIDEOINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3465b-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3465b-109">Return value</span></span>

<span data-ttu-id="3465b-110">Retourne S \_ OK si le format est compatible, ou E \_ INVALIDARG dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3465b-110">Returns S\_OK if the format is compatible, or E\_INVALIDARG otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3465b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3465b-111">Remarks</span></span>

<span data-ttu-id="3465b-112">Cette méthode retourne S \_ OK si le type proposé peut être affiché facilement sous les paramètres d’affichage actuels.</span><span class="sxs-lookup"><span data-stu-id="3465b-112">This method returns S\_OK if the proposed type can be displayed easily under the current display settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="3465b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3465b-113">Requirements</span></span>



| <span data-ttu-id="3465b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3465b-114">Requirement</span></span> | <span data-ttu-id="3465b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="3465b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3465b-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="3465b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3465b-117"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3465b-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3465b-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3465b-118">Library</span></span><br/> | <dl> <span data-ttu-id="3465b-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="3465b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3465b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3465b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3465b-121">**CImageDisplay, classe**</span><span class="sxs-lookup"><span data-stu-id="3465b-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




