---
description: La méthode OnActivate est appelée lorsque la page de propriétés est activée.
ms.assetid: aff843d4-cfb2-4255-a59c-0579f1cd24bd
title: CBasePropertyPage. OnActivate, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnActivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5093cb2ac71e8010bc689e4517b3d8bb758c8436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533348"
---
# <a name="cbasepropertypageonactivate-method"></a><span data-ttu-id="29e2d-103">CBasePropertyPage. OnActivate, méthode</span><span class="sxs-lookup"><span data-stu-id="29e2d-103">CBasePropertyPage.OnActivate method</span></span>

<span data-ttu-id="29e2d-104">La `OnActivate` méthode est appelée lorsque la page de propriétés est activée.</span><span class="sxs-lookup"><span data-stu-id="29e2d-104">The `OnActivate` method is called when the property page is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="29e2d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29e2d-105">Syntax</span></span>


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a><span data-ttu-id="29e2d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29e2d-106">Parameters</span></span>

<span data-ttu-id="29e2d-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="29e2d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="29e2d-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29e2d-108">Return value</span></span>

<span data-ttu-id="29e2d-109">L’implémentation de la classe de base retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="29e2d-109">The base-class implementation returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="29e2d-110">Notes</span><span class="sxs-lookup"><span data-stu-id="29e2d-110">Remarks</span></span>

<span data-ttu-id="29e2d-111">La méthode [**CBasePropertyPage :: Activate**](cbasepropertypage-activate.md) appelle la `OnActivate` méthode.</span><span class="sxs-lookup"><span data-stu-id="29e2d-111">The [**CBasePropertyPage::Activate**](cbasepropertypage-activate.md) method calls the `OnActivate` method.</span></span> <span data-ttu-id="29e2d-112">Dans votre classe dérivée, substituez `OnActivate` pour initialiser la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="29e2d-112">In your derived class, override `OnActivate` to initialize the dialog box.</span></span>

## <a name="examples"></a><span data-ttu-id="29e2d-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="29e2d-113">Examples</span></span>

<span data-ttu-id="29e2d-114">L’exemple suivant initialise un contrôle TrackBar.</span><span class="sxs-lookup"><span data-stu-id="29e2d-114">The following example initializes a trackbar control.</span></span> <span data-ttu-id="29e2d-115">Cet exemple suppose que **m \_ pOwningFilter** est un pointeur vers une interface personnalisée sur le filtre associé à la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="29e2d-115">This example assumes that **m\_pOwningFilter** is a pointer to a custom interface on the filter associated with the property page.</span></span> <span data-ttu-id="29e2d-116">(Utilisez la méthode [**CBasePropertyPage :: OnConnect**](cbasepropertypage-onconnect.md) pour initialiser ces pointeurs.)</span><span class="sxs-lookup"><span data-stu-id="29e2d-116">(Use the [**CBasePropertyPage::OnConnect**](cbasepropertypage-onconnect.md) method to initialize such pointers.)</span></span>


```C++
HRESULT CMyProp::OnActivate(void)
{
    ASSERT(m_pOwningFilter != NULL);
    m_pOwningFilter->GetSomeProperty(&m_lOldVal);
    
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0, MAKELONG(0, 100));
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 10, 0);
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lOldVal);
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="29e2d-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29e2d-117">Requirements</span></span>



| <span data-ttu-id="29e2d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29e2d-118">Requirement</span></span> | <span data-ttu-id="29e2d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="29e2d-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29e2d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="29e2d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="29e2d-121"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29e2d-121"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="29e2d-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="29e2d-122">Library</span></span><br/> | <dl> <span data-ttu-id="29e2d-123"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="29e2d-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29e2d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29e2d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29e2d-125">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="29e2d-125">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




