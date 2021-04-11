---
description: Autorise le propriétaire du module de plateforme sécurisée à activer ou à reprendre le module de plateforme sécurisée.
ms.assetid: 9fb0b0aa-a569-4c0c-859e-8640480dbb3e
title: Activer la méthode de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.Enable
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6fe79ee44cb2ef6494b770a53cb57f7b88943dc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203029"
---
# <a name="enable-method-of-the-win32_tpm-class"></a><span data-ttu-id="9a57a-103">Activer la méthode de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="9a57a-103">Enable method of the Win32\_Tpm class</span></span>

<span data-ttu-id="9a57a-104">La méthode **Enable** de la [**classe \_ TPM Win32**](win32-tpm.md) permet au propriétaire du module de plateforme sécurisée d’activer ou de reprendre le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="9a57a-104">The **Enable** method of the [**Win32\_Tpm**](win32-tpm.md) class allows the TPM owner to enable or resume the TPM.</span></span>

<span data-ttu-id="9a57a-105">Pour exécuter cette méthode, le module de plateforme sécurisée doit déjà avoir un propriétaire.</span><span class="sxs-lookup"><span data-stu-id="9a57a-105">To run this method, the TPM must already have an owner.</span></span> <span data-ttu-id="9a57a-106">Pour activer un module de plateforme sécurisée qui n’a pas encore de propriétaire, utilisez la méthode [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="9a57a-106">To enable a TPM that does not already have an owner, use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a57a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a57a-107">Syntax</span></span>


```mof
uint32 Enable(
  [in, optional] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="9a57a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a57a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a57a-109">*Origine* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="9a57a-109">*OwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9a57a-110">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="9a57a-110">Type: **string**</span></span>

<span data-ttu-id="9a57a-111">Chaîne qui identifie le propriétaire du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="9a57a-111">A string that identifies the TPM owner.</span></span> <span data-ttu-id="9a57a-112">Cette chaîne doit être une chaîne encodée en base64 contenant exactement 20 octets de données binaires.</span><span class="sxs-lookup"><span data-stu-id="9a57a-112">This string must be a base64-encoded string that contains exactly 20 bytes of binary data.</span></span> <span data-ttu-id="9a57a-113">Utilisez la méthode [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) pour convertir une phrase secrète au format attendu.</span><span class="sxs-lookup"><span data-stu-id="9a57a-113">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a passphrase to this expected format.</span></span> <span data-ttu-id="9a57a-114">Le paramètre *origine* est lu à partir du Registre si aucun n’est fourni.</span><span class="sxs-lookup"><span data-stu-id="9a57a-114">The *OwnerAuth* parameter is read from the registry if none is provided.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a57a-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9a57a-115">Return value</span></span>

<span data-ttu-id="9a57a-116">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a57a-116">Type: **uint32**</span></span>

<span data-ttu-id="9a57a-117">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="9a57a-117">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="9a57a-118">Le tableau suivant répertorie certains des codes de retour courants.</span><span class="sxs-lookup"><span data-stu-id="9a57a-118">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="9a57a-119">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="9a57a-119">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="9a57a-120">Description</span><span class="sxs-lookup"><span data-stu-id="9a57a-120">Description</span></span>                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a57a-121"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9a57a-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="9a57a-122">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="9a57a-122">The method was successful.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="9a57a-123"><dt>**Module TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="9a57a-123"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>              | <span data-ttu-id="9a57a-124">La valeur d’autorisation du propriétaire fournie ne peut pas effectuer la requête.</span><span class="sxs-lookup"><span data-stu-id="9a57a-124">The provided owner authorization value cannot perform the request.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="9a57a-125"><dt>**Module TPM \_ E \_ protection des \_ verrous \_ en cours d’exécution**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="9a57a-125"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl> | <span data-ttu-id="9a57a-126">Le module de plateforme sécurisée se défend contre les attaques par dictionnaire et se trouve dans un délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="9a57a-126">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="9a57a-127">Pour plus d’informations, consultez la méthode [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="9a57a-127">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9a57a-128">Notes</span><span class="sxs-lookup"><span data-stu-id="9a57a-128">Remarks</span></span>

<span data-ttu-id="9a57a-129">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="9a57a-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9a57a-130">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="9a57a-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="9a57a-131">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="9a57a-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9a57a-132">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="9a57a-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a57a-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a57a-133">Requirements</span></span>



| <span data-ttu-id="9a57a-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a57a-134">Requirement</span></span> | <span data-ttu-id="9a57a-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a57a-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a57a-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a57a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9a57a-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a57a-137">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9a57a-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a57a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9a57a-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9a57a-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9a57a-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="9a57a-140">Namespace</span></span><br/>                | <span data-ttu-id="9a57a-141">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="9a57a-141">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="9a57a-142">MOF</span><span class="sxs-lookup"><span data-stu-id="9a57a-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a57a-143"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="9a57a-143"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a57a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="9a57a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a57a-145"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="9a57a-145"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a57a-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a57a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a57a-147">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="9a57a-147">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="9a57a-148">**SetPhysicalPresenceRequest**</span><span class="sxs-lookup"><span data-stu-id="9a57a-148">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
