---
description: La méthode IsActivated de la \_ classe TPM Win32 indique si l’appareil est activé.
ms.assetid: 862c386c-c5b5-44d2-89a5-3735b99bf8bc
title: Méthode IsActivated de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsActivated
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6482163a27f211b4f4ce24284a8339f2b7254f3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209672"
---
# <a name="isactivated-method-of-the-win32_tpm-class"></a><span data-ttu-id="481c3-103">Méthode IsActivated de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="481c3-103">IsActivated method of the Win32\_Tpm class</span></span>

<span data-ttu-id="481c3-104">La méthode **isActivated** de la [**classe \_ TPM Win32**](win32-tpm.md) indique si l’appareil est activé.</span><span class="sxs-lookup"><span data-stu-id="481c3-104">The **IsActivated** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="481c3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="481c3-105">Syntax</span></span>


```mof
uint32 IsActivated(
  [out] boolean IsActivated
);
```



## <a name="parameters"></a><span data-ttu-id="481c3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="481c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="481c3-107">*IsActivated* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="481c3-107">*IsActivated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="481c3-108">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="481c3-108">Type: **boolean**</span></span>

<span data-ttu-id="481c3-109">Si la **valeur est true**, l’appareil est activé.</span><span class="sxs-lookup"><span data-stu-id="481c3-109">If **true**, the device is activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="481c3-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="481c3-110">Return value</span></span>

<span data-ttu-id="481c3-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="481c3-111">Type: **uint32**</span></span>

<span data-ttu-id="481c3-112">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="481c3-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="481c3-113">Les codes de retour courants sont répertoriés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="481c3-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="481c3-114">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="481c3-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="481c3-115">Description</span><span class="sxs-lookup"><span data-stu-id="481c3-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="481c3-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="481c3-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="481c3-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="481c3-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="481c3-118">Notes</span><span class="sxs-lookup"><span data-stu-id="481c3-118">Remarks</span></span>

<span data-ttu-id="481c3-119">La désactivation est semblable à la désactivation, mais les modifications de l’état opérationnel sont possibles.</span><span class="sxs-lookup"><span data-stu-id="481c3-119">Deactivation is similar to disabled, but operational state changes are possible.</span></span> <span data-ttu-id="481c3-120">Conformément à la spécification Trusted Computing Group (TCG) v 1.2, seules les commandes suivantes sont disponibles lorsque l’appareil est dans un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="481c3-120">According to the Trusted Computing Group (TCG) v1.2 specification only the following commands are available when the device is in a deactivated state.</span></span>

-   <span data-ttu-id="481c3-121">\_CONTINUESELFTEST TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-121">TPM\_ContinueSelfTest</span></span>
-   <span data-ttu-id="481c3-122">\_DSAP TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-122">TPM\_DSAP</span></span>
-   <span data-ttu-id="481c3-123">\_FLUSHSPECIFIC TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-123">TPM\_FlushSpecific</span></span>
-   <span data-ttu-id="481c3-124">\_GETCAPABILITY TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-124">TPM\_GetCapability</span></span>
-   <span data-ttu-id="481c3-125">\_GETTESTRESULT TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-125">TPM\_GetTestResult</span></span>
-   <span data-ttu-id="481c3-126">\_Initialisation TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-126">TPM\_Init</span></span>
-   <span data-ttu-id="481c3-127">\_OIAP TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-127">TPM\_OIAP</span></span>
-   <span data-ttu-id="481c3-128">\_osap TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-128">TPM\_OSAP</span></span>
-   <span data-ttu-id="481c3-129">\_OWNERSETDISABLE TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-129">TPM\_OwnerSetDisable</span></span>
-   <span data-ttu-id="481c3-130">\_Réinitialisation PCR TPM \_</span><span class="sxs-lookup"><span data-stu-id="481c3-130">TPM\_PCR\_Reset</span></span>
-   <span data-ttu-id="481c3-131">\_PHYSICALDISABLE TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-131">TPM\_PhysicalDisable</span></span>
-   <span data-ttu-id="481c3-132">\_PHYSICALENABLE TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-132">TPM\_PhysicalEnable</span></span>
-   <span data-ttu-id="481c3-133">\_PHYSICALSETDEACTIVATED TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-133">TPM\_PhysicalSetDeactivated</span></span>
-   <span data-ttu-id="481c3-134">\_Réinitialisation TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-134">TPM\_Reset</span></span>
-   <span data-ttu-id="481c3-135">Module de plateforme sécurisée \_ Saacquisition</span><span class="sxs-lookup"><span data-stu-id="481c3-135">TPM\_SaveState</span></span>
-   <span data-ttu-id="481c3-136">\_SELFTESTFULL TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-136">TPM\_SelfTestFull</span></span>
-   <span data-ttu-id="481c3-137">\_SETCAPABILITY TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-137">TPM\_SetCapability</span></span>
-   <span data-ttu-id="481c3-138">\_SHA1COMPLETE TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-138">TPM\_SHA1Complete</span></span>
-   <span data-ttu-id="481c3-139">\_SHA1START TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-139">TPM\_SHA1Start</span></span>
-   <span data-ttu-id="481c3-140">\_SHA1UPDATE TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-140">TPM\_SHA1Update</span></span>
-   <span data-ttu-id="481c3-141">Démarrage du module de plateforme sécurisée \_</span><span class="sxs-lookup"><span data-stu-id="481c3-141">TPM\_Startup</span></span>
-   <span data-ttu-id="481c3-142">\_TAKEOWNERSHIP TPM</span><span class="sxs-lookup"><span data-stu-id="481c3-142">TPM\_TakeOwnership</span></span>
-   <span data-ttu-id="481c3-143">\_Handle de terminaison TPM \_</span><span class="sxs-lookup"><span data-stu-id="481c3-143">TPM\_Terminate\_Handle</span></span>

<span data-ttu-id="481c3-144">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="481c3-144">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="481c3-145">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="481c3-145">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="481c3-146">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="481c3-146">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="481c3-147">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="481c3-147">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="481c3-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="481c3-148">Requirements</span></span>



| <span data-ttu-id="481c3-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="481c3-149">Requirement</span></span> | <span data-ttu-id="481c3-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="481c3-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="481c3-151">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="481c3-151">Minimum supported client</span></span><br/> | <span data-ttu-id="481c3-152">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="481c3-152">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="481c3-153">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="481c3-153">Minimum supported server</span></span><br/> | <span data-ttu-id="481c3-154">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="481c3-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="481c3-155">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="481c3-155">Namespace</span></span><br/>                | <span data-ttu-id="481c3-156">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="481c3-156">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="481c3-157">MOF</span><span class="sxs-lookup"><span data-stu-id="481c3-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="481c3-158"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="481c3-158"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="481c3-159">DLL</span><span class="sxs-lookup"><span data-stu-id="481c3-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="481c3-160"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="481c3-160"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="481c3-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="481c3-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="481c3-162">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="481c3-162">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
