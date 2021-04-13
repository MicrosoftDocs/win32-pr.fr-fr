---
title: Méthode GetStringProperty de la classe Win32_RDMSDeploymentSettings
description: Récupère une propriété de type chaîne pour les paramètres de déploiement d’une collection de bureaux virtuels.
ms.assetid: 468ffdea-57a9-4478-adae-3629e4522762
ms.tgt_platform: multiple
keywords:
- GetStringProperty, méthode Services Bureau à distance
- Méthode GetStringProperty Services Bureau à distance, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f26a570becbbae6b0d768c399acd3dd2954ecdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384327"
---
# <a name="getstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="cd3bc-106">Méthode GetStringProperty de la \_ classe RDMSDeploymentSettings Win32</span><span class="sxs-lookup"><span data-stu-id="cd3bc-106">GetStringProperty method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="cd3bc-107">Récupère une propriété de type chaîne pour les paramètres de déploiement d’une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="cd3bc-107">Retrieves a string property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd3bc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd3bc-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="cd3bc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd3bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd3bc-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="cd3bc-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd3bc-111">Alias de la collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="cd3bc-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="cd3bc-112">*Valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cd3bc-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd3bc-113">Chaîne qui reçoit la valeur récupérée.</span><span class="sxs-lookup"><span data-stu-id="cd3bc-113">A string that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd3bc-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd3bc-114">Requirements</span></span>



| <span data-ttu-id="cd3bc-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd3bc-115">Requirement</span></span> | <span data-ttu-id="cd3bc-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd3bc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd3bc-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd3bc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cd3bc-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd3bc-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="cd3bc-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd3bc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cd3bc-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cd3bc-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="cd3bc-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cd3bc-121">Namespace</span></span><br/>                | <span data-ttu-id="cd3bc-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="cd3bc-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="cd3bc-123">MOF</span><span class="sxs-lookup"><span data-stu-id="cd3bc-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd3bc-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd3bc-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd3bc-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cd3bc-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd3bc-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd3bc-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="cd3bc-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd3bc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd3bc-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="cd3bc-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





