---
title: Méthode QueryOfflineInformation de la classe Win32_TSVm
description: Récupère les propriétés du serveur de bureau virtuel (VDS) actuel, mais uniquement lorsque le serveur est hors connexion.
ms.assetid: f6ce74cb-a4a4-4e05-a0a7-bac0b7f52c45
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode QueryOfflineInformation
- Services Bureau à distance de la méthode QueryOfflineInformation, classe Win32_TSVm
- Win32_TSVm de la classe Services Bureau à distance, méthode QueryOfflineInformation
topic_type:
- apiref
api_name:
- Win32_TSVm.QueryOfflineInformation
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4750ebdb82b08ae1ed0350e1ac448d9aca4003b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843845"
---
# <a name="queryofflineinformation-method-of-the-win32_tsvm-class"></a><span data-ttu-id="4aecd-106">Méthode QueryOfflineInformation de la \_ classe Win32 TSVm</span><span class="sxs-lookup"><span data-stu-id="4aecd-106">QueryOfflineInformation method of the Win32\_TSVm class</span></span>

<span data-ttu-id="4aecd-107">Récupère les propriétés du serveur de bureau virtuel (VDS) actuel, mais uniquement lorsque le serveur est hors connexion.</span><span class="sxs-lookup"><span data-stu-id="4aecd-107">Retrieves the properties of the current virtual desktop server (VDS), but only when the server is offline.</span></span>

## <a name="syntax"></a><span data-ttu-id="4aecd-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4aecd-108">Syntax</span></span>


```mof
uint32 QueryOfflineInformation(
  [out] string  Build,
  [out] string  CurrentVersion,
  [out] string  InstallationType,
  [out] string  EditionId,
  [out] string  SysPrepImageState,
  [out] string  SysPrepMode,
  [out] sint32  ProcArch,
  [out] boolean fIsVmbusCapable,
  [out] boolean fIsRdvIcInstalled
);
```



## <a name="parameters"></a><span data-ttu-id="4aecd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4aecd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4aecd-110">*Créer* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4aecd-110">*Build* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4aecd-111">En cas de réussite, retourne la version de la build du VDS.</span><span class="sxs-lookup"><span data-stu-id="4aecd-111">On a success, returns the build version of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="4aecd-112">*CurrentVersion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4aecd-112">*CurrentVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4aecd-113">En cas de réussite, retourne la version actuelle du VDS.</span><span class="sxs-lookup"><span data-stu-id="4aecd-113">On a success, returns the current version of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="4aecd-114">*INSTALLATIONTYPE* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4aecd-114">*InstallationType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4aecd-115">En cas de réussite, retourne le type d’installation du VDS.</span><span class="sxs-lookup"><span data-stu-id="4aecd-115">On a success, returns the installation type of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="4aecd-116">*EditionId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4aecd-116">*EditionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4aecd-117">En cas de réussite, retourne l’ID d’édition du VDS.</span><span class="sxs-lookup"><span data-stu-id="4aecd-117">On a success, returns the edition ID of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="4aecd-118">*SysPrepImageState* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4aecd-118">*SysPrepImageState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4aecd-119">En cas de réussite, retourne l’état de l’image de préparation du système du VDS.</span><span class="sxs-lookup"><span data-stu-id="4aecd-119">On success, returns the system prep image state of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="4aecd-120">*SysPrepMode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4aecd-120">*SysPrepMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4aecd-121">En cas de réussite, retourne le mode de préparation du système du VDS.</span><span class="sxs-lookup"><span data-stu-id="4aecd-121">On a success, returns the system prep mode of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="4aecd-122">*ProcArch* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4aecd-122">*ProcArch* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4aecd-123">En cas de réussite, retourne une valeur indiquant l’architecture du processeur.</span><span class="sxs-lookup"><span data-stu-id="4aecd-123">On a success, returns a value indicating the processor architecture.</span></span>

<dt>

<span data-ttu-id="4aecd-124">0</span><span class="sxs-lookup"><span data-stu-id="4aecd-124">0</span></span>
</dt> <dd>

<span data-ttu-id="4aecd-125">x86</span><span class="sxs-lookup"><span data-stu-id="4aecd-125">x86</span></span>

</dd> <dt>

<span data-ttu-id="4aecd-126">1</span><span class="sxs-lookup"><span data-stu-id="4aecd-126">1</span></span>
</dt> <dd>

<span data-ttu-id="4aecd-127">amd64</span><span class="sxs-lookup"><span data-stu-id="4aecd-127">amd64</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4aecd-128">*fIsVmbusCapable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4aecd-128">*fIsVmbusCapable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4aecd-129">en cas de réussite, indique si le système est apte à la compatibilité VMBus.</span><span class="sxs-lookup"><span data-stu-id="4aecd-129">on a success, indicates whether the system is VMBus-capable.</span></span>

</dd> <dt>

<span data-ttu-id="4aecd-130">*fIsRdvIcInstalled* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4aecd-130">*fIsRdvIcInstalled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4aecd-131">En cas de réussite, indique si RDVIC est installé.</span><span class="sxs-lookup"><span data-stu-id="4aecd-131">On a success, indicates if RDVIC is installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4aecd-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4aecd-132">Return value</span></span>

<span data-ttu-id="4aecd-133">Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.</span><span class="sxs-lookup"><span data-stu-id="4aecd-133">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="4aecd-134">Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="4aecd-134">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="4aecd-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4aecd-135">Requirements</span></span>



| <span data-ttu-id="4aecd-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4aecd-136">Requirement</span></span> | <span data-ttu-id="4aecd-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="4aecd-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aecd-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4aecd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="4aecd-139">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4aecd-139">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="4aecd-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4aecd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="4aecd-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4aecd-141">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="4aecd-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4aecd-142">Namespace</span></span><br/>                | <span data-ttu-id="4aecd-143">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="4aecd-143">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="4aecd-144">MOF</span><span class="sxs-lookup"><span data-stu-id="4aecd-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4aecd-145"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4aecd-145"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="4aecd-146">DLL</span><span class="sxs-lookup"><span data-stu-id="4aecd-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4aecd-147"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4aecd-147"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4aecd-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4aecd-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4aecd-149">**\_TSVm Win32**</span><span class="sxs-lookup"><span data-stu-id="4aecd-149">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





