---
description: Réinitialise la valeur d’autorisation de la clé de racine de stockage (SRK) pour qu’elle soit compatible avec le système d’exploitation.
ms.assetid: af008733-b43c-4017-9e79-bdd98f2e20b6
title: Méthode ResetSrkAuth de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ResetSrkAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 7d838ded7051511b6a8f9117327ee7cdb1a00d7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320541"
---
# <a name="resetsrkauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="f8a90-103">Méthode ResetSrkAuth de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="f8a90-103">ResetSrkAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="f8a90-104">La méthode **ResetSrkAuth** de la [**classe \_ TPM Win32**](win32-tpm.md) réinitialise la valeur d’autorisation de la clé de racine de stockage (SRK) pour qu’elle soit compatible avec le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f8a90-104">The **ResetSrkAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class resets the Storage Root Key (SRK) authorization value to be compatible with the operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8a90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8a90-105">Syntax</span></span>


```mof
uint32 ResetSrkAuth(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="f8a90-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8a90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8a90-107">*Origine* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f8a90-107">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8a90-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f8a90-108">Type: **string**</span></span>

<span data-ttu-id="f8a90-109">Chaîne qui identifie le propriétaire du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="f8a90-109">A string that identifies the TPM owner.</span></span> <span data-ttu-id="f8a90-110">Cette chaîne doit être une chaîne codée en base64 qui se termine par un caractère null qui contient exactement 20 octets de données binaires.</span><span class="sxs-lookup"><span data-stu-id="f8a90-110">This string must be a base64-encoded null-terminated string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="f8a90-111">Utilisez la méthode [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) pour convertir une phrase secrète au format attendu.</span><span class="sxs-lookup"><span data-stu-id="f8a90-111">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="f8a90-112">Le paramètre *origine* est lu à partir du Registre si aucun n’est fourni.</span><span class="sxs-lookup"><span data-stu-id="f8a90-112">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8a90-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8a90-113">Return value</span></span>

<span data-ttu-id="f8a90-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f8a90-114">Type: **uint32**</span></span>

<span data-ttu-id="f8a90-115">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="f8a90-115">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="f8a90-116">Le tableau suivant répertorie certains des codes de retour courants.</span><span class="sxs-lookup"><span data-stu-id="f8a90-116">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="f8a90-117">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f8a90-117">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="f8a90-118">Description</span><span class="sxs-lookup"><span data-stu-id="f8a90-118">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f8a90-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f8a90-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="f8a90-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="f8a90-120">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="f8a90-121"><dt> **TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="f8a90-121"><dt>**TPM\_E\_AUTHFAIL** </dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>             | <span data-ttu-id="f8a90-122">La valeur d’autorisation du propriétaire fournie ne peut pas satisfaire la requête.</span><span class="sxs-lookup"><span data-stu-id="f8a90-122">The provided owner authorization value cannot fulfill the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="f8a90-123"><dt>**Module TPM \_ E \_ protection des \_ verrous \_ en cours d’exécution**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="f8a90-123"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="f8a90-124">Le module de plateforme sécurisée se défend contre les attaques par dictionnaire et se trouve dans un délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="f8a90-124">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="f8a90-125">Pour plus d’informations, consultez la méthode [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="f8a90-125">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f8a90-126">Notes</span><span class="sxs-lookup"><span data-stu-id="f8a90-126">Remarks</span></span>

<span data-ttu-id="f8a90-127">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="f8a90-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f8a90-128">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="f8a90-128">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f8a90-129">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="f8a90-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f8a90-130">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f8a90-130">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f8a90-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8a90-131">Requirements</span></span>



| <span data-ttu-id="f8a90-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8a90-132">Requirement</span></span> | <span data-ttu-id="f8a90-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8a90-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a90-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8a90-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f8a90-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8a90-135">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f8a90-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8a90-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f8a90-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8a90-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f8a90-138">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f8a90-138">Namespace</span></span><br/>                | <span data-ttu-id="f8a90-139">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="f8a90-139">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="f8a90-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f8a90-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8a90-141"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="f8a90-141"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8a90-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f8a90-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8a90-143"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="f8a90-143"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8a90-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8a90-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8a90-145">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="f8a90-145">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
