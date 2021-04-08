---
title: Méthode GetStringArrayDeploymentSetting de la classe Win32_RDMSDeploymentSettings
description: Récupère les paramètres de déploiement pour une collection de bureaux virtuels.
ms.assetid: ab380618-560e-425b-9bf0-a7de6b30d01a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetStringArrayDeploymentSetting
- Services Bureau à distance de la méthode GetStringArrayDeploymentSetting, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode GetStringArrayDeploymentSetting
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ac0b82441abef8af1b4f6c8e3bd48b89a8cb6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103169"
---
# <a name="getstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="37384-106">Méthode GetStringArrayDeploymentSetting de la \_ classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="37384-106">GetStringArrayDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="37384-107">Récupère les paramètres de déploiement pour une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="37384-107">Retrieves the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="37384-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="37384-108">Syntax</span></span>


```mof
uint32 GetStringArrayDeploymentSetting(
  [in]  string Key,
  [out] string Value[]
);
```



## <a name="parameters"></a><span data-ttu-id="37384-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="37384-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37384-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="37384-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37384-111">Alias de la collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="37384-111">The alias of the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="37384-112">*Valeur* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="37384-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="37384-113">Reçoit un tableau de chaînes qui contient les paramètres de déploiement.</span><span class="sxs-lookup"><span data-stu-id="37384-113">Receives an array of strings that contains the deployment settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37384-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37384-114">Requirements</span></span>



| <span data-ttu-id="37384-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37384-115">Requirement</span></span> | <span data-ttu-id="37384-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="37384-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="37384-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37384-117">Minimum supported client</span></span><br/> | <span data-ttu-id="37384-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="37384-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="37384-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37384-119">Minimum supported server</span></span><br/> | <span data-ttu-id="37384-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="37384-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="37384-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="37384-121">Namespace</span></span><br/>                | <span data-ttu-id="37384-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="37384-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="37384-123">MOF</span><span class="sxs-lookup"><span data-stu-id="37384-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="37384-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="37384-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="37384-125">DLL</span><span class="sxs-lookup"><span data-stu-id="37384-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="37384-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="37384-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="37384-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37384-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37384-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="37384-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





