---
description: La méthode IsEnabled de la \_ classe TPM Win32 indique si l’appareil est activé. Cette valeur peut être modifiée par les méthodes Enable et Disable.
ms.assetid: e1d5513f-33eb-49e3-9582-d6c103ca5d03
title: Méthode IsEnabled de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d808bb68e53b1a24ff668d1b7a9680b5d57b5e9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516632"
---
# <a name="isenabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="eaf57-104">Méthode IsEnabled de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="eaf57-104">IsEnabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="eaf57-105">La méthode **IsEnabled** de la [**classe \_ TPM Win32**](win32-tpm.md) indique si l’appareil est activé.</span><span class="sxs-lookup"><span data-stu-id="eaf57-105">The **IsEnabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device is enabled.</span></span> <span data-ttu-id="eaf57-106">Cette valeur peut être modifiée par les méthodes [**Enable**](enable-win32-tpm.md) et [**Disable**](disable-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="eaf57-106">This value can be changed by the [**Enable**](enable-win32-tpm.md) and [**Disable**](disable-win32-tpm.md) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaf57-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eaf57-107">Syntax</span></span>


```mof
uint32 IsEnabled(
  [out] boolean IsEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="eaf57-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eaf57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaf57-109">*IsEnabled* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="eaf57-109">*IsEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eaf57-110">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="eaf57-110">Type: **boolean**</span></span>

<span data-ttu-id="eaf57-111">Si la **valeur est true**, l’appareil est activé.</span><span class="sxs-lookup"><span data-stu-id="eaf57-111">If **true**, the device is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaf57-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eaf57-112">Return value</span></span>

<span data-ttu-id="eaf57-113">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="eaf57-113">Type: **uint32**</span></span>

<span data-ttu-id="eaf57-114">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="eaf57-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="eaf57-115">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="eaf57-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="eaf57-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="eaf57-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="eaf57-117">Description</span><span class="sxs-lookup"><span data-stu-id="eaf57-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="eaf57-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="eaf57-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="eaf57-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="eaf57-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eaf57-120">Notes</span><span class="sxs-lookup"><span data-stu-id="eaf57-120">Remarks</span></span>

<span data-ttu-id="eaf57-121">Conformément à la spécification Trusted Computing Group (TCG) v 1.2, seules les commandes suivantes sont disponibles lorsque l’appareil est dans un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="eaf57-121">According to the Trusted Computing Group (TCG) v1.2 specification only the following commands are available when the device is in a deactivated state.</span></span>

-   <span data-ttu-id="eaf57-122">\_CONTINUESELFTEST TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-122">TPM\_ContinueSelfTest</span></span>
-   <span data-ttu-id="eaf57-123">\_DSAP TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-123">TPM\_DSAP</span></span>
-   <span data-ttu-id="eaf57-124">\_FLUSHSPECIFIC TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-124">TPM\_FlushSpecific</span></span>
-   <span data-ttu-id="eaf57-125">\_GETCAPABILITY TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-125">TPM\_GetCapability</span></span>
-   <span data-ttu-id="eaf57-126">\_GETTESTRESULT TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-126">TPM\_GetTestResult</span></span>
-   <span data-ttu-id="eaf57-127">\_Initialisation TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-127">TPM\_Init</span></span>
-   <span data-ttu-id="eaf57-128">\_OIAP TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-128">TPM\_OIAP</span></span>
-   <span data-ttu-id="eaf57-129">\_osap TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-129">TPM\_OSAP</span></span>
-   <span data-ttu-id="eaf57-130">\_OWNERSETDISABLE TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-130">TPM\_OwnerSetDisable</span></span>
-   <span data-ttu-id="eaf57-131">\_Réinitialisation PCR TPM \_</span><span class="sxs-lookup"><span data-stu-id="eaf57-131">TPM\_PCR\_Reset</span></span>
-   <span data-ttu-id="eaf57-132">\_PHYSICALDISABLE TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-132">TPM\_PhysicalDisable</span></span>
-   <span data-ttu-id="eaf57-133">\_PHYSICALENABLE TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-133">TPM\_PhysicalEnable</span></span>
-   <span data-ttu-id="eaf57-134">\_PHYSICALSETDEACTIVATED TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-134">TPM\_PhysicalSetDeactivated</span></span>
-   <span data-ttu-id="eaf57-135">\_Réinitialisation TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-135">TPM\_Reset</span></span>
-   <span data-ttu-id="eaf57-136">Module de plateforme sécurisée \_ Saacquisition</span><span class="sxs-lookup"><span data-stu-id="eaf57-136">TPM\_SaveState</span></span>
-   <span data-ttu-id="eaf57-137">\_SELFTESTFULL TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-137">TPM\_SelfTestFull</span></span>
-   <span data-ttu-id="eaf57-138">\_SETCAPABILITY TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-138">TPM\_SetCapability</span></span>
-   <span data-ttu-id="eaf57-139">\_SHA1COMPLETE TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-139">TPM\_SHA1Complete</span></span>
-   <span data-ttu-id="eaf57-140">\_SHA1START TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-140">TPM\_SHA1Start</span></span>
-   <span data-ttu-id="eaf57-141">\_SHA1UPDATE TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-141">TPM\_SHA1Update</span></span>
-   <span data-ttu-id="eaf57-142">Démarrage du module de plateforme sécurisée \_</span><span class="sxs-lookup"><span data-stu-id="eaf57-142">TPM\_Startup</span></span>
-   <span data-ttu-id="eaf57-143">\_TAKEOWNERSHIP TPM</span><span class="sxs-lookup"><span data-stu-id="eaf57-143">TPM\_TakeOwnership</span></span>
-   <span data-ttu-id="eaf57-144">\_Handle de terminaison TPM \_</span><span class="sxs-lookup"><span data-stu-id="eaf57-144">TPM\_Terminate\_Handle</span></span>

<span data-ttu-id="eaf57-145">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="eaf57-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="eaf57-146">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="eaf57-146">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="eaf57-147">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="eaf57-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="eaf57-148">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="eaf57-148">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eaf57-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eaf57-149">Requirements</span></span>



| <span data-ttu-id="eaf57-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eaf57-150">Requirement</span></span> | <span data-ttu-id="eaf57-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="eaf57-151">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf57-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaf57-152">Minimum supported client</span></span><br/> | <span data-ttu-id="eaf57-153">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eaf57-153">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="eaf57-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eaf57-154">Minimum supported server</span></span><br/> | <span data-ttu-id="eaf57-155">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="eaf57-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="eaf57-156">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="eaf57-156">Namespace</span></span><br/>                | <span data-ttu-id="eaf57-157">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="eaf57-157">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="eaf57-158">MOF</span><span class="sxs-lookup"><span data-stu-id="eaf57-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eaf57-159"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="eaf57-159"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="eaf57-160">DLL</span><span class="sxs-lookup"><span data-stu-id="eaf57-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eaf57-161"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="eaf57-161"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaf57-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eaf57-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf57-163">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="eaf57-163">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="eaf57-164">**Désactiver**</span><span class="sxs-lookup"><span data-stu-id="eaf57-164">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="eaf57-165">**Activer**</span><span class="sxs-lookup"><span data-stu-id="eaf57-165">**Enable**</span></span>](enable-win32-tpm.md)
</dt> </dl>

 

 
