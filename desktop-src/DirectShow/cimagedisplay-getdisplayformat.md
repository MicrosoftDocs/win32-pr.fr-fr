---
description: La méthode GetDisplayFormat récupère un format vidéo qui décrit le mode d’affichage actuel.
ms.assetid: 98134704-0453-4090-94de-d92cdf324538
title: Méthode CImageDisplay. GetDisplayFormat (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetDisplayFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 901d61f3597156853b0f2d6f93b43c3cf99ec5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537817"
---
# <a name="cimagedisplaygetdisplayformat-method"></a><span data-ttu-id="c1b51-103">Méthode CImageDisplay. GetDisplayFormat</span><span class="sxs-lookup"><span data-stu-id="c1b51-103">CImageDisplay.GetDisplayFormat method</span></span>

<span data-ttu-id="c1b51-104">La `GetDisplayFormat` méthode récupère un format vidéo qui décrit le mode d’affichage actuel.</span><span class="sxs-lookup"><span data-stu-id="c1b51-104">The `GetDisplayFormat` method retrieves a video format that describes the current display mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1b51-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1b51-105">Syntax</span></span>


```C++
const VIDEOINFO* GetDisplayFormat();
```



## <a name="parameters"></a><span data-ttu-id="c1b51-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1b51-106">Parameters</span></span>

<span data-ttu-id="c1b51-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c1b51-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c1b51-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1b51-108">Return value</span></span>

<span data-ttu-id="c1b51-109">Retourne un pointeur vers une structure [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="c1b51-109">Returns a pointer to a [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1b51-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1b51-110">Requirements</span></span>



| <span data-ttu-id="c1b51-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1b51-111">Requirement</span></span> | <span data-ttu-id="c1b51-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1b51-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1b51-113">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1b51-113">Header</span></span><br/>  | <dl> <span data-ttu-id="c1b51-114"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c1b51-114"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c1b51-115">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c1b51-115">Library</span></span><br/> | <dl> <span data-ttu-id="c1b51-116"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c1b51-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1b51-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1b51-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1b51-118">**CImageDisplay, classe**</span><span class="sxs-lookup"><span data-stu-id="c1b51-118">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




