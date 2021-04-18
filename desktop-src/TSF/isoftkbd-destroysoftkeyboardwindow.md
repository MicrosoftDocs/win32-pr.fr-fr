---
title: Méthode ISoftKbd DestroySoftKeyboardWindow (Softkbdc. h)
description: La méthode ISoftKbd DestroySoftKeyboardWindow détruit une fenêtre de clavier temporaire.
ms.assetid: 44030934-7b4a-46c1-95ea-709fc9004e43
keywords:
- Infrastructure des services de texte de méthode DestroySoftKeyboardWindow
- DestroySoftKeyboardWindow méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode DestroySoftKeyboardWindow
topic_type:
- apiref
api_name:
- ISoftKbd.DestroySoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb0c460912e8b891503771425fc72484fcc471ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543423"
---
# <a name="isoftkbddestroysoftkeyboardwindow-method"></a><span data-ttu-id="458a4-106">ISoftKbd ::D méthode estroySoftKeyboardWindow</span><span class="sxs-lookup"><span data-stu-id="458a4-106">ISoftKbd::DestroySoftKeyboardWindow method</span></span>

<span data-ttu-id="458a4-107">La méthode **ISoftKbd ::D estroysoftkeyboardwindow** détruit une fenêtre de clavier temporaire.</span><span class="sxs-lookup"><span data-stu-id="458a4-107">The **ISoftKbd::DestroySoftKeyboardWindow** method destroys a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="458a4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="458a4-108">Syntax</span></span>


```C++
HRESULT DestroySoftKeyboardWindow();
```



## <a name="parameters"></a><span data-ttu-id="458a4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="458a4-109">Parameters</span></span>

<span data-ttu-id="458a4-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="458a4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="458a4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="458a4-111">Return value</span></span>

<span data-ttu-id="458a4-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="458a4-112">This method can return one of these values.</span></span>



| <span data-ttu-id="458a4-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="458a4-113">Value</span></span>                                                                                | <span data-ttu-id="458a4-114">Description</span><span class="sxs-lookup"><span data-stu-id="458a4-114">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="458a4-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="458a4-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="458a4-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="458a4-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="458a4-117">Notes</span><span class="sxs-lookup"><span data-stu-id="458a4-117">Remarks</span></span>

<span data-ttu-id="458a4-118">Cette méthode supprime une fenêtre de clavier temporaire créée précédemment à l’aide d’un appel à [**ISoftKbd :: CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md).</span><span class="sxs-lookup"><span data-stu-id="458a4-118">This method removes a soft keyboard window previously created with a call to [**ISoftKbd::CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="458a4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="458a4-119">Requirements</span></span>



| <span data-ttu-id="458a4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="458a4-120">Requirement</span></span> | <span data-ttu-id="458a4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="458a4-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="458a4-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="458a4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="458a4-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="458a4-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="458a4-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="458a4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="458a4-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="458a4-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="458a4-126">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="458a4-126">Redistributable</span></span><br/>          | <span data-ttu-id="458a4-127">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="458a4-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="458a4-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="458a4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="458a4-129"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="458a4-129"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="458a4-130">MIDL</span><span class="sxs-lookup"><span data-stu-id="458a4-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="458a4-131"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="458a4-131"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="458a4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="458a4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="458a4-133"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="458a4-133"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="458a4-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="458a4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="458a4-135">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="458a4-135">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="458a4-136">**ISoftKbd::CreateSoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="458a4-136">**ISoftKbd::CreateSoftKeyboardWindow**</span></span>](isoftkbd-createsoftkeyboardwindow.md)
</dt> </dl>

 

 





