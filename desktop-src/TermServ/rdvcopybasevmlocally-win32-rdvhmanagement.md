---
title: Méthode RdvCopyBaseVmLocally de la classe Win32_RdvhManagement
description: Copie un ordinateur virtuel de base local sur un serveur hôte de virtualisation des services Bureau à distance (RDV) spécifié.
ms.assetid: 13c0c629-42c6-4689-9740-f13f31688e42
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RdvCopyBaseVmLocally
- Services Bureau à distance de la méthode RdvCopyBaseVmLocally, classe Win32_RdvhManagement
- Win32_RdvhManagement de la classe Services Bureau à distance, méthode RdvCopyBaseVmLocally
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCopyBaseVmLocally
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d96e01038a4b41edcf32a6a5a9b353403fa6021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385171"
---
# <a name="rdvcopybasevmlocally-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="ee8a0-106">Méthode RdvCopyBaseVmLocally de la \_ classe Win32 RdvhManagement</span><span class="sxs-lookup"><span data-stu-id="ee8a0-106">RdvCopyBaseVmLocally method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="ee8a0-107">Copie un ordinateur virtuel de base local sur un serveur hôte de virtualisation des services Bureau à distance (RDV) spécifié.</span><span class="sxs-lookup"><span data-stu-id="ee8a0-107">Copies a local base virtual machine to a specified remote desktop virtualization (RDV) host server.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee8a0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee8a0-108">Syntax</span></span>


```mof
uint32 RdvCopyBaseVmLocally(
  [in] string BaseVmLocation,
  [in] string FarmName,
  [in] string GoldCacheLocation
);
```



## <a name="parameters"></a><span data-ttu-id="ee8a0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee8a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee8a0-110">*BaseVmLocation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee8a0-110">*BaseVmLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee8a0-111">Emplacement de la machine virtuelle de base.</span><span class="sxs-lookup"><span data-stu-id="ee8a0-111">The base virtual machine location.</span></span>

</dd> <dt>

<span data-ttu-id="ee8a0-112">*FarmName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee8a0-112">*FarmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee8a0-113">Nom de la batterie de serveurs hôtes vers laquelle effectuer la copie.</span><span class="sxs-lookup"><span data-stu-id="ee8a0-113">The name of the host farm to copy to.</span></span>

</dd> <dt>

<span data-ttu-id="ee8a0-114">*GoldCacheLocation* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee8a0-114">*GoldCacheLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee8a0-115">Emplacement du cache Gold.</span><span class="sxs-lookup"><span data-stu-id="ee8a0-115">The gold cache location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee8a0-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ee8a0-116">Return value</span></span>

<span data-ttu-id="ee8a0-117">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="ee8a0-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="ee8a0-118">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="ee8a0-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee8a0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee8a0-119">Requirements</span></span>



| <span data-ttu-id="ee8a0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee8a0-120">Requirement</span></span> | <span data-ttu-id="ee8a0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee8a0-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee8a0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee8a0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ee8a0-123">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee8a0-123">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="ee8a0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee8a0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ee8a0-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ee8a0-125">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="ee8a0-126">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ee8a0-126">Namespace</span></span><br/>                | <span data-ttu-id="ee8a0-127">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="ee8a0-127">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="ee8a0-128">MOF</span><span class="sxs-lookup"><span data-stu-id="ee8a0-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee8a0-129"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee8a0-129"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="ee8a0-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ee8a0-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee8a0-131"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee8a0-131"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee8a0-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ee8a0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee8a0-133">**\_RdvhManagement Win32**</span><span class="sxs-lookup"><span data-stu-id="ee8a0-133">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





