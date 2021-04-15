---
title: Méthode INapEnforcementClientConnection2 GetIsolationInfoEx (NapEnforcementClient. h)
description: Est utilisé pour obtenir des informations d’isolation sur le client.
ms.assetid: ebacd056-5ab8-4096-821c-8f2987d853c4
keywords:
- Méthode GetIsolationInfoEx NAP
- Méthode GetIsolationInfoEx NAP, interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP, méthode GetIsolationInfoEx
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.GetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6586dd5fc277e62d4478e685f49ac132e744bcc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467062"
---
# <a name="inapenforcementclientconnection2getisolationinfoex-method"></a><span data-ttu-id="bc4e6-106">INapEnforcementClientConnection2 :: GetIsolationInfoEx, méthode</span><span class="sxs-lookup"><span data-stu-id="bc4e6-106">INapEnforcementClientConnection2::GetIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="bc4e6-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="bc4e6-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bc4e6-108">La méthode **INapEnforcementClientConnection2 :: GetIsolationInfoEx** est utilisée pour obtenir des informations d’isolation sur le client.</span><span class="sxs-lookup"><span data-stu-id="bc4e6-108">The **INapEnforcementClientConnection2::GetIsolationInfoEx** method is used to get isolation information about the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc4e6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bc4e6-109">Syntax</span></span>


```C++
HRESULT GetIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo
) const;
```



## <a name="parameters"></a><span data-ttu-id="bc4e6-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bc4e6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc4e6-111">*isolationInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bc4e6-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc4e6-112">Pointeur vers un pointeur vers une structure [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) qui contient la connectivité et les informations d’État étendues du client.</span><span class="sxs-lookup"><span data-stu-id="bc4e6-112">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the connectivity and extended state information of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc4e6-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bc4e6-113">Return value</span></span>

<span data-ttu-id="bc4e6-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="bc4e6-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="bc4e6-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bc4e6-115">Return code</span></span>                                                                                     | <span data-ttu-id="bc4e6-116">Description</span><span class="sxs-lookup"><span data-stu-id="bc4e6-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="bc4e6-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bc4e6-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="bc4e6-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="bc4e6-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="bc4e6-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="bc4e6-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="bc4e6-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="bc4e6-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="bc4e6-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bc4e6-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="bc4e6-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="bc4e6-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bc4e6-123">Notes</span><span class="sxs-lookup"><span data-stu-id="bc4e6-123">Remarks</span></span>

<span data-ttu-id="bc4e6-124">Ces informations sont définies par NapAgent après le traitement d’un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) et ne doivent pas être définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="bc4e6-124">This information is set by NapAgent after processing an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

<span data-ttu-id="bc4e6-125">L’algorithme SHA doit libérer la structure [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) en appelant [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span><span class="sxs-lookup"><span data-stu-id="bc4e6-125">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc4e6-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bc4e6-126">Requirements</span></span>



| <span data-ttu-id="bc4e6-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bc4e6-127">Requirement</span></span> | <span data-ttu-id="bc4e6-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc4e6-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc4e6-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc4e6-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bc4e6-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc4e6-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bc4e6-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bc4e6-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bc4e6-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bc4e6-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="bc4e6-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="bc4e6-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc4e6-134"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc4e6-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc4e6-135">MIDL</span><span class="sxs-lookup"><span data-stu-id="bc4e6-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bc4e6-136"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bc4e6-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="bc4e6-137">DLL</span><span class="sxs-lookup"><span data-stu-id="bc4e6-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc4e6-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc4e6-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="bc4e6-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc4e6-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc4e6-140">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="bc4e6-140">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





