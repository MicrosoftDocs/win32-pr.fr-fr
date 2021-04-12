---
title: IVMGuestOS, méthode de redémarrage (VPCCOMInterfaces. h)
description: Redémarre le système d’exploitation invité.
ms.assetid: 328c7aa1-d9bd-452d-95dd-9f6a03fa8c9e
keywords:
- Redémarrage de la méthode Virtual PC
- Méthode de redémarrage de Virtual PC, interface IVMGuestOS
- IVMGuestOS interface Virtual PC, restart, méthode
topic_type:
- apiref
api_name:
- IVMGuestOS.Restart
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 110718e45d04445dd895a2bdb27419fbd24731c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384752"
---
# <a name="ivmguestosrestart-method"></a><span data-ttu-id="0516b-106">IVMGuestOS :: Restart, méthode</span><span class="sxs-lookup"><span data-stu-id="0516b-106">IVMGuestOS::Restart method</span></span>

<span data-ttu-id="0516b-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0516b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0516b-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0516b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0516b-109">Redémarre le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="0516b-109">Restarts the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="0516b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0516b-110">Syntax</span></span>


```C++
HRESULT Restart(
  [in]          VARIANT_BOOL inForced,
  [out, retval] IVMTask      **outRestartTask
);
```



## <a name="parameters"></a><span data-ttu-id="0516b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0516b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0516b-112">*inappliqué* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0516b-112">*inForced* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0516b-113">**Variante \_ TRUE** si un redémarrage forcé est requis et **Variant \_ false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0516b-113">**VARIANT\_TRUE** if a forced restart is required and **VARIANT\_FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="0516b-114">*outRestartTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="0516b-114">*outRestartTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="0516b-115">Objet [**IVMTask**](ivmtask.md) utilisé pour suivre la progression de l’exécution de la séquence de redémarrage.</span><span class="sxs-lookup"><span data-stu-id="0516b-115">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the restart sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0516b-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0516b-116">Return value</span></span>

<span data-ttu-id="0516b-117">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="0516b-117">This method can return one of these values.</span></span>



| <span data-ttu-id="0516b-118">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0516b-118">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="0516b-119">Description</span><span class="sxs-lookup"><span data-stu-id="0516b-119">Description</span></span>                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0516b-120"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0516b-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="0516b-121">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="0516b-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0516b-122"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="0516b-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="0516b-123">Le paramètre *outRestartTask* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="0516b-123">The *outRestartTask* parameter is **NULL**.</span></span><br/>                     |
| <dl> <span data-ttu-id="0516b-124"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0516b-124"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="0516b-125">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="0516b-125">An unexpected error has occurred.</span></span><br/>                               |
| <dl> <span data-ttu-id="0516b-126"><dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="0516b-126"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="0516b-127">L’opération ne s’est pas terminée en temps opportun.</span><span class="sxs-lookup"><span data-stu-id="0516b-127">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="0516b-128"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="0516b-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="0516b-129">L’ordinateur virtuel (VM) doit être en cours d’exécution pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="0516b-129">The virtual machine (VM) must be running for this operation.</span></span><br/>    |
| <dl> <span data-ttu-id="0516b-130"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="0516b-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="0516b-131">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="0516b-131">The configuration is unknown.</span></span><br/>                                   |
| <dl> <span data-ttu-id="0516b-132"><dt>**Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="0516b-132"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="0516b-133">La fonctionnalité composants d’intégration n’est pas installée sur cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0516b-133">The integration components feature is not installed in this VM.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0516b-134">Notes</span><span class="sxs-lookup"><span data-stu-id="0516b-134">Remarks</span></span>

<span data-ttu-id="0516b-135">Les valeurs suivantes peuvent être retournées par le biais de la propriété [**Error**](ivmtask-error.md) de l’objet [**IVMTask**](ivmtask.md) retourné.</span><span class="sxs-lookup"><span data-stu-id="0516b-135">The following values can be returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object.</span></span>



| <span data-ttu-id="0516b-136">Code d' [**erreur**](ivmtask-error.md) /valeur</span><span class="sxs-lookup"><span data-stu-id="0516b-136">[**Error**](ivmtask-error.md) code/Value</span></span>                                                                                                                                                                                                                                                                          | <span data-ttu-id="0516b-137">Description</span><span class="sxs-lookup"><span data-stu-id="0516b-137">Description</span></span>                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0516b-138"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` 0x80070005</span><span class="sxs-lookup"><span data-stu-id="0516b-138"><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0x80070005_"></span><span id="hresult_from_win32_error_access_denied___0x80070005_"></span><span id="HRESULT_FROM_WIN32_ERROR_ACCESS_DENIED___0X80070005_"></span>`HRESULT_FROM_WIN32(ERROR_ACCESS_DENIED)` (0x80070005)</span></span><br/>                             | <span data-ttu-id="0516b-139">L’appelant doit disposer des autorisations d’accès en exécution pour cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="0516b-139">The caller must have execute access permissions for this VM.</span></span><br/>             |
| <span data-ttu-id="0516b-140"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span><span class="sxs-lookup"><span data-stu-id="0516b-140"><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0x800704f7_"></span><span id="hresult_from_win32_error_machine_locked___0x800704f7_"></span><span id="HRESULT_FROM_WIN32_ERROR_MACHINE_LOCKED___0X800704F7_"></span>`HRESULT_FROM_WIN32(ERROR_MACHINE_LOCKED)` (0x800704f7)</span></span><br/>                         | <span data-ttu-id="0516b-141">L’ordinateur est verrouillé et ne peut pas être arrêté sans l’option forcer.</span><span class="sxs-lookup"><span data-stu-id="0516b-141">The computer is locked and cannot be shut down without the force option.</span></span><br/> |
| <span data-ttu-id="0516b-142"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span><span class="sxs-lookup"><span data-stu-id="0516b-142"><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0x80070015_"></span><span id="hresult_from_win32_error_not_ready___0x80070015_"></span><span id="HRESULT_FROM_WIN32_ERROR_NOT_READY___0X80070015_"></span>`HRESULT_FROM_WIN32(ERROR_NOT_READY)` (0x80070015)</span></span><br/>                                             | <span data-ttu-id="0516b-143">Le périphérique n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="0516b-143">The device is not ready.</span></span><br/>                                                 |
| <span data-ttu-id="0516b-144"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span><span class="sxs-lookup"><span data-stu-id="0516b-144"><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0x8007045b_"></span><span id="hresult_from_win32_error_shutdown_in_progress___0x8007045b_"></span><span id="HRESULT_FROM_WIN32_ERROR_SHUTDOWN_IN_PROGRESS___0X8007045B_"></span>`HRESULT_FROM_WIN32(ERROR_SHUTDOWN_IN_PROGRESS)` (0x8007045b)</span></span><br/> | <span data-ttu-id="0516b-145">Un arrêt du système est en cours.</span><span class="sxs-lookup"><span data-stu-id="0516b-145">A system shutdown is in progress.</span></span><br/>                                        |



 

## <a name="requirements"></a><span data-ttu-id="0516b-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0516b-146">Requirements</span></span>



| <span data-ttu-id="0516b-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0516b-147">Requirement</span></span> | <span data-ttu-id="0516b-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="0516b-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0516b-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0516b-149">Minimum supported client</span></span><br/> | <span data-ttu-id="0516b-150">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0516b-150">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0516b-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0516b-151">Minimum supported server</span></span><br/> | <span data-ttu-id="0516b-152">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0516b-152">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0516b-153">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="0516b-153">End of client support</span></span><br/>    | <span data-ttu-id="0516b-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0516b-154">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0516b-155">Produit</span><span class="sxs-lookup"><span data-stu-id="0516b-155">Product</span></span><br/>                  | <span data-ttu-id="0516b-156">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0516b-156">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0516b-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="0516b-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="0516b-158"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="0516b-158"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0516b-159">IID</span><span class="sxs-lookup"><span data-stu-id="0516b-159">IID</span></span><br/>                      | <span data-ttu-id="0516b-160">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="0516b-160">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="0516b-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0516b-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0516b-162">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="0516b-162">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

