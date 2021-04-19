---
title: Méthode GetProvisioningProperties de la classe Win32_RDMSCollectionProperties
description: Récupère les propriétés de configuration de la collection de bureaux virtuels.
ms.assetid: c314b7a5-8546-4711-833e-b47bb682aa53
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetProvisioningProperties
- Services Bureau à distance de la méthode GetProvisioningProperties, classe Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties de la classe Services Bureau à distance, méthode GetProvisioningProperties
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties.GetProvisioningProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ca58f82d2918441e5da3cf53d442497c1a6a2eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511377"
---
# <a name="getprovisioningproperties-method-of-the-win32_rdmscollectionproperties-class"></a><span data-ttu-id="1b979-106">Méthode GetProvisioningProperties de la \_ classe Win32 RDMSCollectionProperties</span><span class="sxs-lookup"><span data-stu-id="1b979-106">GetProvisioningProperties method of the Win32\_RDMSCollectionProperties class</span></span>

<span data-ttu-id="1b979-107">Récupère les propriétés de configuration de la collection de bureaux virtuels.</span><span class="sxs-lookup"><span data-stu-id="1b979-107">Retrieves the provisioning properties of the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b979-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b979-108">Syntax</span></span>


```mof
uint32 GetProvisioningProperties(
  [out] string  PoolVhdType,
  [out] string  MasterVmLocation,
  [out] string  NamePrefix,
  [out] uint32  NameStartIndex,
  [out] string  LocalVmLocation,
  [out] string  LocalGoldVmLocation,
  [out] boolean RunFromSMB,
  [out] string  SMBLocation,
  [out] boolean SMBStreaming,
  [out] string  VmDomain,
  [out] string  VmOU,
  [out] string  ProductKey
);
```



## <a name="parameters"></a><span data-ttu-id="1b979-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b979-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b979-110">*PoolVhdType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b979-110">*PoolVhdType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b979-111">Spécifie le format de disque dur virtuel (VHD) du pool d’ordinateurs virtuels dans la collection.</span><span class="sxs-lookup"><span data-stu-id="1b979-111">Specifies the VHD (virtual hard disk) format of the virtual machine pool in the collection.</span></span>

<dt>

<span data-ttu-id="1b979-112">Clone</span><span class="sxs-lookup"><span data-stu-id="1b979-112">Clone</span></span>
</dt> <dd>

<span data-ttu-id="1b979-113">Disque dur virtuel cloné.</span><span class="sxs-lookup"><span data-stu-id="1b979-113">A cloned VHD.</span></span>

</dd> <dt>

<span data-ttu-id="1b979-114">DiffDisk</span><span class="sxs-lookup"><span data-stu-id="1b979-114">DiffDisk</span></span>
</dt> <dd>

<span data-ttu-id="1b979-115">Disque dur virtuel de différenciation.</span><span class="sxs-lookup"><span data-stu-id="1b979-115">A differencing VHD.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1b979-116">*MasterVmLocation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b979-116">*MasterVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b979-117">Reçoit le chemin d’accès à l’image de machine virtuelle principale.</span><span class="sxs-lookup"><span data-stu-id="1b979-117">Receives the path to the master VM image.</span></span>

</dd> <dt>

<span data-ttu-id="1b979-118">*NamePrefix* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b979-118">*NamePrefix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b979-119">Reçoit le préfixe de nom à ajouter au début des noms de machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="1b979-119">Receives the name prefix to append to the beginning of virtual machine names.</span></span>

</dd> <dt>

<span data-ttu-id="1b979-120">*NameStartIndex* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b979-120">*NameStartIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b979-121">Index de début.</span><span class="sxs-lookup"><span data-stu-id="1b979-121">Start index.</span></span>

</dd> <dt>

<span data-ttu-id="1b979-122">*LocalVmLocation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b979-122">*LocalVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b979-123">Reçoit le chemin d’accès local aux ordinateurs virtuels sur les serveurs Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="1b979-123">Receives the local path to the virtual machines on the Hyper-V servers.</span></span> <span data-ttu-id="1b979-124">Si ce paramètre a la valeur **null** ou s’il est vide, le répertoire par défaut de l’ordinateur virtuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1b979-124">If this parameter is set to **NULL** or if it is empty, the default virtual machine directory will be used.</span></span>

</dd> <dt>

<span data-ttu-id="1b979-125">*LocalGoldVmLocation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b979-125">*LocalGoldVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b979-126">Reçoit le chemin d’accès local à l’image de disque dur virtuel Golden lorsque le paramètre *PoolVhdTpe* a la valeur « DiffDisk ».</span><span class="sxs-lookup"><span data-stu-id="1b979-126">Receives the local path to the golden VHD image when the *PoolVhdTpe* parameter is set to "DiffDisk".</span></span> <span data-ttu-id="1b979-127">Si ce paramètre a la valeur **null** ou s’il est vide, le répertoire par défaut de l’ordinateur virtuel est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1b979-127">If this parameter is set to **NULL** or if it is empty, the default virtual machine directory will be used.</span></span>

</dd> <dt>

<span data-ttu-id="1b979-128">*RunFromSMB* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b979-128">*RunFromSMB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b979-129">Reçoit une valeur qui indique si la collection doit être exécutée à partir d’un partage SMB (Server Message Block).</span><span class="sxs-lookup"><span data-stu-id="1b979-129">Receives a value that indicates whether to run the collection from an Server Message Block (SMB) share.</span></span> <span data-ttu-id="1b979-130">**True** pour exécuter les machines virtuelles à partir d’un partage SBM ; dispose **False**.</span><span class="sxs-lookup"><span data-stu-id="1b979-130">**TRUE** to run the virtual machines from an SBM share; otherwise; **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1b979-131">*SMBLocation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b979-131">*SMBLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b979-132">Reçoit le chemin d’accès au partage SMB si le partage SMB est activé.</span><span class="sxs-lookup"><span data-stu-id="1b979-132">Receives the path to the SMB share if SMB sharing is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="1b979-133">*SMBStreaming* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b979-133">*SMBStreaming* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b979-134">Reçoit une valeur qui indique si la diffusion SMB est activée.</span><span class="sxs-lookup"><span data-stu-id="1b979-134">Receives a value that indicates whether SMB streaming is enabled.</span></span> <span data-ttu-id="1b979-135">**True** si le partage SMB est activé ; dispose **False**.</span><span class="sxs-lookup"><span data-stu-id="1b979-135">**TRUE** if SMB sharing is enabled; otherwise; **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="1b979-136">*VmDomain* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b979-136">*VmDomain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b979-137">Reçoit le nom de domaine des ordinateurs virtuels dans la collection.</span><span class="sxs-lookup"><span data-stu-id="1b979-137">Receives the domain name of the virtual machines in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="1b979-138">*VmOU* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b979-138">*VmOU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b979-139">Reçoit l’unité d’organisation (OU) Active Directory des machines virtuelles de la collection.</span><span class="sxs-lookup"><span data-stu-id="1b979-139">Receives the Active Directory organization unit (OU) of the virtual machines in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="1b979-140">*ProductKey* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b979-140">*ProductKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b979-141">Reçoit les clés de produit du système d’exploitation pour les machines virtuelles de la collection.</span><span class="sxs-lookup"><span data-stu-id="1b979-141">Receives the OS product keys for the virtual machines in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b979-142">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1b979-142">Return value</span></span>

<span data-ttu-id="1b979-143">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="1b979-143">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b979-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b979-144">Requirements</span></span>



| <span data-ttu-id="1b979-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b979-145">Requirement</span></span> | <span data-ttu-id="1b979-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b979-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b979-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b979-147">Minimum supported client</span></span><br/> | <span data-ttu-id="1b979-148">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b979-148">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1b979-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b979-149">Minimum supported server</span></span><br/> | <span data-ttu-id="1b979-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1b979-150">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="1b979-151">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1b979-151">Namespace</span></span><br/>                | <span data-ttu-id="1b979-152">Racine \\ cimv2 cimv2 \\</span><span class="sxs-lookup"><span data-stu-id="1b979-152">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1b979-153">MOF</span><span class="sxs-lookup"><span data-stu-id="1b979-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b979-154"><dt>RDManagement. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1b979-154"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b979-155">DLL</span><span class="sxs-lookup"><span data-stu-id="1b979-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b979-156"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b979-156"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1b979-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b979-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b979-158">**\_RDMSCollectionProperties Win32**</span><span class="sxs-lookup"><span data-stu-id="1b979-158">**Win32\_RDMSCollectionProperties**</span></span>](win32-rdmscollectionproperties.md)
</dt> </dl>

 

 





