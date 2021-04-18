---
description: 'La méthode Show affiche ou masque la boîte de dialogue. Cette méthode implémente la méthode IPropertyPage :: Show.'
ms.assetid: 03796779-ed41-4b68-852d-6b1849a9dc10
title: CBasePropertyPage. Show, méthode (Cprop. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Show
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1dadd1c187773df3ca41ac0e1e4daf06fb54761b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526359"
---
# <a name="cbasepropertypageshow-method"></a><span data-ttu-id="0c191-104">CBasePropertyPage. Show, méthode</span><span class="sxs-lookup"><span data-stu-id="0c191-104">CBasePropertyPage.Show method</span></span>

<span data-ttu-id="0c191-105">La `Show` méthode affiche ou masque la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="0c191-105">The `Show` method shows or hides the dialog box.</span></span> <span data-ttu-id="0c191-106">Cette méthode implémente la méthode [IPropertyPage :: Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .</span><span class="sxs-lookup"><span data-stu-id="0c191-106">This method implements the [IPropertyPage::Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c191-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c191-107">Syntax</span></span>

```C++
HRESULT Show(
   UINT nCmdShow
);
```
## <a name="parameters"></a><span data-ttu-id="0c191-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c191-108">Parameters</span></span>

<span data-ttu-id="0c191-109">*nCmdShow*</span><span class="sxs-lookup"><span data-stu-id="0c191-109">*nCmdShow*</span></span>

<span data-ttu-id="0c191-110">Type : **[uint](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0c191-110">Type: **[UINT](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0c191-111">Valeur qui spécifie s’il faut afficher ou masquer la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0c191-111">Value that specifies whether to show or hide the window.</span></span> <span data-ttu-id="0c191-112">Pour plus d’informations, consultez la méthode [IPropertyPage :: Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) .</span><span class="sxs-lookup"><span data-stu-id="0c191-112">For more information, see the [IPropertyPage::Show](/windows/win32/api/ocidl/nf-ocidl-ipropertypage-show) method.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c191-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c191-113">Return value</span></span>

<span data-ttu-id="0c191-114">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0c191-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0c191-115">Les valeurs possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="0c191-115">Possible values include the following.</span></span>

| <span data-ttu-id="0c191-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0c191-116">Return code</span></span>                                                                                  | <span data-ttu-id="0c191-117">Description</span><span class="sxs-lookup"><span data-stu-id="0c191-117">Description</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="0c191-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0c191-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0c191-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="0c191-119">Success.</span></span><br/>            |
| <dl> <span data-ttu-id="0c191-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0c191-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0c191-121">Argument non valide.</span><span class="sxs-lookup"><span data-stu-id="0c191-121">Invalid argument.</span></span><br/>   |
| <dl> <span data-ttu-id="0c191-122"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="0c191-122"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="0c191-123">Erreur inattendue.</span><span class="sxs-lookup"><span data-stu-id="0c191-123">Unexpected failure.</span></span><br/> |

## <a name="requirements"></a><span data-ttu-id="0c191-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c191-124">Requirements</span></span>

| <span data-ttu-id="0c191-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c191-125">Requirement</span></span> | <span data-ttu-id="0c191-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c191-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c191-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c191-127">Header</span></span>  | <dl> <span data-ttu-id="0c191-128"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c191-128"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="0c191-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0c191-129">Library</span></span> | <dl> <span data-ttu-id="0c191-130"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0c191-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="0c191-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c191-131">See also</span></span>

[<span data-ttu-id="0c191-132">CBasePropertyPage, classe</span><span class="sxs-lookup"><span data-stu-id="0c191-132">CBasePropertyPage Class</span></span>](cbasepropertypage.md)
