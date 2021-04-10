---
title: Méthode ProvisioningPrepJob de la classe Win32_RDMSVirtualDesktopCollection
description: Crée un travail d’approvisionnement de bureaux virtuels.
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ProvisioningPrepJob
- Services Bureau à distance de la méthode ProvisioningPrepJob, Win32_RDMSVirtualDesktopCollection interface
- Win32_RDMSVirtualDesktopCollection Services Bureau à distance de l’interface, méthode ProvisioningPrepJob
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningPrepJob
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9727dec0e31dd199f324ed01a4510041ba3558f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942043"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="2fc18-106">Méthode ProvisioningPrepJob de la \_ classe Win32 RDMSVirtualDesktopCollection</span><span class="sxs-lookup"><span data-stu-id="2fc18-106">ProvisioningPrepJob method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="2fc18-107">Crée un travail d’approvisionnement de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="2fc18-107">Creates a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fc18-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2fc18-108">Syntax</span></span>


```mof
uint32 ProvisioningPrepJob(
  [in]  string  CollectionAlias,
  [in]  string  VMHostName,
  [in]  string  VMName,
  [in]  string  ExportToLocation,
  [in]  boolean bSysPrep,
  [in]  string  MachineName,
  [in]  string  UserName,
  [in]  string  Password,
  [out] string  JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="2fc18-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2fc18-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fc18-110">*CollectionAlias* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fc18-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc18-111">Alias de la collection qui héberge le bureau virtuel.</span><span class="sxs-lookup"><span data-stu-id="2fc18-111">The alias of the collection that hosts the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="2fc18-112">*VMHostName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fc18-112">*VMHostName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc18-113">Nom d’hôte de l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="2fc18-113">The virtual machine host name.</span></span>

</dd> <dt>

<span data-ttu-id="2fc18-114">*Vmname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fc18-114">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc18-115">Nom de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="2fc18-115">The name of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2fc18-116">*ExportToLocation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fc18-116">*ExportToLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc18-117">Chemin d’accès complet de l’emplacement d’exportation du travail d’approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="2fc18-117">The full path the location to export the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="2fc18-118">*bSysPrep* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fc18-118">*bSysPrep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc18-119">Indique si le travail d’approvisionnement représente un déploiement Sysprep.</span><span class="sxs-lookup"><span data-stu-id="2fc18-119">Indicates whether the provisioning job represents a Sysprep deployment.</span></span>

</dd> <dt>

<span data-ttu-id="2fc18-120">*Nomordinateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fc18-120">*MachineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc18-121">Nom de l’ordinateur qui héberge l’ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="2fc18-121">The machine name of the computer that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2fc18-122">*Nom d’utilisateur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fc18-122">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc18-123">Nom d’utilisateur de l’administrateur de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="2fc18-123">The user name of the administrator of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2fc18-124">*Mot de passe* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2fc18-124">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc18-125">Mot de passe de l’administrateur de la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="2fc18-125">The password of the administrator of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="2fc18-126">*JobGuid* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2fc18-126">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fc18-127">**GUID** qui identifie de façon unique le travail d’approvisionnement.</span><span class="sxs-lookup"><span data-stu-id="2fc18-127">The **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fc18-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2fc18-128">Return value</span></span>

<span data-ttu-id="2fc18-129">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="2fc18-129">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fc18-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2fc18-130">Requirements</span></span>



| <span data-ttu-id="2fc18-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2fc18-131">Requirement</span></span> | <span data-ttu-id="2fc18-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="2fc18-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fc18-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fc18-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2fc18-134">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fc18-134">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="2fc18-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2fc18-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2fc18-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fc18-136">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="2fc18-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2fc18-137">Namespace</span></span><br/>                | <span data-ttu-id="2fc18-138">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="2fc18-138">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="2fc18-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2fc18-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fc18-140"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fc18-140"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fc18-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2fc18-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fc18-142"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fc18-142"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="2fc18-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2fc18-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fc18-144">**\_RDMSVirtualDesktopCollection Win32**</span><span class="sxs-lookup"><span data-stu-id="2fc18-144">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





