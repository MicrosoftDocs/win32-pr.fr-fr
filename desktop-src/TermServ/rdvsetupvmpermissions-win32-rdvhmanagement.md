---
title: Méthode RdvSetupVMPermissions de la classe Win32_RdvhManagement
description: Définit les autorisations sur un ordinateur virtuel pour l’utilisateur actuel.
ms.assetid: 6ac45983-d468-4a3b-875f-48717ba23ed0
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RdvSetupVMPermissions
- Services Bureau à distance de la méthode RdvSetupVMPermissions, classe Win32_RdvhManagement
- Win32_RdvhManagement de la classe Services Bureau à distance, méthode RdvSetupVMPermissions
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvSetupVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8028a33bc772f9dd37f25a1dc22074baf771b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465306"
---
# <a name="rdvsetupvmpermissions-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="23415-106">Méthode RdvSetupVMPermissions de la \_ classe Win32 RdvhManagement</span><span class="sxs-lookup"><span data-stu-id="23415-106">RdvSetupVMPermissions method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="23415-107">Définit les autorisations sur un ordinateur virtuel pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="23415-107">Sets the permissions on a virtual machine for the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="23415-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="23415-108">Syntax</span></span>


```mof
uint32 RdvSetupVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a><span data-ttu-id="23415-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="23415-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23415-110">*VmName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="23415-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23415-111">Nom de l’ordinateur virtuel sur lequel définir des autorisations.</span><span class="sxs-lookup"><span data-stu-id="23415-111">The name of the virtual machine to set permissions on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23415-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="23415-112">Return value</span></span>

<span data-ttu-id="23415-113">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="23415-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="23415-114">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="23415-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="23415-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23415-115">Requirements</span></span>



| <span data-ttu-id="23415-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23415-116">Requirement</span></span> | <span data-ttu-id="23415-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="23415-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="23415-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23415-118">Minimum supported client</span></span><br/> | <span data-ttu-id="23415-119">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="23415-119">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="23415-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23415-120">Minimum supported server</span></span><br/> | <span data-ttu-id="23415-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="23415-121">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="23415-122">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="23415-122">Namespace</span></span><br/>                | <span data-ttu-id="23415-123">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="23415-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="23415-124">MOF</span><span class="sxs-lookup"><span data-stu-id="23415-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23415-125"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="23415-125"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="23415-126">DLL</span><span class="sxs-lookup"><span data-stu-id="23415-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23415-127"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23415-127"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23415-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23415-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23415-129">**\_RdvhManagement Win32**</span><span class="sxs-lookup"><span data-stu-id="23415-129">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





