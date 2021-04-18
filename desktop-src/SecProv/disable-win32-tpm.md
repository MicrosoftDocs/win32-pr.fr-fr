---
description: Autorise le propriétaire du module de plateforme sécurisée à désactiver ou à suspendre le module de plateforme sécurisée.
ms.assetid: d910334d-6da6-423d-ae8d-6e86f300dd52
title: Désactivation de la méthode de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Disable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 32012c338646ce11c96d2657233642808fdcdaec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529111"
---
# <a name="disable-method-of-the-win32_tpm-class"></a><span data-ttu-id="cf4a5-103">Désactivation de la méthode de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="cf4a5-103">Disable method of the Win32\_Tpm class</span></span>

<span data-ttu-id="cf4a5-104">La méthode **Disable** de la [**classe \_ TPM Win32**](win32-tpm.md) permet au propriétaire du module de plateforme sécurisée de désactiver ou de suspendre le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="cf4a5-104">The **Disable** method of the [**Win32\_Tpm**](win32-tpm.md) class allows the TPM owner to disable or suspend the TPM.</span></span> <span data-ttu-id="cf4a5-105">Cette méthode suspend BitLocker si l’appel de peut entraîner la nécessité d’une récupération BitLocker.</span><span class="sxs-lookup"><span data-stu-id="cf4a5-105">This method suspends BitLocker if calling could cause BitLocker recovery to be required.</span></span> <span data-ttu-id="cf4a5-106">BitLocker reprendra automatiquement une fois que le module de plateforme sécurisée a été approvisionné.</span><span class="sxs-lookup"><span data-stu-id="cf4a5-106">BitLocker would automatically resume once TPM has been provisioned.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf4a5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf4a5-107">Syntax</span></span>


```mof
uint32 Disable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="cf4a5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf4a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf4a5-109">*Origine* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="cf4a5-109">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cf4a5-110">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf4a5-110">Type: **string**</span></span>

<span data-ttu-id="cf4a5-111">Chaîne qui identifie le propriétaire du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="cf4a5-111">A string that identifies the TPM owner.</span></span> <span data-ttu-id="cf4a5-112">Cette chaîne doit être une chaîne encodée en base64 contenant exactement 20 octets de données binaires.</span><span class="sxs-lookup"><span data-stu-id="cf4a5-112">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="cf4a5-113">Utilisez la méthode [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) pour convertir une phrase secrète au format attendu.</span><span class="sxs-lookup"><span data-stu-id="cf4a5-113">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="cf4a5-114">Le paramètre *origine* est lu à partir du Registre si aucun n’est fourni.</span><span class="sxs-lookup"><span data-stu-id="cf4a5-114">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf4a5-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cf4a5-115">Return value</span></span>

<span data-ttu-id="cf4a5-116">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="cf4a5-116">Type: **uint32**</span></span>

<span data-ttu-id="cf4a5-117">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="cf4a5-117">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="cf4a5-118">Le tableau suivant répertorie certains des codes de retour courants.</span><span class="sxs-lookup"><span data-stu-id="cf4a5-118">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="cf4a5-119">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="cf4a5-119">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="cf4a5-120">Description</span><span class="sxs-lookup"><span data-stu-id="cf4a5-120">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf4a5-121"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="cf4a5-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="cf4a5-122">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="cf4a5-122">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="cf4a5-123"><dt>**Module TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="cf4a5-123"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="cf4a5-124">La valeur d’autorisation du propriétaire fournie ne peut pas effectuer la requête.</span><span class="sxs-lookup"><span data-stu-id="cf4a5-124">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="cf4a5-125"><dt>**Module TPM \_ E \_ protection des \_ verrous \_ en cours d’exécution**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="cf4a5-125"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="cf4a5-126">Le module de plateforme sécurisée se défend contre les attaques par dictionnaire et se trouve dans un délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="cf4a5-126">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="cf4a5-127">Pour plus d’informations, consultez la méthode [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="cf4a5-127">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cf4a5-128">Notes</span><span class="sxs-lookup"><span data-stu-id="cf4a5-128">Remarks</span></span>

<span data-ttu-id="cf4a5-129">Pour désactiver le module de plateforme sécurisée sans avoir la valeur d’autorisation du propriétaire du module de plateforme sécurisée, utilisez la méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="cf4a5-129">To disable the TPM without having the TPM owner authorization value, use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

<span data-ttu-id="cf4a5-130">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="cf4a5-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cf4a5-131">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="cf4a5-131">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="cf4a5-132">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="cf4a5-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cf4a5-133">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="cf4a5-133">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf4a5-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cf4a5-134">Requirements</span></span>



| <span data-ttu-id="cf4a5-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cf4a5-135">Requirement</span></span> | <span data-ttu-id="cf4a5-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="cf4a5-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4a5-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf4a5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="cf4a5-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf4a5-138">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cf4a5-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cf4a5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="cf4a5-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cf4a5-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="cf4a5-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="cf4a5-141">Namespace</span></span><br/>                | <span data-ttu-id="cf4a5-142">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="cf4a5-142">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="cf4a5-143">MOF</span><span class="sxs-lookup"><span data-stu-id="cf4a5-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf4a5-144"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="cf4a5-144"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf4a5-145">DLL</span><span class="sxs-lookup"><span data-stu-id="cf4a5-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf4a5-146"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="cf4a5-146"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf4a5-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf4a5-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf4a5-148">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="cf4a5-148">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="cf4a5-149">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="cf4a5-149">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
