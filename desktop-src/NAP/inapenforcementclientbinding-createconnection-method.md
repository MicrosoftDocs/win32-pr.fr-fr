---
title: INapEnforcementClientBinding CreateConnection, méthode (NapEnforcementClient. h)
description: Est utilisé par les enforceurs pour créer des objets de connexion.
ms.assetid: 4d31928f-1a10-4168-a53c-256cbbf3e5c9
keywords:
- CreateConnection, méthode NAP
- CreateConnection, méthode NAP, interface INapEnforcementClientBinding
- INapEnforcementClientBinding interface NAP, CreateConnection, méthode
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.CreateConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf530b9fefd0e5b361f4f86ef2421712c750be9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032656"
---
# <a name="inapenforcementclientbindingcreateconnection-method"></a><span data-ttu-id="1d596-106">INapEnforcementClientBinding :: CreateConnection, méthode</span><span class="sxs-lookup"><span data-stu-id="1d596-106">INapEnforcementClientBinding::CreateConnection method</span></span>

> [!Note]  
> <span data-ttu-id="1d596-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="1d596-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="1d596-108">La méthode de fabrique **INapEnforcementClientBinding :: CreateConnection** est utilisée par les enforceurs pour créer des objets de connexion.</span><span class="sxs-lookup"><span data-stu-id="1d596-108">The **INapEnforcementClientBinding::CreateConnection** factory method is used by enforcers to create connection objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d596-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d596-109">Syntax</span></span>


```C++
HRESULT CreateConnection(
  [out] INapEnforcementClientConnection **connection
);
```



## <a name="parameters"></a><span data-ttu-id="1d596-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d596-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d596-111">*connexion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1d596-111">*connection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d596-112">Pointeur COM vers une nouvelle interface [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) retournée par le système NAP.</span><span class="sxs-lookup"><span data-stu-id="1d596-112">A COM pointer to a new [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface returned by the NAP system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d596-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d596-113">Return value</span></span>

<span data-ttu-id="1d596-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="1d596-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="1d596-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1d596-115">Return code</span></span>                                                                                     | <span data-ttu-id="1d596-116">Description</span><span class="sxs-lookup"><span data-stu-id="1d596-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d596-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1d596-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="1d596-118">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="1d596-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="1d596-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="1d596-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="1d596-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="1d596-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="1d596-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1d596-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="1d596-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="1d596-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1d596-123">Notes</span><span class="sxs-lookup"><span data-stu-id="1d596-123">Remarks</span></span>

<span data-ttu-id="1d596-124">Le client de contrainte doit appeler la méthode [**INapEnforcementClientBinding :: Initialize**](inapenforcementclientbinding-initialize-method.md) avant d’appeler cette méthode ou toute autre méthode de l’interface [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="1d596-124">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d596-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d596-125">Requirements</span></span>



| <span data-ttu-id="1d596-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d596-126">Requirement</span></span> | <span data-ttu-id="1d596-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d596-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d596-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d596-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1d596-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d596-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1d596-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1d596-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1d596-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1d596-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1d596-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d596-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d596-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d596-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="1d596-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="1d596-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1d596-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1d596-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="1d596-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1d596-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d596-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d596-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="1d596-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d596-138">See also</span></span>

<dl> <span data-ttu-id="1d596-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="1d596-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="1d596-140">**INapEnforcementClientBinding**</span><span class="sxs-lookup"><span data-stu-id="1d596-140">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="1d596-141">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="1d596-141">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





