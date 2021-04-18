---
title: Méthode IVMVirtualMachine AddHardDiskConnection (VPCCOMInterfaces. h)
description: Ajoute une nouvelle connexion de disque dur à la machine virtuelle.
ms.assetid: 0f4e0666-2cfd-4c73-884d-6f8b43186c05
keywords:
- Méthode AddHardDiskConnection Virtual PC
- Méthode AddHardDiskConnection Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode AddHardDiskConnection
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0111577fd5cab614988e7295f3b8cdd59b8805c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512400"
---
# <a name="ivmvirtualmachineaddharddiskconnection-method"></a><span data-ttu-id="83084-106">IVMVirtualMachine :: AddHardDiskConnection, méthode</span><span class="sxs-lookup"><span data-stu-id="83084-106">IVMVirtualMachine::AddHardDiskConnection method</span></span>

<span data-ttu-id="83084-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="83084-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="83084-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="83084-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="83084-109">Ajoute une nouvelle connexion de disque dur à la machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="83084-109">Adds a new hard disk connection to the virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="83084-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83084-110">Syntax</span></span>


```C++
HRESULT AddHardDiskConnection(
  [in]          BSTR                  hardDiskPath,
  [in]          long                  busNumber,
  [in]          long                  deviceNumber,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="parameters"></a><span data-ttu-id="83084-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83084-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83084-112">*hardDiskPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83084-112">*hardDiskPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83084-113">Le chemin d’accès complet du fichier de disque dur virtuel (VHD) pour se connecter.</span><span class="sxs-lookup"><span data-stu-id="83084-113">The full path of the virtual hard disk (VHD) file to connect.</span></span>

</dd> <dt>

<span data-ttu-id="83084-114">*busNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83084-114">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83084-115">Bus auquel le lecteur sera attaché.</span><span class="sxs-lookup"><span data-stu-id="83084-115">The bus to which the drive will be attached.</span></span>



| <span data-ttu-id="83084-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="83084-116">Value</span></span>                                                                        | <span data-ttu-id="83084-117">Signification</span><span class="sxs-lookup"><span data-stu-id="83084-117">Meaning</span></span>                                                  |
|------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="83084-118"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="83084-118"><dt>0</dt></span></span> </dl> | <span data-ttu-id="83084-119">Le lecteur sera attaché au premier bus.</span><span class="sxs-lookup"><span data-stu-id="83084-119">The drive will be attached to the first bus.</span></span><br/>  |
| <dl> <span data-ttu-id="83084-120"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="83084-120"><dt>1</dt></span></span> </dl> | <span data-ttu-id="83084-121">Le lecteur sera attaché au second bus.</span><span class="sxs-lookup"><span data-stu-id="83084-121">The drive will be attached to the second bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="83084-122">*deviceNumber* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83084-122">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83084-123">Appareil auquel le lecteur sera attaché.</span><span class="sxs-lookup"><span data-stu-id="83084-123">The device to which the drive will be attached.</span></span>



| <span data-ttu-id="83084-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="83084-124">Value</span></span>                                                                        | <span data-ttu-id="83084-125">Signification</span><span class="sxs-lookup"><span data-stu-id="83084-125">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="83084-126"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="83084-126"><dt>0</dt></span></span> </dl> | <span data-ttu-id="83084-127">Le lecteur sera attaché au premier périphérique sur le bus.</span><span class="sxs-lookup"><span data-stu-id="83084-127">The drive will be attached to the first device on the bus.</span></span><br/>  |
| <dl> <span data-ttu-id="83084-128"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="83084-128"><dt>1</dt></span></span> </dl> | <span data-ttu-id="83084-129">Le lecteur sera attaché au deuxième périphérique sur le bus.</span><span class="sxs-lookup"><span data-stu-id="83084-129">The drive will be attached to the second device on the bus.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="83084-130">*hardDiskConnection* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="83084-130">*hardDiskConnection* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="83084-131">Objet [**IVMHardDiskConnection**](ivmharddiskconnection.md) .</span><span class="sxs-lookup"><span data-stu-id="83084-131">An [**IVMHardDiskConnection**](ivmharddiskconnection.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83084-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83084-132">Return value</span></span>

<span data-ttu-id="83084-133">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="83084-133">This method can return one of these values.</span></span>



| <span data-ttu-id="83084-134">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="83084-134">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="83084-135">Description</span><span class="sxs-lookup"><span data-stu-id="83084-135">Description</span></span>                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="83084-136"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="83084-136"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="83084-137">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="83084-137">The operation was successful.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="83084-138"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="83084-138"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="83084-139">Le paramètre *hardDiskConnection* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="83084-139">The *hardDiskConnection* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="83084-140"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="83084-140"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="83084-141">Un paramètre *hardDiskPath* a la **valeur null** ou le paramètre *busNumber* ou *deviceNumber* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="83084-141">A *hardDiskPath* parameter is **NULL** or the *busNumber* or *deviceNumber* parameter is not valid.</span></span><br/>                                            |
| <dl> <span data-ttu-id="83084-142">Valeur <dt>**HRESULT \_ FROM \_ Win32 ( \_ fichier d' \_ erreur \_ introuvable)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="83084-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl>   | <span data-ttu-id="83084-143">Le système ne peut pas trouver le fichier spécifié par le paramètre *hardDiskPath* .</span><span class="sxs-lookup"><span data-stu-id="83084-143">The system cannot find the file specified by the *hardDiskPath* parameter.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="83084-144">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ chemin d’erreur \_ \_ introuvable)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="83084-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="83084-145">Le système ne trouve pas le chemin d’accès spécifié par le paramètre *hardDiskPath* .</span><span class="sxs-lookup"><span data-stu-id="83084-145">The system cannot find the path specified by the *hardDiskPath* parameter.</span></span><br/>                                                                     |
| <dl> <span data-ttu-id="83084-146">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ \_ nom non valide)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="83084-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="83084-147">Le paramètre *hardDiskPath* contient un caractère non valide (l’un des caractères \* suivants : «  ? <>/ \| » :»).</span><span class="sxs-lookup"><span data-stu-id="83084-147">The *hardDiskPath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                                        |
| <dl> <span data-ttu-id="83084-148">Valeur <dt>**HRESULT \_ FROM \_ Win32 (erreur \_ de \_ nom de chemin incorrect)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="83084-148"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="83084-149">Le paramètre *hardDiskPath* spécifie un chemin d’accès vide ou relatif.</span><span class="sxs-lookup"><span data-stu-id="83084-149">The *hardDiskPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="83084-150">Un chemin d’accès absolu est requis.</span><span class="sxs-lookup"><span data-stu-id="83084-150">An absolute path is required.</span></span><br/>                                                |
| <dl> <span data-ttu-id="83084-151">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ dépassement de mémoire tampon d’erreur)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="83084-151"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="83084-152">Le chemin d’accès spécifié par le paramètre *hardDiskPath* est trop long.</span><span class="sxs-lookup"><span data-stu-id="83084-152">The path specified by the *hardDiskPath* parameter is too long.</span></span> <span data-ttu-id="83084-153">Le chemin d’accès doit être inférieur à 260 caractères.</span><span class="sxs-lookup"><span data-stu-id="83084-153">The path must be less than 260 characters.</span></span><br/>                                     |
| <dl> <span data-ttu-id="83084-154"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="83084-154"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                              | <span data-ttu-id="83084-155">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="83084-155">The configuration is unknown.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="83084-156"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ en cours d’exécution \_ ou \_**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="83084-156"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>                   | <span data-ttu-id="83084-157">L’ordinateur virtuel est dans un État en cours d’exécution ou enregistré.</span><span class="sxs-lookup"><span data-stu-id="83084-157">The VM is in a running or saved state.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="83084-158"><dt>**Ordinateur virtuel \_ 0xA00400503 \_ \_ de bus \_ de lecteur E \_ en cours d' \_ utilisation**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="83084-158"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl>                | <span data-ttu-id="83084-159">L’emplacement de bus spécifié est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="83084-159">The specified bus location is in use.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="83084-160"><dt>**Ordinateur virtuel \_ E \_ \_ \_ fichier HD 0xA0040682 non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="83084-160"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="83084-161">Le disque dur virtuel est supérieur à 127 Go et ne peut pas être connecté au bus IDE.</span><span class="sxs-lookup"><span data-stu-id="83084-161">The VHD is greater than 127 GB and cannot be connected to the IDE bus.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="83084-162"><dt>**Ordinateur virtuel \_ E \_ \_ \_ \_ type de disque HD non pris en charge**</dt> <dt>0xA00400686</dt></span><span class="sxs-lookup"><span data-stu-id="83084-162"><dt>**VM\_E\_UNSUPPORTED\_HD\_DISK\_TYPE**</dt> <dt>0xA00400686</dt></span></span> </dl>             | <span data-ttu-id="83084-163">Le paramètre *hardDiskPath* fait référence à un disque dur virtuel lié ou à un disque dur virtuel de différenciation sur un disque dur virtuel lié.</span><span class="sxs-lookup"><span data-stu-id="83084-163">The *hardDiskPath* parameter refers to a linked VHD or a differencing VHD to a linked VHD.</span></span> <span data-ttu-id="83084-164">Les disques durs virtuels liés ne peuvent pas être attachés aux machines virtuelles.</span><span class="sxs-lookup"><span data-stu-id="83084-164">Linked VHDs cannot be attached to virtual machines.</span></span><br/> |
| <dl> <span data-ttu-id="83084-165">Valeur <dt>**HRESULT \_ À partir de \_ Win32 \_ ( \_ violation de partage d’erreur)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="83084-165"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="83084-166">Le disque dur virtuel spécifié est déjà connecté à un autre emplacement de bus pour cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="83084-166">The specified VHD is already connected to another bus location for this VM.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="83084-167"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="83084-167"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="83084-168">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="83084-168">An unexpected error has occurred.</span></span><br/>                                                                                                              |



 

## <a name="remarks"></a><span data-ttu-id="83084-169">Notes</span><span class="sxs-lookup"><span data-stu-id="83084-169">Remarks</span></span>

<span data-ttu-id="83084-170">Vous pouvez uniquement ajouter une nouvelle connexion de disque dur à une machine virtuelle arrêtée.</span><span class="sxs-lookup"><span data-stu-id="83084-170">You can only add a new hard disk connection to a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="83084-171">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83084-171">Requirements</span></span>



| <span data-ttu-id="83084-172">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83084-172">Requirement</span></span> | <span data-ttu-id="83084-173">Valeur</span><span class="sxs-lookup"><span data-stu-id="83084-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="83084-174">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83084-174">Minimum supported client</span></span><br/> | <span data-ttu-id="83084-175">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83084-175">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="83084-176">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83084-176">Minimum supported server</span></span><br/> | <span data-ttu-id="83084-177">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="83084-177">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="83084-178">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="83084-178">End of client support</span></span><br/>    | <span data-ttu-id="83084-179">Windows 7</span><span class="sxs-lookup"><span data-stu-id="83084-179">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="83084-180">Produit</span><span class="sxs-lookup"><span data-stu-id="83084-180">Product</span></span><br/>                  | <span data-ttu-id="83084-181">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="83084-181">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="83084-182">En-tête</span><span class="sxs-lookup"><span data-stu-id="83084-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="83084-183"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="83084-183"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="83084-184">IID</span><span class="sxs-lookup"><span data-stu-id="83084-184">IID</span></span><br/>                      | <span data-ttu-id="83084-185">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="83084-185">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="83084-186">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83084-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83084-187">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="83084-187">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

