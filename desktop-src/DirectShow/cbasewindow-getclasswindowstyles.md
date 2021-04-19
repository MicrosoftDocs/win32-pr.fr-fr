---
description: La méthode GetClassWindowStyles récupère les styles de classe et les styles de fenêtre de la fenêtre.
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: Méthode CBaseWindow. GetClassWindowStyles (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetClassWindowStyles
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a34332f84a91ee88d61ee5f29f0b6a0b0cc44714
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541109"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a><span data-ttu-id="6c6d4-103">Méthode CBaseWindow. GetClassWindowStyles</span><span class="sxs-lookup"><span data-stu-id="6c6d4-103">CBaseWindow.GetClassWindowStyles method</span></span>

<span data-ttu-id="6c6d4-104">La `GetClassWindowStyles` méthode récupère les styles de classe et les styles de fenêtre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6c6d4-104">The `GetClassWindowStyles` method retrieves the window's class styles and window styles.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c6d4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c6d4-105">Syntax</span></span>


```C++
virtual LPTSTR GetClassWindowStyles(
   DWORD *pClassStyles,
   DWORD *pWindowStyles,
   DWORD *pWindowStylesEx
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="6c6d4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c6d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c6d4-107">*pClassStyles*</span><span class="sxs-lookup"><span data-stu-id="6c6d4-107">*pClassStyles*</span></span> 
</dt> <dd>

<span data-ttu-id="6c6d4-108">Pointeur vers une variable qui reçoit les styles de classe.</span><span class="sxs-lookup"><span data-stu-id="6c6d4-108">Pointer to a variable that receives the class styles.</span></span>

</dd> <dt>

<span data-ttu-id="6c6d4-109">*pWindowStyles*</span><span class="sxs-lookup"><span data-stu-id="6c6d4-109">*pWindowStyles*</span></span> 
</dt> <dd>

<span data-ttu-id="6c6d4-110">Pointeur vers une variable qui reçoit les styles de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6c6d4-110">Pointer to a variable that receives the window styles.</span></span>

</dd> <dt>

<span data-ttu-id="6c6d4-111">*pWindowStylesEx*</span><span class="sxs-lookup"><span data-stu-id="6c6d4-111">*pWindowStylesEx*</span></span> 
</dt> <dd>

<span data-ttu-id="6c6d4-112">Pointeur vers une variable qui reçoit les styles de fenêtre étendus.</span><span class="sxs-lookup"><span data-stu-id="6c6d4-112">Pointer to a variable that receives the extended window styles.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c6d4-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c6d4-113">Return value</span></span>

<span data-ttu-id="6c6d4-114">Retourne une chaîne de texte statique qui contient le nom de la classe.</span><span class="sxs-lookup"><span data-stu-id="6c6d4-114">Returns a static text string that contains the class name.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c6d4-115">Notes</span><span class="sxs-lookup"><span data-stu-id="6c6d4-115">Remarks</span></span>

<span data-ttu-id="6c6d4-116">La méthode [**CBaseWindow ::P reparewindow**](cbasewindow-preparewindow.md) appelle cette méthode pour récupérer les styles de classe et les styles de fenêtre de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6c6d4-116">The [**CBaseWindow::PrepareWindow**](cbasewindow-preparewindow.md) method calls this method to retrieve the window's class styles and window styles.</span></span>

<span data-ttu-id="6c6d4-117">Cette méthode est virtuelle pure ; la classe dérivée doit l’implémenter.</span><span class="sxs-lookup"><span data-stu-id="6c6d4-117">This method is pure virtual; the derived class must implement it.</span></span> <span data-ttu-id="6c6d4-118">L’exemple suivant illustre une implémentation possible :</span><span class="sxs-lookup"><span data-stu-id="6c6d4-118">The following example shows a possible implementation:</span></span>


```C++
LPTSTR CMyWindowClass::GetClassWindowStyles(DWORD *pClassStyles,
                                            DWORD *pWindowStyles,
                                            DWORD *pWindowStylesEx)
{
    *pClassStyles = CS_HREDRAW | CS_VREDRAW;
    *pWindowStyles = WS_OVERLAPPEDWINDOW | WS_CLIPCHILDREN;
    *pWindowStylesEx = WS_EX_WINDOWEDGE;
    return TEXT("MyWindowClass");
}
```



<span data-ttu-id="6c6d4-119">L’objet utilise le style de classe pour le membre **lpszClassName** d’une structure WNDCLASS, qu’il transmet à la fonction **registerClass** .</span><span class="sxs-lookup"><span data-stu-id="6c6d4-119">The object uses the class style for the **lpszClassName** member of a WNDCLASS structure, which it passes to the **RegisterClass** function.</span></span> <span data-ttu-id="6c6d4-120">L’objet utilise les styles de fenêtre pour les paramètres *dwExStyle* et *dwStyle* de la fonction **CreateWindowEx** .</span><span class="sxs-lookup"><span data-stu-id="6c6d4-120">The object uses the window styles for the *dwExStyle* and *dwStyle* parameters of the **CreateWindowEx** function.</span></span> <span data-ttu-id="6c6d4-121">Pour plus d’informations, consultez le kit de développement Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="6c6d4-121">For more information, see the Platform SDK.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c6d4-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c6d4-122">Requirements</span></span>



| <span data-ttu-id="6c6d4-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c6d4-123">Requirement</span></span> | <span data-ttu-id="6c6d4-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c6d4-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c6d4-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c6d4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="6c6d4-126"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c6d4-126"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6c6d4-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6c6d4-127">Library</span></span><br/> | <dl> <span data-ttu-id="6c6d4-128"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6c6d4-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c6d4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c6d4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c6d4-130">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="6c6d4-130">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




