---
title: Méthode RdvMigrateVmToDifferentHost de la classe Win32_RdvhManagement
description: Lance une migration dynamique d’un ordinateur virtuel vers un ordinateur hôte spécifié.
ms.assetid: aa4b1e57-a97c-410b-9b9d-423a1c77de70
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RdvMigrateVmToDifferentHost
- Services Bureau à distance de la méthode RdvMigrateVmToDifferentHost, classe Win32_RdvhManagement
- Win32_RdvhManagement de la classe Services Bureau à distance, méthode RdvMigrateVmToDifferentHost
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvMigrateVmToDifferentHost
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3def1be6332397fb3830ffe8c90f324afc9f1b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741493"
---
# <a name="rdvmigratevmtodifferenthost-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="74df6-106">Méthode RdvMigrateVmToDifferentHost de la \_ classe Win32 RdvhManagement</span><span class="sxs-lookup"><span data-stu-id="74df6-106">RdvMigrateVmToDifferentHost method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="74df6-107">Lance une migration dynamique d’un ordinateur virtuel vers un ordinateur hôte spécifié.</span><span class="sxs-lookup"><span data-stu-id="74df6-107">Initiates a live migration of a virtual machine to a specified host.</span></span>

## <a name="syntax"></a><span data-ttu-id="74df6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74df6-108">Syntax</span></span>


```mof
uint32 RdvMigrateVmToDifferentHost(
  [in] string VmName,
  [in] string DestinationHost
);
```



## <a name="parameters"></a><span data-ttu-id="74df6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="74df6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74df6-110">*VmName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74df6-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74df6-111">Nom de la machine virtuelle à migrer.</span><span class="sxs-lookup"><span data-stu-id="74df6-111">Name of the virtual machine to migrate.</span></span>

</dd> <dt>

<span data-ttu-id="74df6-112">*DestinationHost* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="74df6-112">*DestinationHost* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74df6-113">nom de l’hôte de destination.</span><span class="sxs-lookup"><span data-stu-id="74df6-113">name of the destination host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74df6-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="74df6-114">Return value</span></span>

<span data-ttu-id="74df6-115">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="74df6-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="74df6-116">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="74df6-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="74df6-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74df6-117">Requirements</span></span>



| <span data-ttu-id="74df6-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74df6-118">Requirement</span></span> | <span data-ttu-id="74df6-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="74df6-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="74df6-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74df6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="74df6-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="74df6-121">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="74df6-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74df6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="74df6-123">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="74df6-123">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="74df6-124">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="74df6-124">Namespace</span></span><br/>                | <span data-ttu-id="74df6-125">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="74df6-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="74df6-126">MOF</span><span class="sxs-lookup"><span data-stu-id="74df6-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74df6-127"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74df6-127"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="74df6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="74df6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74df6-129"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74df6-129"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74df6-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74df6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74df6-131">**\_RdvhManagement Win32**</span><span class="sxs-lookup"><span data-stu-id="74df6-131">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





