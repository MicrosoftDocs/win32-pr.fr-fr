---
title: Méthode ISoftKbd CreateSoftKeyboardWindow (Softkbdc. h)
description: La méthode ISoftKbd CreateSoftKeyboardWindow crée une fenêtre de clavier temporaire.
ms.assetid: e9aa9d88-d0bb-407f-9b53-98c8747be5d3
keywords:
- Infrastructure des services de texte de méthode CreateSoftKeyboardWindow
- CreateSoftKeyboardWindow méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode CreateSoftKeyboardWindow
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ed6f9f91f335945d40dd0b995226a400965ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508994"
---
# <a name="isoftkbdcreatesoftkeyboardwindow-method"></a><span data-ttu-id="e5828-106">ISoftKbd :: CreateSoftKeyboardWindow, méthode</span><span class="sxs-lookup"><span data-stu-id="e5828-106">ISoftKbd::CreateSoftKeyboardWindow method</span></span>

<span data-ttu-id="e5828-107">La méthode **ISoftKbd :: CreateSoftKeyboardWindow** crée une fenêtre de clavier temporaire.</span><span class="sxs-lookup"><span data-stu-id="e5828-107">The **ISoftKbd::CreateSoftKeyboardWindow** method creates a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5828-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5828-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardWindow(
  [in] HWND          hOwner,
  [in] TITLEBAR_TYPE Titlebar_type,
  [in] INT           xPos,
  [in] INT           yPos,
  [in] INT           width,
  [in] INT           height
);
```



## <a name="parameters"></a><span data-ttu-id="e5828-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5828-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5828-110">*hOwner* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5828-110">*hOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5828-111">Handle de la fenêtre qui contient le clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="e5828-111">Handle of the window to contain the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="e5828-112">*\_ Type de TitleBar* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5828-112">*Titlebar\_type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5828-113">Type de barre de titre de la fenêtre du clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="e5828-113">Type of title bar for the soft keyboard window.</span></span> <span data-ttu-id="e5828-114">Les types possibles sont définis par l’énumération de [**\_ type TITLEBAR**](titlebar-type.md) .</span><span class="sxs-lookup"><span data-stu-id="e5828-114">Possible types are defined by the [**TITLEBAR\_TYPE**](titlebar-type.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="e5828-115">*xpos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5828-115">*xPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5828-116">Position x du coin supérieur gauche de la fenêtre de clavier temporaire.</span><span class="sxs-lookup"><span data-stu-id="e5828-116">The x position of the upper left corner of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="e5828-117">*Posy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5828-117">*yPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5828-118">Position y du coin supérieur gauche de la fenêtre de clavier temporaire.</span><span class="sxs-lookup"><span data-stu-id="e5828-118">The y position of the upper left corner of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="e5828-119">*largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5828-119">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5828-120">Largeur de la fenêtre de clavier temporaire.</span><span class="sxs-lookup"><span data-stu-id="e5828-120">The width of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="e5828-121">*hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e5828-121">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5828-122">Hauteur de la fenêtre du clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="e5828-122">The height of the soft keyboard window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5828-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e5828-123">Return value</span></span>

<span data-ttu-id="e5828-124">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="e5828-124">This method can return one of these values.</span></span>



| <span data-ttu-id="e5828-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5828-125">Value</span></span>                                                                                        | <span data-ttu-id="e5828-126">Description</span><span class="sxs-lookup"><span data-stu-id="e5828-126">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="e5828-127"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e5828-127"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="e5828-128">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="e5828-128">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="e5828-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e5828-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="e5828-130">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="e5828-130">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e5828-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e5828-131">Requirements</span></span>



| <span data-ttu-id="e5828-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e5828-132">Requirement</span></span> | <span data-ttu-id="e5828-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="e5828-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5828-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5828-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e5828-135">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5828-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e5828-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e5828-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e5828-137">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e5828-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e5828-138">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="e5828-138">Redistributable</span></span><br/>          | <span data-ttu-id="e5828-139">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="e5828-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="e5828-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="e5828-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5828-141"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5828-141"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="e5828-142">MIDL</span><span class="sxs-lookup"><span data-stu-id="e5828-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e5828-143"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e5828-143"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="e5828-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e5828-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5828-145"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5828-145"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5828-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5828-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5828-147">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="e5828-147">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="e5828-148">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span><span class="sxs-lookup"><span data-stu-id="e5828-148">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> <dt>

[<span data-ttu-id="e5828-149">**ISoftKbd ::D estroySoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="e5828-149">**ISoftKbd::DestroySoftKeyboardWindow**</span></span>](isoftkbd-destroysoftkeyboardwindow.md)
</dt> <dt>

[<span data-ttu-id="e5828-150">**ISoftKbd::ShowSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="e5828-150">**ISoftKbd::ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)
</dt> <dt>

[<span data-ttu-id="e5828-151">**TYPE de TITLEBAR \_**</span><span class="sxs-lookup"><span data-stu-id="e5828-151">**TITLEBAR\_TYPE**</span></span>](titlebar-type.md)
</dt> </dl>

 

 





