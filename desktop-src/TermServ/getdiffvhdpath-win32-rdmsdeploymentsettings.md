---
title: Méthode GetDiffVHDPath de la classe Win32_RDMSDeploymentSettings
description: Récupère le chemin d’accès du répertoire dans lequel les disques de différenciation sont déployés pour une collection de bureaux virtuels.
ms.assetid: 4340c817-2276-48a1-a856-b4c9e91ea981
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetDiffVHDPath
- Services Bureau à distance de la méthode GetDiffVHDPath, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode GetDiffVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7391315013cf8487d93b32f645933d14f06db2d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384055"
---
# <a name="getdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="1ec45-106">Méthode GetDiffVHDPath de la \_ classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="1ec45-106">GetDiffVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="1ec45-107">Récupère le chemin d’accès du répertoire dans lequel les disques de différenciation sont déployés pour une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="1ec45-107">Retrieves the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec45-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ec45-108">Syntax</span></span>


```mof
uint32 GetDiffVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="1ec45-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ec45-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ec45-110">*DirectoryPath* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1ec45-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1ec45-111">Reçoit le nouveau chemin d’accès de disque de différenciation.</span><span class="sxs-lookup"><span data-stu-id="1ec45-111">Receives the new differencing disk path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ec45-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ec45-112">Return value</span></span>

<span data-ttu-id="1ec45-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="1ec45-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec45-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ec45-114">Requirements</span></span>



| <span data-ttu-id="1ec45-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ec45-115">Requirement</span></span> | <span data-ttu-id="1ec45-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ec45-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec45-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ec45-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1ec45-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ec45-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1ec45-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1ec45-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1ec45-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1ec45-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="1ec45-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1ec45-121">Namespace</span></span><br/>                | <span data-ttu-id="1ec45-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="1ec45-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1ec45-123">MOF</span><span class="sxs-lookup"><span data-stu-id="1ec45-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ec45-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1ec45-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ec45-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1ec45-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ec45-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ec45-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1ec45-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ec45-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec45-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="1ec45-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





