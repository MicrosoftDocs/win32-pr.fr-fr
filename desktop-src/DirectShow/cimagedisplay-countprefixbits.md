---
description: La méthode CountPrefixBits calcule le nombre de bits zéro au début d’un champ de bits spécifié.
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: Méthode CImageDisplay. CountPrefixBits (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountPrefixBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4333e1b0826b4fac7bfff463531b5d2e10704418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539962"
---
# <a name="cimagedisplaycountprefixbits-method"></a><span data-ttu-id="ce070-103">Méthode CImageDisplay. CountPrefixBits</span><span class="sxs-lookup"><span data-stu-id="ce070-103">CImageDisplay.CountPrefixBits method</span></span>

<span data-ttu-id="ce070-104">La `CountPrefixBits` méthode calcule le nombre de bits zéro au début d’un champ de bits spécifié.</span><span class="sxs-lookup"><span data-stu-id="ce070-104">The `CountPrefixBits` method calculates the number of zero bits at the start of a specified bit field.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce070-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce070-105">Syntax</span></span>


```C++
DWORD CountPrefixBits(
   const DWORD Field
);
```



## <a name="parameters"></a><span data-ttu-id="ce070-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce070-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce070-107">*Champ*</span><span class="sxs-lookup"><span data-stu-id="ce070-107">*Field*</span></span> 
</dt> <dd>

<span data-ttu-id="ce070-108">Spécifie un champ de bits comme valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="ce070-108">Specifies a bit field as a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce070-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce070-109">Return value</span></span>

<span data-ttu-id="ce070-110">Retourne le nombre de bits zéro qui se produisent avant le premier bit 1, ou 0x80000000 si tous les bits sont nuls.</span><span class="sxs-lookup"><span data-stu-id="ce070-110">Returns the number of zero bits that occur before the first 1 bit, or 0x80000000 if all bits are zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce070-111">Notes</span><span class="sxs-lookup"><span data-stu-id="ce070-111">Remarks</span></span>

<span data-ttu-id="ce070-112">Cette méthode est utile pour utiliser des masques de couleur dans les structures [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="ce070-112">This method is useful for working with color masks in [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce070-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce070-113">Requirements</span></span>



| <span data-ttu-id="ce070-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce070-114">Requirement</span></span> | <span data-ttu-id="ce070-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce070-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce070-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce070-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ce070-117"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce070-117"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ce070-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ce070-118">Library</span></span><br/> | <dl> <span data-ttu-id="ce070-119"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ce070-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce070-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce070-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce070-121">**CImageDisplay, classe**</span><span class="sxs-lookup"><span data-stu-id="ce070-121">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




