---
title: Méthode SetStringArrayDeploymentSetting de la classe Win32_RDMSDeploymentSettings
description: Met à jour les paramètres de déploiement pour une collection de bureaux virtuels.
ms.assetid: 386594bd-a793-4e5d-ad2c-217951bee9f6
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetStringArrayDeploymentSetting
- Services Bureau à distance de la méthode SetStringArrayDeploymentSetting, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode SetStringArrayDeploymentSetting
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb5ecc6d1238b739f8fe19d02e96ba427ed09b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743492"
---
# <a name="setstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="11d07-106">Méthode SetStringArrayDeploymentSetting de la \_ classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="11d07-106">SetStringArrayDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="11d07-107">Met à jour les paramètres de déploiement pour une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="11d07-107">Updates the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="11d07-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11d07-108">Syntax</span></span>


```mof
uint32 SetStringArrayDeploymentSetting(
  [in] string Key,
  [in] string Value[]
);
```



## <a name="parameters"></a><span data-ttu-id="11d07-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11d07-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11d07-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="11d07-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11d07-111">Alias de la collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="11d07-111">The alias of the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="11d07-112">*Valeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="11d07-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11d07-113">Tableau de chaînes qui contient les nouveaux paramètres de déploiement.</span><span class="sxs-lookup"><span data-stu-id="11d07-113">An array of strings that contains the new deployment settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11d07-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11d07-114">Requirements</span></span>



| <span data-ttu-id="11d07-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11d07-115">Requirement</span></span> | <span data-ttu-id="11d07-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="11d07-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="11d07-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11d07-117">Minimum supported client</span></span><br/> | <span data-ttu-id="11d07-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="11d07-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="11d07-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="11d07-119">Minimum supported server</span></span><br/> | <span data-ttu-id="11d07-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="11d07-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="11d07-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="11d07-121">Namespace</span></span><br/>                | <span data-ttu-id="11d07-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="11d07-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="11d07-123">MOF</span><span class="sxs-lookup"><span data-stu-id="11d07-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11d07-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11d07-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="11d07-125">DLL</span><span class="sxs-lookup"><span data-stu-id="11d07-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11d07-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11d07-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="11d07-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11d07-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11d07-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="11d07-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





