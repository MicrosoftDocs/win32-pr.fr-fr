---
description: 'La méthode GetPageInfo récupère des informations sur la page de propriétés. Cette méthode implémente la méthode IPropertyPage :: GetPageInfo.'
ms.assetid: f2e04652-7c71-48b2-b964-4e07ac98d367
title: Méthode CBasePropertyPage. GetPageInfo (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.GetPageInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27faecf50381b098dfcbee34d1494e37c77a36ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537793"
---
# <a name="cbasepropertypagegetpageinfo-method"></a><span data-ttu-id="891f2-104">Méthode CBasePropertyPage. GetPageInfo</span><span class="sxs-lookup"><span data-stu-id="891f2-104">CBasePropertyPage.GetPageInfo method</span></span>

<span data-ttu-id="891f2-105">La `GetPageInfo` méthode récupère des informations sur la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="891f2-105">The `GetPageInfo` method retrieves information about the property page.</span></span> <span data-ttu-id="891f2-106">Cette méthode implémente la méthode **IPropertyPage :: GetPageInfo** .</span><span class="sxs-lookup"><span data-stu-id="891f2-106">This method implements the **IPropertyPage::GetPageInfo** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="891f2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="891f2-107">Syntax</span></span>


```C++
HRESULT GetPageInfo(
   LPPROPPAGEINFO pPageInfo
);
```



## <a name="parameters"></a><span data-ttu-id="891f2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="891f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="891f2-109">*pPageInfo*</span><span class="sxs-lookup"><span data-stu-id="891f2-109">*pPageInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="891f2-110">Pointeur vers une structure **PROPPAGEINFO** allouée par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="891f2-110">Pointer to a caller-allocated **PROPPAGEINFO** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="891f2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="891f2-111">Return value</span></span>

<span data-ttu-id="891f2-112">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="891f2-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="891f2-113">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="891f2-113">Possible values include the following.</span></span>



| <span data-ttu-id="891f2-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="891f2-114">Return code</span></span>                                                                                   | <span data-ttu-id="891f2-115">Description</span><span class="sxs-lookup"><span data-stu-id="891f2-115">Description</span></span>                     |
|-----------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="891f2-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="891f2-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="891f2-117">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="891f2-117">Success.</span></span><br/>             |
| <dl> <span data-ttu-id="891f2-118"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="891f2-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="891f2-119">Mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="891f2-119">Insufficient memory.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="891f2-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="891f2-120">Requirements</span></span>



| <span data-ttu-id="891f2-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="891f2-121">Requirement</span></span> | <span data-ttu-id="891f2-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="891f2-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="891f2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="891f2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="891f2-124"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="891f2-124"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="891f2-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="891f2-125">Library</span></span><br/> | <dl> <span data-ttu-id="891f2-126"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="891f2-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="891f2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="891f2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="891f2-128">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="891f2-128">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




