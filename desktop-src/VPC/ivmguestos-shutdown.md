---
title: IVMGuestOS méthode Shutdown (VPCCOMInterfaces. h)
description: Arrête le système d’exploitation invité sur la machine virtuelle.
ms.assetid: a1453ad1-c4c2-47bb-a612-d203a6ee8c18
keywords:
- Méthode d’arrêt Virtual PC
- Méthode d’arrêt Virtual PC, interface IVMGuestOS
- IVMGuestOS interface Virtual PC, méthode Shutdown
topic_type:
- apiref
api_name:
- IVMGuestOS.Shutdown
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63025270752af044a572cf9b6299e54b31b89ffe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742061"
---
# <a name="ivmguestosshutdown-method"></a><span data-ttu-id="2c534-106">IVMGuestOS :: Shutdown, méthode</span><span class="sxs-lookup"><span data-stu-id="2c534-106">IVMGuestOS::Shutdown method</span></span>

<span data-ttu-id="2c534-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2c534-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2c534-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2c534-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2c534-109">Arrête le système d’exploitation invité sur la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="2c534-109">Shuts down the guest operating system in the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="2c534-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c534-110">Syntax</span></span>


```C++
HRESULT Shutdown(
  [in]          VARIANT_BOOL isForced,
  [out, retval] IVMTask      **outShutdownTask
);
```



## <a name="parameters"></a><span data-ttu-id="2c534-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c534-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c534-112">*isForced* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2c534-112">*isForced* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c534-113">**Variante \_ TRUE** si l’arrêt doit être forcé, **\_ false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2c534-113">**VARIANT\_TRUE** if the shutdown is to be forced, **VARIANT\_FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="2c534-114">*outShutdownTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2c534-114">*outShutdownTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2c534-115">Objet [**IVMTask**](ivmtask.md) utilisé pour suivre l’achèvement du processus d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="2c534-115">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the shutdown process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c534-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c534-116">Return value</span></span>

<span data-ttu-id="2c534-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="2c534-117">This method can return one of these values.</span></span>



| <span data-ttu-id="2c534-118">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2c534-118">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="2c534-119">Description</span><span class="sxs-lookup"><span data-stu-id="2c534-119">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2c534-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2c534-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="2c534-121">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="2c534-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2c534-122"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="2c534-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="2c534-123">Le paramètre *outShutdownTask* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="2c534-123">The *outShutdownTask* parameter is **NULL**.</span></span><br/>                    |
| <dl> <span data-ttu-id="2c534-124"><dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="2c534-124"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="2c534-125">L’opération ne s’est pas terminée en temps opportun.</span><span class="sxs-lookup"><span data-stu-id="2c534-125">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="2c534-126"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="2c534-126"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="2c534-127">La machine virtuelle est introuvable.</span><span class="sxs-lookup"><span data-stu-id="2c534-127">The VM could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="2c534-128"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="2c534-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="2c534-129">La machine virtuelle doit être en cours d’exécution pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="2c534-129">The VM must be running for this operation.</span></span><br/>                      |
| <dl> <span data-ttu-id="2c534-130">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ accès à l’erreur \_ refusé)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="2c534-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="2c534-131">L’appelant doit disposer des autorisations d’accès en exécution pour cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="2c534-131">The caller must have execute access permissions for this VM.</span></span><br/>    |
| <dl> <span data-ttu-id="2c534-132"><dt>**Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="2c534-132"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>       | <span data-ttu-id="2c534-133">La fonctionnalité composants d’intégration n’est pas installée sur cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="2c534-133">The integration components feature is not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="2c534-134"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2c534-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="2c534-135">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="2c534-135">An unexpected error has occurred.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="2c534-136">Notes</span><span class="sxs-lookup"><span data-stu-id="2c534-136">Remarks</span></span>

<span data-ttu-id="2c534-137">La machine virtuelle doit être en cours d’exécution et la fonctionnalité composants d’intégration doit être installée lorsque cette méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="2c534-137">The VM must be running and integration components feature must be installed when this method is invoked.</span></span> <span data-ttu-id="2c534-138">Cette méthode est uniquement prise en charge pour les systèmes d’exploitation invités basés sur Windows.</span><span class="sxs-lookup"><span data-stu-id="2c534-138">This method is only supported for Windows-based guest operating systems.</span></span>

<span data-ttu-id="2c534-139">Les valeurs suivantes peuvent être retournées par le biais de la propriété [**Error**](ivmtask-error.md) de l’objet [**IVMTask**](ivmtask.md) retourné.</span><span class="sxs-lookup"><span data-stu-id="2c534-139">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="2c534-140">Code d' [**erreur**](ivmtask-error.md) /valeur</span><span class="sxs-lookup"><span data-stu-id="2c534-140">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="2c534-141">Description</span><span class="sxs-lookup"><span data-stu-id="2c534-141">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2c534-142"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` 0x80070005</span><span class="sxs-lookup"><span data-stu-id="2c534-142"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)</span></span><br/>                             | <span data-ttu-id="2c534-143">L’appelant doit disposer des autorisations d’accès en exécution pour cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="2c534-143">The caller must have execute access permissions for this VM.</span></span><br/>             |
| <span data-ttu-id="2c534-144"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span><span class="sxs-lookup"><span data-stu-id="2c534-144"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span></span><br/>                         | <span data-ttu-id="2c534-145">L’ordinateur est verrouillé et ne peut pas être arrêté sans l’option forcer.</span><span class="sxs-lookup"><span data-stu-id="2c534-145">The computer is locked and cannot be shut down without the force option.</span></span><br/> |
| <span data-ttu-id="2c534-146"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span><span class="sxs-lookup"><span data-stu-id="2c534-146"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span></span><br/>                                             | <span data-ttu-id="2c534-147">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="2c534-147">The device is not ready.</span></span><br/>                                                 |
| <span data-ttu-id="2c534-148"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span><span class="sxs-lookup"><span data-stu-id="2c534-148"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span></span><br/> | <span data-ttu-id="2c534-149">Un arrêt du système est en cours.</span><span class="sxs-lookup"><span data-stu-id="2c534-149">A system shutdown is in progress.</span></span><br/>                                        |



 

## <a name="requirements"></a><span data-ttu-id="2c534-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c534-150">Requirements</span></span>



| <span data-ttu-id="2c534-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c534-151">Requirement</span></span> | <span data-ttu-id="2c534-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c534-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c534-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c534-153">Minimum supported client</span></span><br/> | <span data-ttu-id="2c534-154">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c534-154">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2c534-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c534-155">Minimum supported server</span></span><br/> | <span data-ttu-id="2c534-156">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c534-156">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2c534-157">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="2c534-157">End of client support</span></span><br/>    | <span data-ttu-id="2c534-158">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2c534-158">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2c534-159">Produit</span><span class="sxs-lookup"><span data-stu-id="2c534-159">Product</span></span><br/>                  | <span data-ttu-id="2c534-160">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2c534-160">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2c534-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c534-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c534-162"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c534-162"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2c534-163">IID</span><span class="sxs-lookup"><span data-stu-id="2c534-163">IID</span></span><br/>                      | <span data-ttu-id="2c534-164">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="2c534-164">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="2c534-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c534-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c534-166">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="2c534-166">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

