---
title: Méthode SetSMBPath de la classe Win32_RDMSDeploymentSettings
description: Met à jour le chemin d’accès UNC au partage SMB sur lequel les machines virtuelles de la collection de bureaux virtuels sont déployées.
ms.assetid: 0b0b5b17-7b52-41e5-b9c6-c5f3e51c7853
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSMBPath
- Services Bureau à distance de la méthode SetSMBPath, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode SetSMBPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40598a3217ff1ca7c6082b3af09097352962309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942408"
---
# <a name="setsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="959c6-106">Méthode SetSMBPath de la \_ classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="959c6-106">SetSMBPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="959c6-107">Met à jour le chemin d’accès UNC au partage SMB sur lequel les machines virtuelles de la collection de bureaux virtuels sont déployées.</span><span class="sxs-lookup"><span data-stu-id="959c6-107">Updates the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="959c6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="959c6-108">Syntax</span></span>


```mof
uint32 SetSMBPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="959c6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="959c6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="959c6-110">*DirectoryPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="959c6-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="959c6-111">Nouveau chemin d’accès au partage SMB, au format UNC.</span><span class="sxs-lookup"><span data-stu-id="959c6-111">The new path to the SMB share, in UNC format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="959c6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="959c6-112">Return value</span></span>

<span data-ttu-id="959c6-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="959c6-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="959c6-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="959c6-114">Requirements</span></span>



| <span data-ttu-id="959c6-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="959c6-115">Requirement</span></span> | <span data-ttu-id="959c6-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="959c6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="959c6-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="959c6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="959c6-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="959c6-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="959c6-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="959c6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="959c6-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="959c6-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="959c6-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="959c6-121">Namespace</span></span><br/>                | <span data-ttu-id="959c6-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="959c6-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="959c6-123">MOF</span><span class="sxs-lookup"><span data-stu-id="959c6-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="959c6-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="959c6-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="959c6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="959c6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="959c6-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="959c6-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="959c6-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="959c6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="959c6-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="959c6-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





