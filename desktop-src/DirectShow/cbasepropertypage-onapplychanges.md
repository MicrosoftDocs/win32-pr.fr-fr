---
description: La méthode OnApplyChanges est appelée lorsque l’utilisateur applique des modifications à la page de propriétés.
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: Méthode CBasePropertyPage. OnApplyChanges (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnApplyChanges
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cbcea308a8daaa8b9fdf15be765dc5d3a0df182c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525632"
---
# <a name="cbasepropertypageonapplychanges-method"></a><span data-ttu-id="1bd5f-103">Méthode CBasePropertyPage. OnApplyChanges</span><span class="sxs-lookup"><span data-stu-id="1bd5f-103">CBasePropertyPage.OnApplyChanges method</span></span>

<span data-ttu-id="1bd5f-104">La `OnApplyChanges` méthode est appelée lorsque l’utilisateur applique des modifications à la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="1bd5f-104">The `OnApplyChanges` method is called when the user applies changes to the property page.</span></span>

## <a name="syntax"></a><span data-ttu-id="1bd5f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bd5f-105">Syntax</span></span>


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a><span data-ttu-id="1bd5f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bd5f-106">Parameters</span></span>

<span data-ttu-id="1bd5f-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1bd5f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1bd5f-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1bd5f-108">Return value</span></span>

<span data-ttu-id="1bd5f-109">L’implémentation de la classe de base retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1bd5f-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1bd5f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1bd5f-110">Remarks</span></span>

<span data-ttu-id="1bd5f-111">La méthode [**CBasePropertyPage :: apply**](cbasepropertypage-apply.md) appelle `OnApplyChanges` si l’indicateur [**CBasePropertyPage :: m \_ bDirty**](cbasepropertypage-m-bdirty.md) a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="1bd5f-111">The [**CBasePropertyPage::Apply**](cbasepropertypage-apply.md) method calls `OnApplyChanges` if the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag is **TRUE**.</span></span> <span data-ttu-id="1bd5f-112">Remplacez `OnApplyChanges` pour traiter les modifications et réinitialisez **m \_ bDirty** sur **false**.</span><span class="sxs-lookup"><span data-stu-id="1bd5f-112">Override `OnApplyChanges` to process the changes and reset **m\_bDirty** to **FALSE**.</span></span>

## <a name="examples"></a><span data-ttu-id="1bd5f-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="1bd5f-113">Examples</span></span>


```C++
HRESULT CMyProp::OnApplyChanges(void)
{
    ASSERT(m_pOwningFilter != NULL);
    return m_pOwningFilter->SetSomeProperty(&m_lNewVal);
}
```



## <a name="requirements"></a><span data-ttu-id="1bd5f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1bd5f-114">Requirements</span></span>



| <span data-ttu-id="1bd5f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1bd5f-115">Requirement</span></span> | <span data-ttu-id="1bd5f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1bd5f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1bd5f-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="1bd5f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1bd5f-118"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1bd5f-118"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="1bd5f-119">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1bd5f-119">Library</span></span><br/> | <dl> <span data-ttu-id="1bd5f-120"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="1bd5f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1bd5f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1bd5f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1bd5f-122">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="1bd5f-122">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




