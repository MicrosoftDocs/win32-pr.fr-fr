---
description: La méthode OnReceiveMessage est appelée lorsque la boîte de dialogue reçoit un message.
ms.assetid: ea93500d-fd0f-4820-a54a-a186c40899ad
title: Méthode CBasePropertyPage. OnReceiveMessage (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69d9da708d45524d15f735273d47f242104ee22f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520809"
---
# <a name="cbasepropertypageonreceivemessage-method"></a><span data-ttu-id="ceb74-103">Méthode CBasePropertyPage. OnReceiveMessage</span><span class="sxs-lookup"><span data-stu-id="ceb74-103">CBasePropertyPage.OnReceiveMessage method</span></span>

<span data-ttu-id="ceb74-104">La `OnReceiveMessage` méthode est appelée lorsque la boîte de dialogue reçoit un message.</span><span class="sxs-lookup"><span data-stu-id="ceb74-104">The `OnReceiveMessage` method is called when the dialog box receives a message.</span></span>

## <a name="syntax"></a><span data-ttu-id="ceb74-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ceb74-105">Syntax</span></span>


```C++
virtual INT_PTR OnReceiveMessage(
   HWND   hwnd,
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="ceb74-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ceb74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ceb74-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="ceb74-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="ceb74-108">Handle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="ceb74-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="ceb74-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="ceb74-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="ceb74-110">Message.</span><span class="sxs-lookup"><span data-stu-id="ceb74-110">Message.</span></span>

</dd> <dt>

<span data-ttu-id="ceb74-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ceb74-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ceb74-112">Premier paramètre de message.</span><span class="sxs-lookup"><span data-stu-id="ceb74-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ceb74-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ceb74-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ceb74-114">Deuxième paramètre de message.</span><span class="sxs-lookup"><span data-stu-id="ceb74-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ceb74-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ceb74-115">Return value</span></span>

<span data-ttu-id="ceb74-116">Retourne une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="ceb74-116">Returns a Boolean value.</span></span> <span data-ttu-id="ceb74-117">La procédure de dialogue retourne cette valeur ; Pour plus d’informations, consultez la documentation du kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="ceb74-117">The dialog procedure returns this value; for more information, see the Platform SDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ceb74-118">Notes</span><span class="sxs-lookup"><span data-stu-id="ceb74-118">Remarks</span></span>

<span data-ttu-id="ceb74-119">L’implémentation de la classe de base appelle **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="ceb74-119">The base-class implementation calls **DefWindowProc**.</span></span> <span data-ttu-id="ceb74-120">Substituez cette méthode pour gérer les messages liés aux contrôles de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ceb74-120">Override this method to handle messages that relate to the dialog controls.</span></span> <span data-ttu-id="ceb74-121">Si la méthode de substitution ne gère pas un message particulier, elle doit appeler la méthode de la classe de base.</span><span class="sxs-lookup"><span data-stu-id="ceb74-121">If the overriding method does not handle a particular message, it should call the base-class method.</span></span>

<span data-ttu-id="ceb74-122">Si l’utilisateur modifie des propriétés via les contrôles de boîte de dialogue, affectez la valeur **true** à l’indicateur [**CBasePropertyPage :: m \_ bDirty**](cbasepropertypage-m-bdirty.md) .</span><span class="sxs-lookup"><span data-stu-id="ceb74-122">If the user changes any properties via the dialog controls, set the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag to **TRUE**.</span></span> <span data-ttu-id="ceb74-123">Appelez ensuite la méthode **IPropertyPageSite :: OnStatusChange** sur le pointeur [**CBasePropertyPage :: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) pour informer le frame.</span><span class="sxs-lookup"><span data-stu-id="ceb74-123">Then call the **IPropertyPageSite::OnStatusChange** method on the [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) pointer to inform the frame.</span></span>

## <a name="examples"></a><span data-ttu-id="ceb74-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="ceb74-124">Examples</span></span>

<span data-ttu-id="ceb74-125">L’exemple suivant répond à un clic sur un bouton en mettant à jour une variable membre, qui est supposée être définie dans la classe dérivée.</span><span class="sxs-lookup"><span data-stu-id="ceb74-125">The following example responds to a button click by updating a member variable, which is assumed to be defined in the derived class.</span></span> <span data-ttu-id="ceb74-126">Cet exemple montre également une fonction d’assistance pour définir l’état d’intégrité de la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="ceb74-126">This example also shows a helper function for setting the property page's dirty status.</span></span>


```C++
INT_PTR CMyProp::OnReceiveMessage(HWND hwnd,
  UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_BUTTON1)
        {
            m_lNewVal = GetDlgItemInt(m_Dlg, IDC_EDIT1, 0, TRUE);
            SetDirty();
            return (INT_PTR)TRUE;
        }
        break;
    } // switch

    // Did not handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd, uMsg, wParam, lParam);
}

// Helper function to update the dirty status.
void CMyProp::SetDirty()
{
    m_bDirty = TRUE;
    if (m_pPageSite)
    {
        m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
    }
}
```



## <a name="requirements"></a><span data-ttu-id="ceb74-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ceb74-127">Requirements</span></span>



| <span data-ttu-id="ceb74-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ceb74-128">Requirement</span></span> | <span data-ttu-id="ceb74-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="ceb74-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ceb74-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="ceb74-130">Header</span></span><br/>  | <dl> <span data-ttu-id="ceb74-131"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ceb74-131"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="ceb74-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ceb74-132">Library</span></span><br/> | <dl> <span data-ttu-id="ceb74-133"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="ceb74-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ceb74-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ceb74-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ceb74-135">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="ceb74-135">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




