---
title: Méthode IMsRdpClient9 detachEvent
description: Détache un événement.
ms.assetid: 6a3ca713-1d5c-4070-a527-ad4f532a4cbf
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode detachEvent
- méthode detachEvent Services Bureau à distance, interface IMsRdpClient9
- Services Bureau à distance de l’interface IMsRdpClient9, méthode detachEvent
- méthode detachEvent Services Bureau à distance, interface IMsRdpClient10
- Services Bureau à distance de l’interface IMsRdpClient10, méthode detachEvent
topic_type:
- apiref
api_name:
- IMsRdpClient9.detachEvent
- IMsRdpClient10.detachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399611ea526338f4cfe40ef3a4d6543bf27f134a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102940"
---
# <a name="imsrdpclient9detachevent-method"></a><span data-ttu-id="40a82-108">IMsRdpClient9 ::d méthode etachEvent</span><span class="sxs-lookup"><span data-stu-id="40a82-108">IMsRdpClient9::detachEvent method</span></span>

<span data-ttu-id="40a82-109">Détache un événement.</span><span class="sxs-lookup"><span data-stu-id="40a82-109">Detaches an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="40a82-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40a82-110">Syntax</span></span>


```C++
HRESULT detachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a><span data-ttu-id="40a82-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40a82-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40a82-112">*EventName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="40a82-112">*eventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40a82-113">Nom de l’événement.</span><span class="sxs-lookup"><span data-stu-id="40a82-113">Name of the event.</span></span>

</dd> <dt>

<span data-ttu-id="40a82-114">*rappel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="40a82-114">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40a82-115">Rappel associé à l’événement.</span><span class="sxs-lookup"><span data-stu-id="40a82-115">The callback associated with the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40a82-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="40a82-116">Return value</span></span>

<span data-ttu-id="40a82-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="40a82-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="40a82-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="40a82-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="40a82-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40a82-119">Requirements</span></span>



| <span data-ttu-id="40a82-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40a82-120">Requirement</span></span> | <span data-ttu-id="40a82-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="40a82-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40a82-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40a82-122">Minimum supported client</span></span><br/> | <span data-ttu-id="40a82-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="40a82-123">Windows 8.1</span></span><br/>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="40a82-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40a82-124">Minimum supported server</span></span><br/> | <span data-ttu-id="40a82-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="40a82-125">Windows Server 2012 R2</span></span><br/>                                                                                                                                                                                                                                       |
| <span data-ttu-id="40a82-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="40a82-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="40a82-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40a82-127"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="40a82-128">DLL</span><span class="sxs-lookup"><span data-stu-id="40a82-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40a82-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40a82-129"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                  |
| <span data-ttu-id="40a82-130">IID</span><span class="sxs-lookup"><span data-stu-id="40a82-130">IID</span></span><br/>                      | <span data-ttu-id="40a82-131">Le CLSID \_ MsRdpClient9 est défini en tant que 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="40a82-131">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="40a82-132">Le CLSID \_ MsRdpClient9NotSafeForScripting est défini en tant que 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="40a82-132">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> <span data-ttu-id="40a82-133">IID \_ IMsRdpClient9 est défini en tant que 28904001-04B6-436C-A55B-0AF1A0883DC9</span><span class="sxs-lookup"><span data-stu-id="40a82-133">IID\_IMsRdpClient9 is defined as 28904001-04B6-436C-A55B-0AF1A0883DC9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40a82-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="40a82-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40a82-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="40a82-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> <dt>

[<span data-ttu-id="40a82-136">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="40a82-136">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> </dl>

 

 





