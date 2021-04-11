---
description: La méthode OnStart est une méthode facultative qui peut être implémentée par l’analyse. Le MCSVC appelle cette méthode pour demander que le moniteur démarre la capture.
ms.assetid: 992ee27e-aaba-4e65-989b-e3f0fbd542ea
title: 'IMonitor :: OnStart, méthode (NetMon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStart
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: ca9e5e17de1d6baf2c79cc0077c5e2036a2a6246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112207"
---
# <a name="imonitoronstart-method"></a><span data-ttu-id="f1a07-104">IMonitor :: OnStart, méthode</span><span class="sxs-lookup"><span data-stu-id="f1a07-104">IMonitor::OnStart method</span></span>

<span data-ttu-id="f1a07-105">La méthode **OnStart** est une méthode facultative qui peut être implémentée par l’analyse.</span><span class="sxs-lookup"><span data-stu-id="f1a07-105">The **OnStart** method is an optional method that can be implemented by the monitor.</span></span> <span data-ttu-id="f1a07-106">Le MCSVC appelle cette méthode pour demander que le moniteur démarre la capture.</span><span class="sxs-lookup"><span data-stu-id="f1a07-106">The MCSVC calls this method to request that the monitor start the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1a07-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1a07-107">Syntax</span></span>


```C++
HRESULT OnStart(
  [in] IUnknown *pUnkNPP
);
```



## <a name="parameters"></a><span data-ttu-id="f1a07-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1a07-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1a07-109">*pUnkNPP* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f1a07-109">*pUnkNPP* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1a07-110">Pointeur [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) vers l’interface [IRTC](irtc.md) .</span><span class="sxs-lookup"><span data-stu-id="f1a07-110">An [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer to the [IRTC](irtc.md) interface.</span></span> <span data-ttu-id="f1a07-111">Le moniteur peut utiliser cette interface pour obtenir des statistiques qui peuvent être utilisées pour déterminer si la capture doit être démarrée.</span><span class="sxs-lookup"><span data-stu-id="f1a07-111">The monitor can use this interface to obtain statistics that can be used to determine if the capture should be started.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1a07-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f1a07-112">Return value</span></span>

<span data-ttu-id="f1a07-113">Si la méthode réussit, la valeur de retour est S \_ OK (ce qui est identique à la valeur de l’erreur).</span><span class="sxs-lookup"><span data-stu-id="f1a07-113">If the method is successful, the return value is S\_OK (which is the same as NOERROR).</span></span> <span data-ttu-id="f1a07-114">Lorsque \_ la méthode S OK est retournée, MCSVC appelle la méthode [IRTC :: Start](irtc-start.md) .</span><span class="sxs-lookup"><span data-stu-id="f1a07-114">When S\_OK is returned, the MCSVC calls the [IRTC::Start](irtc-start.md) method.</span></span>

<span data-ttu-id="f1a07-115">Si la méthode échoue, la valeur de retour est un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="f1a07-115">If the method is unsuccessful, the return value is an error code.</span></span> <span data-ttu-id="f1a07-116">Le MCSVC ne démarre pas la capture si un code d’erreur est retourné.</span><span class="sxs-lookup"><span data-stu-id="f1a07-116">The MCSVC will not start the capture if any error code is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1a07-117">Notes</span><span class="sxs-lookup"><span data-stu-id="f1a07-117">Remarks</span></span>

<span data-ttu-id="f1a07-118">Le MCSVC appelle cette méthode avant que la méthode [IRTC :: Start](irtc-start.md) du NPP soit appelée pour démarrer la capture.</span><span class="sxs-lookup"><span data-stu-id="f1a07-118">The MCSVC calls this method before the NPP's [IRTC::Start](irtc-start.md) method is called to start the capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1a07-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1a07-119">Requirements</span></span>



| <span data-ttu-id="f1a07-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1a07-120">Requirement</span></span> | <span data-ttu-id="f1a07-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1a07-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f1a07-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1a07-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f1a07-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1a07-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f1a07-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1a07-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f1a07-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1a07-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f1a07-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1a07-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1a07-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1a07-127"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1a07-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1a07-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1a07-129">IMonitor</span><span class="sxs-lookup"><span data-stu-id="f1a07-129">IMonitor</span></span>](imonitor.md)
</dt> <dt>

[<span data-ttu-id="f1a07-130">Fournisseurs de paquets réseau</span><span class="sxs-lookup"><span data-stu-id="f1a07-130">Network Packet Providers</span></span>](network-packet-providers.md)
</dt> </dl>

 

