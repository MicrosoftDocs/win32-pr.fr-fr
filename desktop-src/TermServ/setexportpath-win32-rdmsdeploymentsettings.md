---
title: Méthode SetExportPath de la classe Win32_RDMSDeploymentSettings
description: Met à jour le chemin d’accès au répertoire dans lequel les machines virtuelles sont déployées pour une collection de bureaux virtuels.
ms.assetid: e52b79c8-6724-4264-93d5-4a2a14c89b6b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetExportPath
- Services Bureau à distance de la méthode SetExportPath, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode SetExportPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32dbc844aecf86d4c62fada6c5cd68d514a69272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510958"
---
# <a name="setexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="b8e34-106">Méthode SetExportPath de la \_ classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="b8e34-106">SetExportPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="b8e34-107">Met à jour le chemin d’accès au répertoire dans lequel les machines virtuelles sont déployées pour une collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="b8e34-107">Updates the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8e34-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8e34-108">Syntax</span></span>


```mof
uint32 SetExportPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="b8e34-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8e34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8e34-110">*DirectoryPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b8e34-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8e34-111">Nouveau chemin d’accès au répertoire.</span><span class="sxs-lookup"><span data-stu-id="b8e34-111">The new directory path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8e34-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b8e34-112">Return value</span></span>

<span data-ttu-id="b8e34-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="b8e34-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8e34-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b8e34-114">Requirements</span></span>



| <span data-ttu-id="b8e34-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b8e34-115">Requirement</span></span> | <span data-ttu-id="b8e34-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="b8e34-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8e34-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8e34-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b8e34-118">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8e34-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b8e34-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b8e34-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b8e34-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8e34-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="b8e34-121">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b8e34-121">Namespace</span></span><br/>                | <span data-ttu-id="b8e34-122">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="b8e34-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b8e34-123">MOF</span><span class="sxs-lookup"><span data-stu-id="b8e34-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8e34-124"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8e34-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8e34-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b8e34-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8e34-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8e34-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b8e34-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8e34-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8e34-128">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="b8e34-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





