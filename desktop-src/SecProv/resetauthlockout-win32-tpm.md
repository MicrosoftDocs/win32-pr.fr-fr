---
description: Réinitialise le délai d’attente ou tout autre mécanisme que les fabricants de module de plateforme sécurisée implémentent pour se protéger contre les attaques par dictionnaire sur les valeurs d’autorisation TPM.
ms.assetid: c2fba6a2-2d03-4ffd-9841-4a9eac0a20ac
title: Méthode ResetAuthLockOut de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetAuthLockOut
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d28287e410fbaf65ce5b1e617113c35cfece160b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514160"
---
# <a name="resetauthlockout-method-of-the-win32_tpm-class"></a><span data-ttu-id="5aa7f-103">Méthode ResetAuthLockOut de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="5aa7f-103">ResetAuthLockOut method of the Win32\_Tpm class</span></span>

<span data-ttu-id="5aa7f-104">La méthode **ResetAuthLockOut** de la [**classe \_ TPM Win32**](win32-tpm.md) réinitialise le délai d’attente ou tout autre mécanisme que les fabricants de module de plateforme sécurisée implémentent pour se protéger contre les attaques par dictionnaire sur les valeurs d’autorisation du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-104">The **ResetAuthLockOut** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the time-out period or other mechanism that TPM manufacturers implement to protect against dictionary attacks on TPM authorization values.</span></span> <span data-ttu-id="5aa7f-105">Dans le cadre d’une attaque par dictionnaire, une personne malveillante tente de deviner une valeur d’autorisation TPM correcte en tentant de façon exhaustive toutes les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-105">In a dictionary attack, an attacker tries to guess a correct TPM authorization value by exhaustively attempting all possible values.</span></span>

<span data-ttu-id="5aa7f-106">Utilisez cette méthode si le module de plateforme sécurisée est verrouillé en raison d’un trop grand nombre de tentatives incorrectes lors de l’entrée de l’autorisation du propriétaire ou d’autres valeurs d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-106">Use this method if the TPM is locked out due to too many incorrect attempts at entering the owner authorization or other authorization values.</span></span> <span data-ttu-id="5aa7f-107">Lorsque le module de plateforme sécurisée est verrouillé, une partie ou l’ensemble des commandes émises dans le module de plateforme sécurisée (TPM) retournent une erreur, TPM \_ E \_ défendre le \_ verrou \_ en cours d’exécution (0x80280803)</span><span class="sxs-lookup"><span data-stu-id="5aa7f-107">When the TPM is locked out, some or all commands issued to the TPM will return an error, TPM\_E\_DEFEND\_LOCK\_RUNNING (0x80280803).</span></span>

> [!Note]  
> <span data-ttu-id="5aa7f-108">Cette méthode ne peut être utilisée qu’une seule fois lorsque le module de plateforme sécurisée est verrouillé. Si l’autorisation du propriétaire fournie à cette méthode est incorrecte, le module de plateforme sécurisée est verrouillé pour l’intégralité du délai d’attente et les tentatives supplémentaires de réinitialisation du verrou échouent.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-108">This method can only be used exactly once when the TPM is locked out. If the owner authorization provided to this method is incorrect, the TPM will lock out for the entire time-out period and additional attempts at resetting the lock will fail.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5aa7f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5aa7f-109">Syntax</span></span>


```mof
uint32 ResetAuthLockOut(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="5aa7f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5aa7f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5aa7f-111">*Origine* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="5aa7f-111">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5aa7f-112">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="5aa7f-112">Type: **string**</span></span>

<span data-ttu-id="5aa7f-113">Chaîne qui identifie le propriétaire du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-113">A string that identifies the TPM owner.</span></span>

<span data-ttu-id="5aa7f-114">Cette chaîne doit être une chaîne codée en base64 qui se termine par un caractère null qui contient exactement 20 octets de données binaires.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-114">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="5aa7f-115">Utilisez la méthode [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) pour convertir une phrase secrète au format attendu.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-115">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="5aa7f-116">Le paramètre *origine* est lu à partir du Registre si aucun n’est fourni.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-116">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5aa7f-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5aa7f-117">Return value</span></span>

<span data-ttu-id="5aa7f-118">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5aa7f-118">Type: **uint32**</span></span>

<span data-ttu-id="5aa7f-119">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-119">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span> <span data-ttu-id="5aa7f-120">Le tableau suivant répertorie certaines des valeurs de retour courantes.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-120">The following table lists some of the common return values.</span></span>



| <span data-ttu-id="5aa7f-121">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5aa7f-121">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="5aa7f-122">Description</span><span class="sxs-lookup"><span data-stu-id="5aa7f-122">Description</span></span>                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5aa7f-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5aa7f-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                            | <span data-ttu-id="5aa7f-124">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="5aa7f-125"><dt>**Module TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="5aa7f-125"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl> | <span data-ttu-id="5aa7f-126">La valeur d’autorisation du propriétaire fournie est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-126">The provided owner authorization value is incorrect.</span></span> <span data-ttu-id="5aa7f-127">Les tentatives supplémentaires de réinitialisation du verrou échouent avec la même erreur.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-127">Additional attempts at resetting the lock will fail with this same error.</span></span> <span data-ttu-id="5aa7f-128">Veuillez patienter jusqu’à expiration du délai d’attente ou d’un autre mécanisme propre au fabricant avant de réessayer les commandes TPM verrouillées.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-128">Please wait until the time-out period or other manufacturer-specific mechanism has expired before retrying locked TPM commands.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5aa7f-129">Notes</span><span class="sxs-lookup"><span data-stu-id="5aa7f-129">Remarks</span></span>

<span data-ttu-id="5aa7f-130">Cette méthode appelle la \_ commande TPM ResetLockValue sur le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-130">This method calls the TPM\_ResetLockValue command on the TPM.</span></span> <span data-ttu-id="5aa7f-131">Le comportement exact de cette méthode varie selon les fabricants de module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-131">The exact behavior of this method varies among TPM manufacturers.</span></span> <span data-ttu-id="5aa7f-132">La documentation du fabricant de l’ordinateur ou du module de plateforme sécurisée peut fournir des informations supplémentaires sur l’implémentation du mécanisme d’attaque anti-dictionnaire.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-132">Documentation from the computer or TPM manufacturer may provide additional information on the implementation of the anti-dictionary attack mechanism.</span></span>

<span data-ttu-id="5aa7f-133">En général, les fabricants peuvent détecter les attaques par dictionnaire en effectuant le suivi des authentifications ayant échoué.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-133">In general, manufacturers can detect dictionary attacks by keeping track of failed authentications.</span></span> <span data-ttu-id="5aa7f-134">Si le nombre ou la fréquence des échecs est suffisamment élevé, le module de plateforme sécurisée verrouille les commandes supplémentaires pendant un certain temps.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-134">If the number or frequency of failures become high enough, the TPM will lock out further commands for a certain time.</span></span> <span data-ttu-id="5aa7f-135">En règle générale, le délai d’attente initial sera court, afin de permettre à un utilisateur légitime de corriger la situation.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-135">Generally, the initial time-out period will be short, to allow a legitimate user a chance to correct the situation.</span></span> <span data-ttu-id="5aa7f-136">Si les défaillances se poursuivent, la durée de chaque délai d’expiration suivant peut augmenter rapidement.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-136">If failures continue, the duration of each subsequent time-out period may increase rapidly.</span></span>

<span data-ttu-id="5aa7f-137">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="5aa7f-137">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5aa7f-138">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-138">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5aa7f-139">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="5aa7f-139">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5aa7f-140">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5aa7f-140">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5aa7f-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5aa7f-141">Requirements</span></span>



| <span data-ttu-id="5aa7f-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5aa7f-142">Requirement</span></span> | <span data-ttu-id="5aa7f-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="5aa7f-143">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5aa7f-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5aa7f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="5aa7f-145">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5aa7f-145">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5aa7f-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5aa7f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="5aa7f-147">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5aa7f-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5aa7f-148">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="5aa7f-148">Namespace</span></span><br/>                | <span data-ttu-id="5aa7f-149">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="5aa7f-149">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="5aa7f-150">MOF</span><span class="sxs-lookup"><span data-stu-id="5aa7f-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5aa7f-151"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="5aa7f-151"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="5aa7f-152">DLL</span><span class="sxs-lookup"><span data-stu-id="5aa7f-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5aa7f-153"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="5aa7f-153"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5aa7f-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5aa7f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5aa7f-155">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="5aa7f-155">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
