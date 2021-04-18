---
description: La méthode RefreshDisplayType met à jour le format vidéo de l’objet pour qu’il corresponde à l’affichage spécifié.
ms.assetid: cc2bdfeb-80f1-4fb6-859d-977d644a5e08
title: Méthode CImageDisplay. RefreshDisplayType (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.RefreshDisplayType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9f8010dcfe490363903ff455bedb61254b69b825
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526736"
---
# <a name="cimagedisplayrefreshdisplaytype-method"></a><span data-ttu-id="db093-103">Méthode CImageDisplay. RefreshDisplayType</span><span class="sxs-lookup"><span data-stu-id="db093-103">CImageDisplay.RefreshDisplayType method</span></span>

<span data-ttu-id="db093-104">La `RefreshDisplayType` méthode met à jour le format vidéo de l’objet pour qu’il corresponde à l’affichage spécifié.</span><span class="sxs-lookup"><span data-stu-id="db093-104">The `RefreshDisplayType` method updates the object's video format to match the specified display.</span></span>

## <a name="syntax"></a><span data-ttu-id="db093-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db093-105">Syntax</span></span>


```C++
HRESULT RefreshDisplayType(
   LPSTR szDeviceName
);
```



## <a name="parameters"></a><span data-ttu-id="db093-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db093-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db093-107">*szDeviceName*</span><span class="sxs-lookup"><span data-stu-id="db093-107">*szDeviceName*</span></span> 
</dt> <dd>

<span data-ttu-id="db093-108">Pointeur vers une chaîne qui contient le nom du périphérique d’affichage, tel que retourné par la fonction GDI **EnumDisplayDevices** .</span><span class="sxs-lookup"><span data-stu-id="db093-108">Pointer to a string that contains the name of the display device, as returned by the GDI **EnumDisplayDevices** function.</span></span> <span data-ttu-id="db093-109">Pour utiliser le périphérique d’affichage principal, attribuez la valeur **null** à ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="db093-109">To use the main display device, set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db093-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="db093-110">Return value</span></span>

<span data-ttu-id="db093-111">Retourne S \_ OK en cas de réussite, ou \_ si E échoue en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="db093-111">Returns S\_OK if successful, or E\_FAIL if unsuccessful.</span></span>

## <a name="remarks"></a><span data-ttu-id="db093-112">Notes</span><span class="sxs-lookup"><span data-stu-id="db093-112">Remarks</span></span>

<span data-ttu-id="db093-113">Cette méthode initialise le membre **d' \_ affichage m** sur un type vidéo qui correspond au mode d’affichage sur le périphérique spécifié.</span><span class="sxs-lookup"><span data-stu-id="db093-113">This method initializes the **m\_Display** member to a video type that corresponds to the display mode on the specified device.</span></span>

<span data-ttu-id="db093-114">Appelez cette méthode chaque fois qu’un \_ message DISPLAYCHANGED WM est reçu, ou pour spécifier un périphérique d’affichage secondaire.</span><span class="sxs-lookup"><span data-stu-id="db093-114">Call this method whenever a WM\_DISPLAYCHANGED message is received, or to specify a secondary display device.</span></span>

## <a name="requirements"></a><span data-ttu-id="db093-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db093-115">Requirements</span></span>



| <span data-ttu-id="db093-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db093-116">Requirement</span></span> | <span data-ttu-id="db093-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="db093-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db093-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="db093-118">Header</span></span><br/>  | <dl> <span data-ttu-id="db093-119"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="db093-119"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="db093-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="db093-120">Library</span></span><br/> | <dl> <span data-ttu-id="db093-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="db093-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db093-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db093-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db093-123">**CImageDisplay, classe**</span><span class="sxs-lookup"><span data-stu-id="db093-123">**CImageDisplay Class**</span></span>](cimagedisplay.md)
</dt> </dl>

 

 




