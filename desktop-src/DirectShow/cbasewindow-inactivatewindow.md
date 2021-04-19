---
description: La méthode InactivateWindow désactive la fenêtre. Dans la classe de base, cette méthode masque la fenêtre.
ms.assetid: b575d4fd-dee1-4ae5-abb4-e92ae361e82a
title: Méthode CBaseWindow. InactivateWindow (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InactivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d1c5e925a3d9b510918636a221d5ad6e1b7da736
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542574"
---
# <a name="cbasewindowinactivatewindow-method"></a><span data-ttu-id="6c693-104">Méthode CBaseWindow. InactivateWindow</span><span class="sxs-lookup"><span data-stu-id="6c693-104">CBaseWindow.InactivateWindow method</span></span>

<span data-ttu-id="6c693-105">La `InactivateWindow` méthode désactive la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6c693-105">The `InactivateWindow` method inactivates the window.</span></span> <span data-ttu-id="6c693-106">Dans la classe de base, cette méthode masque la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6c693-106">In the base class, this method hides the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c693-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c693-107">Syntax</span></span>


```C++
virtual HRESULT InactivateWindow();
```



## <a name="parameters"></a><span data-ttu-id="6c693-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c693-108">Parameters</span></span>

<span data-ttu-id="6c693-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="6c693-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6c693-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c693-110">Return value</span></span>

<span data-ttu-id="6c693-111">Retourne l’une des valeurs **HRESULT** indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6c693-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="6c693-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6c693-112">Return code</span></span>                                                                             | <span data-ttu-id="6c693-113">Description</span><span class="sxs-lookup"><span data-stu-id="6c693-113">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="6c693-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6c693-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="6c693-115">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="6c693-115">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="6c693-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="6c693-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="6c693-117">La fenêtre est déjà inactive.</span><span class="sxs-lookup"><span data-stu-id="6c693-117">Window is already inactive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6c693-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c693-118">Requirements</span></span>



| <span data-ttu-id="6c693-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c693-119">Requirement</span></span> | <span data-ttu-id="6c693-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c693-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c693-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c693-121">Header</span></span><br/>  | <dl> <span data-ttu-id="6c693-122"><dt>Winutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c693-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6c693-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6c693-123">Library</span></span><br/> | <dl> <span data-ttu-id="6c693-124"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="6c693-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c693-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c693-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c693-126">**CBaseWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="6c693-126">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




