---
description: Obsolète. Le PenInputPanel a été remplacé par le panneau de saisie de texte (TIP). Se produit lorsque le focus d’entrée est modifié avant que l’objet PenInputPanel ait pu insérer une entrée d’utilisateur dans le contrôle attaché.
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: Événement PenInputPanel. InputFailed (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 198c2b466dc03357d9851d7c8a6b7f44c6bf6884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529471"
---
# <a name="peninputpanelinputfailed-event"></a><span data-ttu-id="3c104-104">Événement PenInputPanel. InputFailed</span><span class="sxs-lookup"><span data-stu-id="3c104-104">PenInputPanel.InputFailed event</span></span>

<span data-ttu-id="3c104-105">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="3c104-105">Deprecated.</span></span> <span data-ttu-id="3c104-106">Le [**PenInputPanel**](peninputpanel-class.md) a été remplacé par le [panneau de saisie de texte (TIP)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="3c104-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="3c104-107">Se produit lorsque le focus d’entrée est modifié avant que l’objet [**PenInputPanel**](peninputpanel-class.md) ait pu insérer une entrée d’utilisateur dans le contrôle attaché.</span><span class="sxs-lookup"><span data-stu-id="3c104-107">Occurs when input focus changes before the [**PenInputPanel**](peninputpanel-class.md) object was able to insert user input into the attached control.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c104-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c104-108">Syntax</span></span>


```C++
HRESULT InputFailed(
  [in] long  hWnd,
  [in] long  Key,
  [in] BSTR  Text,
  [in] short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="3c104-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c104-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c104-110">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c104-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c104-111">Handle de fenêtre du contrôle qui a appelé l’objet [**PenInputPanel**](peninputpanel-class.md) .</span><span class="sxs-lookup"><span data-stu-id="3c104-111">The window handle of the control that invoked the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="3c104-112">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c104-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c104-113">Touche virtuelle correspondant à la touche enfoncée.</span><span class="sxs-lookup"><span data-stu-id="3c104-113">The virtual key corresponding to the key pressed.</span></span>

</dd> <dt>

<span data-ttu-id="3c104-114">*Texte* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c104-114">*Text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c104-115">Chaîne qui doit être insérée dans le contrôle représenté par le paramètre *HWND* lorsque l’événement **InputFailed** a été déclenché.</span><span class="sxs-lookup"><span data-stu-id="3c104-115">The string that was to be inserted into the control represented by the *hWnd* parameter when the **InputFailed** event was raised.</span></span>

<span data-ttu-id="3c104-116">Pour plus d’informations sur le type de données BSTR, consultez [utilisation de la bibliothèque com](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="3c104-116">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="3c104-117">*ShiftKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c104-117">*ShiftKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c104-118">État des modificateurs de clavier, y compris les touches Maj, Maj, CTRL et ALT.</span><span class="sxs-lookup"><span data-stu-id="3c104-118">The state of the keyboard modifiers, including SHIFT, CAPS, CTRL, and ALT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c104-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c104-119">Return value</span></span>

<span data-ttu-id="3c104-120">Si cet événement a la valeur, il retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3c104-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3c104-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3c104-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c104-122">Notes</span><span class="sxs-lookup"><span data-stu-id="3c104-122">Remarks</span></span>

<span data-ttu-id="3c104-123">L’événement **InputFailed** se produit lorsque le focus d’entrée est modifié avant l’insertion de l’entrée utilisateur dans le contrôle attaché.</span><span class="sxs-lookup"><span data-stu-id="3c104-123">The **InputFailed** event occurs when input focus changes before user input was inserted into the attached control.</span></span> <span data-ttu-id="3c104-124">Par exemple, si l’utilisateur entre de l’encre dans le bloc d’écriture, puis appuie sur un autre contrôle d’édition avant que le module de reconnaissance ait pu terminer, cet événement se déclenche.</span><span class="sxs-lookup"><span data-stu-id="3c104-124">For example, if the user enters ink into the writing pad, then taps on another edit control before the recognizer has had a chance to finish, this event fires.</span></span>

<span data-ttu-id="3c104-125">À l’aide du handle de fenêtre passé dans cet événement, vous pouvez choisir d’insérer le texte vous-même lorsque cet événement se produit.</span><span class="sxs-lookup"><span data-stu-id="3c104-125">Using the window handle passed into this event, you can choose to insert the text yourself when this event occurs.</span></span>

> [!Note]  
> <span data-ttu-id="3c104-126">À compter de Microsoft Windows XP Édition Tablet PC 2005, l’événement **InputFailed** ne s’applique plus.</span><span class="sxs-lookup"><span data-stu-id="3c104-126">Starting with Microsoft Windows XP Tablet PC Edition 2005, the **InputFailed** event no longer applies.</span></span> <span data-ttu-id="3c104-127">Le texte est toujours inséré avant la modification du focus.</span><span class="sxs-lookup"><span data-stu-id="3c104-127">Text is always inserted before focus changes.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c104-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c104-128">Requirements</span></span>



| <span data-ttu-id="3c104-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c104-129">Requirement</span></span> | <span data-ttu-id="3c104-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c104-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c104-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c104-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3c104-132">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c104-132">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3c104-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c104-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3c104-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c104-134">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3c104-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c104-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c104-136"><dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3c104-136"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3c104-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3c104-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="3c104-138"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c104-138"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3c104-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c104-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c104-140">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="3c104-140">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




