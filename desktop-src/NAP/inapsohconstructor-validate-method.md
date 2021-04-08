---
title: INapSoHConstructor Validate, méthode (NapProtocol. h)
description: Vérifie la validité du paquet SoH.
ms.assetid: 66338213-43c0-461a-a794-5f18d56bd505
keywords:
- Valider la méthode NAP
- Valider la méthode NAP, interface INapSoHConstructor
- INapSoHConstructor interface NAP, Validate, méthode
topic_type:
- apiref
api_name:
- INapSoHConstructor.Validate
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7db8a52d7986348e85c724171b6d417996c7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742605"
---
# <a name="inapsohconstructorvalidate-method"></a><span data-ttu-id="7164a-106">INapSoHConstructor :: Validate, méthode</span><span class="sxs-lookup"><span data-stu-id="7164a-106">INapSoHConstructor::Validate method</span></span>

> [!Note]  
> <span data-ttu-id="7164a-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="7164a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7164a-108">La méthode **INapSoHConstructor :: Validate** vérifie la validité du paquet SOH.</span><span class="sxs-lookup"><span data-stu-id="7164a-108">The **INapSoHConstructor::Validate** method checks the validity of the SoH packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="7164a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7164a-109">Syntax</span></span>


```C++
HRESULT Validate(
  [in] const SoH  *soh,
  [in]       BOOL isRequest
);
```



## <a name="parameters"></a><span data-ttu-id="7164a-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7164a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7164a-111">*SOH* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7164a-111">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7164a-112">Pointeur vers le paquet [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) construit.</span><span class="sxs-lookup"><span data-stu-id="7164a-112">A pointer to the constructed [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="7164a-113">*isRequest* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7164a-113">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7164a-114">Valeur **booléenne** qui est **true** si le paquet est un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) et **false** s’il s’agit d’un **SoHResponse**.</span><span class="sxs-lookup"><span data-stu-id="7164a-114">A **BOOL** that is **TRUE** if the packet is an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is an **SoHResponse**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7164a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7164a-115">Return value</span></span>

<span data-ttu-id="7164a-116">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="7164a-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="7164a-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7164a-117">Return code</span></span>                                                                                            | <span data-ttu-id="7164a-118">Description</span><span class="sxs-lookup"><span data-stu-id="7164a-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7164a-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7164a-119"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="7164a-120">Le paquet SoH est valide.</span><span class="sxs-lookup"><span data-stu-id="7164a-120">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="7164a-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="7164a-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="7164a-122">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="7164a-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="7164a-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7164a-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="7164a-124">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="7164a-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="7164a-125"><dt>**\_paquet NAP E \_ non valide \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7164a-125"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="7164a-126">Le paquet SoH n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7164a-126">The SoH packet is invalid.</span></span><br/>                              |



 

## <a name="requirements"></a><span data-ttu-id="7164a-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7164a-127">Requirements</span></span>



| <span data-ttu-id="7164a-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7164a-128">Requirement</span></span> | <span data-ttu-id="7164a-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="7164a-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7164a-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7164a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="7164a-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7164a-131">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7164a-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7164a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="7164a-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7164a-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="7164a-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="7164a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="7164a-135"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="7164a-135"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="7164a-136">MIDL</span><span class="sxs-lookup"><span data-stu-id="7164a-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7164a-137"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7164a-137"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="7164a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="7164a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7164a-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7164a-139"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7164a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7164a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7164a-141">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="7164a-141">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





