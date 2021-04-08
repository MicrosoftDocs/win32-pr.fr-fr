---
description: Installe un propriétaire pour le module de plateforme sécurisée.
ms.assetid: 7b4c8785-0925-41a8-a878-7c1f38d31853
title: Méthode TakeOwnership de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.TakeOwnership
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: acb0cb03f5e422695623bf6e183d1fd89f63ab60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035160"
---
# <a name="takeownership-method-of-the-win32_tpm-class"></a><span data-ttu-id="87c09-103">Méthode TakeOwnership de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="87c09-103">TakeOwnership method of the Win32\_Tpm class</span></span>

<span data-ttu-id="87c09-104">La méthode **TakeOwnership** de la [**classe \_ TPM Win32**](win32-tpm.md) installe un propriétaire pour le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="87c09-104">The **TakeOwnership** method of the [**Win32\_Tpm**](win32-tpm.md) class installs an owner for the TPM.</span></span> <span data-ttu-id="87c09-105">Le propriétaire du module de plateforme sécurisée peut tirer pleinement parti des fonctionnalités du module TPM.</span><span class="sxs-lookup"><span data-stu-id="87c09-105">The owner of the TPM can make full use of TPM capabilities.</span></span> <span data-ttu-id="87c09-106">Une fois qu’un propriétaire est défini, aucun autre utilisateur ou logiciel ne peut réclamer la propriété du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="87c09-106">After an owner is set, no other user or software can claim ownership of the TPM.</span></span>

<span data-ttu-id="87c09-107">Les méthodes [**IsEnabled**](isenabled-win32-tpm.md), [**isActivated**](isactivated-win32-tpm.md)et [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) doivent toutes avoir la valeur true pour que la méthode **TakeOwnership** puisse fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="87c09-107">The [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md), and [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) methods must all be true before the **TakeOwnership** method can succeed.</span></span>

## <a name="syntax"></a><span data-ttu-id="87c09-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87c09-108">Syntax</span></span>


```mof
uint32 TakeOwnership(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="87c09-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87c09-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87c09-110">*Origine* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="87c09-110">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="87c09-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="87c09-111">Type: **string**</span></span>

<span data-ttu-id="87c09-112">Chaîne qui identifie le propriétaire du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="87c09-112">A string that identifies the TPM owner.</span></span> <span data-ttu-id="87c09-113">Cette chaîne doit être une chaîne codée en base64 qui se termine par un caractère null qui contient exactement 20 octets de données binaires.</span><span class="sxs-lookup"><span data-stu-id="87c09-113">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="87c09-114">Utilisez la méthode [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) pour convertir une phrase secrète au format attendu.</span><span class="sxs-lookup"><span data-stu-id="87c09-114">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="87c09-115">Le paramètre *origine* est lu à partir du Registre si aucun n’est fourni.</span><span class="sxs-lookup"><span data-stu-id="87c09-115">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87c09-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87c09-116">Return value</span></span>

<span data-ttu-id="87c09-117">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87c09-117">Type: **uint32**</span></span>

<span data-ttu-id="87c09-118">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="87c09-118">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="87c09-119">Le tableau suivant répertorie certains des codes de retour courants.</span><span class="sxs-lookup"><span data-stu-id="87c09-119">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="87c09-120">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="87c09-120">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="87c09-121">Description</span><span class="sxs-lookup"><span data-stu-id="87c09-121">Description</span></span>                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="87c09-122"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="87c09-122"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="87c09-123">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="87c09-123">The method was successful.</span></span><br/>                                                                                                                                                                              |
| <dl> <span data-ttu-id="87c09-124"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="87c09-124"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="87c09-125">Le paramètre *origine* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="87c09-125">The *OwnerAuth* parameter is not valid.</span></span><br/>                                                                                                                                                                 |
| <dl> <span data-ttu-id="87c09-126"><dt>**Module TPM \_ \_ \_ Jeu de propriétaires E**</dt> <dt>2150105108 (0x80280014)</dt></span><span class="sxs-lookup"><span data-stu-id="87c09-126"><dt>**TPM\_E\_OWNER\_SET**</dt> <dt>2150105108 (0x80280014)</dt></span></span> </dl>            | <span data-ttu-id="87c09-127">Un propriétaire existe déjà sur le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="87c09-127">An owner already exists on the TPM.</span></span><br/>                                                                                                                                                                     |
| <dl> <span data-ttu-id="87c09-128"><dt>**Module TPM \_ E \_ non \_ endossement**</dt> <dt>2150105123 (0x80280023)</dt></span><span class="sxs-lookup"><span data-stu-id="87c09-128"><dt>**TPM\_E\_NO\_ENDORSEMENT**</dt> <dt>2150105123 (0x80280023)</dt></span></span> </dl>       | <span data-ttu-id="87c09-129">Aucune clé de type EK ne peut être trouvée sur le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="87c09-129">No endorsement key can be found on the TPM.</span></span><br/> <span data-ttu-id="87c09-130">Pour créer une paire de clés de type EK sur le module de plateforme sécurisée, consultez la méthode [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="87c09-130">To create an endorsement key pair on the TPM, see the [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) method.</span></span><br/>             |
| <dl> <span data-ttu-id="87c09-131"><dt>**Module TPM \_ E \_ installation \_ désactivée**</dt> <dt>2150105099 (0x8028000B)</dt></span><span class="sxs-lookup"><span data-stu-id="87c09-131"><dt>**TPM\_E\_INSTALL\_DISABLED**</dt> <dt>2150105099 (0x8028000B)</dt></span></span> </dl>     | <span data-ttu-id="87c09-132">Un propriétaire ne peut pas être installé sur ce module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="87c09-132">An owner cannot be installed on this TPM.</span></span><br/> <span data-ttu-id="87c09-133">Pour plus d’informations sur la façon d’autoriser l’installation d’un propriétaire d’appareil, consultez [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md).</span><span class="sxs-lookup"><span data-stu-id="87c09-133">For information about how to allow installation of a device owner, see [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md).</span></span><br/> |
| <dl> <span data-ttu-id="87c09-134"><dt>**Module TPM \_ E \_ protection des \_ verrous \_ en cours d’exécution**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="87c09-134"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="87c09-135">Le module de plateforme sécurisée se défend contre les attaques par dictionnaire et se trouve dans un délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="87c09-135">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="87c09-136">Pour plus d’informations, consultez la méthode [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="87c09-136">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/>                               |



 

## <a name="remarks"></a><span data-ttu-id="87c09-137">Notes</span><span class="sxs-lookup"><span data-stu-id="87c09-137">Remarks</span></span>

<span data-ttu-id="87c09-138">Les méthodes [**IsEnabled**](isenabled-win32-tpm.md), [**isActivated**](isactivated-win32-tpm.md)et [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) doivent toutes avoir la valeur true pour que **TakeOwnership** puisse s’effectuer correctement.</span><span class="sxs-lookup"><span data-stu-id="87c09-138">The methods [**IsEnabled**](isenabled-win32-tpm.md), [**IsActivated**](isactivated-win32-tpm.md), and [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md) must all be true before **TakeOwnership** can succeed.</span></span>

<span data-ttu-id="87c09-139">Vous devez utiliser la méthode [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) pour remplacer une phrase secrète par la valeur d’entrée utilisée pour le paramètre *origine* .</span><span class="sxs-lookup"><span data-stu-id="87c09-139">You should use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to change a passphrase into the input value used for the *OwnerAuth* parameter.</span></span>

<span data-ttu-id="87c09-140">La méthode **TakeOwnership** sauvegarde la valeur d’autorisation du propriétaire sur Active Directory si les paramètres de stratégie de groupe appropriés ont été configurés.</span><span class="sxs-lookup"><span data-stu-id="87c09-140">The **TakeOwnership** method backs up the owner authorization value to Active Directory if the appropriate Group Policy settings have been configured.</span></span>

<span data-ttu-id="87c09-141">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="87c09-141">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="87c09-142">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="87c09-142">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="87c09-143">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="87c09-143">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="87c09-144">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="87c09-144">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87c09-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87c09-145">Requirements</span></span>



| <span data-ttu-id="87c09-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87c09-146">Requirement</span></span> | <span data-ttu-id="87c09-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="87c09-147">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="87c09-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87c09-148">Minimum supported client</span></span><br/> | <span data-ttu-id="87c09-149">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87c09-149">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="87c09-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87c09-150">Minimum supported server</span></span><br/> | <span data-ttu-id="87c09-151">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87c09-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="87c09-152">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="87c09-152">Namespace</span></span><br/>                | <span data-ttu-id="87c09-153">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="87c09-153">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="87c09-154">MOF</span><span class="sxs-lookup"><span data-stu-id="87c09-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87c09-155"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="87c09-155"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="87c09-156">DLL</span><span class="sxs-lookup"><span data-stu-id="87c09-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87c09-157"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="87c09-157"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87c09-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87c09-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87c09-159">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="87c09-159">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
