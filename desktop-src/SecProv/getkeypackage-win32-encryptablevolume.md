---
description: Exporte des informations qui peuvent aider à récupérer les données chiffrées lorsque le lecteur est gravement endommagé et qu’il n’existe aucun fichier de sauvegarde de données.
ms.assetid: 3d376a02-3392-433e-b842-24c73074610c
title: Méthode GetKeyPackage de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyPackage
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d1b2348a90b6b3cd01685c740fdfa67ad5a2d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522143"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="0e274-103">Méthode GetKeyPackage de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="0e274-103">GetKeyPackage method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="0e274-104">La méthode **GetKeyPackage** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) exporte des informations qui peuvent aider à récupérer des données chiffrées lorsque le lecteur est gravement endommagé et qu’il n’existe aucun fichier de sauvegarde de données.</span><span class="sxs-lookup"><span data-stu-id="0e274-104">The **GetKeyPackage** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class exports information that may help salvage encrypted data when the drive is severely damaged and no data backup files exist.</span></span>

<span data-ttu-id="0e274-105">Les informations exportées se composent de la clé de chiffrement du volume sécurisée par un protecteur de clé du type « mot de passe numérique » ou « clé externe ».</span><span class="sxs-lookup"><span data-stu-id="0e274-105">The exported information consists of the volume's encryption key secured by a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="0e274-106">Pour utiliser ce package, vous devez également enregistrer le mot de passe numérique ou la clé externe correspondant.</span><span class="sxs-lookup"><span data-stu-id="0e274-106">To make use of this package, you must also save the corresponding numerical password or external key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0e274-107">Si vous choisissez d’exporter un package de clés, veillez à conserver ces informations dans un emplacement bien protégé.</span><span class="sxs-lookup"><span data-stu-id="0e274-107">If you choose to export a key package, make certain to keep this information in a well-protected location.</span></span> <span data-ttu-id="0e274-108">Ne transmettent pas ces informations avec votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0e274-108">Do not carry this information with your computer.</span></span> <span data-ttu-id="0e274-109">Si ce package de clés est perdu ou volé, vous devez déchiffrer le volume et le rechiffrer à l’aide d’une nouvelle clé.</span><span class="sxs-lookup"><span data-stu-id="0e274-109">If this key package is lost or stolen, you will need to decrypt the volume and reencrypt it by using a new key.</span></span>

 

<span data-ttu-id="0e274-110">En cas de défaillance d’un disque, l’outil de réparation BitLocker existe pour aider à récupérer les données disponibles.</span><span class="sxs-lookup"><span data-stu-id="0e274-110">In the event of a drive failure, the BitLocker Repair Tool exists to help salvage available data.</span></span> <span data-ttu-id="0e274-111">Pour plus d’informations sur la façon dont cet outil peut utiliser le package de clé, consultez [comment utiliser l’outil de réparation BitLocker pour faciliter la récupération de données à partir d’un volume chiffré dans Windows Vista](https://support.microsoft.com/kb/928201).</span><span class="sxs-lookup"><span data-stu-id="0e274-111">For more information about how this tool can use the key package, see [How to use the BitLocker Repair Tool to help recover data from an encrypted volume in Windows Vista](https://support.microsoft.com/kb/928201).</span></span>

## <a name="syntax"></a><span data-ttu-id="0e274-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e274-112">Syntax</span></span>


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a><span data-ttu-id="0e274-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0e274-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e274-114">*VolumeKeyProtectorID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0e274-114">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0e274-115">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0e274-115">Type: **string**</span></span>

<span data-ttu-id="0e274-116">Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="0e274-116">A unique string identifier used to manage an encrypted volume key protector.</span></span> <span data-ttu-id="0e274-117">Pour exporter un package de clés, vous devez utiliser un protecteur de clé de type « numérique de mot de passe » ou « clé externe ».</span><span class="sxs-lookup"><span data-stu-id="0e274-117">To export a key package, you must use a key protector of type "Numerical Password" or "External Key".</span></span>

</dd> <dt>

<span data-ttu-id="0e274-118">*Keypackage \[ \]* en \[ sortie\]</span><span class="sxs-lookup"><span data-stu-id="0e274-118">*KeyPackage\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e274-119">Type : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="0e274-119">Type: **uint8**</span></span>

<span data-ttu-id="0e274-120">Flux d’octets qui contient la clé de chiffrement d’un volume, sécurisée par le protecteur de clé spécifié.</span><span class="sxs-lookup"><span data-stu-id="0e274-120">A byte stream that contains the encryption key for a volume, secured by the specified key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e274-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0e274-121">Return value</span></span>

<span data-ttu-id="0e274-122">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e274-122">Type: **uint32**</span></span>

<span data-ttu-id="0e274-123">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="0e274-123">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="0e274-124">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0e274-124">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="0e274-125">Description</span><span class="sxs-lookup"><span data-stu-id="0e274-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0e274-126"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0e274-126"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="0e274-127">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="0e274-127">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="0e274-128"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="0e274-128"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>           | <span data-ttu-id="0e274-129">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="0e274-129">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="0e274-130"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="0e274-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="0e274-131">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="0e274-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="0e274-132">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0e274-132">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="0e274-133"><dt>**FVE \_ \_Protecteur E \_ \_ introuvable**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="0e274-133"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="0e274-134">Le protecteur de clé fourni n’existe pas sur le volume.</span><span class="sxs-lookup"><span data-stu-id="0e274-134">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="0e274-135"><dt>**FVE \_ E \_ \_ \_ type de protecteur non valide**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="0e274-135"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="0e274-136">Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé du type « mot de passe numérique » ou « clé externe ».</span><span class="sxs-lookup"><span data-stu-id="0e274-136">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="0e274-137">Utilisez la méthode [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) ou [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) pour créer un protecteur de clé du type approprié.</span><span class="sxs-lookup"><span data-stu-id="0e274-137">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0e274-138">Notes</span><span class="sxs-lookup"><span data-stu-id="0e274-138">Remarks</span></span>

<span data-ttu-id="0e274-139">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="0e274-139">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0e274-140">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="0e274-140">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="0e274-141">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="0e274-141">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0e274-142">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="0e274-142">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e274-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e274-143">Requirements</span></span>



| <span data-ttu-id="0e274-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e274-144">Requirement</span></span> | <span data-ttu-id="0e274-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e274-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e274-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e274-146">Minimum supported client</span></span><br/> | <span data-ttu-id="0e274-147">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e274-147">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0e274-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0e274-148">Minimum supported server</span></span><br/> | <span data-ttu-id="0e274-149">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0e274-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0e274-150">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0e274-150">Namespace</span></span><br/>                | <span data-ttu-id="0e274-151">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="0e274-151">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="0e274-152">MOF</span><span class="sxs-lookup"><span data-stu-id="0e274-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e274-153"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0e274-153"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e274-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e274-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e274-155">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="0e274-155">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
