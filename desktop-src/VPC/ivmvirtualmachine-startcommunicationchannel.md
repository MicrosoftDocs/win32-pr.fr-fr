---
title: Méthode IVMVirtualMachine StartCommunicationChannel (VPCCOMInterfaces. h)
description: Configure un canal de communication entre l’hôte et le système d’exploitation invité.
ms.assetid: e4b04aa8-8400-4aa4-ad54-71ef57dec82a
keywords:
- Méthode StartCommunicationChannel Virtual PC
- Méthode StartCommunicationChannel Virtual PC, interface IVMVirtualMachine
- IVMVirtualMachine interface Virtual PC, méthode StartCommunicationChannel
topic_type:
- apiref
api_name:
- IVMVirtualMachine.StartCommunicationChannel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac6ab73b6a955b6810eaea280dc25732e2a6721
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466379"
---
# <a name="ivmvirtualmachinestartcommunicationchannel-method"></a><span data-ttu-id="abd06-106">IVMVirtualMachine :: StartCommunicationChannel, méthode</span><span class="sxs-lookup"><span data-stu-id="abd06-106">IVMVirtualMachine::StartCommunicationChannel method</span></span>

<span data-ttu-id="abd06-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="abd06-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="abd06-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="abd06-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="abd06-109">Configure un canal de communication entre l’hôte et le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="abd06-109">Sets up a communication channel between host and guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="abd06-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abd06-110">Syntax</span></span>


```C++
HRESULT StartCommunicationChannel(
  [in] VMEndpointType inHostEndpointType,
  [in] BSTR           inHostEndPointName,
  [in] VMEndpointType inGuestEndpointType,
  [in] BSTR           inGuestEndpointName
);
```



## <a name="parameters"></a><span data-ttu-id="abd06-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abd06-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abd06-112">*inHostEndpointType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="abd06-112">*inHostEndpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abd06-113">Ce paramètre doit être **vmEndpoint \_ NamedPipe** (0).</span><span class="sxs-lookup"><span data-stu-id="abd06-113">This parameter must be **vmEndpoint\_NamedPipe** (0).</span></span>

</dd> <dt>

<span data-ttu-id="abd06-114">*inHostEndPointName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="abd06-114">*inHostEndPointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abd06-115">Nom de canal unique.</span><span class="sxs-lookup"><span data-stu-id="abd06-115">The unique pipe name.</span></span> <span data-ttu-id="abd06-116">Cette chaîne doit avoir la forme suivante : " \\ \\ . \\ canal \\ *pipeName*".</span><span class="sxs-lookup"><span data-stu-id="abd06-116">This string must have the following form: "\\\\.\\pipe\\*pipename*".</span></span> <span data-ttu-id="abd06-117">La partie *pipeName* du nom peut inclure n’importe quel caractère autre qu’une barre oblique inverse, y compris des chiffres et des caractères spéciaux.</span><span class="sxs-lookup"><span data-stu-id="abd06-117">The *pipename* part of the name can include any character other than a backslash, including numbers and special characters.</span></span> <span data-ttu-id="abd06-118">La chaîne du nom de canal entier peut comporter jusqu’à 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="abd06-118">The entire pipe name string can be up to 256 characters long.</span></span> <span data-ttu-id="abd06-119">Les noms de canaux ne respectent pas la casse.</span><span class="sxs-lookup"><span data-stu-id="abd06-119">Pipe names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="abd06-120">*inGuestEndpointType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="abd06-120">*inGuestEndpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abd06-121">Ce paramètre doit être **vmEndpoint \_ tcpip** (1).</span><span class="sxs-lookup"><span data-stu-id="abd06-121">This parameter must be **vmEndpoint\_TCPIP** (1).</span></span>

</dd> <dt>

<span data-ttu-id="abd06-122">*inGuestEndpointName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="abd06-122">*inGuestEndpointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abd06-123">Numéro de port sur lequel le serveur TCP de l’invité écoute.</span><span class="sxs-lookup"><span data-stu-id="abd06-123">The port number on which the TCP server in the guest is listening.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abd06-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="abd06-124">Return value</span></span>

<span data-ttu-id="abd06-125">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="abd06-125">This method can return one of these values.</span></span>



| <span data-ttu-id="abd06-126">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="abd06-126">Return code/value</span></span>                                                                                                                                                                                  | <span data-ttu-id="abd06-127">Description</span><span class="sxs-lookup"><span data-stu-id="abd06-127">Description</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="abd06-128"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="abd06-128"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                        | <span data-ttu-id="abd06-129">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="abd06-129">The operation was successful.</span></span><br/>                                                                                                                    |
| <dl> <span data-ttu-id="abd06-130"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="abd06-130"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                       | <span data-ttu-id="abd06-131">Le paramètre *inHostEndpointType* n’est pas **vmEndpoint \_ NamedPipe** (0) ou le paramètre *inGuestEndpointType* n’est pas **vmEndpoint \_ tcpip** (1).</span><span class="sxs-lookup"><span data-stu-id="abd06-131">The *inHostEndpointType* parameter is not **vmEndpoint\_NamedPipe** (0) or the *inGuestEndpointType* parameter is not **vmEndpoint\_TCPIP** (1).</span></span><br/> |
| <dl> <span data-ttu-id="abd06-132"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="abd06-132"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                          | <span data-ttu-id="abd06-133">Le paramètre *inHostEndPointName* ou *inGuestEndpointName* est **null** ou n’est pas une valeur valide.</span><span class="sxs-lookup"><span data-stu-id="abd06-133">The *inHostEndPointName* or *inGuestEndpointName* parameter is **NULL** or not a valid value.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="abd06-134"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="abd06-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                                  | <span data-ttu-id="abd06-135">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="abd06-135">An unexpected error has occurred.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="abd06-136">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (handle d’erreur \_ non valide \_ )**</dt> <dt>0x80070006</dt></span><span class="sxs-lookup"><span data-stu-id="abd06-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_HANDLE)**</dt> <dt>0x80070006</dt></span></span> </dl>        | <span data-ttu-id="abd06-137">Un descripteur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="abd06-137">A handle is not valid.</span></span><br/>                                                                                                                           |
| <dl> <span data-ttu-id="abd06-138">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="abd06-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>            | <span data-ttu-id="abd06-139">La mémoire disponible est insuffisante pour effectuer cette requête.</span><span class="sxs-lookup"><span data-stu-id="abd06-139">There is not enough memory available to complete this request.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="abd06-140">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (erreur \_ non \_ prête)**</dt> <dt>0x80070015</dt></span><span class="sxs-lookup"><span data-stu-id="abd06-140"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_READY)**</dt> <dt>0x80070015</dt></span></span> </dl>             | <span data-ttu-id="abd06-141">Le système sous-jacent qu’il utilise pour fournir les services réseau est actuellement en cours d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="abd06-141">The underlying system it uses to provide network services is currently being initialized.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="abd06-142">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (l’erreur \_ \_ existe déjà)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="abd06-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>        | <span data-ttu-id="abd06-143">Le nom du canal est déjà utilisé.</span><span class="sxs-lookup"><span data-stu-id="abd06-143">The pipe name is already in use.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="abd06-144">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (canal d’erreur \_ \_ occupé)**</dt> <dt>0x800700e7</dt></span><span class="sxs-lookup"><span data-stu-id="abd06-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PIPE\_BUSY)**</dt> <dt>0x800700e7</dt></span></span> </dl>             | <span data-ttu-id="abd06-145">Un ou plusieurs canaux sont en cours d’exécution et peuvent bientôt être disponibles.</span><span class="sxs-lookup"><span data-stu-id="abd06-145">One or more channels are running down and may become available shortly.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="abd06-146">Valeur <dt>**HRESULT \_ À partir de \_ Win32 (nombre maximal d’erreurs de \_ \_ sessions \_ atteint)**</dt> <dt>0x80070161</dt></span><span class="sxs-lookup"><span data-stu-id="abd06-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_MAX\_SESSIONS\_REACHED)**</dt> <dt>0x80070161</dt></span></span> </dl> | <span data-ttu-id="abd06-147">Le nombre maximal de canaux de communication disponibles est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="abd06-147">The maximum numbers of communication channels available are in-use.</span></span> <span data-ttu-id="abd06-148">Impossible de démarrer un autre canal pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="abd06-148">Another channel cannot be started at this time.</span></span><br/>                              |
| <dl> <span data-ttu-id="abd06-149">Valeur <dt>**HRESULT \_ FROM \_ Win32 ( \_ \_ incompatibilité de révision d’erreur)**</dt> <dt>0x8007051a</dt></span><span class="sxs-lookup"><span data-stu-id="abd06-149"><dt>**HRESULT\_FROM\_WIN32(ERROR\_REVISION\_MISMATCH)**</dt> <dt>0x8007051a</dt></span></span> </dl>     | <span data-ttu-id="abd06-150">Il existe une incompatibilité entre la version des sous-systèmes hôtes et invités.</span><span class="sxs-lookup"><span data-stu-id="abd06-150">There is a mismatch between the version of the host and guest subsystems.</span></span> <span data-ttu-id="abd06-151">Pour plus d’informations, consultez le journal des événements Windows.</span><span class="sxs-lookup"><span data-stu-id="abd06-151">See the Windows Event Log for more detail.</span></span><br/>                             |
| <dl> <span data-ttu-id="abd06-152"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="abd06-152"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                             | <span data-ttu-id="abd06-153">La machine virtuelle n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="abd06-153">The VM is not running.</span></span><br/>                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="abd06-154">Notes</span><span class="sxs-lookup"><span data-stu-id="abd06-154">Remarks</span></span>

<span data-ttu-id="abd06-155">L’implémentation actuelle prend en charge uniquement l’interface de canal nommé sur l’hôte et l’interface TCP/IP sur le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="abd06-155">The current implementation supports only named pipe interface on the host and TCP/IP interface on the guest operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="abd06-156">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="abd06-156">Requirements</span></span>



| <span data-ttu-id="abd06-157">Condition requise</span><span class="sxs-lookup"><span data-stu-id="abd06-157">Requirement</span></span> | <span data-ttu-id="abd06-158">Valeur</span><span class="sxs-lookup"><span data-stu-id="abd06-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="abd06-159">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abd06-159">Minimum supported client</span></span><br/> | <span data-ttu-id="abd06-160">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="abd06-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="abd06-161">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="abd06-161">Minimum supported server</span></span><br/> | <span data-ttu-id="abd06-162">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="abd06-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="abd06-163">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="abd06-163">End of client support</span></span><br/>    | <span data-ttu-id="abd06-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="abd06-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="abd06-165">Produit</span><span class="sxs-lookup"><span data-stu-id="abd06-165">Product</span></span><br/>                  | <span data-ttu-id="abd06-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="abd06-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="abd06-167">En-tête</span><span class="sxs-lookup"><span data-stu-id="abd06-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="abd06-168"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="abd06-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="abd06-169">IID</span><span class="sxs-lookup"><span data-stu-id="abd06-169">IID</span></span><br/>                      | <span data-ttu-id="abd06-170">IID \_ IVMVirtualMachine est défini en tant que f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="abd06-170">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="abd06-171">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abd06-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abd06-172">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="abd06-172">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="abd06-173">**VMEndpointType**</span><span class="sxs-lookup"><span data-stu-id="abd06-173">**VMEndpointType**</span></span>](vmendpointtype.md)
</dt> </dl>

 

