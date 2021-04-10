---
description: Se produit lorsque la sélection d’encre dans le contrôle InkPicture va être modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de sélection.
ms.assetid: a8ae30ff-fb0d-44cc-a5d3-295117addafd
title: InkPicture. SelectionChanging, événement (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b8a35d57aeb9367bb9d30647cb074a7e0e6fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868289"
---
# <a name="inkpictureselectionchanging-event"></a><span data-ttu-id="6a0db-103">InkPicture. SelectionChanging, événement</span><span class="sxs-lookup"><span data-stu-id="6a0db-103">InkPicture.SelectionChanging event</span></span>

<span data-ttu-id="6a0db-104">Se produit lorsque la sélection d’encre dans le contrôle [InkPicture](inkpicture-control-reference.md) va être modifiée, par exemple par le biais de modifications de l’interface utilisateur, de procédures couper-coller ou de la propriété de [**sélection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="6a0db-104">Occurs when the selection of ink within the [InkPicture](inkpicture-control-reference.md) control is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a0db-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a0db-105">Syntax</span></span>


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a><span data-ttu-id="6a0db-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a0db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a0db-107">*NewSelection* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a0db-107">*NewSelection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a0db-108">Nouvelle collection de [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) qui est sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="6a0db-108">The new collection of [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) that is being selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a0db-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a0db-109">Return value</span></span>

<span data-ttu-id="6a0db-110">Cet événement ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="6a0db-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a0db-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6a0db-111">Remarks</span></span>

<span data-ttu-id="6a0db-112">Cette méthode d’événement est définie dans les dispinterfaces **\_ IInkOverlayEvents** et **\_ IInkPictureEvents** (dispinterfaces) avec l’ID DISPID \_ IOESelectionChanging.</span><span class="sxs-lookup"><span data-stu-id="6a0db-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanging.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a0db-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a0db-113">Requirements</span></span>



| <span data-ttu-id="6a0db-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a0db-114">Requirement</span></span> | <span data-ttu-id="6a0db-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a0db-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a0db-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a0db-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6a0db-117">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a0db-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6a0db-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a0db-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6a0db-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a0db-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6a0db-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a0db-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a0db-121"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="6a0db-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6a0db-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6a0db-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="6a0db-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a0db-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6a0db-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a0db-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a0db-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="6a0db-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="6a0db-126">[**Propriété de sélection, \[ contrôle InkPicture\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="6a0db-126">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> </dl>

 

