---
description: Se produit lorsque l’utilisateur appuie sur une touche et la relâche, tandis que le contrôle InkEdit a le focus.
ms.assetid: 8284ab41-dfac-4da2-b101-6968a43b15d7
title: Événement InkEdit. KeyPress (Y2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e49264f82b2cfe3c6998666339f08340a540791
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523271"
---
# <a name="inkeditkeypress-event"></a><span data-ttu-id="5d9a4-103">Événement InkEdit. KeyPress</span><span class="sxs-lookup"><span data-stu-id="5d9a4-103">InkEdit.KeyPress event</span></span>

<span data-ttu-id="5d9a4-104">Se produit lorsque l’utilisateur appuie sur une touche et la relâche, tandis que le contrôle [InkEdit](inkedit-control-reference.md) a le focus.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-104">Occurs when the user presses and releases a key while the [InkEdit](inkedit-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d9a4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d9a4-105">Syntax</span></span>


```C++
HRESULT KeyPress(
   Long *Char
);
```



## <a name="parameters"></a><span data-ttu-id="5d9a4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d9a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d9a4-107">*Char*</span><span class="sxs-lookup"><span data-stu-id="5d9a4-107">*Char*</span></span> 
</dt> <dd>

<span data-ttu-id="5d9a4-108">Entier qui retourne un code de KeyANSI numérique standard.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-108">An integer that returns a standard numeric ANSI keycode.</span></span> <span data-ttu-id="5d9a4-109">Le paramètre *char* est passé par référence ; la modification de celui-ci envoie un caractère différent au contrôle.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-109">The *Char* parameter is passed by reference; changing it sends a different character to the control.</span></span> <span data-ttu-id="5d9a4-110">La modification du paramètre *char* en 0 annule l’événement.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-110">Changing the *Char* parameter to 0 cancels the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d9a4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d9a4-111">Return value</span></span>

<span data-ttu-id="5d9a4-112">Si cet événement a la valeur, il retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-112">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5d9a4-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d9a4-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d9a4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="5d9a4-114">Remarks</span></span>

<span data-ttu-id="5d9a4-115">Cette méthode d’événement est définie dans l’interface **\_ IInkEditEvents** .</span><span class="sxs-lookup"><span data-stu-id="5d9a4-115">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="5d9a4-116">L’interface **\_ IInkEditEvents** implémente l’interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) avec un identificateur de DISPID \_ IeeKeyPress.</span><span class="sxs-lookup"><span data-stu-id="5d9a4-116">The **\_IInkEditEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IeeKeyPress.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d9a4-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d9a4-117">Requirements</span></span>



| <span data-ttu-id="5d9a4-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d9a4-118">Requirement</span></span> | <span data-ttu-id="5d9a4-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d9a4-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d9a4-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d9a4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5d9a4-121">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d9a4-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="5d9a4-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d9a4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5d9a4-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d9a4-123">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="5d9a4-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d9a4-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d9a4-125"><dt>« Y2. h » (nécessite également l' \_ entrée i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5d9a4-125"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5d9a4-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5d9a4-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="5d9a4-127"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d9a4-127"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="5d9a4-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d9a4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d9a4-129">InkEdit</span><span class="sxs-lookup"><span data-stu-id="5d9a4-129">InkEdit</span></span>](inkedit-control-reference.md)
</dt> <dt>

<span data-ttu-id="5d9a4-130">[**KeyOut, événement \[ InkEdit, contrôle\]**](inkedit-keydown.md)</span><span class="sxs-lookup"><span data-stu-id="5d9a4-130">[**KeyDown Event \[InkEdit Control\]**](inkedit-keydown.md)</span></span>
</dt> <dt>

<span data-ttu-id="5d9a4-131">[**Événement KeyUp \[ contrôle InkEdit\]**](inkedit-keyup.md)</span><span class="sxs-lookup"><span data-stu-id="5d9a4-131">[**KeyUp Event \[InkEdit Control\]**](inkedit-keyup.md)</span></span>
</dt> </dl>

 

