---
title: Méthode INapClientManagement RegisterSystemHealthAgent (NapManagement. h)
description: Inscrit un SHA auprès du système NAP.
ms.assetid: 37acfd11-8282-42ba-ae02-9a45c4509b8b
keywords:
- Méthode RegisterSystemHealthAgent NAP
- Méthode RegisterSystemHealthAgent NAP, interface INapClientManagement
- INapClientManagement interface NAP, méthode RegisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581c49a117a2b8aaa2c4dda2c6573e4a6327b688
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466042"
---
# <a name="inapclientmanagementregistersystemhealthagent-method"></a><span data-ttu-id="ab513-106">INapClientManagement :: RegisterSystemHealthAgent, méthode</span><span class="sxs-lookup"><span data-stu-id="ab513-106">INapClientManagement::RegisterSystemHealthAgent method</span></span>

> [!Note]  
> <span data-ttu-id="ab513-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="ab513-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ab513-108">La méthode **RegisterSystemHealthAgent** inscrit un SHA auprès du système NAP.</span><span class="sxs-lookup"><span data-stu-id="ab513-108">The **RegisterSystemHealthAgent** method registers an SHA with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab513-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab513-109">Syntax</span></span>


```C++
HRESULT RegisterSystemHealthAgent(
  [in] const NapComponentRegistrationInfo *agent
);
```



## <a name="parameters"></a><span data-ttu-id="ab513-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab513-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab513-111">*agent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab513-111">*agent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab513-112">Pointeur vers une structure [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) qui contient les informations d’inscription pour l’algorithme SHA.</span><span class="sxs-lookup"><span data-stu-id="ab513-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structure that contains the registration information for the SHA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab513-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ab513-113">Return value</span></span>

<span data-ttu-id="ab513-114">La méthode retourne un code d’État HRESULT incluant, sans s’y limiter, l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="ab513-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="ab513-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ab513-115">Return code</span></span>                                                                                            | <span data-ttu-id="ab513-116">Description</span><span class="sxs-lookup"><span data-stu-id="ab513-116">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ab513-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ab513-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="ab513-118">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="ab513-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="ab513-119"><dt>**\_ACCESSDENIED E**</dt></span><span class="sxs-lookup"><span data-stu-id="ab513-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>         | <span data-ttu-id="ab513-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="ab513-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="ab513-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="ab513-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="ab513-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="ab513-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ab513-123"><dt>**\_ID en \_ conflit NAP \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="ab513-123"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="ab513-124">Un SHA qui utilise cet ID est déjà inscrit.</span><span class="sxs-lookup"><span data-stu-id="ab513-124">An SHA that uses this ID is already registered.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="ab513-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab513-125">Requirements</span></span>



| <span data-ttu-id="ab513-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab513-126">Requirement</span></span> | <span data-ttu-id="ab513-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab513-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab513-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab513-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ab513-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab513-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ab513-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab513-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ab513-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab513-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ab513-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab513-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab513-133"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab513-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="ab513-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="ab513-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ab513-135"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ab513-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="ab513-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ab513-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab513-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab513-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="ab513-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab513-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab513-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="ab513-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





