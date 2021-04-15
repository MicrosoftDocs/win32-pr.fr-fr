---
description: La méthode de neuroinitialize doit être implémentée par l’analyse. Le MCSVC appelle cette méthode pour obtenir un filtre de capture immédiatement avant d’appeler la méthode NPPs IRTCConnect.
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: Méthode IMonitorDoInitialize (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoInitialize
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 93133ce8204e49d080f87635ad6952685f2ba82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525114"
---
# <a name="imonitordoinitialize-method"></a><span data-ttu-id="b86ab-104">IMonitor ::D méthode oInitialize</span><span class="sxs-lookup"><span data-stu-id="b86ab-104">IMonitor::DoInitialize method</span></span>

<span data-ttu-id="b86ab-105">La méthode de **neuroinitialize** doit être implémentée par l’analyse.</span><span class="sxs-lookup"><span data-stu-id="b86ab-105">The **DoInitialize** method must be implemented by the monitor.</span></span> <span data-ttu-id="b86ab-106">Le MCSVC appelle cette méthode pour obtenir un filtre de capture immédiatement avant d’appeler la méthode [IRTC :: Connect](irtc-connect.md) du NPP.</span><span class="sxs-lookup"><span data-stu-id="b86ab-106">The MCSVC calls this method to obtain a capture filter immediately before calling the NPP's [IRTC::Connect](irtc-connect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b86ab-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b86ab-107">Syntax</span></span>


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a><span data-ttu-id="b86ab-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b86ab-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b86ab-109">*pUnkMonitorCtrl* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b86ab-109">*pUnkMonitorCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b86ab-110">Pointeur [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) passé par MCSVC.</span><span class="sxs-lookup"><span data-stu-id="b86ab-110">An [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer passed in by the MCSVC.</span></span> <span data-ttu-id="b86ab-111">Pour obtenir une interface de contrôle d’analyse prise en charge, l’analyse doit appeler [IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le pointeur.</span><span class="sxs-lookup"><span data-stu-id="b86ab-111">To obtain a supported monitor control interface, the monitor must call [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the pointer.</span></span>

</dd> <dt>

<span data-ttu-id="b86ab-112">*hNPPBlob* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b86ab-112">*hNPPBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b86ab-113">En entrée, handle vers un objet BLOB NPP.</span><span class="sxs-lookup"><span data-stu-id="b86ab-113">On input, a handle to an NPP BLOB.</span></span>

<span data-ttu-id="b86ab-114">Lors de la sortie, un objet BLOB NPP contenant un filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="b86ab-114">On output, an NPP BLOB that contains a capture filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b86ab-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b86ab-115">Return value</span></span>

<span data-ttu-id="b86ab-116">Si la méthode réussit, la valeur de retour est S \_ OK (ce qui est identique à la valeur de l’erreur).</span><span class="sxs-lookup"><span data-stu-id="b86ab-116">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span>

<span data-ttu-id="b86ab-117">Si la méthode échoue, la valeur de retour est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b86ab-117">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="b86ab-118">En cas d’erreur, MCSVC ne crée pas le moniteur ni n’appelle [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur le pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="b86ab-118">On error, the MCSVC will not create the monitor or call [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) on the interface pointer.</span></span>

## <a name="remarks"></a><span data-ttu-id="b86ab-119">Notes</span><span class="sxs-lookup"><span data-stu-id="b86ab-119">Remarks</span></span>

<span data-ttu-id="b86ab-120">MCSVC appelle la méthode **noinitialize** pour effectuer toute initialisation de moniteur nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b86ab-120">The MCSVC calls the **DoInitialize** method to perform any required monitor initialization.</span></span>

## <a name="requirements"></a><span data-ttu-id="b86ab-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b86ab-121">Requirements</span></span>



| <span data-ttu-id="b86ab-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b86ab-122">Requirement</span></span> | <span data-ttu-id="b86ab-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b86ab-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b86ab-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b86ab-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b86ab-125">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b86ab-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b86ab-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b86ab-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b86ab-127">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b86ab-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b86ab-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="b86ab-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b86ab-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b86ab-129"><dt>Netmon.h</dt></span></span> </dl> |



 

