---
title: Interface INapComponentConfig3 (NapCommon. h)
description: Fournit des méthodes de configuration du système NAP pour les programmes de validation d’intégrité système (SHV) afin de définir et de modifier les données de configuration d’un ID de configuration spécifique.
ms.assetid: dbb78f7a-7c6b-4bf1-b471-374857d5dafe
keywords:
- NAP de l’interface INapComponentConfig3
- INapComponentConfig3 interface NAP, Description
topic_type:
- apiref
api_name:
- INapComponentConfig3
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac0cfead891da106a1a950ba83b9108b5950a738
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510304"
---
# <a name="inapcomponentconfig3-interface"></a><span data-ttu-id="6a0ce-105">Interface INapComponentConfig3</span><span class="sxs-lookup"><span data-stu-id="6a0ce-105">INapComponentConfig3 interface</span></span>

> [!Note]  
> <span data-ttu-id="6a0ce-106">La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="6a0ce-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6a0ce-107">L’interface **INapComponentConfig3** fournit des méthodes de configuration du système NAP pour les programmes de validation d’intégrité système (SHV) afin de définir et de modifier les données de configuration d’un ID de configuration spécifique.</span><span class="sxs-lookup"><span data-stu-id="6a0ce-107">The **INapComponentConfig3** interface provides NAP system configuration methods for system health validators (SHVs) to set and modify configuration data for a specific configuration ID.</span></span>

> [!Note]  
> <span data-ttu-id="6a0ce-108">Cette interface hérite de toutes les méthodes de [**INapComponentConfig2**](inapcomponentconfig2.md) et doit être utilisée à la place.</span><span class="sxs-lookup"><span data-stu-id="6a0ce-108">This interface inherits all the methods of [**INapComponentConfig2**](inapcomponentconfig2.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="6a0ce-109">Membres</span><span class="sxs-lookup"><span data-stu-id="6a0ce-109">Members</span></span>

<span data-ttu-id="6a0ce-110">L’interface **INapComponentConfig3** hérite de [**INapComponentConfig2**](inapcomponentconfig2.md).</span><span class="sxs-lookup"><span data-stu-id="6a0ce-110">The **INapComponentConfig3** interface inherits from [**INapComponentConfig2**](inapcomponentconfig2.md).</span></span> <span data-ttu-id="6a0ce-111">**INapComponentConfig3** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6a0ce-111">**INapComponentConfig3** also has these types of members:</span></span>

-   [<span data-ttu-id="6a0ce-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6a0ce-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6a0ce-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6a0ce-113">Methods</span></span>

<span data-ttu-id="6a0ce-114">L’interface **INapComponentConfig3** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6a0ce-114">The **INapComponentConfig3** interface has these methods.</span></span>



| <span data-ttu-id="6a0ce-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="6a0ce-115">Method</span></span>                                                                                | <span data-ttu-id="6a0ce-116">Description</span><span class="sxs-lookup"><span data-stu-id="6a0ce-116">Description</span></span>                                                                                                    |
|:--------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a0ce-117">**INapComponentConfig3 ::D eleteAllConfig**</span><span class="sxs-lookup"><span data-stu-id="6a0ce-117">**INapComponentConfig3::DeleteAllConfig**</span></span>](inapcomponentconfig3-deleteallconfig.md) | <span data-ttu-id="6a0ce-118">Implémenté par les validateurs d’intégrité du système pour fournir un moyen de réinitialiser le magasin SHV à son état d’origine après l’installation.</span><span class="sxs-lookup"><span data-stu-id="6a0ce-118">Implemented by SHVs to provide a way to reset the SHV store to its original state after setup.</span></span><br/>      |
| [<span data-ttu-id="6a0ce-119">**INapComponentConfig3 ::D eleteConfig**</span><span class="sxs-lookup"><span data-stu-id="6a0ce-119">**INapComponentConfig3::DeleteConfig**</span></span>](inapcomponentconfig3-deleteconfig.md)       | <span data-ttu-id="6a0ce-120">Implémenté par les validateurs d’intégrité du système pour fournir un moyen de supprimer des données de configuration pour un ID de configuration spécifique.</span><span class="sxs-lookup"><span data-stu-id="6a0ce-120">Implemented by SHVs to provide a way to delete configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="6a0ce-121">**INapComponentConfig3::GetConfigFromID**</span><span class="sxs-lookup"><span data-stu-id="6a0ce-121">**INapComponentConfig3::GetConfigFromID**</span></span>](inapcomponentconfig3-getconfigfromid.md) | <span data-ttu-id="6a0ce-122">Implémenté par les validateurs d’intégrité du système pour fournir un moyen d’obtenir des données de configuration pour un ID de configuration spécifique.</span><span class="sxs-lookup"><span data-stu-id="6a0ce-122">Implemented by SHVs to provide a way to obtain configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="6a0ce-123">**INapComponentConfig3 :: NewConfig**</span><span class="sxs-lookup"><span data-stu-id="6a0ce-123">**INapComponentConfig3::NewConfig**</span></span>](inapcomponentconfig3-newconfig.md)             | <span data-ttu-id="6a0ce-124">Implémenté par les validateurs d’intégrité du système pour fournir un moyen de créer des données de configuration pour un ID de configuration spécifique.</span><span class="sxs-lookup"><span data-stu-id="6a0ce-124">Implemented by SHVs to provide a way to create configuration data for a specific configuration ID.</span></span><br/>  |
| [<span data-ttu-id="6a0ce-125">**INapComponentConfig3::SetConfigToID**</span><span class="sxs-lookup"><span data-stu-id="6a0ce-125">**INapComponentConfig3::SetConfigToID**</span></span>](inapcomponentconfig3-setconfigtoid.md)     | <span data-ttu-id="6a0ce-126">Implémenté par les validateurs d’intégrité du système pour fournir un moyen de définir les données de configuration pour un ID de configuration spécifique.</span><span class="sxs-lookup"><span data-stu-id="6a0ce-126">Implemented by SHVs to provide a way to set the configuration data for a specific configuration ID.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6a0ce-127">Notes</span><span class="sxs-lookup"><span data-stu-id="6a0ce-127">Remarks</span></span>

<span data-ttu-id="6a0ce-128">Cette interface ne doit pas être implémentée par les agents d’intégrité système (SHA) ou les clients de contrainte de mise en quarantaine (QEC).</span><span class="sxs-lookup"><span data-stu-id="6a0ce-128">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a0ce-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a0ce-129">Requirements</span></span>



| <span data-ttu-id="6a0ce-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a0ce-130">Requirement</span></span> | <span data-ttu-id="6a0ce-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a0ce-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a0ce-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a0ce-132">Minimum supported client</span></span><br/> | <span data-ttu-id="6a0ce-133">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a0ce-133">None supported</span></span><br/>                                                                |
| <span data-ttu-id="6a0ce-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a0ce-134">Minimum supported server</span></span><br/> | <span data-ttu-id="6a0ce-135">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a0ce-135">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a0ce-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="6a0ce-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a0ce-137"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a0ce-137"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a0ce-138">MIDL</span><span class="sxs-lookup"><span data-stu-id="6a0ce-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6a0ce-139"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6a0ce-139"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a0ce-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a0ce-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a0ce-141">**INapComponentConfig2**</span><span class="sxs-lookup"><span data-stu-id="6a0ce-141">**INapComponentConfig2**</span></span>](inapcomponentconfig2.md)
</dt> <dt>

[<span data-ttu-id="6a0ce-142">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="6a0ce-142">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="6a0ce-143">Référence NAP</span><span class="sxs-lookup"><span data-stu-id="6a0ce-143">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





