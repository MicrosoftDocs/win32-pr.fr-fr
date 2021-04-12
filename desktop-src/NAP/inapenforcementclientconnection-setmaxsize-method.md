---
title: Méthode INapEnforcementClientConnection SetMaxSize (NapEnforcementClient. h)
description: Définit la taille maximale du paquet SoH pour ce client.
ms.assetid: 30d3747d-bcf8-41b3-b0af-29f20d48417b
keywords:
- Méthode SetMaxSize NAP
- Méthode SetMaxSize NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, méthode SetMaxSize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b10d7bc1a023371683f17bb3e6e12cd578fa964
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384387"
---
# <a name="inapenforcementclientconnectionsetmaxsize-method"></a><span data-ttu-id="fa632-106">INapEnforcementClientConnection :: SetMaxSize, méthode</span><span class="sxs-lookup"><span data-stu-id="fa632-106">INapEnforcementClientConnection::SetMaxSize method</span></span>

> [!Note]  
> <span data-ttu-id="fa632-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="fa632-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="fa632-108">La méthode **INapEnforcementClientConnection :: SetMaxSize** définit la taille maximale du paquet SOH pour ce client.</span><span class="sxs-lookup"><span data-stu-id="fa632-108">The **INapEnforcementClientConnection::SetMaxSize** method sets the maximum size of the SoH packet for this client.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa632-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa632-109">Syntax</span></span>


```C++
HRESULT SetMaxSize(
  [in] ProtocolMaxSize maxSize
);
```



## <a name="parameters"></a><span data-ttu-id="fa632-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa632-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa632-111">*MaxSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa632-111">*maxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa632-112">Structure [**ProtocolMaxSize**](nap-datatypes.md) qui indique la taille maximale, en octets, du paquet SOH.</span><span class="sxs-lookup"><span data-stu-id="fa632-112">A [**ProtocolMaxSize**](nap-datatypes.md) structure that indicates the maximum size, in bytes, of the SoH packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa632-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa632-113">Return value</span></span>

<span data-ttu-id="fa632-114">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="fa632-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="fa632-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fa632-115">Return code</span></span>                                                                                     | <span data-ttu-id="fa632-116">Description</span><span class="sxs-lookup"><span data-stu-id="fa632-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="fa632-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fa632-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="fa632-118">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="fa632-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fa632-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="fa632-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="fa632-120">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="fa632-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="fa632-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="fa632-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="fa632-122">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="fa632-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fa632-123">Notes</span><span class="sxs-lookup"><span data-stu-id="fa632-123">Remarks</span></span>

<span data-ttu-id="fa632-124">Cette valeur est définie par le client de mise en œuvre.</span><span class="sxs-lookup"><span data-stu-id="fa632-124">This value is set by the enforcement client.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa632-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa632-125">Requirements</span></span>



| <span data-ttu-id="fa632-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa632-126">Requirement</span></span> | <span data-ttu-id="fa632-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa632-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa632-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa632-128">Minimum supported client</span></span><br/> | <span data-ttu-id="fa632-129">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa632-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="fa632-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa632-130">Minimum supported server</span></span><br/> | <span data-ttu-id="fa632-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa632-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fa632-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa632-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa632-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa632-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa632-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="fa632-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fa632-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fa632-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="fa632-136">DLL</span><span class="sxs-lookup"><span data-stu-id="fa632-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa632-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa632-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="fa632-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa632-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa632-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="fa632-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





