---
description: La méthode DoRealisePalette réalise la palette actuelle de la fenêtre.
ms.assetid: dd023c81-0cd0-48c6-bc63-5891f2a4acf7
title: Méthode CBaseWindow. DoRealisePalette (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.DoRealisePalette
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: be1e02d355ab5991c9d0e95dbff30d4c8e0162ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530413"
---
# <a name="cbasewindowdorealisepalette-method"></a><span data-ttu-id="df776-103">Méthode CBaseWindow. DoRealisePalette</span><span class="sxs-lookup"><span data-stu-id="df776-103">CBaseWindow.DoRealisePalette method</span></span>

<span data-ttu-id="df776-104">La `DoRealisePalette` méthode réalise la palette actuelle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="df776-104">The `DoRealisePalette` method realizes the window's current palette.</span></span>

## <a name="syntax"></a><span data-ttu-id="df776-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df776-105">Syntax</span></span>


```C++
virtual HRESULT DoRealisePalette(
   BOOL bForceBackground
);
```



## <a name="parameters"></a><span data-ttu-id="df776-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df776-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df776-107">*bForceBackground*</span><span class="sxs-lookup"><span data-stu-id="df776-107">*bForceBackground*</span></span> 
</dt> <dd>

<span data-ttu-id="df776-108">Valeur booléenne qui spécifie si la palette est forcée à être une palette d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="df776-108">Boolean value that specifies whether the palette is forced to be a background palette.</span></span> <span data-ttu-id="df776-109">Pour plus d’informations, consultez **SelectPalette** dans le kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="df776-109">For more information, see **SelectPalette** in the Platform SDK.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df776-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df776-110">Return value</span></span>

<span data-ttu-id="df776-111">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="df776-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="df776-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="df776-112">Return code</span></span>                                                                             | <span data-ttu-id="df776-113">Description</span><span class="sxs-lookup"><span data-stu-id="df776-113">Description</span></span>                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="df776-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="df776-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="df776-115">Un appel interne à **GdiFlush** a retourné une erreur.</span><span class="sxs-lookup"><span data-stu-id="df776-115">An internal call to **GdiFlush** returned an error.</span></span><br/> |
| <dl> <span data-ttu-id="df776-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="df776-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="df776-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="df776-117">Success.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="df776-118">Notes</span><span class="sxs-lookup"><span data-stu-id="df776-118">Remarks</span></span>

<span data-ttu-id="df776-119">La méthode [**CBaseWindow :: OnPaletteChange**](cbasewindow-onpalettechange.md) appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="df776-119">The [**CBaseWindow::OnPaletteChange**](cbasewindow-onpalettechange.md) method calls this method.</span></span> <span data-ttu-id="df776-120">Pour définir une nouvelle palette, appelez la méthode [**CBaseWindow :: SetPalette**](cbasewindow-setpalette.md) .</span><span class="sxs-lookup"><span data-stu-id="df776-120">To set a new palette, call the [**CBaseWindow::SetPalette**](cbasewindow-setpalette.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="df776-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df776-121">Requirements</span></span>



| <span data-ttu-id="df776-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df776-122">Requirement</span></span> | <span data-ttu-id="df776-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="df776-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df776-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="df776-124">Header</span></span><br/>  | <dl> <span data-ttu-id="df776-125"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df776-125"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="df776-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="df776-126">Library</span></span><br/> | <dl> <span data-ttu-id="df776-127"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="df776-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df776-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df776-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df776-129">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="df776-129">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




