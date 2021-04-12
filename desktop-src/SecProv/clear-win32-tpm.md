---
description: Réinitialise le module de plateforme sécurisée à son état d’usine par défaut.
ms.assetid: 55d6702f-bd57-43e3-b790-617940dd2e01
title: Méthode Clear de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Clear
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cf75a8af6764e542cecd9bd296c1b1511c4f4513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104209674"
---
# <a name="clear-method-of-the-win32_tpm-class"></a><span data-ttu-id="c1e8e-103">Méthode Clear de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="c1e8e-103">Clear method of the Win32\_Tpm class</span></span>

<span data-ttu-id="c1e8e-104">La méthode **Clear** de la [**classe \_ TPM Win32**](win32-tpm.md) réinitialise le module de plateforme sécurisée (TPM) à son état d’usine par défaut.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-104">The **Clear** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the TPM to its factory-default state.</span></span> <span data-ttu-id="c1e8e-105">Un propriétaire du module de plateforme sécurisée peut utiliser cette méthode pour annuler la propriété du module de plateforme sécurisée et invalider les matériaux de chiffrement créés par le propriétaire précédent.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-105">A TPM owner can use this method to cancel TPM ownership and invalidate cryptographic materials created by the previous owner.</span></span> <span data-ttu-id="c1e8e-106">Cette méthode suspend BitLocker si l’appel de peut entraîner la nécessité d’une récupération BitLocker.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-106">This method suspends BitLocker if calling could cause BitLocker recovery to be required.</span></span> <span data-ttu-id="c1e8e-107">BitLocker reprendra automatiquement une fois que le module de plateforme sécurisée a été approvisionné.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-107">BitLocker would automatically resume once TPM has been provisioned.</span></span>

> [!Caution]  
> <span data-ttu-id="c1e8e-108">En effaçant le module de plateforme sécurisée, vous perdez toutes les clés TPM créées et utilisées par les applications.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-108">By clearing the TPM, you will lose all TPM keys created and used by applications.</span></span> <span data-ttu-id="c1e8e-109">Si ces clés ont été utilisées pour chiffrer les données, assurez-vous de disposer d’une autre méthode pour accéder aux données avant d’effacer le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-109">If these keys were used to encrypt data, ensure that you have another way to access the data before clearing the TPM.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c1e8e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1e8e-110">Syntax</span></span>


```mof
uint32 Clear(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="c1e8e-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1e8e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1e8e-112">*Origine* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c1e8e-112">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c1e8e-113">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="c1e8e-113">Type: **string**</span></span>

<span data-ttu-id="c1e8e-114">Chaîne qui identifie le propriétaire du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-114">A string that identifies the TPM owner.</span></span> <span data-ttu-id="c1e8e-115">Cette chaîne doit être une chaîne encodée en base64 contenant exactement 20 octets de données binaires.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-115">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="c1e8e-116">Utilisez la méthode [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) pour convertir une phrase secrète au format attendu.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-116">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="c1e8e-117">Le paramètre *origine* est lu à partir du Registre si aucun n’est fourni.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-117">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1e8e-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c1e8e-118">Return value</span></span>

<span data-ttu-id="c1e8e-119">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c1e8e-119">Type: **uint32**</span></span>

<span data-ttu-id="c1e8e-120">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-120">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="c1e8e-121">Le tableau suivant répertorie certains des codes de retour courants.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-121">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="c1e8e-122">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c1e8e-122">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="c1e8e-123">Description</span><span class="sxs-lookup"><span data-stu-id="c1e8e-123">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c1e8e-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c1e8e-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="c1e8e-125">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-125">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="c1e8e-126"><dt>**Module TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="c1e8e-126"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="c1e8e-127">La valeur d’autorisation du propriétaire fournie ne peut pas effectuer la requête.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-127">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="c1e8e-128"><dt>**Module TPM \_ E \_ protection des \_ verrous \_ en cours d’exécution**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="c1e8e-128"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="c1e8e-129">Le module de plateforme sécurisée se défend contre les attaques par dictionnaire et se trouve dans un délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-129">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="c1e8e-130">Pour plus d’informations, consultez la méthode [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="c1e8e-130">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c1e8e-131">Notes</span><span class="sxs-lookup"><span data-stu-id="c1e8e-131">Remarks</span></span>

<span data-ttu-id="c1e8e-132">L’exécution de cette méthode peut aider à préparer un ordinateur équipé d’un module de plateforme sécurisée pour le recyclage.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-132">Running this method can help prepare a TPM-equipped computer for recycling.</span></span>

<span data-ttu-id="c1e8e-133">Pour effacer le module de plateforme sécurisée mais n’avoir plus l’autorisation de propriétaire du module de plateforme sécurisée, vous devez disposer d’un accès physique à l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-133">To clear the TPM but no longer have the TPM owner authorization, you need physical access to the computer.</span></span> <span data-ttu-id="c1e8e-134">La méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) comprend des fonctionnalités permettant d’effacer le module de plateforme sécurisée sans l’autorisation du propriétaire du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-134">The [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method includes functionality to help clear the TPM without TPM owner authorization.</span></span>

<span data-ttu-id="c1e8e-135">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c1e8e-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c1e8e-136">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-136">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c1e8e-137">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c1e8e-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c1e8e-138">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c1e8e-138">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c1e8e-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1e8e-139">Requirements</span></span>



| <span data-ttu-id="c1e8e-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c1e8e-140">Requirement</span></span> | <span data-ttu-id="c1e8e-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1e8e-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1e8e-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1e8e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c1e8e-143">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1e8e-143">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c1e8e-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1e8e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c1e8e-145">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1e8e-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c1e8e-146">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c1e8e-146">Namespace</span></span><br/>                | <span data-ttu-id="c1e8e-147">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="c1e8e-147">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="c1e8e-148">MOF</span><span class="sxs-lookup"><span data-stu-id="c1e8e-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1e8e-149"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="c1e8e-149"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1e8e-150">DLL</span><span class="sxs-lookup"><span data-stu-id="c1e8e-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1e8e-151"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="c1e8e-151"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1e8e-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1e8e-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1e8e-153">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="c1e8e-153">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
