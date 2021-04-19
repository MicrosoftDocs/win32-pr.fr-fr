---
description: La méthode GetReader retourne un pointeur vers l’interface IAsyncReader de la broche de sortie.
ms.assetid: bb7ed3f2-a5bc-496c-8a52-f9915a75105e
title: Méthode CPullPin. GetReader (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.GetReader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3a20bbb689c4ee5e3ac12c510098163d9fbb224e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541670"
---
# <a name="cpullpingetreader-method"></a><span data-ttu-id="72d0f-103">Méthode CPullPin. GetReader</span><span class="sxs-lookup"><span data-stu-id="72d0f-103">CPullPin.GetReader method</span></span>

<span data-ttu-id="72d0f-104">La `GetReader` méthode retourne un pointeur vers l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) de la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="72d0f-104">The `GetReader` method returns a pointer to the output pin's [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="72d0f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="72d0f-105">Syntax</span></span>


```C++
IAsyncReader* GetReader();
```



## <a name="parameters"></a><span data-ttu-id="72d0f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="72d0f-106">Parameters</span></span>

<span data-ttu-id="72d0f-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="72d0f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="72d0f-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="72d0f-108">Return value</span></span>

<span data-ttu-id="72d0f-109">Retourne un pointeur vers l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="72d0f-109">Returns a pointer to the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="72d0f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="72d0f-110">Remarks</span></span>

<span data-ttu-id="72d0f-111">L’interface retournée a un nombre de références en attente.</span><span class="sxs-lookup"><span data-stu-id="72d0f-111">The returned interface has an outstanding reference count.</span></span> <span data-ttu-id="72d0f-112">L’appelant doit libérer l’interface.</span><span class="sxs-lookup"><span data-stu-id="72d0f-112">The caller must release the interface.</span></span>

<span data-ttu-id="72d0f-113">La méthode ne vérifie pas la valeur du pointeur d’interface avant d’appeler **AddRef**, donc n’appelez pas cette méthode tant que vous n’avez pas appelé la méthode [**CPullPin :: Connect**](cpullpin-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="72d0f-113">The method does not check the value of the interface pointer before calling **AddRef**, so do not call this until you have successfully called the [**CPullPin::Connect**](cpullpin-connect.md) method.</span></span> <span data-ttu-id="72d0f-114">Dans le cas contraire, le pointeur d’interface peut être **null** et l’appel de **AddRef** lèvera une exception.</span><span class="sxs-lookup"><span data-stu-id="72d0f-114">Otherwise, the interface pointer might be **NULL** and calling **AddRef** will throw an exception.</span></span>

## <a name="requirements"></a><span data-ttu-id="72d0f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="72d0f-115">Requirements</span></span>



| <span data-ttu-id="72d0f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="72d0f-116">Requirement</span></span> | <span data-ttu-id="72d0f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="72d0f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72d0f-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="72d0f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="72d0f-119"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="72d0f-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="72d0f-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="72d0f-120">Library</span></span><br/> | <dl> <span data-ttu-id="72d0f-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="72d0f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72d0f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="72d0f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72d0f-123">**CPullPin, classe**</span><span class="sxs-lookup"><span data-stu-id="72d0f-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




