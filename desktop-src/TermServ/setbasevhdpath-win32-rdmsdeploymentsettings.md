---
title: Méthode SetBaseVHDPath de la classe Win32_RDMSDeploymentSettings
description: Récupère le chemin d’accès de base au répertoire dans lequel les disques durs virtuels de la collection de bureaux virtuels sont déployés. | Méthode SetBaseVHDPath de la classe Win32_RDMSDeploymentSettings
ms.assetid: 1ea4cd93-ef17-4ec9-82f9-382c549f189c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetBaseVHDPath
- Services Bureau à distance de la méthode SetBaseVHDPath, classe Win32_RDMSDeploymentSettings
- Win32_RDMSDeploymentSettings de la classe Services Bureau à distance, méthode SetBaseVHDPath
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7907640a9641cff3c94475318bf499415b25184
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523125"
---
# <a name="setbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="7b877-107">Méthode SetBaseVHDPath de la \_ classe Win32 RDMSDeploymentSettings</span><span class="sxs-lookup"><span data-stu-id="7b877-107">SetBaseVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="7b877-108">Récupère le chemin d’accès de base au répertoire dans lequel les disques durs virtuels de la collection de bureaux virtuels sont déployés.</span><span class="sxs-lookup"><span data-stu-id="7b877-108">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b877-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b877-109">Syntax</span></span>


```mof
uint32 SetBaseVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="7b877-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b877-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b877-111">*DirectoryPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7b877-111">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7b877-112">Nouveau chemin de déploiement du disque dur virtuel.</span><span class="sxs-lookup"><span data-stu-id="7b877-112">The new VHD deployment path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b877-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7b877-113">Return value</span></span>

<span data-ttu-id="7b877-114">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="7b877-114">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b877-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b877-115">Requirements</span></span>



| <span data-ttu-id="7b877-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b877-116">Requirement</span></span> | <span data-ttu-id="7b877-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b877-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b877-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b877-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7b877-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b877-119">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="7b877-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b877-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7b877-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7b877-121">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="7b877-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7b877-122">Namespace</span></span><br/>                | <span data-ttu-id="7b877-123">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="7b877-123">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="7b877-124">MOF</span><span class="sxs-lookup"><span data-stu-id="7b877-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b877-125"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b877-125"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b877-126">DLL</span><span class="sxs-lookup"><span data-stu-id="7b877-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b877-127"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b877-127"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="7b877-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b877-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b877-129">**\_RDMSDeploymentSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="7b877-129">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





