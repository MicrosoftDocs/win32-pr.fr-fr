---
description: 'La méthode Activate crée la fenêtre de boîte de dialogue. Cette méthode implémente la méthode IPropertyPage :: Activate.'
ms.assetid: 8f030dc5-1d14-46b5-9d40-7f07a1177dbe
title: CBasePropertyPage. Activate, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Activate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b851cfc4490d25e7e30dfd2cf0e7c33b0e76224
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525476"
---
# <a name="cbasepropertypageactivate-method"></a><span data-ttu-id="abf41-104">CBasePropertyPage. Activate, méthode</span><span class="sxs-lookup"><span data-stu-id="abf41-104">CBasePropertyPage.Activate method</span></span>

<span data-ttu-id="abf41-105">La `Activate` méthode crée la fenêtre de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="abf41-105">The `Activate` method creates the dialog box window.</span></span> <span data-ttu-id="abf41-106">Cette méthode implémente la méthode **IPropertyPage :: Activate** .</span><span class="sxs-lookup"><span data-stu-id="abf41-106">This method implements the **IPropertyPage::Activate** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="abf41-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abf41-107">Syntax</span></span>


```C++
HRESULT Activate(
   HWND    hwndParent,
   LPCRECT prect,
   BOOL    fModal
);
```



## <a name="parameters"></a><span data-ttu-id="abf41-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abf41-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abf41-109">*hwndParent*</span><span class="sxs-lookup"><span data-stu-id="abf41-109">*hwndParent*</span></span> 
</dt> <dd>

<span data-ttu-id="abf41-110">Handle de la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="abf41-110">Handle to the parent window of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="abf41-111">*prect*</span><span class="sxs-lookup"><span data-stu-id="abf41-111">*prect*</span></span> 
</dt> <dd>

<span data-ttu-id="abf41-112">Pointeur vers une structure **Rect** qui contient des informations de positionnement pour la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="abf41-112">Pointer to a **RECT** structure that contains positioning information for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="abf41-113">*fModal*</span><span class="sxs-lookup"><span data-stu-id="abf41-113">*fModal*</span></span> 
</dt> <dd>

<span data-ttu-id="abf41-114">Valeur booléenne indiquant si le cadre de la boîte de dialogue est modal (**true**) ou non modal (**false**).</span><span class="sxs-lookup"><span data-stu-id="abf41-114">Boolean value indicating whether the dialog box frame is modal (**TRUE**) or modeless (**FALSE**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abf41-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="abf41-115">Return value</span></span>

<span data-ttu-id="abf41-116">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="abf41-116">Returns an **HRESULT** value.</span></span> <span data-ttu-id="abf41-117">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="abf41-117">Possible values include the following.</span></span>



| <span data-ttu-id="abf41-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="abf41-118">Return code</span></span>                                                                                   | <span data-ttu-id="abf41-119">Description</span><span class="sxs-lookup"><span data-stu-id="abf41-119">Description</span></span>                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="abf41-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="abf41-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="abf41-121">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="abf41-121">Success.</span></span><br/>                   |
| <dl> <span data-ttu-id="abf41-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="abf41-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="abf41-123">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="abf41-123">Insufficient memory.</span></span><br/>       |
| <dl> <span data-ttu-id="abf41-124"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="abf41-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="abf41-125">Argument de pointeur **null** .</span><span class="sxs-lookup"><span data-stu-id="abf41-125">**NULL** pointer argument.</span></span><br/> |
| <dl> <span data-ttu-id="abf41-126"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="abf41-126"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="abf41-127">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="abf41-127">Unexpected failure.</span></span><br/>        |



 

## <a name="requirements"></a><span data-ttu-id="abf41-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abf41-128">Requirements</span></span>



| <span data-ttu-id="abf41-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abf41-129">Requirement</span></span> | <span data-ttu-id="abf41-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="abf41-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abf41-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="abf41-131">Header</span></span><br/>  | <dl> <span data-ttu-id="abf41-132"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="abf41-132"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="abf41-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="abf41-133">Library</span></span><br/> | <dl> <span data-ttu-id="abf41-134"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="abf41-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abf41-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abf41-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abf41-136">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="abf41-136">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> <dt>

[<span data-ttu-id="abf41-137">**CBasePropertyPage :: OnActivate**</span><span class="sxs-lookup"><span data-stu-id="abf41-137">**CBasePropertyPage::OnActivate**</span></span>](cbasepropertypage-onactivate.md)
</dt> </dl>

 

 




