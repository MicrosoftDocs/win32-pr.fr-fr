---
title: Méthode INapClientManagement RegisterEnforcementClient (NapManagement. h)
description: Inscrit un client de mise en œuvre auprès du système NAP.
ms.assetid: 26ea45ea-a366-4162-91dc-06bcd0261c56
keywords:
- Méthode RegisterEnforcementClient NAP
- Méthode RegisterEnforcementClient NAP, interface INapClientManagement
- INapClientManagement interface NAP, méthode RegisterEnforcementClient
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc8ed4b5fe5a97d60b764341f21f25628c3c3434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104695"
---
# <a name="inapclientmanagementregisterenforcementclient-method"></a><span data-ttu-id="a692e-106">INapClientManagement :: RegisterEnforcementClient, méthode</span><span class="sxs-lookup"><span data-stu-id="a692e-106">INapClientManagement::RegisterEnforcementClient method</span></span>

> [!Note]  
> <span data-ttu-id="a692e-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="a692e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a692e-108">La méthode **RegisterEnforcementClient** inscrit un client de mise en œuvre auprès du système NAP.</span><span class="sxs-lookup"><span data-stu-id="a692e-108">The **RegisterEnforcementClient** method registers an enforcement client with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a692e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a692e-109">Syntax</span></span>


```C++
HRESULT RegisterEnforcementClient(
  [in] const NapComponentRegistrationInfo *enforcer
);
```



## <a name="parameters"></a><span data-ttu-id="a692e-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a692e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a692e-111">*application* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a692e-111">*enforcer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a692e-112">Pointeur vers une structure de données [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) qui contient les informations d’inscription associées au client de contrainte.</span><span class="sxs-lookup"><span data-stu-id="a692e-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structure that contains the registration information that is associated with the enforcement client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a692e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a692e-113">Return value</span></span>

<span data-ttu-id="a692e-114">La méthode retourne un code d’État HRESULT incluant, sans s’y limiter, l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="a692e-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="a692e-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a692e-115">Return code</span></span>                                                                                            | <span data-ttu-id="a692e-116">Description</span><span class="sxs-lookup"><span data-stu-id="a692e-116">Description</span></span>                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a692e-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a692e-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="a692e-118">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="a692e-118">Operation successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="a692e-119"><dt>**\_ACCESSDENIED E**</dt></span><span class="sxs-lookup"><span data-stu-id="a692e-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>         | <span data-ttu-id="a692e-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="a692e-120">Permissions error, access denied.</span></span><br/>                                      |
| <dl> <span data-ttu-id="a692e-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="a692e-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="a692e-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="a692e-122">System resource limit, could not perform the operation.</span></span><br/>                |
| <dl> <span data-ttu-id="a692e-123"><dt>**\_ID en \_ conflit NAP \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="a692e-123"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="a692e-124">Un agent d’application utilisant l’identificateur donné est déjà inscrit.</span><span class="sxs-lookup"><span data-stu-id="a692e-124">An enforcement agent using the given identifier is already registered.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a692e-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a692e-125">Requirements</span></span>



| <span data-ttu-id="a692e-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a692e-126">Requirement</span></span> | <span data-ttu-id="a692e-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="a692e-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a692e-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a692e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a692e-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a692e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a692e-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a692e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a692e-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a692e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a692e-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="a692e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a692e-133"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="a692e-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="a692e-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="a692e-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a692e-135"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a692e-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="a692e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a692e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a692e-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a692e-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="a692e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a692e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a692e-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="a692e-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





