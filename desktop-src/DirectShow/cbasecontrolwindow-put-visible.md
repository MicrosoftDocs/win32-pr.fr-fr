---
description: La \_ méthode put visible permet d’afficher ou de masquer la fenêtre.
ms.assetid: 77e8d071-f876-4e35-945c-d1daf96ad02b
title: Méthode CBaseControlWindow.put_Visible (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_Visible
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf713b4ccb9932b1201e7ced40fddcd87407ef6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543961"
---
# <a name="cbasecontrolwindowput_visible-method"></a><span data-ttu-id="0c20a-103">Méthode visible CBaseControlWindow. put \_</span><span class="sxs-lookup"><span data-stu-id="0c20a-103">CBaseControlWindow.put\_Visible method</span></span>

<span data-ttu-id="0c20a-104">La `put_Visible` méthode permet d’afficher ou de masquer la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="0c20a-104">The `put_Visible` method makes shows or hides the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c20a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c20a-105">Syntax</span></span>


```C++
HRESULT put_Visible(
   long Visible
);
```



## <a name="parameters"></a><span data-ttu-id="0c20a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c20a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c20a-107">*Visible*</span><span class="sxs-lookup"><span data-stu-id="0c20a-107">*Visible*</span></span> 
</dt> <dd>

<span data-ttu-id="0c20a-108">Indicateur booléen Automation (0 signifie que la fenêtre est masquée, 1 signifie que la fenêtre est affichée).</span><span class="sxs-lookup"><span data-stu-id="0c20a-108">Automation Boolean flag (0 means window is hidden,  1 means window is shown).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c20a-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0c20a-109">Return value</span></span>

<span data-ttu-id="0c20a-110">Retourne une valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0c20a-110">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c20a-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c20a-111">Requirements</span></span>



| <span data-ttu-id="0c20a-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c20a-112">Requirement</span></span> | <span data-ttu-id="0c20a-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c20a-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c20a-114">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c20a-114">Header</span></span><br/>  | <dl> <span data-ttu-id="0c20a-115"><dt>Ctlutil. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c20a-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0c20a-116">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0c20a-116">Library</span></span><br/> | <dl> <span data-ttu-id="0c20a-117"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="0c20a-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c20a-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c20a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c20a-119">**CBaseControlWindow, classe**</span><span class="sxs-lookup"><span data-stu-id="0c20a-119">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




