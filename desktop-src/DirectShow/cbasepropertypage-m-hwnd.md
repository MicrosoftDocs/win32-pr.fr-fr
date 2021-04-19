---
description: La \_ variable de membre HWND de m contient un handle vers la fenêtre de dialogue. Cette variable membre est initialisée une fois que l’objet a créé la fenêtre de boîte de dialogue, lorsque la fonction CreateDialogParam retourne.
ms.assetid: f985c06f-a1f9-458b-b9f3-cabe9f583313
title: 'Membre CBasePropertyPage :: m_hwnd (Cprop. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hwnd
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94a249d9b8f887750360ceb83f876f315d4fd43f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542552"
---
# <a name="cbasepropertypagem_hwnd-member"></a><span data-ttu-id="c0d12-104">CBasePropertyPage :: m, \_ membre HWND</span><span class="sxs-lookup"><span data-stu-id="c0d12-104">CBasePropertyPage::m\_hwnd member</span></span>

<span data-ttu-id="c0d12-105">La `m_hwnd` variable membre contient un handle vers la fenêtre de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="c0d12-105">The `m_hwnd` member variable contains a handle to the dialog window.</span></span> <span data-ttu-id="c0d12-106">Cette variable membre est initialisée une fois que l’objet a créé la fenêtre de boîte de dialogue, lorsque la fonction **CreateDialogParam** retourne.</span><span class="sxs-lookup"><span data-stu-id="c0d12-106">This member variable is initialized after the object creates the dialog window, when the **CreateDialogParam** function returns.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0d12-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0d12-107">Syntax</span></span>


```C++
HWND m_hwnd;
```



## <a name="requirements"></a><span data-ttu-id="c0d12-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0d12-108">Requirements</span></span>



| <span data-ttu-id="c0d12-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0d12-109">Requirement</span></span> | <span data-ttu-id="c0d12-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0d12-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0d12-111">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0d12-111">Header</span></span><br/>  | <dl> <span data-ttu-id="c0d12-112"><dt>Cprop. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0d12-112"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="c0d12-113">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c0d12-113">Library</span></span><br/> | <dl> <span data-ttu-id="c0d12-114"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="c0d12-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0d12-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0d12-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0d12-116">**CBasePropertyPage, classe**</span><span class="sxs-lookup"><span data-stu-id="c0d12-116">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




