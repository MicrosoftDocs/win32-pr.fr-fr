---
description: Se produit après la modification de la propriété ModeAffichage du contrôle InkPicture.
ms.assetid: ae56b5a2-e3e2-468c-a572-a9b46eb1d39d
title: InkPicture. SizeModeChanged, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f270ea141bc8803cbcf1ce4e54b0f73318ed69d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320438"
---
# <a name="inkpicturesizemodechanged-event"></a><span data-ttu-id="d2a7e-103">InkPicture. SizeModeChanged, événement</span><span class="sxs-lookup"><span data-stu-id="d2a7e-103">InkPicture.SizeModeChanged event</span></span>

<span data-ttu-id="d2a7e-104">Se produit après la modification de la propriété [**ModeAffichage**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) du contrôle [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="d2a7e-104">Occurs after the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property of the [InkPicture](inkpicture-control-reference.md) control has been changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a7e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2a7e-105">Syntax</span></span>


```C++
void SizeModeChanged(
  [in] InkPictureSizeMode NewMode,
  [in] InkPictureSizeMode OldMode
);
```



## <a name="parameters"></a><span data-ttu-id="d2a7e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2a7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a7e-107">*NewMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2a7e-107">*NewMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a7e-108">Nouvel État du contrôle [InkPicture](inkpicture-control-reference.md) , en fonction de la nouvelle valeur de la propriété [**ModeAffichage**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .</span><span class="sxs-lookup"><span data-stu-id="d2a7e-108">The new state of the [InkPicture](inkpicture-control-reference.md) control, based on the new value of the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property.</span></span>

</dd> <dt>

<span data-ttu-id="d2a7e-109">*OldMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2a7e-109">*OldMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2a7e-110">Ancien état du contrôle [InkPicture](inkpicture-control-reference.md) , en fonction de l’ancienne valeur de la propriété [**ModeAffichage**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) .</span><span class="sxs-lookup"><span data-stu-id="d2a7e-110">The old state of the [InkPicture](inkpicture-control-reference.md) control, based on the old value of the [**SizeMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_sizemode) property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a7e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2a7e-111">Return value</span></span>

<span data-ttu-id="d2a7e-112">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d2a7e-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2a7e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="d2a7e-113">Remarks</span></span>

<span data-ttu-id="d2a7e-114">Cette méthode d’événement est définie dans l’interface **\_ IInkPictureEvents** .</span><span class="sxs-lookup"><span data-stu-id="d2a7e-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="d2a7e-115">L’interface **\_ IInkPictureEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IPESizeModeChanged.</span><span class="sxs-lookup"><span data-stu-id="d2a7e-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPESizeModeChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2a7e-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2a7e-116">Requirements</span></span>



| <span data-ttu-id="d2a7e-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2a7e-117">Requirement</span></span> | <span data-ttu-id="d2a7e-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2a7e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a7e-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2a7e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d2a7e-120">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2a7e-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="d2a7e-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2a7e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d2a7e-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2a7e-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="d2a7e-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2a7e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2a7e-124"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="d2a7e-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="d2a7e-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d2a7e-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="d2a7e-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2a7e-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="d2a7e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2a7e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2a7e-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="d2a7e-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

