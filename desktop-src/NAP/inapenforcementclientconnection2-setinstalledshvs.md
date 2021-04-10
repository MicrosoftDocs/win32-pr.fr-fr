---
title: Méthode INapEnforcementClientConnection2 SetInstalledShvs (NapEnforcementClient. h)
description: Utilisé par l’agent NAP pour définir les programmes de validation d’intégrité système (SHV) installés sur le client.
ms.assetid: 38aa99b9-a15a-414d-91fc-128de8f5a654
keywords:
- Méthode SetInstalledShvs NAP
- Méthode SetInstalledShvs NAP, interface INapEnforcementClientConnection2
- INapEnforcementClientConnection2 interface NAP, méthode SetInstalledShvs
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6651cd5248094f82d9faa1862492f82648e94125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106513"
---
# <a name="inapenforcementclientconnection2setinstalledshvs-method"></a><span data-ttu-id="ac369-106">INapEnforcementClientConnection2 :: SetInstalledShvs, méthode</span><span class="sxs-lookup"><span data-stu-id="ac369-106">INapEnforcementClientConnection2::SetInstalledShvs method</span></span>

> [!Note]  
> <span data-ttu-id="ac369-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="ac369-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ac369-108">La méthode **SetInstalledShvs** est utilisée par l’agent NAP pour définir les validateurs d’intégrité du système installés sur le client.</span><span class="sxs-lookup"><span data-stu-id="ac369-108">The **SetInstalledShvs** method is used by the NAP Agent to set the installed System Health Validators (SHVs) on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac369-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac369-109">Syntax</span></span>


```C++
HRESULT SetInstalledShvs(
  [in] SystemHealthEntityCount count,
  [in] SystemHealthEntityId    *ids
);
```



## <a name="parameters"></a><span data-ttu-id="ac369-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac369-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac369-111">*nombre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac369-111">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac369-112">Valeur [SystemHealthEntityCount](nap-datatypes.md) qui spécifie le nombre de validateurs d’intégrité de l’installation dans *IDS*.</span><span class="sxs-lookup"><span data-stu-id="ac369-112">A [SystemHealthEntityCount](nap-datatypes.md) value that specifies the number of SHVs to install in *ids*.</span></span>

</dd> <dt>

<span data-ttu-id="ac369-113">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ac369-113">*ids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac369-114">Pointeur vers une valeur [SystemHealthEntityId](nap-datatypes.md) qui contient une liste d’ID SHV à installer.</span><span class="sxs-lookup"><span data-stu-id="ac369-114">A pointer to a [SystemHealthEntityId](nap-datatypes.md) value that contains a list of SHV IDs to install.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac369-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ac369-115">Return value</span></span>

<span data-ttu-id="ac369-116">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="ac369-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ac369-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ac369-117">Return code</span></span>                                                                                  | <span data-ttu-id="ac369-118">Description</span><span class="sxs-lookup"><span data-stu-id="ac369-118">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="ac369-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ac369-119"><dt>**S\_OK** </dt></span></span> </dl>        | <span data-ttu-id="ac369-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="ac369-120">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="ac369-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ac369-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="ac369-122">Le paramètre *Count* était 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="ac369-122">The *count* parameter was 0 (zero).</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ac369-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ac369-123">Requirements</span></span>



| <span data-ttu-id="ac369-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ac369-124">Requirement</span></span> | <span data-ttu-id="ac369-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ac369-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac369-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac369-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ac369-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac369-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ac369-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ac369-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ac369-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ac369-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ac369-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="ac369-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac369-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ac369-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="ac369-132">MIDL</span><span class="sxs-lookup"><span data-stu-id="ac369-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ac369-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ac369-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="ac369-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ac369-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ac369-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ac369-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="ac369-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ac369-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac369-137">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="ac369-137">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





