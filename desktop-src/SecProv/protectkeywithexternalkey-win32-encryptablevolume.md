---
description: Sécurise la clé de chiffrement du volume à l’aide d’une clé externe 256 bits.
ms.assetid: 768cef38-a00f-4faa-bbe3-9d4a19be2f6d
title: Méthode ProtectKeyWithExternalKey de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: adcbdfdb9ea55139626bf3d1657b2e154c8d2b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516229"
---
# <a name="protectkeywithexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="f1969-103">Méthode ProtectKeyWithExternalKey de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="f1969-103">ProtectKeyWithExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="f1969-104">La méthode **ProtectKeyWithExternalKey** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) sécurise la clé de chiffrement du volume à l’aide d’une clé externe 256 bits.</span><span class="sxs-lookup"><span data-stu-id="f1969-104">The **ProtectKeyWithExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key with a 256-bit external key.</span></span> <span data-ttu-id="f1969-105">Cette clé externe peut être utilisée pour récupérer des échecs d’authentification d’autres protecteurs de clé (par exemple, TPM).</span><span class="sxs-lookup"><span data-stu-id="f1969-105">This external key can be used to recover from the authentication failures of other key protectors (for example, TPM).</span></span>

<span data-ttu-id="f1969-106">Utilisez la méthode [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) pour enregistrer cette clé externe dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="f1969-106">Use the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method to save this external key to a file.</span></span> <span data-ttu-id="f1969-107">Les périphériques de mémoire USB qui contiennent cette clé externe peuvent être utilisés comme clé de démarrage ou clé de récupération au démarrage de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="f1969-107">USB memory devices that contain this external key can be used as a startup key or a recovery key when the computer starts.</span></span>

<span data-ttu-id="f1969-108">Un protecteur de clé de type « clé externe » est créé pour le volume.</span><span class="sxs-lookup"><span data-stu-id="f1969-108">A key protector of type "External Key" is created for the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1969-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1969-109">Syntax</span></span>


```mof
uint32 ProtectKeyWithExternalKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="f1969-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1969-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1969-111">*FriendlyName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f1969-111">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f1969-112">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1969-112">Type: **string**</span></span>

<span data-ttu-id="f1969-113">Chaîne qui spécifie un identificateur affecté à l’utilisateur pour ce protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="f1969-113">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="f1969-114">Si ce paramètre n’est pas spécifié, une valeur vide est utilisée.</span><span class="sxs-lookup"><span data-stu-id="f1969-114">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="f1969-115">*ExternalKey* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f1969-115">*ExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f1969-116">Type : **UInt8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="f1969-116">Type: **uint8\[\]**</span></span>

<span data-ttu-id="f1969-117">Tableau d’octets qui spécifie la clé externe 256 bits utilisée pour déverrouiller le volume.</span><span class="sxs-lookup"><span data-stu-id="f1969-117">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span>

<span data-ttu-id="f1969-118">Si aucune clé externe n’est spécifiée, une clé est générée de façon aléatoire.</span><span class="sxs-lookup"><span data-stu-id="f1969-118">If no external key is specified, one is randomly generated.</span></span> <span data-ttu-id="f1969-119">Utilisez la méthode [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) pour obtenir la clé générée de façon aléatoire.</span><span class="sxs-lookup"><span data-stu-id="f1969-119">Use the [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) method to obtain the randomly generated key.</span></span>

</dd> <dt>

<span data-ttu-id="f1969-120">*VolumeKeyProtectorID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f1969-120">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1969-121">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="f1969-121">Type: **string**</span></span>

<span data-ttu-id="f1969-122">Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="f1969-122">A unique string identifier used to manage an encrypted volume key protector.</span></span>

<span data-ttu-id="f1969-123">Si le lecteur prend en charge le chiffrement matériel et que BitLocker n’a pas pris possession de la bande, la chaîne d’ID est définie sur « BitLocker » et le protecteur de clé est écrit dans les métadonnées par bande.</span><span class="sxs-lookup"><span data-stu-id="f1969-123">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1969-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f1969-124">Return value</span></span>

<span data-ttu-id="f1969-125">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1969-125">Type: **uint32**</span></span>

<span data-ttu-id="f1969-126">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="f1969-126">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="f1969-127">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="f1969-127">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="f1969-128">Description</span><span class="sxs-lookup"><span data-stu-id="f1969-128">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1969-129"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f1969-129"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="f1969-130">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="f1969-130">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="f1969-131"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="f1969-131"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="f1969-132">Le paramètre *ExternalKey* est fourni, mais n’est pas un tableau de taille 4.</span><span class="sxs-lookup"><span data-stu-id="f1969-132">The *ExternalKey* parameter is provided but is not an array of size 4.</span></span><br/>            |
| <dl> <span data-ttu-id="f1969-133"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="f1969-133"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="f1969-134">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="f1969-134">The volume is locked.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="f1969-135"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="f1969-135"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="f1969-136">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="f1969-136">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="f1969-137">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="f1969-137">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="f1969-138">Notes</span><span class="sxs-lookup"><span data-stu-id="f1969-138">Remarks</span></span>

<span data-ttu-id="f1969-139">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="f1969-139">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f1969-140">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="f1969-140">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f1969-141">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="f1969-141">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f1969-142">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f1969-142">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1969-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1969-143">Requirements</span></span>



| <span data-ttu-id="f1969-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1969-144">Requirement</span></span> | <span data-ttu-id="f1969-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1969-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1969-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1969-146">Minimum supported client</span></span><br/> | <span data-ttu-id="f1969-147">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1969-147">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="f1969-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1969-148">Minimum supported server</span></span><br/> | <span data-ttu-id="f1969-149">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1969-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1969-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f1969-150">Namespace</span></span><br/>                | <span data-ttu-id="f1969-151">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="f1969-151">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="f1969-152">MOF</span><span class="sxs-lookup"><span data-stu-id="f1969-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1969-153"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1969-153"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1969-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1969-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1969-155">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="f1969-155">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
