---
description: Se produit après le redimensionnement du contrôle InkPicture, en particulier après la modification de la valeur de la propriété Width ou Height.
ms.assetid: a5fc6c82-f9c8-4104-8abe-082c47c56be9
title: InkPicture. SizeChanged, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5675d2a581d9e8973b88fa9fb6e213f54c0e283
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952916"
---
# <a name="inkpicturesizechanged-event"></a><span data-ttu-id="df475-103">InkPicture. SizeChanged, événement</span><span class="sxs-lookup"><span data-stu-id="df475-103">InkPicture.SizeChanged event</span></span>

<span data-ttu-id="df475-104">Se produit après le redimensionnement du contrôle [InkPicture](inkpicture-control-reference.md) , en particulier après la modification de la valeur de la propriété [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) ou [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) .</span><span class="sxs-lookup"><span data-stu-id="df475-104">Occurs after the [InkPicture](inkpicture-control-reference.md) control has been resized, specifically, after the [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width) or [**Height**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_height) property value changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="df475-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df475-105">Syntax</span></span>


```C++
void SizeChanged(
  [in] long Left,
  [in] long Top,
  [in] long Right,
  [in] long Bottom
);
```



## <a name="parameters"></a><span data-ttu-id="df475-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df475-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df475-107">À *gauche* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df475-107">*Left* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df475-108">Coordonnée x du côté gauche du contrôle [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="df475-108">The x-coordinate of the left side of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="df475-109">En *haut* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df475-109">*Top* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df475-110">Coordonnée y du haut du contrôle [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="df475-110">The y-coordinate of the top of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="df475-111">À *droite* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df475-111">*Right* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df475-112">Coordonnée x du côté droit du contrôle [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="df475-112">The x-coordinate of the right side of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> <dt>

<span data-ttu-id="df475-113">En *bas* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df475-113">*Bottom* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df475-114">Coordonnée y du bas du contrôle [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="df475-114">The y-coordinate of the bottom of the [InkPicture](inkpicture-control-reference.md) control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df475-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df475-115">Return value</span></span>

<span data-ttu-id="df475-116">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="df475-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df475-117">Notes</span><span class="sxs-lookup"><span data-stu-id="df475-117">Remarks</span></span>

<span data-ttu-id="df475-118">Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="df475-118">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="df475-119">L’interface **\_ IInkPictureEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IPESizeChanged.</span><span class="sxs-lookup"><span data-stu-id="df475-119">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPESizeChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="df475-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df475-120">Requirements</span></span>



| <span data-ttu-id="df475-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df475-121">Requirement</span></span> | <span data-ttu-id="df475-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="df475-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df475-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df475-123">Minimum supported client</span></span><br/> | <span data-ttu-id="df475-124">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="df475-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="df475-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="df475-125">Minimum supported server</span></span><br/> | <span data-ttu-id="df475-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="df475-126">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="df475-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="df475-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="df475-128"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="df475-128"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="df475-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="df475-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="df475-130"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df475-130"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="df475-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df475-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df475-132">InkPicture</span><span class="sxs-lookup"><span data-stu-id="df475-132">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

