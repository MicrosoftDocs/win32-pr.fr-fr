---
title: ITSRemoteProgram propriété RemoteProgramMode
description: Mode RemoteApp de Windows Server 2008 R2.
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RemoteProgramMode
- Services Bureau à distance de la propriété RemoteProgramMode, interface ITSRemoteProgram
- Services Bureau à distance de l’interface ITSRemoteProgram, propriété RemoteProgramMode
- Services Bureau à distance de la propriété RemoteProgramMode, interface ITSRemoteProgram2
- Services Bureau à distance de l’interface ITSRemoteProgram2, propriété RemoteProgramMode
- Services Bureau à distance de la propriété RemoteProgramMode, interface ITSRemoteProgram3
- Services Bureau à distance de l’interface ITSRemoteProgram3, propriété RemoteProgramMode
topic_type:
- apiref
api_name:
- ITSRemoteProgram.RemoteProgramMode
- ITSRemoteProgram.get_RemoteProgramMode
- ITSRemoteProgram.put_RemoteProgramMode
- ITSRemoteProgram2.RemoteProgramMode
- ITSRemoteProgram2.get_RemoteProgramMode
- ITSRemoteProgram2.put_RemoteProgramMode
- ITSRemoteProgram3.RemoteProgramMode
- ITSRemoteProgram3.get_RemoteProgramMode
- ITSRemoteProgram3.put_RemoteProgramMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8582824e2f6349e37b125ffd974847b602ad6fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512583"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a><span data-ttu-id="c4701-110">ITSRemoteProgram :: RemoteProgramMode, propriété</span><span class="sxs-lookup"><span data-stu-id="c4701-110">ITSRemoteProgram::RemoteProgramMode property</span></span>

<span data-ttu-id="c4701-111">Mode RemoteApp de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="c4701-111">The Windows Server 2008 R2 RemoteApp mode.</span></span>

<span data-ttu-id="c4701-112">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c4701-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4701-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4701-113">Syntax</span></span>


```C++
HRESULT put_RemoteProgramMode(
  [in]  VARIANT_BOOL vboolRemoteProgramMode
);

HRESULT get_RemoteProgramMode(
  [out] VARIANT_BOOL *pvboolRemoteProgramMode
);
```



## <a name="property-value"></a><span data-ttu-id="c4701-114">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c4701-114">Property value</span></span>

<span data-ttu-id="c4701-115">Mode RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="c4701-115">The RemoteApp mode.</span></span> <span data-ttu-id="c4701-116">Si la valeur **est \_ true**, le mode RemoteApp est activé et la session à distance héberge les programmes RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="c4701-116">If set to **VARIANT\_TRUE**, RemoteApp mode is enabled, and the remote session will host RemoteApp programs.</span></span> <span data-ttu-id="c4701-117">Si la valeur **Variant est \_ false** (valeur par défaut), le mode RemoteApp n’est pas activé.</span><span class="sxs-lookup"><span data-stu-id="c4701-117">If set to **VARIANT\_FALSE** (the default), RemoteApp mode is not enabled.</span></span> <span data-ttu-id="c4701-118">La session à distance hébergera un bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="c4701-118">The remote session will host a remote desktop.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c4701-119">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="c4701-119">Error codes</span></span>

<span data-ttu-id="c4701-120">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="c4701-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4701-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4701-121">Requirements</span></span>



| <span data-ttu-id="c4701-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4701-122">Requirement</span></span> | <span data-ttu-id="c4701-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4701-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4701-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4701-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c4701-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4701-125">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c4701-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4701-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c4701-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4701-127">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c4701-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c4701-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="c4701-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4701-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4701-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c4701-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4701-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4701-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4701-132">IID</span><span class="sxs-lookup"><span data-stu-id="c4701-132">IID</span></span><br/>                      | <span data-ttu-id="c4701-133">IID \_ ITSRemoteProgram est défini en tant que FDD029F9-467A-4c49-8529-64B521DBD1B4</span><span class="sxs-lookup"><span data-stu-id="c4701-133">IID\_ITSRemoteProgram is defined as FDD029F9-467A-4c49-8529-64B521DBD1B4</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="c4701-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c4701-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4701-135">**ITSRemoteProgram2**</span><span class="sxs-lookup"><span data-stu-id="c4701-135">**ITSRemoteProgram2**</span></span>](itsremoteprogram2.md)
</dt> <dt>

[<span data-ttu-id="c4701-136">**ITSRemoteProgram3**</span><span class="sxs-lookup"><span data-stu-id="c4701-136">**ITSRemoteProgram3**</span></span>](itsremoteprogram3.md)
</dt> <dt>

[<span data-ttu-id="c4701-137">**ITSRemoteProgram**</span><span class="sxs-lookup"><span data-stu-id="c4701-137">**ITSRemoteProgram**</span></span>](itsremoteprogram.md)
</dt> </dl>

 

 





