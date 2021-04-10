---
title: Énumération ControlCloseStatus
description: Indique si l’application contenant le contrôle peut fermer le contrôle immédiatement.
ms.assetid: ac2e1c68-81b1-4b51-aa7e-0ff703e619a2
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’énumération ControlCloseStatus
topic_type:
- apiref
api_name:
- ControlCloseStatus
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6b94e0ce5cd040a2ade970f566897d2eac339dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941761"
---
# <a name="controlclosestatus-enumeration"></a><span data-ttu-id="d375b-104">Énumération ControlCloseStatus</span><span class="sxs-lookup"><span data-stu-id="d375b-104">ControlCloseStatus enumeration</span></span>

<span data-ttu-id="d375b-105">Indique si l’application contenant le contrôle peut fermer le contrôle immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d375b-105">Indicates whether the application containing the control can close the control immediately.</span></span>

## <a name="syntax"></a><span data-ttu-id="d375b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d375b-106">Syntax</span></span>


```C++
enum ControlCloseStatus {
  controlCloseCanProceed     = 0x0000, 
  controlCloseWaitForEvents  = 0x0001 

};
```



## <a name="constants"></a><span data-ttu-id="d375b-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="d375b-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d375b-108"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed**</span><span class="sxs-lookup"><span data-stu-id="d375b-108"><span id="controlCloseCanProceed"></span><span id="controlclosecanproceed"></span><span id="CONTROLCLOSECANPROCEED"></span>**controlCloseCanProceed**</span></span>
</dt> <dd>

<span data-ttu-id="d375b-109">Le conteneur peut continuer immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d375b-109">Container can go ahead with close immediately.</span></span> <span data-ttu-id="d375b-110">Cela peut se produire si le contrôle n’est pas connecté.</span><span class="sxs-lookup"><span data-stu-id="d375b-110">This can happen if the control is not connected.</span></span>

</dd> <dt>

<span data-ttu-id="d375b-111"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**</span><span class="sxs-lookup"><span data-stu-id="d375b-111"><span id="controlCloseWaitForEvents"></span><span id="controlclosewaitforevents"></span><span id="CONTROLCLOSEWAITFOREVENTS"></span>**controlCloseWaitForEvents**</span></span>
</dt> <dd>

<span data-ttu-id="d375b-112">Le conteneur doit attendre les événements [**IMsTscAxEvents :: OnDisconnected**](imstscaxevents-ondisconnected.md) ou [**IMsTscAxEvents :: OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span><span class="sxs-lookup"><span data-stu-id="d375b-112">Container should wait for events [**IMsTscAxEvents::OnDisconnected**](imstscaxevents-ondisconnected.md) or [**IMsTscAxEvents::OnConfirmClose**](imstscaxevents-onconfirmclose.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d375b-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d375b-113">Requirements</span></span>



| <span data-ttu-id="d375b-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d375b-114">Requirement</span></span> | <span data-ttu-id="d375b-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="d375b-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d375b-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d375b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d375b-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d375b-117">Windows 8.1</span></span><br/>                                                                 |
| <span data-ttu-id="d375b-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d375b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d375b-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d375b-119">Windows Server 2012 R2</span></span><br/>                                                      |
| <span data-ttu-id="d375b-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d375b-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="d375b-121"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d375b-121"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d375b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d375b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d375b-123">**IMsRdpClient::RequestClose**</span><span class="sxs-lookup"><span data-stu-id="d375b-123">**IMsRdpClient::RequestClose**</span></span>](imsrdpclient-requestclose.md)
</dt> <dt>

[<span data-ttu-id="d375b-124">**IMsTscAxEvents::OnConfirmClose**</span><span class="sxs-lookup"><span data-stu-id="d375b-124">**IMsTscAxEvents::OnConfirmClose**</span></span>](imstscaxevents-onconfirmclose.md)
</dt> <dt>

[<span data-ttu-id="d375b-125">**IMsTscAxEvents::OnDisconnected**</span><span class="sxs-lookup"><span data-stu-id="d375b-125">**IMsTscAxEvents::OnDisconnected**</span></span>](imstscaxevents-ondisconnected.md)
</dt> </dl>

 

 





