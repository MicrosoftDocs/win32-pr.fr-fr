---
title: IVMGuestOS propriété TerminalServerPort
description: Port utilisé par Services Bureau à distance dans le système d’exploitation invité.
ms.assetid: 25a9114a-0992-4a9d-997a-37138d389970
keywords:
- TerminalServerPort propriété Virtual PC
- TerminalServerPort, propriété Virtual PC, IVMGuestOS, interface
- IVMGuestOS interface Virtual PC, propriété TerminalServerPort
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServerPort
- IVMGuestOS.get_TerminalServerPort
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64415057eeeb91bfb85b664f5cbb44a66546005
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105817"
---
# <a name="ivmguestosterminalserverport-property"></a><span data-ttu-id="30bd2-106">IVMGuestOS :: TerminalServerPort, propriété</span><span class="sxs-lookup"><span data-stu-id="30bd2-106">IVMGuestOS::TerminalServerPort property</span></span>

<span data-ttu-id="30bd2-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="30bd2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="30bd2-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="30bd2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="30bd2-109">Port utilisé par Services Bureau à distance (anciennement services Terminal Server) dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="30bd2-109">Port used by Remote Desktop Services (formerly known as Terminal Services) in the guest operating system.</span></span>

<span data-ttu-id="30bd2-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="30bd2-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="30bd2-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30bd2-111">Syntax</span></span>


```C++
HRESULT get_TerminalServerPort(
  [out, retval] long *tsPort = 3389
);
```



## <a name="property-value"></a><span data-ttu-id="30bd2-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="30bd2-112">Property value</span></span>

<span data-ttu-id="30bd2-113">Retourne le port utilisé par Services Bureau à distance dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="30bd2-113">Returns the port used by Remote Desktop Services in the guest operating system.</span></span>



| <span data-ttu-id="30bd2-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="30bd2-114">Value</span></span>                                                                              | <span data-ttu-id="30bd2-115">Signification</span><span class="sxs-lookup"><span data-stu-id="30bd2-115">Meaning</span></span>                                       |
|------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="30bd2-116"><dt>3389</dt></span><span class="sxs-lookup"><span data-stu-id="30bd2-116"><dt>3389</dt></span></span> </dl>    | <span data-ttu-id="30bd2-117">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="30bd2-117">Default value</span></span><br/>                      |
| <dl> <span data-ttu-id="30bd2-118"><dt>1 65535</dt></span><span class="sxs-lookup"><span data-stu-id="30bd2-118"><dt>1 65535</dt></span></span> </dl> | <span data-ttu-id="30bd2-119">Plage valide</span><span class="sxs-lookup"><span data-stu-id="30bd2-119">Valid range</span></span><br/>                        |
| <dl> <span data-ttu-id="30bd2-120"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="30bd2-120"><dt>0</dt></span></span> </dl>       | <span data-ttu-id="30bd2-121">La valeur de port valide n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="30bd2-121">Valid port value is not available.</span></span><br/> |



 

## <a name="error-codes"></a><span data-ttu-id="30bd2-122">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="30bd2-122">Error codes</span></span>



| <span data-ttu-id="30bd2-123">Nom/valeur</span><span class="sxs-lookup"><span data-stu-id="30bd2-123">Name/value</span></span>                                                                                                                                                                       | <span data-ttu-id="30bd2-124">Signification</span><span class="sxs-lookup"><span data-stu-id="30bd2-124">Meaning</span></span>                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="30bd2-125"><dt>S \_ OK</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="30bd2-125"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="30bd2-126">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="30bd2-126">The operation was successful.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="30bd2-127"><dt>S \_ FALSe</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="30bd2-127"><dt>S\_FALSE</dt> <dt>1</dt></span></span> </dl>                                       | <span data-ttu-id="30bd2-128">Services Bureau à distance n’est pas encore initialisée dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="30bd2-128">Remote Desktop Services is not yet initialized in the guest operating system.</span></span><br/> |
| <dl> <span data-ttu-id="30bd2-129"><dt>E \_ POINTEUR</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="30bd2-129"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                            | <span data-ttu-id="30bd2-130">Le paramètre *tsPort* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="30bd2-130">The *tsPort* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="30bd2-131"><dt>Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="30bd2-131"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="30bd2-132">L’ordinateur virtuel n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="30bd2-132">The virtual machine is not running.</span></span><br/>                                           |
| <dl> <span data-ttu-id="30bd2-133"><dt>Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_ </dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="30bd2-133"><dt>VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="30bd2-134">Les composants d’intégration ne sont pas installés sur cet ordinateur virtuel.</span><span class="sxs-lookup"><span data-stu-id="30bd2-134">Integration components are not installed in this virtual machine.</span></span><br/>             |
| <dl> <span data-ttu-id="30bd2-135"><dt>DISP \_ E \_ exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="30bd2-135"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="30bd2-136">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="30bd2-136">An unexpected error has occurred.</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="30bd2-137">Notes</span><span class="sxs-lookup"><span data-stu-id="30bd2-137">Remarks</span></span>

<span data-ttu-id="30bd2-138">La valeur de cette propriété n’est pas valide, sauf si la propriété [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) est définie sur **\_ true**.</span><span class="sxs-lookup"><span data-stu-id="30bd2-138">The value of this property is not valid unless the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_TRUE**.</span></span>

<span data-ttu-id="30bd2-139">Si la valeur de la propriété [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) est **\_ false** en raison d’une erreur de connexion sur le port, la valeur retournée par la propriété **TerminalServerPort** contient la valeur de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="30bd2-139">If the [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) property is **VARIANT\_FALSE** due to a connection error on the port, then the value returned by the **TerminalServerPort** property contains the error value.</span></span>

## <a name="requirements"></a><span data-ttu-id="30bd2-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="30bd2-140">Requirements</span></span>



| <span data-ttu-id="30bd2-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30bd2-141">Requirement</span></span> | <span data-ttu-id="30bd2-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="30bd2-142">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="30bd2-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30bd2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="30bd2-144">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="30bd2-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="30bd2-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="30bd2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="30bd2-146">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="30bd2-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="30bd2-147">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="30bd2-147">End of client support</span></span><br/>    | <span data-ttu-id="30bd2-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="30bd2-148">Windows 7</span></span><br/>                                                                      |
| <span data-ttu-id="30bd2-149">MIDL</span><span class="sxs-lookup"><span data-stu-id="30bd2-149">IDL</span></span><br/>                      | <dl> <span data-ttu-id="30bd2-150"><dt>IVMGuestOS. idl</dt></span><span class="sxs-lookup"><span data-stu-id="30bd2-150"><dt>IVMGuestOS.idl</dt></span></span> </dl> |
| <span data-ttu-id="30bd2-151">IID</span><span class="sxs-lookup"><span data-stu-id="30bd2-151">IID</span></span><br/>                      | <span data-ttu-id="30bd2-152">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="30bd2-152">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="30bd2-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30bd2-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30bd2-154">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="30bd2-154">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

