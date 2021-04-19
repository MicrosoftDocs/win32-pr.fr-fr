---
description: Indique l’action de l’utilisateur nécessaire pour effectuer l’opération de présence physique Module de plateforme sécurisée (TPM) (TPM). Utilisez la méthode SetPhysicalPresenceRequest pour demander une opération.
ms.assetid: abbd9702-c3a7-468a-bc83-2b7739d0b7bf
title: Méthode GetPhysicalPresenceTransition de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceTransition
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 4e6a3ab2295cc26cd439465b569f594dd1e0580a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534680"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a><span data-ttu-id="dbe6d-104">Méthode GetPhysicalPresenceTransition de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="dbe6d-104">GetPhysicalPresenceTransition method of the Win32\_Tpm class</span></span>

<span data-ttu-id="dbe6d-105">La méthode **GetPhysicalPresenceTransition** de la [**classe \_ TPM Win32**](win32-tpm.md) indique l’action de l’utilisateur nécessaire pour effectuer l’opération de présence physique module de plateforme sécurisée (TPM) (TPM).</span><span class="sxs-lookup"><span data-stu-id="dbe6d-105">The **GetPhysicalPresenceTransition** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates the user action that is needed to perform the Trusted Platform Module (TPM) physical presence operation.</span></span> <span data-ttu-id="dbe6d-106">Utilisez la méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) pour demander une opération.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-106">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span> <span data-ttu-id="dbe6d-107">L’action utilisateur requise est définie pour votre ordinateur au moment de la fabrication.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-107">The required user action is set for your computer at the time of manufacture.</span></span> <span data-ttu-id="dbe6d-108">En règle générale, un redémarrage de l’ordinateur est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-108">Usually a computer restart is needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe6d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dbe6d-109">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a><span data-ttu-id="dbe6d-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dbe6d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbe6d-111">*Transition* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dbe6d-111">*Transition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dbe6d-112">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbe6d-112">Type: **uint32**</span></span>

<span data-ttu-id="dbe6d-113">Valeur entière qui spécifie la transition nécessaire pour effectuer une opération de présence physique TPM.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-113">An integer value that specifies the transition needed to perform a TPM physical presence operation.</span></span>



| <span data-ttu-id="dbe6d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbe6d-114">Value</span></span>                                                                        | <span data-ttu-id="dbe6d-115">Signification</span><span class="sxs-lookup"><span data-stu-id="dbe6d-115">Meaning</span></span>                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dbe6d-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dbe6d-116"><dt>0</dt></span></span> </dl> | <span data-ttu-id="dbe6d-117">Aucune action de l’utilisateur n’est nécessaire pour effectuer une opération de présence physique TPM.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-117">No user action is needed to perform a TPM physical presence operation.</span></span><br/>                                                                                                                                                                              |
| <dl> <span data-ttu-id="dbe6d-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="dbe6d-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="dbe6d-119">Pour effectuer une opération de présence physique TPM, l’utilisateur doit arrêter l’ordinateur, puis le réactiver à l’aide du bouton d’alimentation.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-119">To perform a TPM physical presence operation, the user must shutdown the computer and then turn it back on by using the power button.</span></span> <span data-ttu-id="dbe6d-120">L’utilisateur doit être physiquement présent sur l’ordinateur pour accepter ou refuser la modification quand le BIOS le demande.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-120">The user must be physically present at the computer to accept or reject the change when prompted by the BIOS.</span></span><br/> |
| <dl> <span data-ttu-id="dbe6d-121"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dbe6d-121"><dt>2</dt></span></span> </dl> | <span data-ttu-id="dbe6d-122">Pour effectuer une opération de présence physique TPM, l’utilisateur doit redémarrer l’ordinateur à l’aide d’un redémarrage à chaud.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-122">To perform a TPM physical presence operation, the user must restart the computer by using a warm reboot.</span></span> <span data-ttu-id="dbe6d-123">L’utilisateur doit être physiquement présent sur l’ordinateur pour accepter ou refuser la modification quand le BIOS le demande.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-123">The user must be physically present at the computer to accept or reject the change when prompted by the BIOS.</span></span><br/>                              |
| <dl> <span data-ttu-id="dbe6d-124"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="dbe6d-124"><dt>3</dt></span></span> </dl> | <span data-ttu-id="dbe6d-125">L’action requise de l’utilisateur est inconnue.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-125">The required user action is unknown.</span></span><br/>                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbe6d-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dbe6d-126">Return value</span></span>

<span data-ttu-id="dbe6d-127">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="dbe6d-127">Type: **uint32**</span></span>

<span data-ttu-id="dbe6d-128">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-128">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="dbe6d-129">Le tableau suivant répertorie certains des codes de retour courants.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-129">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="dbe6d-130">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="dbe6d-130">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="dbe6d-131">Description</span><span class="sxs-lookup"><span data-stu-id="dbe6d-131">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dbe6d-132"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="dbe6d-132"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="dbe6d-133">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-133">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="dbe6d-134"><dt>**Module TPM \_ \_ \_ \_ Erreur ACPI PPP**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="dbe6d-134"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="dbe6d-135">Une défaillance matérielle s’est produite.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-135">A hardware failure occurred.</span></span> <span data-ttu-id="dbe6d-136">Pour plus d'informations, consultez le fabricant de votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-136">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dbe6d-137">Notes</span><span class="sxs-lookup"><span data-stu-id="dbe6d-137">Remarks</span></span>

<span data-ttu-id="dbe6d-138">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="dbe6d-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="dbe6d-139">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="dbe6d-140">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="dbe6d-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="dbe6d-141">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="dbe6d-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbe6d-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbe6d-142">Requirements</span></span>



| <span data-ttu-id="dbe6d-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dbe6d-143">Requirement</span></span> | <span data-ttu-id="dbe6d-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="dbe6d-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe6d-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbe6d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="dbe6d-146">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbe6d-146">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="dbe6d-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dbe6d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="dbe6d-148">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dbe6d-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="dbe6d-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="dbe6d-149">Namespace</span></span><br/>                | <span data-ttu-id="dbe6d-150">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="dbe6d-150">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="dbe6d-151">MOF</span><span class="sxs-lookup"><span data-stu-id="dbe6d-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dbe6d-152"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="dbe6d-152"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="dbe6d-153">DLL</span><span class="sxs-lookup"><span data-stu-id="dbe6d-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dbe6d-154"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="dbe6d-154"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbe6d-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dbe6d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe6d-156">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="dbe6d-156">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="dbe6d-157">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="dbe6d-157">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
