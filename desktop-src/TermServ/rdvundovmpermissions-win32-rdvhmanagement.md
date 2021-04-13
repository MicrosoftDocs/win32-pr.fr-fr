---
title: Méthode RdvUndoVMPermissions de la classe Win32_RdvhManagement
description: Restaure les autorisations définies par RdvSetupVMPermissions sur la machine virtuelle spécifiée.
ms.assetid: 3331430e-7427-42f7-ab09-27fece8dc3ca
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RdvUndoVMPermissions
- Services Bureau à distance de la méthode RdvUndoVMPermissions, classe Win32_RdvhManagement
- Win32_RdvhManagement de la classe Services Bureau à distance, méthode RdvUndoVMPermissions
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvUndoVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1dc8892435522dcd2c7457fe4b74a0d9671740
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466742"
---
# <a name="rdvundovmpermissions-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="51d48-106">Méthode RdvUndoVMPermissions de la \_ classe Win32 RdvhManagement</span><span class="sxs-lookup"><span data-stu-id="51d48-106">RdvUndoVMPermissions method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="51d48-107">Restaure les autorisations définies par [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md) sur la machine virtuelle spécifiée.</span><span class="sxs-lookup"><span data-stu-id="51d48-107">Reverts permissions set by [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md) on the specified virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="51d48-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51d48-108">Syntax</span></span>


```mof
uint32 RdvUndoVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a><span data-ttu-id="51d48-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51d48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51d48-110">*VmName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="51d48-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51d48-111">Nom de l’ordinateur virtuel sur lequel annuler les autorisations.</span><span class="sxs-lookup"><span data-stu-id="51d48-111">Name of the virtual machine to undo permissions on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51d48-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51d48-112">Return value</span></span>

<span data-ttu-id="51d48-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="51d48-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="51d48-114">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="51d48-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="51d48-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51d48-115">Requirements</span></span>



| <span data-ttu-id="51d48-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51d48-116">Requirement</span></span> | <span data-ttu-id="51d48-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="51d48-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="51d48-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51d48-118">Minimum supported client</span></span><br/> | <span data-ttu-id="51d48-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="51d48-119">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="51d48-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51d48-120">Minimum supported server</span></span><br/> | <span data-ttu-id="51d48-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="51d48-121">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="51d48-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="51d48-122">Namespace</span></span><br/>                | <span data-ttu-id="51d48-123">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="51d48-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="51d48-124">MOF</span><span class="sxs-lookup"><span data-stu-id="51d48-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="51d48-125"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="51d48-125"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="51d48-126">DLL</span><span class="sxs-lookup"><span data-stu-id="51d48-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51d48-127"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51d48-127"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51d48-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51d48-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51d48-129">**\_RdvhManagement Win32**</span><span class="sxs-lookup"><span data-stu-id="51d48-129">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





