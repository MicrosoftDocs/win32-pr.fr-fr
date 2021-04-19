---
description: Fonction de créateur statique qui peut créer un XamlUIPresenter pour une surface de rendu dans une application de bureau.
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: CreateXamlUIPresenter fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateXamlUIPresenter
api_type:
- DllExport
api_location:
- Windows.UI.Xaml.dll
ms.openlocfilehash: f9561a179ec4501406e26cb2bbc38ea69b64b979
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532278"
---
# <a name="createxamluipresenter-function"></a><span data-ttu-id="d540f-103">CreateXamlUIPresenter fonction)</span><span class="sxs-lookup"><span data-stu-id="d540f-103">CreateXamlUIPresenter function</span></span>

<span data-ttu-id="d540f-104">Fonction de créateur statique qui peut créer un [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) pour une surface de rendu dans une application de bureau.</span><span class="sxs-lookup"><span data-stu-id="d540f-104">A static creator function that can create a [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) for a render surface in a desktop app.</span></span>

## <a name="syntax"></a><span data-ttu-id="d540f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d540f-105">Syntax</span></span>


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a><span data-ttu-id="d540f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d540f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d540f-107">*pPresentSite* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d540f-107">*pPresentSite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d540f-108">Une interface d’hébergement existante.</span><span class="sxs-lookup"><span data-stu-id="d540f-108">An existing hosting interface.</span></span> <span data-ttu-id="d540f-109">Consultez **IViewObjectPresentNotifySite** dans la documentation d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="d540f-109">See **IViewObjectPresentNotifySite** in Internet Explorer documentation.</span></span>

</dd> <dt>

<span data-ttu-id="d540f-110">*ppPresenter* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d540f-110">*ppPresenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d540f-111">Interface **\[ exclusiveto \]** pour un [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).</span><span class="sxs-lookup"><span data-stu-id="d540f-111">The **\[exclusiveto\]** interface for a [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d540f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d540f-112">Return value</span></span>

<span data-ttu-id="d540f-113">**HRESULT** standard, **S \_ OK** pour réussite.</span><span class="sxs-lookup"><span data-stu-id="d540f-113">A standard **HResult**, **S\_OK** for success.</span></span>

## <a name="remarks"></a><span data-ttu-id="d540f-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d540f-114">Remarks</span></span>

<span data-ttu-id="d540f-115">L’appel de cette méthode requiert un **DllImport** de Windows.UI.Xaml.dll.</span><span class="sxs-lookup"><span data-stu-id="d540f-115">Calling this method requires a **DllImport** from Windows.UI.Xaml.dll.</span></span>

<span data-ttu-id="d540f-116">Vous ne pouvez pas appeler cette méthode à partir d’une application du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="d540f-116">You cannot call this method from a Windows Store app.</span></span>

## <a name="requirements"></a><span data-ttu-id="d540f-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d540f-117">Requirements</span></span>



| <span data-ttu-id="d540f-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d540f-118">Requirement</span></span> | <span data-ttu-id="d540f-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d540f-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d540f-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="d540f-120">Header</span></span><br/> | <dl> <span data-ttu-id="d540f-121"><dt>Windows. UI. Xaml-coretypes. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d540f-121"><dt>Windows.ui.xaml-coretypes.idl</dt></span></span> </dl> |
| <span data-ttu-id="d540f-122">DLL</span><span class="sxs-lookup"><span data-stu-id="d540f-122">DLL</span></span><br/>    | <dl> <span data-ttu-id="d540f-123"><dt>Windows.UI.Xaml.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d540f-123"><dt>Windows.UI.Xaml.dll</dt></span></span> </dl>           |



## <a name="see-also"></a><span data-ttu-id="d540f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d540f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d540f-125">**XamlUIPresenter**</span><span class="sxs-lookup"><span data-stu-id="d540f-125">**XamlUIPresenter**</span></span>](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
