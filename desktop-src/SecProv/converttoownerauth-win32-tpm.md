---
description: Traduit une entrée de phrase secrète fournie par l’utilisateur en une autorisation de propriétaire de 20 octets qui peut être utilisée pour interagir avec le module de plateforme sécurisée. Les méthodes telles que TakeOwnership et ResetAuthLockOut requièrent la valeur d’autorisation du propriétaire qui en résulte.
ms.assetid: 69eed934-1668-495a-b5b7-cd4a87df1ab3
title: Méthode ConvertToOwnerAuth de la classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ConvertToOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f3de5803d10458156fb453e964d782f7c9760333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536738"
---
# <a name="converttoownerauth-method-of-the-win32_tpm-class"></a><span data-ttu-id="75994-104">Méthode ConvertToOwnerAuth de la \_ classe TPM Win32</span><span class="sxs-lookup"><span data-stu-id="75994-104">ConvertToOwnerAuth method of the Win32\_Tpm class</span></span>

<span data-ttu-id="75994-105">La méthode **ConvertToOwnerAuth** de la [**classe \_ TPM Win32**](win32-tpm.md) traduit une entrée de phrase secrète fournie par l’utilisateur en une autorisation de propriétaire de 20 octets qui peut être utilisée pour interagir avec le module de plateforme sécurisée.</span><span class="sxs-lookup"><span data-stu-id="75994-105">The **ConvertToOwnerAuth** method of the [**Win32\_Tpm**](win32-tpm.md) class translates a user-provided passphrase input into a 20-byte owner authorization that can be used to interact with the TPM.</span></span> <span data-ttu-id="75994-106">Les méthodes telles que [**TakeOwnership**](takeownership-win32-tpm.md) et [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) requièrent la valeur d’autorisation du propriétaire qui en résulte.</span><span class="sxs-lookup"><span data-stu-id="75994-106">Methods such as [**TakeOwnership**](takeownership-win32-tpm.md) and [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) require the resulting owner authorization value.</span></span>

<span data-ttu-id="75994-107">Le processus de conversion suit les spécifications de la [Trusted Computing Group](https://www.trustedcomputinggroup.org/).</span><span class="sxs-lookup"><span data-stu-id="75994-107">The conversion process follows the specifications from the [Trusted Computing Group](https://www.trustedcomputinggroup.org/).</span></span>

## <a name="syntax"></a><span data-ttu-id="75994-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75994-108">Syntax</span></span>


```mof
uint32 ConvertToOwnerAuth(
  [in]  string OwnerPassPhrase,
  [out] string OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="75994-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75994-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75994-110">*OwnerPassPhrase* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="75994-110">*OwnerPassPhrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75994-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="75994-111">Type: **string**</span></span>

<span data-ttu-id="75994-112">Chaîne à convertir en valeur d’autorisation du propriétaire.</span><span class="sxs-lookup"><span data-stu-id="75994-112">A string to convert to an owner authorization value.</span></span> <span data-ttu-id="75994-113">La chaîne peut contenir un nombre quelconque de caractères alphanumériques.</span><span class="sxs-lookup"><span data-stu-id="75994-113">The string can contain any number of alphanumeric characters.</span></span>

</dd> <dt>

<span data-ttu-id="75994-114">*Origine* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="75994-114">*OwnerAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75994-115">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="75994-115">Type: **string**</span></span>

<span data-ttu-id="75994-116">Chaîne dérivée du paramètre *OwnerPassPhrase* .</span><span class="sxs-lookup"><span data-stu-id="75994-116">A string derived from the *OwnerPassPhrase* parameter.</span></span> <span data-ttu-id="75994-117">Cette valeur est une valeur binaire de 20 octets encodée en une chaîne de 28 octets se terminant par un caractère **null**.</span><span class="sxs-lookup"><span data-stu-id="75994-117">This value is a 20-byte binary value encoded to a 28-byte base64 **null**-terminated string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75994-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="75994-118">Return value</span></span>

<span data-ttu-id="75994-119">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="75994-119">Type: **uint32**</span></span>

<span data-ttu-id="75994-120">Toutes les erreurs de module de plateforme sécurisée, ainsi que les erreurs spécifiques aux services de base TPM, peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="75994-120">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="75994-121">Les tableaux suivants répertorient certains des codes de retour courants.</span><span class="sxs-lookup"><span data-stu-id="75994-121">The following tables lists some of the common return codes.</span></span>



| <span data-ttu-id="75994-122">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="75994-122">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="75994-123">Description</span><span class="sxs-lookup"><span data-stu-id="75994-123">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="75994-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="75994-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="75994-125">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="75994-125">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="75994-126">Notes</span><span class="sxs-lookup"><span data-stu-id="75994-126">Remarks</span></span>

<span data-ttu-id="75994-127">Une chaîne encodée UTF-16LE Unicode est convertie en valeur d’autorisation du propriétaire du module de plateforme sécurisée (TPM) de 20 octets en acceptant le hachage SHA-1 de la représentation binaire de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="75994-127">A Unicode UTF-16LE encoded string is converted to the 20-byte TPM owner authorization value by taking the SHA-1 hash of the string's binary representation.</span></span> <span data-ttu-id="75994-128">La fin **null** de la chaîne Unicode n’est pas incluse dans le hachage.</span><span class="sxs-lookup"><span data-stu-id="75994-128">The **null** termination of the Unicode string is not included in the hash.</span></span> <span data-ttu-id="75994-129">Aucun Salt n’est utilisé dans le hachage SHA-1.</span><span class="sxs-lookup"><span data-stu-id="75994-129">No salt is used in the SHA-1 hash.</span></span>

<span data-ttu-id="75994-130">Par exemple, pour convertir la phrase secrète du propriétaire du module de plateforme sécurisée « 1Sample » en valeur d’autorisation du propriétaire du module de plateforme sécurisée, le hachage SHA-1 est extrait du flux d’octets suivant :</span><span class="sxs-lookup"><span data-stu-id="75994-130">For example, to convert the TPM owner passphrase "1Sample" to a TPM owner authorization value, the SHA-1 hash is taken from the following byte stream:</span></span>

`0x31 0x00 0x53 0x00 0x61 0x00 0x6D 0x00 0x70 0x00 0x6C 0x00 0x65 0x00`

<span data-ttu-id="75994-131">Pour convertir une phrase secrète de longueur nulle en valeur d’autorisation du propriétaire, le hachage SHA-1 est pris dans le flux d’octets **null** .</span><span class="sxs-lookup"><span data-stu-id="75994-131">To convert a zero-length passphrase to an owner authorization value, the SHA-1 hash is taken of the **NULL** byte stream.</span></span>

<span data-ttu-id="75994-132">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="75994-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="75994-133">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="75994-133">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="75994-134">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="75994-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="75994-135">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="75994-135">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75994-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="75994-136">Requirements</span></span>



| <span data-ttu-id="75994-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="75994-137">Requirement</span></span> | <span data-ttu-id="75994-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="75994-138">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="75994-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75994-139">Minimum supported client</span></span><br/> | <span data-ttu-id="75994-140">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75994-140">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="75994-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="75994-141">Minimum supported server</span></span><br/> | <span data-ttu-id="75994-142">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="75994-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="75994-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="75994-143">Namespace</span></span><br/>                | <span data-ttu-id="75994-144">Racine \\ de \\ sécurité cimv2 \\ MicrosoftTpm</span><span class="sxs-lookup"><span data-stu-id="75994-144">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="75994-145">MOF</span><span class="sxs-lookup"><span data-stu-id="75994-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75994-146"><dt>\_TPM. mof Win32</dt></span><span class="sxs-lookup"><span data-stu-id="75994-146"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="75994-147">DLL</span><span class="sxs-lookup"><span data-stu-id="75994-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75994-148"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="75994-148"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75994-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75994-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75994-150">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="75994-150">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="75994-151">**TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="75994-151">**TakeOwnership**</span></span>](takeownership-win32-tpm.md)
</dt> </dl>

 

 
