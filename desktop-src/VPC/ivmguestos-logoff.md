---
title: Méthode de déconnexion IVMGuestOS (VPCCOMInterfaces. h)
description: Déconnecte tous les utilisateurs du système d’exploitation invité.
ms.assetid: 224aa7cb-0892-4e8a-84bd-78dd5cb724df
keywords:
- Méthode de fermeture de session Virtual PC
- Méthode de déconnexion Virtual PC, interface IVMGuestOS
- IVMGuestOS interface Virtual PC, méthode Logoff
topic_type:
- apiref
api_name:
- IVMGuestOS.Logoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c67e917cc9ff93d162bc340185f426fe9eee3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033219"
---
# <a name="ivmguestoslogoff-method"></a><span data-ttu-id="3135e-106">IVMGuestOS :: Logoff, méthode</span><span class="sxs-lookup"><span data-stu-id="3135e-106">IVMGuestOS::Logoff method</span></span>

<span data-ttu-id="3135e-107">\[Windows Virtual PC n’est plus disponible pour une utilisation à partir de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3135e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3135e-108">Au lieu de cela, utilisez le [fournisseur WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3135e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3135e-109">Déconnecte tous les utilisateurs du système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="3135e-109">Logs off all users from the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3135e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3135e-110">Syntax</span></span>


```C++
HRESULT Logoff(
  [out, retval] IVMTask **outLogoffTask
);
```



## <a name="parameters"></a><span data-ttu-id="3135e-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3135e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3135e-112">*outLogoffTask* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3135e-112">*outLogoffTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3135e-113">Objet [**IVMTask**](ivmtask.md) utilisé pour suivre la progression de l’exécution de la séquence de fermeture de session.</span><span class="sxs-lookup"><span data-stu-id="3135e-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion progress of the logoff sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3135e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3135e-114">Return value</span></span>

<span data-ttu-id="3135e-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="3135e-115">This method can return one of these values.</span></span>



| <span data-ttu-id="3135e-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3135e-116">Return code/value</span></span>                                                                                                                                                                          | <span data-ttu-id="3135e-117">Description</span><span class="sxs-lookup"><span data-stu-id="3135e-117">Description</span></span>                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3135e-118"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3135e-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                | <span data-ttu-id="3135e-119">L'opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="3135e-119">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="3135e-120"><dt>**DISP \_ E \_ exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3135e-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                          | <span data-ttu-id="3135e-121">Une erreur inattendue s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3135e-121">An unexpected error has occurred.</span></span><br/>                                            |
| <dl> <span data-ttu-id="3135e-122"><dt>**E \_ POINTEUR**</dt> <dt>0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3135e-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                  | <span data-ttu-id="3135e-123">Le paramètre a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="3135e-123">The parameter is **NULL**.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="3135e-124">Valeur <dt>**HRESULT \_ À partir de \_ Win32 ( \_ accès à l’erreur \_ refusé)**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="3135e-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ACCESS\_DENIED)**</dt> <dt>0x80070005</dt></span></span> </dl> | <span data-ttu-id="3135e-125">L’appelant doit disposer des autorisations d’accès en exécution pour cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="3135e-125">The caller must have execute access permissions for this VM.</span></span><br/>                 |
| <dl> <span data-ttu-id="3135e-126"><dt>**Ordinateur virtuel \_ E \_ a \_ expiré**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="3135e-126"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                           | <span data-ttu-id="3135e-127">L’opération ne s’est pas terminée en temps opportun.</span><span class="sxs-lookup"><span data-stu-id="3135e-127">The operation did not complete in a timely manner.</span></span><br/>                           |
| <dl> <span data-ttu-id="3135e-128"><dt>**Ordinateur virtuel \_ La \_ fonctionnalité d’ajouts E \_ \_ n’est pas disponible \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="3135e-128"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>       | <span data-ttu-id="3135e-129">La fonctionnalité composants d’intégration n’est pas installée sur cette machine virtuelle.</span><span class="sxs-lookup"><span data-stu-id="3135e-129">The integration components feature is not installed in this virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="3135e-130"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_ non \_ exécutée**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="3135e-130"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                     | <span data-ttu-id="3135e-131">L’ordinateur virtuel (VM) doit être en cours d’exécution pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="3135e-131">The virtual machine (VM) must be running for this operation.</span></span><br/>                 |
| <dl> <span data-ttu-id="3135e-132"><dt>**Ordinateur virtuel \_ \_Machine virtuelle \_**</dt> <dt>0xA0040207</dt> inconnue</span><span class="sxs-lookup"><span data-stu-id="3135e-132"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                          | <span data-ttu-id="3135e-133">La configuration est inconnue.</span><span class="sxs-lookup"><span data-stu-id="3135e-133">The configuration is unknown.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="3135e-134">Notes</span><span class="sxs-lookup"><span data-stu-id="3135e-134">Remarks</span></span>

<span data-ttu-id="3135e-135">`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) est retourné via la propriété [**Error**](ivmtask-error.md) de l’objet [**IVMTask**](ivmtask.md) retourné il n’y a aucune session de connexion dans le système d’exploitation invité.</span><span class="sxs-lookup"><span data-stu-id="3135e-135">`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (0x80070520) is returned through the [**Error**](ivmtask-error.md) property of the returned [**IVMTask**](ivmtask.md) object there are no logon sessions in the guest operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="3135e-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3135e-136">Requirements</span></span>



| <span data-ttu-id="3135e-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3135e-137">Requirement</span></span> | <span data-ttu-id="3135e-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="3135e-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3135e-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3135e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3135e-140">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3135e-140">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3135e-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3135e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3135e-142">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="3135e-142">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3135e-143">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="3135e-143">End of client support</span></span><br/>    | <span data-ttu-id="3135e-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3135e-144">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3135e-145">Produit</span><span class="sxs-lookup"><span data-stu-id="3135e-145">Product</span></span><br/>                  | <span data-ttu-id="3135e-146">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3135e-146">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3135e-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="3135e-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="3135e-148"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="3135e-148"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3135e-149">IID</span><span class="sxs-lookup"><span data-stu-id="3135e-149">IID</span></span><br/>                      | <span data-ttu-id="3135e-150">IID \_ IVMGuestOS est défini en tant que 99fea0db-4880-499a-B6D8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="3135e-150">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="3135e-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3135e-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3135e-152">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="3135e-152">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

