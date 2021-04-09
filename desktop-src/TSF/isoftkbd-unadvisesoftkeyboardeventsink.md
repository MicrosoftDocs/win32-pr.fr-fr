---
title: Méthode ISoftKbd UnadviseSoftKeyboardEventSink (Softkbdc. h)
description: La méthode ISoftKbd UnadviseSoftKeyboardEventSink supprime un récepteur d’événements de clavier conditionnel.
ms.assetid: 785340bd-c4f6-4c80-a492-6e60d1c1d552
keywords:
- Infrastructure des services de texte de méthode UnadviseSoftKeyboardEventSink
- UnadviseSoftKeyboardEventSink méthode Text Services Framework, interface ISoftKbd
- ISoftKbd interface Text Services Framework, méthode UnadviseSoftKeyboardEventSink
topic_type:
- apiref
api_name:
- ISoftKbd.UnadviseSoftKeyboardEventSink
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a77129d1b5df024964af4ab19318963708d4b3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742788"
---
# <a name="isoftkbdunadvisesoftkeyboardeventsink-method"></a><span data-ttu-id="7b54d-106">ISoftKbd :: UnadviseSoftKeyboardEventSink, méthode</span><span class="sxs-lookup"><span data-stu-id="7b54d-106">ISoftKbd::UnadviseSoftKeyboardEventSink method</span></span>

<span data-ttu-id="7b54d-107">La méthode **ISoftKbd :: UnadviseSoftKeyboardEventSink** supprime un récepteur d’événements de clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="7b54d-107">The **ISoftKbd::UnadviseSoftKeyboardEventSink** method removes a soft keyboard event sink.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b54d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b54d-108">Syntax</span></span>


```C++
HRESULT UnadviseSoftKeyboardEventSink(
  [in] TfClientId tid
);
```



## <a name="parameters"></a><span data-ttu-id="7b54d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b54d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b54d-110">*TID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7b54d-110">*tid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b54d-111">Identificateur du client qui possède le récepteur d’événements de clavier conditionnel.</span><span class="sxs-lookup"><span data-stu-id="7b54d-111">Identifier of the client that owns the soft keyboard event sink.</span></span> <span data-ttu-id="7b54d-112">Cette valeur a été passée lorsque le récepteur d’événements a été installé à l’aide de [ISoftKbd :: AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).</span><span class="sxs-lookup"><span data-stu-id="7b54d-112">This value was passed when the event sink was installed using [ISoftKbd::AdviseSoftKeyboardEventSink](isoftkbd-advisesoftkeyboardeventsink.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b54d-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7b54d-113">Return value</span></span>

<span data-ttu-id="7b54d-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="7b54d-114">This method can return one of these values.</span></span>



| <span data-ttu-id="7b54d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b54d-115">Value</span></span>                                                                                                   | <span data-ttu-id="7b54d-116">Description</span><span class="sxs-lookup"><span data-stu-id="7b54d-116">Description</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="7b54d-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7b54d-117"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="7b54d-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="7b54d-118">The method was successful.</span></span><br/>                         |
| <dl> <span data-ttu-id="7b54d-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7b54d-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>            | <span data-ttu-id="7b54d-120">Le paramètre *TID* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7b54d-120">The *tid* parameter is invalid.</span></span><br/>                    |
| <dl> <span data-ttu-id="7b54d-121"><dt>**CONNECTER \_ E \_ noconnexion**</dt></span><span class="sxs-lookup"><span data-stu-id="7b54d-121"><dt>**CONNECT\_E\_NOCONNECTION**</dt></span></span> </dl> | <span data-ttu-id="7b54d-122">Le récepteur de notifications identifié par *TID* est introuvable.</span><span class="sxs-lookup"><span data-stu-id="7b54d-122">The advise sink identified by *tid* was not found.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7b54d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b54d-123">Requirements</span></span>



| <span data-ttu-id="7b54d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b54d-124">Requirement</span></span> | <span data-ttu-id="7b54d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b54d-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b54d-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b54d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7b54d-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b54d-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7b54d-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b54d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7b54d-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b54d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7b54d-130">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="7b54d-130">Redistributable</span></span><br/>          | <span data-ttu-id="7b54d-131">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="7b54d-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="7b54d-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b54d-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b54d-133"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b54d-133"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="7b54d-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="7b54d-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7b54d-135"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7b54d-135"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="7b54d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7b54d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b54d-137"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b54d-137"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b54d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b54d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b54d-139">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="7b54d-139">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="7b54d-140">ISoftKbd::AdviseSoftKeyboardEventSink</span><span class="sxs-lookup"><span data-stu-id="7b54d-140">ISoftKbd::AdviseSoftKeyboardEventSink</span></span>](isoftkbd-advisesoftkeyboardeventsink.md)
</dt> </dl>

 

 





