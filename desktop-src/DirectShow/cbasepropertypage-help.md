---
description: 'La méthode Help appelle l’aide de la page de propriétés. Cette méthode implémente la méthode IPropertyPage :: help.'
ms.assetid: 8fe72b2e-a9f1-435d-8eda-27056f112c6d
title: CBasePropertyPage. Help, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Help
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b87c8ba76928fbf0e465a8b6a3a0aaf4730759f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526793"
---
# <a name="cbasepropertypagehelp-method"></a><span data-ttu-id="6f650-104">CBasePropertyPage. Help, méthode</span><span class="sxs-lookup"><span data-stu-id="6f650-104">CBasePropertyPage.Help method</span></span>

<span data-ttu-id="6f650-105">La `Help` méthode appelle l’aide de la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="6f650-105">The `Help` method invokes the property page help.</span></span> <span data-ttu-id="6f650-106">Cette méthode implémente la méthode **IPropertyPage :: help** .</span><span class="sxs-lookup"><span data-stu-id="6f650-106">This method implements the **IPropertyPage::Help** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f650-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f650-107">Syntax</span></span>


```C++
HRESULT Help(
   LPCWSTR lpszHelpDir
);
```



## <a name="parameters"></a><span data-ttu-id="6f650-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f650-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f650-109">*lpszHelpDir*</span><span class="sxs-lookup"><span data-stu-id="6f650-109">*lpszHelpDir*</span></span> 
</dt> <dd>

<span data-ttu-id="6f650-110">Pointeur vers la chaîne sous la clé **helpDir** dans les informations de CLSID de la page de propriétés dans le registre.</span><span class="sxs-lookup"><span data-stu-id="6f650-110">Pointer to the string under the **HelpDir** key in the property page's CLSID information in the registry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f650-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f650-111">Return value</span></span>

<span data-ttu-id="6f650-112">Retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="6f650-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f650-113">Notes</span><span class="sxs-lookup"><span data-stu-id="6f650-113">Remarks</span></span>

<span data-ttu-id="6f650-114">Dans la classe de base, la méthode retourne toujours E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="6f650-114">In the base class, the method always returns E\_NOTIMPL.</span></span> <span data-ttu-id="6f650-115">Lorsque la méthode échoue, le frame appelle **IPropertyPage :: GetPageInfo** pour obtenir le nom du fichier d’aide et de l’identificateur de contexte.</span><span class="sxs-lookup"><span data-stu-id="6f650-115">When the method fails, the frame calls **IPropertyPage::GetPageInfo** to get the name of the help file and context identifier.</span></span> <span data-ttu-id="6f650-116">Par défaut, il s’agit de la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="6f650-116">By default, these are **NULL**.</span></span> <span data-ttu-id="6f650-117">Par conséquent, pour fournir de l’aide, la classe dérivée peut substituer la méthode `Help` ou la méthode [**CBasePropertyPage :: GetPageInfo**](cbasepropertypage-getpageinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="6f650-117">To provide help, therefore, the derived class can override either the `Help` method or the [**CBasePropertyPage::GetPageInfo**](cbasepropertypage-getpageinfo.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f650-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f650-118">Requirements</span></span>



| <span data-ttu-id="6f650-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f650-119">Requirement</span></span> | <span data-ttu-id="6f650-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f650-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f650-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f650-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6f650-122"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f650-122"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="6f650-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6f650-123">Library</span></span><br/> | <dl> <span data-ttu-id="6f650-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6f650-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f650-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f650-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f650-126">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="6f650-126">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




