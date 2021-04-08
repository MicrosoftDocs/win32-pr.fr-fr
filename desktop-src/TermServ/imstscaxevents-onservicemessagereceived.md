---
title: Méthode IMsTscAxEvents OnServiceMessageReceived
description: Appelé lorsque le client reçoit un message système.
ms.assetid: 9D230AA3-30F8-4BDF-89D6-D33AF42D0E85
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode OnServiceMessageReceived
- Méthode OnServiceMessageReceived Services Bureau à distance, interface IMsTscAxEvents
- Services Bureau à distance de l’interface IMsTscAxEvents, méthode OnServiceMessageReceived
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnServiceMessageReceived
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a26b78fa31667fb550848d4edd7918aa2bde3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742092"
---
# <a name="imstscaxeventsonservicemessagereceived-method"></a><span data-ttu-id="b3989-106">IMsTscAxEvents :: OnServiceMessageReceived, méthode</span><span class="sxs-lookup"><span data-stu-id="b3989-106">IMsTscAxEvents::OnServiceMessageReceived method</span></span>

<span data-ttu-id="b3989-107">Appelé lorsque le client reçoit un message système.</span><span class="sxs-lookup"><span data-stu-id="b3989-107">Called when the client receives a system message.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3989-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b3989-108">Syntax</span></span>


```C++
void OnServiceMessageReceived(
  [in] BSTR serviceMessage
);
```



## <a name="parameters"></a><span data-ttu-id="b3989-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b3989-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3989-110">*serviceMessage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b3989-110">*serviceMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3989-111">Spécifie le message système.</span><span class="sxs-lookup"><span data-stu-id="b3989-111">Specifies the system message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3989-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b3989-112">Return value</span></span>

<span data-ttu-id="b3989-113">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b3989-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3989-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b3989-114">Remarks</span></span>

<span data-ttu-id="b3989-115">Pour plus d’informations sur les messages système, consultez [configurer la messagerie pour un serveur de passerelle Bureau à distance](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="b3989-115">For more information about system messages, see [Configure Messaging for a Remote Desktop Gateway Server](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd834700(v=ws.11)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b3989-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b3989-116">Requirements</span></span>



| <span data-ttu-id="b3989-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b3989-117">Requirement</span></span> | <span data-ttu-id="b3989-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b3989-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3989-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3989-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b3989-120">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b3989-120">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="b3989-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b3989-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b3989-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b3989-122">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="b3989-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b3989-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="b3989-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3989-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b3989-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b3989-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3989-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3989-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="b3989-127">IID</span><span class="sxs-lookup"><span data-stu-id="b3989-127">IID</span></span><br/>                      | <span data-ttu-id="b3989-128">IMsTscAxEvents est défini en tant que 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="b3989-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="b3989-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3989-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3989-130">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="b3989-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

