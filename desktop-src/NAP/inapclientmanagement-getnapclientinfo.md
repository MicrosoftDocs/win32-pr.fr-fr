---
title: Méthode INapClientManagement GetNapClientInfo (NapManagement. h)
description: Récupère des informations sur le client NAP.
ms.assetid: c0b57cab-729b-40b2-81d2-32a961e377a5
keywords:
- Méthode GetNapClientInfo NAP
- Méthode GetNapClientInfo NAP, interface INapClientManagement
- INapClientManagement interface NAP, méthode GetNapClientInfo
topic_type:
- apiref
api_name:
- INapClientManagement.GetNapClientInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a11fc496374f2a7f0b7842e22212013149f44f22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508886"
---
# <a name="inapclientmanagementgetnapclientinfo-method"></a><span data-ttu-id="886f1-106">INapClientManagement :: GetNapClientInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="886f1-106">INapClientManagement::GetNapClientInfo method</span></span>

> [!Note]  
> <span data-ttu-id="886f1-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="886f1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="886f1-108">La méthode **GetNapClientInfo** récupère des informations sur le client NAP.</span><span class="sxs-lookup"><span data-stu-id="886f1-108">The **GetNapClientInfo** method retrieves information about the NAP client.</span></span>

## <a name="syntax"></a><span data-ttu-id="886f1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="886f1-109">Syntax</span></span>


```C++
HRESULT GetNapClientInfo(
  [out] BOOL          *isNapEnabled,
  [out] CountedString **clientName,
  [out] CountedString **clientDescription,
  [out] CountedString **protocolVersion
) const;
```



## <a name="parameters"></a><span data-ttu-id="886f1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="886f1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="886f1-111">*isNapEnabled* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="886f1-111">*isNapEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="886f1-112">Pointeur vers un booléen dont la valeur est **true** si la protection d’accès réseau est activée ; Sinon, elle a la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="886f1-112">A pointer to a BOOL that is set to **TRUE** if NAP is enabled; otherwise it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="886f1-113">*clientName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="886f1-113">*clientName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="886f1-114">Pointeur vers un pointeur vers une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient le nom du client.</span><span class="sxs-lookup"><span data-stu-id="886f1-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the client name.</span></span>

</dd> <dt>

<span data-ttu-id="886f1-115">*clientDescription* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="886f1-115">*clientDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="886f1-116">Pointeur vers un pointeur vers une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient la description du client.</span><span class="sxs-lookup"><span data-stu-id="886f1-116">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the client description.</span></span>

</dd> <dt>

<span data-ttu-id="886f1-117">*protocolVersion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="886f1-117">*protocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="886f1-118">Pointeur vers un pointeur vers une structure [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) qui contient la version du protocole.</span><span class="sxs-lookup"><span data-stu-id="886f1-118">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="886f1-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="886f1-119">Return value</span></span>

<span data-ttu-id="886f1-120">La méthode retourne un code d’État HRESULT incluant, sans s’y limiter, l’un des éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="886f1-120">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="886f1-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="886f1-121">Return code</span></span>                                                                                         | <span data-ttu-id="886f1-122">Description</span><span class="sxs-lookup"><span data-stu-id="886f1-122">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="886f1-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="886f1-123"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="886f1-124">L’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="886f1-124">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="886f1-125"><dt>**\_ACCESSDENIED E**</dt></span><span class="sxs-lookup"><span data-stu-id="886f1-125"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="886f1-126">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="886f1-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="886f1-127"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="886f1-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="886f1-128">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="886f1-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="886f1-129"><dt>**RPC \_ E \_ déconnecté**</dt></span><span class="sxs-lookup"><span data-stu-id="886f1-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="886f1-130">NapAgent n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="886f1-130">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="886f1-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="886f1-131">Requirements</span></span>



| <span data-ttu-id="886f1-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="886f1-132">Requirement</span></span> | <span data-ttu-id="886f1-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="886f1-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="886f1-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="886f1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="886f1-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="886f1-135">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="886f1-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="886f1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="886f1-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="886f1-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="886f1-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="886f1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="886f1-139"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="886f1-139"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="886f1-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="886f1-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="886f1-141"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="886f1-141"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="886f1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="886f1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="886f1-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="886f1-143"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="886f1-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="886f1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="886f1-145">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="886f1-145">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





