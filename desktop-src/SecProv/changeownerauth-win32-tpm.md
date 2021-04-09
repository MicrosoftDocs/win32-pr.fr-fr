---
description: Modifie la valeur d’autorisation du propriétaire du module de plateforme sécurisée.
ms.assetid: ed280037-2360-4889-baba-cfa9e4fd473e
title: Méthode ChangeOwnerAuth de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ChangeOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: fc4b044d58dcaca5364f0ba669b09030cf3b34dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112643"
---
# <a name="changeownerauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="29a0f-103">Méthode ChangeOwnerAuth de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="29a0f-103">ChangeOwnerAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="29a0f-104">La méthode **ChangeOwnerAuth** de la [**classe \_ TPM Win32**](win32-tpm.md) modifie la valeur d’autorisation du propriétaire du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="29a0f-104">The **ChangeOwnerAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class changes the TPM owner authorization value.</span></span>

## <a name="syntax"></a><span data-ttu-id="29a0f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="29a0f-105">Syntax</span></span>


```mof
uint32 ChangeOwnerAuth(
  [in, optional] string OldOwnerAuth,
  [in, optional] string NewOwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="29a0f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="29a0f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29a0f-107">*OldOwnerAuth* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="29a0f-107">*OldOwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="29a0f-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="29a0f-108">Type: **string**</span></span>

<span data-ttu-id="29a0f-109">Chaîne qui nomme la valeur d’autorisation du propriétaire du module de plateforme sécurisée (TPM) actuelle de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="29a0f-109">A string that names the current TPM owner authorization value of the device.</span></span> <span data-ttu-id="29a0f-110">Utilisez la méthode [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) pour convertir un mot de passe en cette valeur d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="29a0f-110">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a password to this authorization value.</span></span> <span data-ttu-id="29a0f-111">Le paramètre *OldOwnerAuth* n’est pas fourni ou une chaîne vide est fournie, cette méthode obtient la valeur du Registre si elle est présente.</span><span class="sxs-lookup"><span data-stu-id="29a0f-111">The *OldOwnerAuth* parameter is not supplied or an empty string is provided, this method gets the value from the registry if present.</span></span>

</dd> <dt>

<span data-ttu-id="29a0f-112">*NewOwnerAuth* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="29a0f-112">*NewOwnerAuth* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="29a0f-113">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="29a0f-113">Type: **string**</span></span>

<span data-ttu-id="29a0f-114">Chaîne qui nomme la nouvelle valeur d’autorisation du propriétaire du module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="29a0f-114">A string that names the new TPM owner authorization value.</span></span> <span data-ttu-id="29a0f-115">Utilisez la méthode [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) pour convertir un mot de passe en cette valeur d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="29a0f-115">Use the [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md) method to translate a password to this authorization value.</span></span> <span data-ttu-id="29a0f-116">Le paramètre *NewOwnerAuth* ne peut pas être vide ou avoir la **valeur null.**</span><span class="sxs-lookup"><span data-stu-id="29a0f-116">The *NewOwnerAuth* parameter cannot be empty or **NULL.**</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29a0f-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="29a0f-117">Return value</span></span>

<span data-ttu-id="29a0f-118">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="29a0f-118">Type: **uint32**</span></span>

<span data-ttu-id="29a0f-119">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="29a0f-119">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="29a0f-120">Le tableau suivant répertorie certains des codes de retour courants.</span><span class="sxs-lookup"><span data-stu-id="29a0f-120">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="29a0f-121">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="29a0f-121">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="29a0f-122">Description</span><span class="sxs-lookup"><span data-stu-id="29a0f-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="29a0f-123"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="29a0f-123"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                              | <span data-ttu-id="29a0f-124">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="29a0f-124">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="29a0f-125"><dt>**Module TPM \_ E \_ AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span><span class="sxs-lookup"><span data-stu-id="29a0f-125"><dt>**TPM\_E\_AUTHFAIL**</dt> <dt>2150105089 (0x80280001)</dt></span></span> </dl>                   | <span data-ttu-id="29a0f-126">La valeur actuelle de l’autorisation du propriétaire du module de plateforme sécurisée est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="29a0f-126">The current TPM owner authorization value is incorrect.</span></span><br/>                                                                                                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="29a0f-127"><dt>**Module TPM \_ E \_ protection des \_ verrous \_ en cours d’exécution**</dt> <dt>2150107139 (0x80280803)</dt></span><span class="sxs-lookup"><span data-stu-id="29a0f-127"><dt>**TPM\_E\_DEFEND\_LOCK\_RUNNING**</dt> <dt>2150107139 (0x80280803)</dt></span></span> </dl>      | <span data-ttu-id="29a0f-128">Le module de plateforme sécurisée se défend contre les attaques par dictionnaire et se trouve dans un délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="29a0f-128">The TPM is defending against dictionary attacks and is in a time-out period.</span></span> <span data-ttu-id="29a0f-129">Pour plus d’informations, consultez la méthode [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="29a0f-129">For more information, see the [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) method.</span></span><br/>                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="29a0f-130"><dt>**FVE \_ Le \_ schéma E ad \_ \_ n’est pas \_ installé**</dt> <dt>2150694922 (0x8031000A)</dt></span><span class="sxs-lookup"><span data-stu-id="29a0f-130"><dt>**FVE\_E\_AD\_SCHEMA\_NOT\_INSTALLED**</dt> <dt>2150694922 (0x8031000A)</dt></span></span> </dl> | <span data-ttu-id="29a0f-131">Impossible d’enregistrer les informations de récupération sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="29a0f-131">Cannot save recovery information to the network.</span></span> <span data-ttu-id="29a0f-132">L’ordinateur a été configuré pour stocker les informations de récupération à Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="29a0f-132">The computer has been configured to store recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="29a0f-133">Pour obtenir des instructions sur la configuration de Active Directory, consultez [chiffrement de lecteur BitLocker Guide de configuration : sauvegarde des informations de récupération BitLocker et TPM dans Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="29a0f-133">For instructions on how to set up Active Directory, see [BitLocker Drive Encryption Configuration Guide: Backing Up BitLocker and TPM Recovery Information to Active Directory](/previous-versions/windows/it-pro/windows-vista/cc766015(v=ws.10)).</span></span><br/> |
| <dl> <span data-ttu-id="29a0f-134"><dt>**Échec**</dt> <dt>de la connexion 2147943755 (0x8007054B)</dt></span><span class="sxs-lookup"><span data-stu-id="29a0f-134"><dt>**Connection Failed**</dt> <dt>2147943755 (0x8007054B)</dt></span></span> </dl>                  | <span data-ttu-id="29a0f-135">Impossible d’enregistrer les informations de récupération sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="29a0f-135">Cannot save recovery information to the network.</span></span> <span data-ttu-id="29a0f-136">L’ordinateur a été configuré pour stocker les informations de récupération à Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="29a0f-136">The computer has been configured to store recovery information to Active Directory Domain Services.</span></span> <span data-ttu-id="29a0f-137">Une connexion réseau est nécessaire pour continuer.</span><span class="sxs-lookup"><span data-stu-id="29a0f-137">A network connection is required to continue.</span></span><br/>                                                                                                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="29a0f-138">Notes</span><span class="sxs-lookup"><span data-stu-id="29a0f-138">Remarks</span></span>

<span data-ttu-id="29a0f-139">La méthode **ChangeOwnerAuth** sauvegarde la nouvelle autorisation du propriétaire du module de plateforme sécurisée sur Active Directory Domain Services si les paramètres de stratégie de groupe appropriés ont été configurés.</span><span class="sxs-lookup"><span data-stu-id="29a0f-139">The **ChangeOwnerAuth** method backs up the new TPM owner authorization to Active Directory Domain Services if the appropriate Group Policy settings have been configured.</span></span>

<span data-ttu-id="29a0f-140">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="29a0f-140">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="29a0f-141">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="29a0f-141">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="29a0f-142">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="29a0f-142">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="29a0f-143">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="29a0f-143">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="29a0f-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29a0f-144">Requirements</span></span>



| <span data-ttu-id="29a0f-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29a0f-145">Requirement</span></span> | <span data-ttu-id="29a0f-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="29a0f-146">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="29a0f-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29a0f-147">Minimum supported client</span></span><br/> | <span data-ttu-id="29a0f-148">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29a0f-148">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="29a0f-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29a0f-149">Minimum supported server</span></span><br/> | <span data-ttu-id="29a0f-150">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29a0f-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="29a0f-151">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="29a0f-151">Namespace</span></span><br/>                | <span data-ttu-id="29a0f-152">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="29a0f-152">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="29a0f-153">MOF</span><span class="sxs-lookup"><span data-stu-id="29a0f-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="29a0f-154"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="29a0f-154"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="29a0f-155">DLL</span><span class="sxs-lookup"><span data-stu-id="29a0f-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="29a0f-156"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="29a0f-156"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29a0f-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29a0f-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29a0f-158">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="29a0f-158">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
