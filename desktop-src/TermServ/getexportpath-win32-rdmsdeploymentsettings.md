---
title: Méthode GetExportPath de la classe Win32_RDMSDeploymentSettings
description: Récupère le chemin d’accès du répertoire dans lequel les ordinateurs virtuels sont déployés pour une collection de bureaux virtuels.
ms.assetid: 8df79e31-b960-46ae-b49c-8052b356e1a8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetExportPath
- Services Bureau à distance de la méthode GetExportPath, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode GetExportPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baf96d1d71554f1b8ea310759d36d0918a511cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511128"
---
# <a name="getexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="87344-106">Méthode GetExportPath de la \_ classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="87344-106">GetExportPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="87344-107">Récupère le chemin d’accès du répertoire dans lequel les ordinateurs virtuels sont déployés pour une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="87344-107">Retrieves the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="87344-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87344-108">Syntax</span></span>


```mof
uint32 GetExportPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="87344-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87344-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87344-110">*DirectoryPath* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="87344-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="87344-111">Reçoit le chemin d’accès au répertoire.</span><span class="sxs-lookup"><span data-stu-id="87344-111">Receives the directory path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87344-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87344-112">Return value</span></span>

<span data-ttu-id="87344-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="87344-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="87344-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87344-114">Requirements</span></span>



| <span data-ttu-id="87344-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87344-115">Requirement</span></span> | <span data-ttu-id="87344-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="87344-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="87344-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87344-117">Minimum supported client</span></span><br/> | <span data-ttu-id="87344-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="87344-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="87344-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87344-119">Minimum supported server</span></span><br/> | <span data-ttu-id="87344-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="87344-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="87344-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="87344-121">Namespace</span></span><br/>                | <span data-ttu-id="87344-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="87344-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="87344-123">MOF</span><span class="sxs-lookup"><span data-stu-id="87344-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87344-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87344-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="87344-125">DLL</span><span class="sxs-lookup"><span data-stu-id="87344-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87344-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87344-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="87344-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87344-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87344-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="87344-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





