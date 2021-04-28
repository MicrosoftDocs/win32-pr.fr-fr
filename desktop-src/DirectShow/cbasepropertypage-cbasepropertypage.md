---
description: Méthode constructeur CBasePropertyPage. CBasePropertyPage.
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
ms.openlocfilehash: 95821062b6b1199ea98a5329934d76e2197901d4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119947"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a><span data-ttu-id="d4b78-103">Constructeur CBasePropertyPage. CBasePropertyPage</span><span class="sxs-lookup"><span data-stu-id="d4b78-103">CBasePropertyPage.CBasePropertyPage constructor</span></span>

<span data-ttu-id="d4b78-104">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="d4b78-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4b78-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4b78-105">Syntax</span></span>


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a><span data-ttu-id="d4b78-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4b78-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4b78-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="d4b78-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="d4b78-108">Chaîne qui contient le nom de l’objet, à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="d4b78-108">String that contains the name of the object, for debugging purposes.</span></span> <span data-ttu-id="d4b78-109">Pour plus d’informations, consultez [**CBaseObject :: CBaseObject**](cbaseobject-cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="d4b78-109">For more information, see [**CBaseObject::CBaseObject**](cbaseobject-cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4b78-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="d4b78-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="d4b78-111">Pointeur vers l’interface **IUnknown** d’agrégation.</span><span class="sxs-lookup"><span data-stu-id="d4b78-111">Pointer to the aggregating **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="d4b78-112">*DialogId*</span><span class="sxs-lookup"><span data-stu-id="d4b78-112">*DialogId*</span></span> 
</dt> <dd>

<span data-ttu-id="d4b78-113">ID de ressource de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d4b78-113">Resource ID for the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="d4b78-114">*TitleId*</span><span class="sxs-lookup"><span data-stu-id="d4b78-114">*TitleId*</span></span> 
</dt> <dd>

<span data-ttu-id="d4b78-115">ID de ressource pour la chaîne qui contient le titre de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d4b78-115">Resource ID for the string that contains the dialog box title.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d4b78-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="d4b78-116">Examples</span></span>


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a><span data-ttu-id="d4b78-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4b78-117">Requirements</span></span>



| <span data-ttu-id="d4b78-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4b78-118">Requirement</span></span> | <span data-ttu-id="d4b78-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4b78-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4b78-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4b78-120">Header</span></span><br/>  | <dl> <span data-ttu-id="d4b78-121"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4b78-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="d4b78-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4b78-122">Library</span></span><br/> | <dl> <span data-ttu-id="d4b78-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d4b78-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4b78-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4b78-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4b78-125">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="d4b78-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




