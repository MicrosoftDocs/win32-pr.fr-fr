---
description: Méthode de constructeur.
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: Constructeur CBasePropertyPage. CBasePropertyPage (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 915bc42cfb7f152cc061dab76caede6c998edf8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539177"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a><span data-ttu-id="86973-103">Constructeur CBasePropertyPage. CBasePropertyPage</span><span class="sxs-lookup"><span data-stu-id="86973-103">CBasePropertyPage.CBasePropertyPage constructor</span></span>

<span data-ttu-id="86973-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="86973-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="86973-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86973-105">Syntax</span></span>


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a><span data-ttu-id="86973-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86973-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86973-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="86973-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="86973-108">Chaîne qui contient le nom de l’objet, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="86973-108">String that contains the name of the object, for debugging purposes.</span></span> <span data-ttu-id="86973-109">Pour plus d’informations, consultez [**CBaseObject :: CBaseObject**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="86973-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="86973-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="86973-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="86973-111">Pointeur vers l’interface **IUnknown** d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="86973-111">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="86973-112">*DialogId*</span><span class="sxs-lookup"><span data-stu-id="86973-112">*DialogId*</span></span> 
</dt> <dd>

<span data-ttu-id="86973-113">ID de ressource de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="86973-113">Resource ID for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="86973-114">*TitleId*</span><span class="sxs-lookup"><span data-stu-id="86973-114">*TitleId*</span></span> 
</dt> <dd>

<span data-ttu-id="86973-115">ID de ressource pour la chaîne qui contient le titre de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="86973-115">Resource ID for the string that contains the dialog box title.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="86973-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="86973-116">Examples</span></span>


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a><span data-ttu-id="86973-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86973-117">Requirements</span></span>



| <span data-ttu-id="86973-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86973-118">Requirement</span></span> | <span data-ttu-id="86973-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="86973-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86973-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="86973-120">Header</span></span><br/>  | <dl> <span data-ttu-id="86973-121"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="86973-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="86973-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="86973-122">Library</span></span><br/> | <dl> <span data-ttu-id="86973-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="86973-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86973-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86973-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86973-125">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="86973-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




