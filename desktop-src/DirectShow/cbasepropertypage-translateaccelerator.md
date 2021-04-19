---
description: 'La méthode TranslateAccelerator demande à la page de propriétés de traiter une séquence de touches. Cette méthode implémente la méthode IPropertyPage :: TranslateAccelerator.'
ms.assetid: 2da214c9-35dc-470c-9b7f-2f4ef6bcd40a
title: CBasePropertyPage. TranslateAccelerator, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.TranslateAccelerator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3116e85eec8fbf3a00bf434a1f88c8cac662ed0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528775"
---
# <a name="cbasepropertypagetranslateaccelerator-method"></a><span data-ttu-id="6ef8a-104">CBasePropertyPage. TranslateAccelerator, méthode</span><span class="sxs-lookup"><span data-stu-id="6ef8a-104">CBasePropertyPage.TranslateAccelerator method</span></span>

<span data-ttu-id="6ef8a-105">La `TranslateAccelerator` méthode indique à la page de propriétés de traiter une séquence de touches.</span><span class="sxs-lookup"><span data-stu-id="6ef8a-105">The `TranslateAccelerator` method instructs the property page to process a keystroke.</span></span> <span data-ttu-id="6ef8a-106">Cette méthode implémente la méthode **IPropertyPage :: TranslateAccelerator** .</span><span class="sxs-lookup"><span data-stu-id="6ef8a-106">This method implements the **IPropertyPage::TranslateAccelerator** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ef8a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ef8a-107">Syntax</span></span>


```C++
HRESULT TranslateAccelerator(
   LPMSG lpMsg
);
```



## <a name="parameters"></a><span data-ttu-id="6ef8a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ef8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ef8a-109">*lpMsg*</span><span class="sxs-lookup"><span data-stu-id="6ef8a-109">*lpMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="6ef8a-110">Pointeur vers une structure **MSG** décrivant la séquence de touches à traiter.</span><span class="sxs-lookup"><span data-stu-id="6ef8a-110">Pointer to a **MSG** structure describing the keystroke to process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ef8a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6ef8a-111">Return value</span></span>

<span data-ttu-id="6ef8a-112">Retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="6ef8a-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ef8a-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6ef8a-113">Remarks</span></span>

<span data-ttu-id="6ef8a-114">Substituez cette méthode si vous souhaitez fournir des accélérateurs de clavier pour la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="6ef8a-114">Override this method if you want to provide keyboard accelerators for the property page.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ef8a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ef8a-115">Requirements</span></span>



| <span data-ttu-id="6ef8a-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ef8a-116">Requirement</span></span> | <span data-ttu-id="6ef8a-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ef8a-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef8a-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="6ef8a-118">Header</span></span><br/>  | <dl> <span data-ttu-id="6ef8a-119"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6ef8a-119"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="6ef8a-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6ef8a-120">Library</span></span><br/> | <dl> <span data-ttu-id="6ef8a-121"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6ef8a-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ef8a-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ef8a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef8a-123">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="6ef8a-123">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




