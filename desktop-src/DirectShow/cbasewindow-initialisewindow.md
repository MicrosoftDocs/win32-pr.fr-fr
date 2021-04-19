---
description: La méthode InitialiseWindow initialise la fenêtre.
ms.assetid: 0cf07714-6846-4271-8095-bc4ab865171f
title: CBaseWindow.Iniméthode tialiseWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InitialiseWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75668846c700c33a26b7bb7ad2af2a3fd6e8eea2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545472"
---
# <a name="cbasewindowinitialisewindow-method"></a><span data-ttu-id="9f0b4-103">CBaseWindow.Iniméthode tialiseWindow</span><span class="sxs-lookup"><span data-stu-id="9f0b4-103">CBaseWindow.InitialiseWindow method</span></span>

<span data-ttu-id="9f0b4-104">La `InitialiseWindow` méthode initialise la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-104">The `InitialiseWindow` method initializes the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f0b4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f0b4-105">Syntax</span></span>


```C++
virtual HRESULT InitialiseWindow(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="9f0b4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f0b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f0b4-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="9f0b4-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="9f0b4-108">Handle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-108">Handle to the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f0b4-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f0b4-109">Return value</span></span>

<span data-ttu-id="9f0b4-110">Retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f0b4-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9f0b4-111">Remarks</span></span>

<span data-ttu-id="9f0b4-112">Par défaut, cette méthode récupère un handle vers le contexte de périphérique (DC) de la fenêtre et crée un DC de mémoire compatible.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-112">By default, this method retrieves a handle to the window's device context (DC) and creates a compatible memory DC.</span></span> <span data-ttu-id="9f0b4-113">Toutefois, si la valeur de l’indicateur [**CBaseWindow :: m \_ BDoGetDC**](cbasewindow-m-bdogetdc.md) est **false**, cette méthode ne récupère pas les contextes de périphérique.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-113">If the value of the [**CBaseWindow::m\_bDoGetDC**](cbasewindow-m-bdogetdc.md) flag is **FALSE**, however, this method does not retrieve the device contexts.</span></span> <span data-ttu-id="9f0b4-114">Le DC de mémoire est utile pour sélectionner des bitmaps avant de les blitting dans la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-114">The memory DC is useful for selecting bitmaps before blitting them to the window.</span></span>

<span data-ttu-id="9f0b4-115">La méthode [**CBaseWindow ::D ocreatewindow**](cbasewindow-docreatewindow.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-115">The [**CBaseWindow::DoCreateWindow**](cbasewindow-docreatewindow.md) method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f0b4-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f0b4-116">Requirements</span></span>



| <span data-ttu-id="9f0b4-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f0b4-117">Requirement</span></span> | <span data-ttu-id="9f0b4-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f0b4-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f0b4-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f0b4-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9f0b4-120"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f0b4-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9f0b4-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9f0b4-121">Library</span></span><br/> | <dl> <span data-ttu-id="9f0b4-122"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="9f0b4-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f0b4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f0b4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f0b4-124">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="9f0b4-124">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




