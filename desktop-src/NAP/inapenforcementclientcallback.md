---
title: Interface INapEnforcementClientCallback (NapEnforcementClient. h)
description: Les clients de contrainte doivent implémenter pour permettre à NapAgent de communiquer avec eux.
ms.assetid: d7d63c5b-7952-4f04-9d3d-3f13b0b52d97
keywords:
- NAP de l’interface INapEnforcementClientCallback
- INapEnforcementClientCallback interface NAP, Description
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d5c7e066115a6d51879775d9b8cfab3cbe4888
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516503"
---
# <a name="inapenforcementclientcallback-interface"></a><span data-ttu-id="71919-105">Interface INapEnforcementClientCallback</span><span class="sxs-lookup"><span data-stu-id="71919-105">INapEnforcementClientCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="71919-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="71919-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="71919-107">L’interface **INapEnforcementClientCallback** fournit des méthodes de rappel que les clients de mise en œuvre doivent implémenter pour permettre à NapAgent de communiquer avec eux.</span><span class="sxs-lookup"><span data-stu-id="71919-107">The **INapEnforcementClientCallback** interface provides callback methods that enforcement clients must implement to enable the NapAgent to communicate with them.</span></span>

## <a name="members"></a><span data-ttu-id="71919-108">Membres</span><span class="sxs-lookup"><span data-stu-id="71919-108">Members</span></span>

<span data-ttu-id="71919-109">L’interface **INapEnforcementClientCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="71919-109">The **INapEnforcementClientCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="71919-110">**INapEnforcementClientCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="71919-110">**INapEnforcementClientCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="71919-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="71919-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="71919-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="71919-112">Methods</span></span>

<span data-ttu-id="71919-113">L’interface **INapEnforcementClientCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="71919-113">The **INapEnforcementClientCallback** interface has these methods.</span></span>



| <span data-ttu-id="71919-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="71919-114">Method</span></span>                                                                                                         | <span data-ttu-id="71919-115">Description</span><span class="sxs-lookup"><span data-stu-id="71919-115">Description</span></span>                                                                      |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="71919-116">**INapEnforcementClientCallback::GetConnections**</span><span class="sxs-lookup"><span data-stu-id="71919-116">**INapEnforcementClientCallback::GetConnections**</span></span>](inapenforcementclientcallback-getconnections-method.md)   | <span data-ttu-id="71919-117">Utilisé par NapAgent pour récupérer des connexions.</span><span class="sxs-lookup"><span data-stu-id="71919-117">Used by the NapAgent to retrieve connections.</span></span><br/>                         |
| [<span data-ttu-id="71919-118">**INapEnforcementClientCallback::NotifySoHChange**</span><span class="sxs-lookup"><span data-stu-id="71919-118">**INapEnforcementClientCallback::NotifySoHChange**</span></span>](inapenforcementclientcallback-notifysohchange-method.md) | <span data-ttu-id="71919-119">Utilisé par NapAgent pour informer le client de contrainte des modifications de SoH.</span><span class="sxs-lookup"><span data-stu-id="71919-119">Used by the NapAgent to inform the enforcement client of SoH changes.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="71919-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71919-120">Requirements</span></span>



| <span data-ttu-id="71919-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71919-121">Requirement</span></span> | <span data-ttu-id="71919-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="71919-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71919-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71919-123">Minimum supported client</span></span><br/> | <span data-ttu-id="71919-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71919-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="71919-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="71919-125">Minimum supported server</span></span><br/> | <span data-ttu-id="71919-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="71919-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="71919-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="71919-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="71919-128"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="71919-128"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="71919-129">MIDL</span><span class="sxs-lookup"><span data-stu-id="71919-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="71919-130"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="71919-130"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



 

