---
title: Méthode ISoftKbd AdviseSoftKeyboardEventSink (Softkbdc. h)
description: La méthode ISoftKbd AdviseSoftKeyboardEventSink installe un récepteur d’événements de clavier logiciel pour gérer les notifications OnKeySelection à partir du clavier logiciel.
ms.assetid: f7a441dc-7bef-4fc0-bc62-c153a55a844c
keywords:
- Infrastructure des services de texte de méthode AdviseSoftKeyboardEventSink
- AdviseSoftKeyboardEventSink méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode AdviseSoftKeyboardEventSink
topic_type:
- apiref
api_name:
- ISoftKbd.AdviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ab17de2104c6104b044f027152cfc45cca968b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385048"
---
# <a name="isoftkbdadvisesoftkeyboardeventsink-method"></a><span data-ttu-id="c9d93-106">ISoftKbd :: AdviseSoftKeyboardEventSink, méthode</span><span class="sxs-lookup"><span data-stu-id="c9d93-106">ISoftKbd::AdviseSoftKeyboardEventSink method</span></span>

<span data-ttu-id="c9d93-107">La méthode **ISoftKbd :: AdviseSoftKeyboardEventSink** installe un récepteur d’événements de clavier logiciel pour gérer les notifications OnKeySelection à partir du clavier logiciel.</span><span class="sxs-lookup"><span data-stu-id="c9d93-107">The **ISoftKbd::AdviseSoftKeyboardEventSink** method installs a soft keyboard event sink to handle OnKeySelection notifications from the soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9d93-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9d93-108">Syntax</span></span>


```C++
HRESULT AdviseSoftKeyboardEventSink(
  [in]  DWORD    dwKeyboardId,
  [in]  REFIID   riid,
  [in]  IUnknown *punk,
  [out] DWORD    *pdwCookie
);
```



## <a name="parameters"></a><span data-ttu-id="c9d93-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9d93-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9d93-110">*dwKeyboardId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9d93-110">*dwKeyboardId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9d93-111">Identificateur du clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="c9d93-111">Identifier of the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="c9d93-112">*riid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9d93-112">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9d93-113">Identificateur d’interface de l’interface du récepteur.</span><span class="sxs-lookup"><span data-stu-id="c9d93-113">Interface identifier for the sink interface.</span></span>

</dd> <dt>

<span data-ttu-id="c9d93-114">*punk* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9d93-114">*punk* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9d93-115">Pointeur vers [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pour l’interface du récepteur spécifiée par *riid*.</span><span class="sxs-lookup"><span data-stu-id="c9d93-115">Pointer to [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) for the sink interface specified by *riid*.</span></span> <span data-ttu-id="c9d93-116">Ce paramètre ne peut pas avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="c9d93-116">This parameter cannot be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c9d93-117">*pdwCookie* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c9d93-117">*pdwCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9d93-118">Pointeur vers la mémoire tampon dans laquelle cette méthode récupère le « cookie » de clavier logiciel utilisé pour la connexion au client.</span><span class="sxs-lookup"><span data-stu-id="c9d93-118">Pointer to the buffer in which this method retrieves the soft keyboard "cookie" used for connection to the client.</span></span> <span data-ttu-id="c9d93-119">Le cookie doit être unique pour chaque connexion.</span><span class="sxs-lookup"><span data-stu-id="c9d93-119">The cookie must be unique for each connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9d93-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9d93-120">Return value</span></span>

<span data-ttu-id="c9d93-121">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="c9d93-121">This method can return one of these values.</span></span>



| <span data-ttu-id="c9d93-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9d93-122">Value</span></span>                                                                                        | <span data-ttu-id="c9d93-123">Description</span><span class="sxs-lookup"><span data-stu-id="c9d93-123">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="c9d93-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c9d93-124"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="c9d93-125">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="c9d93-125">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="c9d93-126"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="c9d93-126"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="c9d93-127">Un ou plusieurs paramètres ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="c9d93-127">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9d93-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9d93-128">Requirements</span></span>



| <span data-ttu-id="c9d93-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9d93-129">Requirement</span></span> | <span data-ttu-id="c9d93-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9d93-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9d93-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9d93-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c9d93-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9d93-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c9d93-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9d93-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c9d93-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9d93-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="c9d93-135">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="c9d93-135">Redistributable</span></span><br/>          | <span data-ttu-id="c9d93-136">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="c9d93-136">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="c9d93-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9d93-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9d93-138"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9d93-138"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="c9d93-139">MIDL</span><span class="sxs-lookup"><span data-stu-id="c9d93-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9d93-140"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9d93-140"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="c9d93-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c9d93-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9d93-142"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9d93-142"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9d93-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9d93-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9d93-144">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="c9d93-144">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="c9d93-145">**ISoftKbd::UnadviseSoftKeyboardEventSink**</span><span class="sxs-lookup"><span data-stu-id="c9d93-145">**ISoftKbd::UnadviseSoftKeyboardEventSink**</span></span>](isoftkbd-unadvisesoftkeyboardeventsink.md)
</dt> </dl>

 

