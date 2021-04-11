---
title: INapSoHProcessor Initialize, méthode (NapProtocol. h)
description: Initialise le paquet de protocole et le système du processeur SoH. Cette méthode doit être appelée exactement une fois.
ms.assetid: 4fccc847-3c4d-4fc5-935d-28fb2964a9be
keywords:
- Initialiser la méthode NAP
- Méthode Initialize NAP, interface INapSoHProcessor
- INapSoHProcessor interface NAP, Initialize, méthode
topic_type:
- apiref
api_name:
- INapSoHProcessor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ff3a32bb213caf19964ccea8175a43e5016f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942128"
---
# <a name="inapsohprocessorinitialize-method"></a><span data-ttu-id="0d045-107">INapSoHProcessor :: Initialize, méthode</span><span class="sxs-lookup"><span data-stu-id="0d045-107">INapSoHProcessor::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="0d045-108">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="0d045-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0d045-109">La méthode **INapSoHProcessor :: Initialize** Initialise le paquet de protocole et le système du processeur SOH.</span><span class="sxs-lookup"><span data-stu-id="0d045-109">The **INapSoHProcessor::Initialize** method initializes the protocol packet and SoH processor system.</span></span> <span data-ttu-id="0d045-110">Cette méthode doit être appelée exactement une fois.</span><span class="sxs-lookup"><span data-stu-id="0d045-110">This method must be called exactly once.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d045-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d045-111">Syntax</span></span>


```C++
HRESULT Initialize(
  [in]  const SoH                  *soh,
  [in]        BOOL                 isRequest,
  [out]       SystemHealthEntityId *id
);
```



## <a name="parameters"></a><span data-ttu-id="0d045-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d045-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d045-113">*SOH* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d045-113">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d045-114">Pointeur vers le paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) à traiter.</span><span class="sxs-lookup"><span data-stu-id="0d045-114">A pointer to the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="0d045-115">*isRequest* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d045-115">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d045-116">Valeur **booléenne** qui est **true** si le paquet est un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) et **false** s’il s’agit d’un **SoHResponse**.</span><span class="sxs-lookup"><span data-stu-id="0d045-116">A **BOOL** that is **TRUE** if the packet is an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is an **SoHResponse**.</span></span>

</dd> <dt>

<span data-ttu-id="0d045-117">*ID* \[ sortant\]</span><span class="sxs-lookup"><span data-stu-id="0d045-117">*id* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d045-118">[SystemHealthEntityId](nap-datatypes.md) unique qui contient l’ID de l’agent SHA ou SHV qui a construit le paquet.</span><span class="sxs-lookup"><span data-stu-id="0d045-118">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA or SHV that constructed the packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d045-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d045-119">Return value</span></span>

<span data-ttu-id="0d045-120">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="0d045-120">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="0d045-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0d045-121">Return code</span></span>                                                                                            | <span data-ttu-id="0d045-122">Description</span><span class="sxs-lookup"><span data-stu-id="0d045-122">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d045-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0d045-123"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="0d045-124">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="0d045-124">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="0d045-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0d045-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="0d045-126">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="0d045-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0d045-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0d045-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="0d045-128">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="0d045-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="0d045-129"><dt>**\_paquet NAP E \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0d045-129"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="0d045-130">Le paquet SoH n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="0d045-130">The SoH packet is invalid.</span></span><br/>                              |



 

## <a name="requirements"></a><span data-ttu-id="0d045-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d045-131">Requirements</span></span>



| <span data-ttu-id="0d045-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d045-132">Requirement</span></span> | <span data-ttu-id="0d045-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d045-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d045-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d045-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0d045-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d045-135">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0d045-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d045-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0d045-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d045-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0d045-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d045-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d045-139"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d045-139"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d045-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="0d045-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0d045-141"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d045-141"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="0d045-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0d045-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d045-143"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d045-143"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="0d045-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d045-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d045-145">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="0d045-145">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





