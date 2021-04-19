---
title: Méthode INapEnforcementClientConnection2 SetIsolationInfoEx (NapEnforcementClient. h)
description: Est utilisé par NapAgent pour définir les informations d’isolation pour le client.
ms.assetid: 1b1a41a1-73a6-4c81-8366-15d06c67e228
keywords:
- Méthode SetIsolationInfoEx NAP
- Méthode SetIsolationInfoEx NAP, interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP, méthode SetIsolationInfoEx
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 711b4bfd27c3bd92d48a78f4767f5ed452b2d4f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106515486"
---
# <a name="inapenforcementclientconnection2setisolationinfoex-method"></a><span data-ttu-id="d2cd8-106">INapEnforcementClientConnection2 :: SetIsolationInfoEx, méthode</span><span class="sxs-lookup"><span data-stu-id="d2cd8-106">INapEnforcementClientConnection2::SetIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="d2cd8-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="d2cd8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d2cd8-108">La méthode **INapEnforcementClientConnection2 :: SetIsolationInfoEx** est utilisée par le NapAgent pour définir les informations d’isolation pour le client.</span><span class="sxs-lookup"><span data-stu-id="d2cd8-108">The **INapEnforcementClientConnection2::SetIsolationInfoEx** method is used by the NapAgent to set the isolation information for the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2cd8-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2cd8-109">Syntax</span></span>


```C++
HRESULT SetIsolationInfoEx(
  [in] const IsolationInfoEx *isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d2cd8-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d2cd8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2cd8-111">*isolationInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d2cd8-111">*isolationInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d2cd8-112">Pointeur vers une structure [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) qui contient l’état de connectivité du client.</span><span class="sxs-lookup"><span data-stu-id="d2cd8-112">A pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2cd8-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d2cd8-113">Return value</span></span>

<span data-ttu-id="d2cd8-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="d2cd8-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="d2cd8-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d2cd8-115">Return code</span></span>                                                                                     | <span data-ttu-id="d2cd8-116">Description</span><span class="sxs-lookup"><span data-stu-id="d2cd8-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d2cd8-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d2cd8-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="d2cd8-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="d2cd8-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d2cd8-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d2cd8-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="d2cd8-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="d2cd8-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="d2cd8-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d2cd8-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="d2cd8-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="d2cd8-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d2cd8-123">Notes</span><span class="sxs-lookup"><span data-stu-id="d2cd8-123">Remarks</span></span>

<span data-ttu-id="d2cd8-124">Ces informations sont définies par NapAgent après le traitement d’un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) et ne doivent pas être définies par l’application.</span><span class="sxs-lookup"><span data-stu-id="d2cd8-124">This information is set by NapAgent after processing an [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2cd8-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d2cd8-125">Requirements</span></span>



| <span data-ttu-id="d2cd8-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d2cd8-126">Requirement</span></span> | <span data-ttu-id="d2cd8-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="d2cd8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2cd8-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2cd8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d2cd8-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2cd8-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d2cd8-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d2cd8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d2cd8-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d2cd8-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d2cd8-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="d2cd8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2cd8-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2cd8-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="d2cd8-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="d2cd8-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d2cd8-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d2cd8-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="d2cd8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d2cd8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2cd8-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2cd8-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="d2cd8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d2cd8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2cd8-139">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="d2cd8-139">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





