---
title: Méthode GetSMBPath de la classe Win32_RDMSDeploymentSettings
description: Récupère le chemin d’accès UNC au partage SMB vers lequel les machines virtuelles de la collection de bureaux virtuels sont déployées.
ms.assetid: 0a5d3c11-6a77-48f7-a3ea-6f82725ff01f
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetSMBPath
- Services Bureau à distance de la méthode GetSMBPath, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode GetSMBPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1738faf82a6405018495dd762ba9585daa3e1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385291"
---
# <a name="getsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="040b0-106">Méthode GetSMBPath de la \_ classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="040b0-106">GetSMBPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="040b0-107">Récupère le chemin d’accès UNC au partage SMB vers lequel les machines virtuelles de la collection de bureaux virtuels sont déployées.</span><span class="sxs-lookup"><span data-stu-id="040b0-107">Retrieves the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="040b0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="040b0-108">Syntax</span></span>


```mof
uint32 GetSMBPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="040b0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="040b0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="040b0-110">*DirectoryPath* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="040b0-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="040b0-111">Reçoit un chemin d’accès au format UNC au partage SMB.</span><span class="sxs-lookup"><span data-stu-id="040b0-111">Receives a UNC formatted path to the SMB share.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="040b0-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="040b0-112">Return value</span></span>

<span data-ttu-id="040b0-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="040b0-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="040b0-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="040b0-114">Requirements</span></span>



| <span data-ttu-id="040b0-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="040b0-115">Requirement</span></span> | <span data-ttu-id="040b0-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="040b0-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="040b0-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="040b0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="040b0-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="040b0-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="040b0-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="040b0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="040b0-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="040b0-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="040b0-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="040b0-121">Namespace</span></span><br/>                | <span data-ttu-id="040b0-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="040b0-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="040b0-123">MOF</span><span class="sxs-lookup"><span data-stu-id="040b0-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="040b0-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="040b0-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="040b0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="040b0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="040b0-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="040b0-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="040b0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="040b0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="040b0-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="040b0-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





