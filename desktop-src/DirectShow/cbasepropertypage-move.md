---
description: 'La méthode Move positionne et redimensionne la boîte de dialogue. Cette méthode implémente la méthode IPropertyPage :: Move.'
ms.assetid: b6cabb5c-196d-489b-9dd4-194d26f4de83
title: CBasePropertyPage. Move, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Move
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4d293f6ccb6a1bcd730ce997367c179f1747f66e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526324"
---
# <a name="cbasepropertypagemove-method"></a><span data-ttu-id="5a55c-104">CBasePropertyPage. Move, méthode</span><span class="sxs-lookup"><span data-stu-id="5a55c-104">CBasePropertyPage.Move method</span></span>

<span data-ttu-id="5a55c-105">La `Move` méthode positionne et redimensionne la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="5a55c-105">The `Move` method positions and resizes the dialog box.</span></span> <span data-ttu-id="5a55c-106">Cette méthode implémente la méthode **IPropertyPage :: Move** .</span><span class="sxs-lookup"><span data-stu-id="5a55c-106">This method implements the **IPropertyPage::Move** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a55c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a55c-107">Syntax</span></span>


```C++
HRESULT Move(
   LPCRECT prect
);
```



## <a name="parameters"></a><span data-ttu-id="5a55c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a55c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a55c-109">*prect*</span><span class="sxs-lookup"><span data-stu-id="5a55c-109">*prect*</span></span> 
</dt> <dd>

<span data-ttu-id="5a55c-110">Pointeur vers une structure **Rect** contenant les informations de positionnement.</span><span class="sxs-lookup"><span data-stu-id="5a55c-110">Pointer to a **RECT** structure containing the positioning information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a55c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a55c-111">Return value</span></span>

<span data-ttu-id="5a55c-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5a55c-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5a55c-113">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="5a55c-113">Possible values include the following.</span></span>



| <span data-ttu-id="5a55c-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5a55c-114">Return code</span></span>                                                                                  | <span data-ttu-id="5a55c-115">Description</span><span class="sxs-lookup"><span data-stu-id="5a55c-115">Description</span></span>                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5a55c-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5a55c-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5a55c-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="5a55c-117">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="5a55c-118"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="5a55c-118"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="5a55c-119">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="5a55c-119">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="5a55c-120"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="5a55c-120"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="5a55c-121">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="5a55c-121">Unexpected failure.</span></span><br/>        |



 

## <a name="requirements"></a><span data-ttu-id="5a55c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a55c-122">Requirements</span></span>



| <span data-ttu-id="5a55c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a55c-123">Requirement</span></span> | <span data-ttu-id="5a55c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a55c-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a55c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a55c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5a55c-126"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a55c-126"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="5a55c-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5a55c-127">Library</span></span><br/> | <dl> <span data-ttu-id="5a55c-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="5a55c-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a55c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a55c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a55c-130">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="5a55c-130">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




