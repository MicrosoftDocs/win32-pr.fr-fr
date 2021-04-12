---
title: Méthode SetDiffVHDPath de la classe Win32_RDMSDeploymentSettings
description: Met à jour le chemin d’accès du répertoire dans lequel les disques de différenciation sont déployés pour une collection de bureaux virtuels.
ms.assetid: 665ffbf9-0250-4956-9bce-f5a6714b47e4
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetDiffVHDPath
- Services Bureau à distance de la méthode SetDiffVHDPath, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode SetDiffVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e52d206c9e0cbff19f26e38a2a02f04ea0acc03d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384560"
---
# <a name="setdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="75acf-106">Méthode SetDiffVHDPath de la \_ classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="75acf-106">SetDiffVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="75acf-107">Met à jour le chemin d’accès du répertoire dans lequel les disques de différenciation sont déployés pour une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="75acf-107">Updates the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="75acf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75acf-108">Syntax</span></span>


```mof
uint32 SetDiffVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="75acf-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75acf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75acf-110">*DirectoryPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75acf-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75acf-111">Nouveau chemin d’accès de disque de différenciation.</span><span class="sxs-lookup"><span data-stu-id="75acf-111">The new differencing disk path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75acf-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75acf-112">Return value</span></span>

<span data-ttu-id="75acf-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="75acf-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="75acf-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75acf-114">Requirements</span></span>



| <span data-ttu-id="75acf-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75acf-115">Requirement</span></span> | <span data-ttu-id="75acf-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="75acf-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="75acf-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75acf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="75acf-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="75acf-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="75acf-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75acf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="75acf-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="75acf-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="75acf-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="75acf-121">Namespace</span></span><br/>                | <span data-ttu-id="75acf-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="75acf-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="75acf-123">MOF</span><span class="sxs-lookup"><span data-stu-id="75acf-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75acf-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75acf-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="75acf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="75acf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75acf-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75acf-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="75acf-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75acf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75acf-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="75acf-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





