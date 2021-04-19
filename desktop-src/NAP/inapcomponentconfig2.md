---
title: Interface INapComponentConfig2 (NapCommon. h)
description: Fournit des méthodes de configuration du système NAP pour les programmes de validation d’intégrité système afin de configurer une interface utilisateur de serveur de stratégie réseau (NPS) à distance.
ms.assetid: 35150184-300c-4ea4-bff9-b3c33fa3156b
keywords:
- NAP de l’interface INapComponentConfig2
- INapComponentConfig2 interface NAP, Description
topic_type:
- apiref
api_name:
- INapComponentConfig2
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29bd6fbea7696d0e4d5eacefd028ce7d33e549e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513772"
---
# <a name="inapcomponentconfig2-interface"></a><span data-ttu-id="43bfa-105">Interface INapComponentConfig2</span><span class="sxs-lookup"><span data-stu-id="43bfa-105">INapComponentConfig2 interface</span></span>

> [!Note]  
> <span data-ttu-id="43bfa-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="43bfa-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="43bfa-107">L’interface **INapComponentConfig2** fournit des méthodes de configuration du système NAP pour les programmes de validation d’intégrité système afin de configurer une interface utilisateur de serveur de stratégie réseau (NPS) à distance.</span><span class="sxs-lookup"><span data-stu-id="43bfa-107">The **INapComponentConfig2** interface provides NAP system configuration methods for system health validators (SHVs) to configure a network policy server (NPS) user interface remotely.</span></span>

> [!Note]  
> <span data-ttu-id="43bfa-108">Cette interface hérite de toutes les méthodes de [**INapComponentConfig**](inapcomponentconfig.md) et doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="43bfa-108">This interface inherits all the methods of [**INapComponentConfig**](inapcomponentconfig.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="43bfa-109">Membres</span><span class="sxs-lookup"><span data-stu-id="43bfa-109">Members</span></span>

<span data-ttu-id="43bfa-110">L’interface **INapComponentConfig2** hérite de [**INapComponentConfig**](inapcomponentconfig.md).</span><span class="sxs-lookup"><span data-stu-id="43bfa-110">The **INapComponentConfig2** interface inherits from [**INapComponentConfig**](inapcomponentconfig.md).</span></span> <span data-ttu-id="43bfa-111">**INapComponentConfig2** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="43bfa-111">**INapComponentConfig2** also has these types of members:</span></span>

-   [<span data-ttu-id="43bfa-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="43bfa-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="43bfa-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="43bfa-113">Methods</span></span>

<span data-ttu-id="43bfa-114">L’interface **INapComponentConfig2** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="43bfa-114">The **INapComponentConfig2** interface has these methods.</span></span>



| <span data-ttu-id="43bfa-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="43bfa-115">Method</span></span>                                                                                                | <span data-ttu-id="43bfa-116">Description</span><span class="sxs-lookup"><span data-stu-id="43bfa-116">Description</span></span>                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43bfa-117">**INapComponentConfig2::InvokeUIForMachine**</span><span class="sxs-lookup"><span data-stu-id="43bfa-117">**INapComponentConfig2::InvokeUIForMachine**</span></span>](inapcomponentconfig2-invokeuiformachine.md)           | <span data-ttu-id="43bfa-118">Implémenté par les validateurs d’intégrité du système pour gérer la configuration distante directement sur l’ordinateur spécifié.</span><span class="sxs-lookup"><span data-stu-id="43bfa-118">Implemented by SHVs as needed to manage remote configuration directly on the machine specified.</span></span><br/>                                                                 |
| [<span data-ttu-id="43bfa-119">**INapComponentConfig2::InvokeUIFromConfigBlob**</span><span class="sxs-lookup"><span data-stu-id="43bfa-119">**INapComponentConfig2::InvokeUIFromConfigBlob**</span></span>](inapcomponentconfig2-invokeuifromconfigblob.md)   | <span data-ttu-id="43bfa-120">Implémenté par les validateurs d’intégrité du système en fonction des besoins pour charger la configuration de l’ordinateur distant en mémoire et afficher une interface utilisateur qui permet la manipulation des données de configuration.</span><span class="sxs-lookup"><span data-stu-id="43bfa-120">Implemented by SHVs as needed to load the configuration of the remote machine in memory and to display a UI that allows manipulation of the configuration data.</span></span><br/> |
| [<span data-ttu-id="43bfa-121">**INapComponentConfig2::IsRemoteConfigSupported**</span><span class="sxs-lookup"><span data-stu-id="43bfa-121">**INapComponentConfig2::IsRemoteConfigSupported**</span></span>](inapcomponentconfig2-isremoteconfigsupported.md) | <span data-ttu-id="43bfa-122">Implémenté par les validateurs d’intégrité du système pour indiquer si la configuration distante est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="43bfa-122">Implemented by SHVs to indicate whether remote configuration is supported.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="43bfa-123">Notes</span><span class="sxs-lookup"><span data-stu-id="43bfa-123">Remarks</span></span>

<span data-ttu-id="43bfa-124">Cette interface ne doit pas être implémentée par les agents d’intégrité système (SHA) ou les clients de contrainte de mise en quarantaine (QEC).</span><span class="sxs-lookup"><span data-stu-id="43bfa-124">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="43bfa-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43bfa-125">Requirements</span></span>



| <span data-ttu-id="43bfa-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43bfa-126">Requirement</span></span> | <span data-ttu-id="43bfa-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="43bfa-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="43bfa-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43bfa-128">Minimum supported client</span></span><br/> | <span data-ttu-id="43bfa-129">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="43bfa-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="43bfa-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43bfa-130">Minimum supported server</span></span><br/> | <span data-ttu-id="43bfa-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43bfa-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="43bfa-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="43bfa-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="43bfa-133"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="43bfa-133"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="43bfa-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="43bfa-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="43bfa-135"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="43bfa-135"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43bfa-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43bfa-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43bfa-137">**INapComponentConfig**</span><span class="sxs-lookup"><span data-stu-id="43bfa-137">**INapComponentConfig**</span></span>](inapcomponentconfig.md)
</dt> <dt>

[<span data-ttu-id="43bfa-138">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="43bfa-138">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="43bfa-139">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="43bfa-139">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





