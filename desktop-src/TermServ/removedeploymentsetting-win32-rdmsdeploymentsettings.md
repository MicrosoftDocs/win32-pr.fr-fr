---
title: Méthode RemoveDeploymentSetting de la classe Win32_RDMSDeploymentSettings
description: Supprime les paramètres de déploiement pour une collection de bureaux virtuels.
ms.assetid: 68e102a3-8f3f-4997-bdf0-c2ae3640ed42
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveDeploymentSetting
- Services Bureau à distance de la méthode RemoveDeploymentSetting, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode RemoveDeploymentSetting
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.RemoveDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 336b93f86d6b96074341dde4851813b26eb66fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844306"
---
# <a name="removedeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="8323c-106">Méthode RemoveDeploymentSetting de la \_ classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="8323c-106">RemoveDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="8323c-107">Supprime les paramètres de déploiement pour une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="8323c-107">Deletes the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8323c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8323c-108">Syntax</span></span>


```mof
uint32 RemoveDeploymentSetting(
  [in] string Key
);
```



## <a name="parameters"></a><span data-ttu-id="8323c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8323c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8323c-110">*Clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8323c-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8323c-111">Alias de la collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="8323c-111">The alias of the virtual desktop collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8323c-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8323c-112">Requirements</span></span>



| <span data-ttu-id="8323c-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8323c-113">Requirement</span></span> | <span data-ttu-id="8323c-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="8323c-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8323c-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8323c-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8323c-116">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="8323c-116">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="8323c-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8323c-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8323c-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8323c-118">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="8323c-119">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8323c-119">Namespace</span></span><br/>                | <span data-ttu-id="8323c-120">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="8323c-120">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="8323c-121">MOF</span><span class="sxs-lookup"><span data-stu-id="8323c-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8323c-122"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8323c-122"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="8323c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="8323c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8323c-124"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8323c-124"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="8323c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8323c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8323c-126">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="8323c-126">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





