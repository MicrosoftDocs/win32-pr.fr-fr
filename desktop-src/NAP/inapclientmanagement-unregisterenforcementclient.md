---
title: Méthode INapClientManagement UnregisterEnforcementClient (NapManagement. h)
description: Annule l’inscription d’un client de contrainte auprès du système NAP.
ms.assetid: 549683de-7f2c-4da6-9616-862e0e99d21f
keywords:
- Méthode UnregisterEnforcementClient NAP
- Méthode UnregisterEnforcementClient NAP, interface INapClientManagement
- INapClientManagement interface NAP, méthode UnregisterEnforcementClient
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea318cf632ac00d54451b11428907c88159809df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104692"
---
# <a name="inapclientmanagementunregisterenforcementclient-method"></a><span data-ttu-id="2dbe0-106">INapClientManagement :: UnregisterEnforcementClient, méthode</span><span class="sxs-lookup"><span data-stu-id="2dbe0-106">INapClientManagement::UnregisterEnforcementClient method</span></span>

> [!Note]  
> <span data-ttu-id="2dbe0-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="2dbe0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2dbe0-108">La méthode **UnregisterEnforcementClient** annule l’inscription d’un client de contrainte auprès du système NAP.</span><span class="sxs-lookup"><span data-stu-id="2dbe0-108">The **UnregisterEnforcementClient** method unregisters an enforcement client with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dbe0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2dbe0-109">Syntax</span></span>


```C++
HRESULT UnregisterEnforcementClient(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="2dbe0-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2dbe0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dbe0-111">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2dbe0-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dbe0-112">Valeur [**EnforcementEntityId**](nap-datatypes.md) qui identifie le client de mise en œuvre dont l’inscription doit être annulée.</span><span class="sxs-lookup"><span data-stu-id="2dbe0-112">An [**EnforcementEntityId**](nap-datatypes.md) value that identifies the enforcement client to unregister.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dbe0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2dbe0-113">Return value</span></span>

<span data-ttu-id="2dbe0-114">La méthode retourne un code d’État HRESULT incluant, sans s’y limiter, l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="2dbe0-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="2dbe0-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2dbe0-115">Return code</span></span>                                                                                         | <span data-ttu-id="2dbe0-116">Description</span><span class="sxs-lookup"><span data-stu-id="2dbe0-116">Description</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2dbe0-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2dbe0-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="2dbe0-118">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2dbe0-118">Operation successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="2dbe0-119"><dt>**\_ACCESSDENIED E**</dt></span><span class="sxs-lookup"><span data-stu-id="2dbe0-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="2dbe0-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="2dbe0-120">Permissions error, access denied.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2dbe0-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="2dbe0-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="2dbe0-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="2dbe0-122">System resource limit, could not perform the operation.</span></span><br/>             |
| <dl> <span data-ttu-id="2dbe0-123"><dt>**la protection NAP est \_ \_ toujours \_ liée**</dt></span><span class="sxs-lookup"><span data-stu-id="2dbe0-123"><dt>**NAP\_E\_STILL\_BOUND**</dt></span></span> </dl> | <span data-ttu-id="2dbe0-124">Le client de contrainte n’a pas pu être désinscrit et reste lié.</span><span class="sxs-lookup"><span data-stu-id="2dbe0-124">The enforcement client could not be unregistered and remains bound.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2dbe0-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2dbe0-125">Requirements</span></span>



| <span data-ttu-id="2dbe0-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2dbe0-126">Requirement</span></span> | <span data-ttu-id="2dbe0-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="2dbe0-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dbe0-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2dbe0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2dbe0-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2dbe0-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2dbe0-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2dbe0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2dbe0-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2dbe0-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2dbe0-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="2dbe0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dbe0-133"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dbe0-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="2dbe0-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="2dbe0-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2dbe0-135"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2dbe0-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="2dbe0-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2dbe0-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2dbe0-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dbe0-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="2dbe0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2dbe0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dbe0-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="2dbe0-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





