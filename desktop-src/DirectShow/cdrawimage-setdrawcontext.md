---
description: La méthode SetDrawContext définit les contextes de périphérique utilisés pour le dessin.
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: Méthode CDrawImage. SetDrawContext (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d329dd45d1a02afd2cbd0daf8d0da8390b0b395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542530"
---
# <a name="cdrawimagesetdrawcontext-method"></a><span data-ttu-id="86300-103">Méthode CDrawImage. SetDrawContext</span><span class="sxs-lookup"><span data-stu-id="86300-103">CDrawImage.SetDrawContext method</span></span>

<span data-ttu-id="86300-104">La `SetDrawContext` méthode définit les contextes de périphérique utilisés pour le dessin.</span><span class="sxs-lookup"><span data-stu-id="86300-104">The `SetDrawContext` method sets the device contexts used for drawing.</span></span>

## <a name="syntax"></a><span data-ttu-id="86300-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86300-105">Syntax</span></span>


```C++
void SetDrawContext();
```



## <a name="parameters"></a><span data-ttu-id="86300-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86300-106">Parameters</span></span>

<span data-ttu-id="86300-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="86300-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="86300-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86300-108">Return value</span></span>

<span data-ttu-id="86300-109">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="86300-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="86300-110">Notes</span><span class="sxs-lookup"><span data-stu-id="86300-110">Remarks</span></span>

<span data-ttu-id="86300-111">Cette méthode récupère les contextes de la fenêtre et du périphérique de mémoire à partir de l’objet [**CBaseWindow**](cbasewindow.md) propriétaire.</span><span class="sxs-lookup"><span data-stu-id="86300-111">This method retrieves the window and memory device contexts from the owning [**CBaseWindow**](cbasewindow.md) object.</span></span> <span data-ttu-id="86300-112">Appelez cette méthode après l’initialisation de la fenêtre, mais avant de commencer le dessin.</span><span class="sxs-lookup"><span data-stu-id="86300-112">Call this method after the window is initialized, but before you begin drawing.</span></span>

## <a name="requirements"></a><span data-ttu-id="86300-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86300-113">Requirements</span></span>



| <span data-ttu-id="86300-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86300-114">Requirement</span></span> | <span data-ttu-id="86300-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="86300-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86300-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="86300-116">Header</span></span><br/>  | <dl> <span data-ttu-id="86300-117"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86300-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="86300-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="86300-118">Library</span></span><br/> | <dl> <span data-ttu-id="86300-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="86300-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86300-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86300-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86300-121">**CDrawImage, classe**</span><span class="sxs-lookup"><span data-stu-id="86300-121">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




