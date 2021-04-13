---
title: INapEnforcementClientConnection Initialize, méthode (NapEnforcementClient. h)
description: Initialise la connexion cliente.
ms.assetid: da72bfc3-9551-4fb0-b9a5-2931c14f618f
keywords:
- Initialiser la méthode NAP
- Méthode Initialize NAP, interface INapEnforcementClientConnection
- INapEnforcementClientConnection interface NAP, Initialize, méthode
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b51f12025bbddb8a9e795a97f2ed443344327a17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464826"
---
# <a name="inapenforcementclientconnectioninitialize-method"></a><span data-ttu-id="3c151-106">INapEnforcementClientConnection :: Initialize, méthode</span><span class="sxs-lookup"><span data-stu-id="3c151-106">INapEnforcementClientConnection::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="3c151-107">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="3c151-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3c151-108">La méthode **INapEnforcementClientConnection :: Initialize** initialise la connexion cliente.</span><span class="sxs-lookup"><span data-stu-id="3c151-108">The **INapEnforcementClientConnection::Initialize** method initializes the client connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c151-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3c151-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="3c151-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3c151-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c151-111">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3c151-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c151-112">Pointeur vers un [**EnforementEntityId**](nap-datatypes.md) qui identifie le client de contrainte qui demande la connexion.</span><span class="sxs-lookup"><span data-stu-id="3c151-112">A pointer to an [**EnforementEntityId**](nap-datatypes.md) that identifies the enforcement client requesting the connection.</span></span> <span data-ttu-id="3c151-113">Cette valeur est définie par le NapAgent lors de la création de la connexion.</span><span class="sxs-lookup"><span data-stu-id="3c151-113">This value is set by the NapAgent during connection creation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c151-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3c151-114">Return value</span></span>

<span data-ttu-id="3c151-115">D’autres codes d’erreur spécifiques à COM peuvent également être retournés.</span><span class="sxs-lookup"><span data-stu-id="3c151-115">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="3c151-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3c151-116">Return code</span></span>                                                                                     | <span data-ttu-id="3c151-117">Description</span><span class="sxs-lookup"><span data-stu-id="3c151-117">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c151-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3c151-118"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="3c151-119">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="3c151-119">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3c151-120"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="3c151-120"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="3c151-121">Erreur d’autorisation, accès refusé.</span><span class="sxs-lookup"><span data-stu-id="3c151-121">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="3c151-122"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3c151-122"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="3c151-123">Limite du système, impossible d’effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="3c151-123">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3c151-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3c151-124">Requirements</span></span>



| <span data-ttu-id="3c151-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3c151-125">Requirement</span></span> | <span data-ttu-id="3c151-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3c151-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c151-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c151-127">Minimum supported client</span></span><br/> | <span data-ttu-id="3c151-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c151-128">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3c151-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c151-129">Minimum supported server</span></span><br/> | <span data-ttu-id="3c151-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3c151-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3c151-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="3c151-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c151-132"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c151-132"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c151-133">MIDL</span><span class="sxs-lookup"><span data-stu-id="3c151-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3c151-134"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3c151-134"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="3c151-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3c151-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c151-136"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c151-136"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="3c151-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3c151-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c151-138">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="3c151-138">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





