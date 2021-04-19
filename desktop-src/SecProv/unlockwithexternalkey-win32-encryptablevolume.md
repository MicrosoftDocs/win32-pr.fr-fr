---
description: Utilise une clé externe fournie pour accéder au contenu d’un volume de données.
ms.assetid: e383767e-8557-469c-bc44-f67591c46f23
title: Méthode UnlockWithExternalKey de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 4b599f098856937ae5610156cba96a1deea1f64b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536613"
---
# <a name="unlockwithexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="87269-103">Méthode UnlockWithExternalKey de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="87269-103">UnlockWithExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="87269-104">La méthode **UnlockWithExternalKey** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) utilise une clé externe fournie pour accéder au contenu d’un volume de données.</span><span class="sxs-lookup"><span data-stu-id="87269-104">The **UnlockWithExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses a provided external key to access the contents of a data volume.</span></span>

<span data-ttu-id="87269-105">La clé de chiffrement du volume doit avoir été sécurisée avec un ou plusieurs protecteurs de clé du type « clé externe » à l’aide de la méthode [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) pour pouvoir déverrouiller le volume avec cette méthode.</span><span class="sxs-lookup"><span data-stu-id="87269-105">The volume's encryption key must have been secured with one or more key protectors of the type "External Key" using the [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to be able to unlock the volume with this method.</span></span>

> [!Note]  
> <span data-ttu-id="87269-106">Si le disque prend en charge le chiffrement matériel, cette fonction définit l’état de la bande sur « déverrouillé ».</span><span class="sxs-lookup"><span data-stu-id="87269-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="87269-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87269-107">Syntax</span></span>


```mof
uint32 UnlockWithExternalKey(
  [in] uint8 ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="87269-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87269-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87269-109">*ExternalKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="87269-109">*ExternalKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87269-110">Type : **UInt8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="87269-110">Type: **uint8\[\]**</span></span>

<span data-ttu-id="87269-111">Tableau d’octets qui spécifie la clé externe 256 bits utilisée pour déverrouiller le volume.</span><span class="sxs-lookup"><span data-stu-id="87269-111">An array of bytes that specifies the 256-bit external key used to unlock the volume.</span></span> <span data-ttu-id="87269-112">Cette clé peut être obtenue en appelant la méthode [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="87269-112">This key can be obtained by calling the [**GetExternalKeyFromFile**](getexternalkeyfromfile-win32-encryptablevolume.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87269-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="87269-113">Return value</span></span>

<span data-ttu-id="87269-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87269-114">Type: **uint32**</span></span>

<span data-ttu-id="87269-115">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="87269-115">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="87269-116">Si le volume est déjà déverrouillé, cette méthode retourne 0.</span><span class="sxs-lookup"><span data-stu-id="87269-116">If the volume is already unlocked, this method returns 0.</span></span>



| <span data-ttu-id="87269-117">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="87269-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="87269-118">Description</span><span class="sxs-lookup"><span data-stu-id="87269-118">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="87269-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="87269-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="87269-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="87269-120">The method was successful.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="87269-121"><dt>**Erreur \_ Aucune valeur donnée n' \_ a été trouvée**</dt> <dt>(0x)</dt></span><span class="sxs-lookup"><span data-stu-id="87269-121"><dt>**ERROR\_NOT\_FOUND**</dt> <dt>No value given (0x)</dt></span></span> </dl>          | <span data-ttu-id="87269-122">Le volume n’a pas de protecteur de clé du type « clé externe ».</span><span class="sxs-lookup"><span data-stu-id="87269-122">The volume does not have a key protector of the type "External Key".</span></span><br/>                                                             |
| <dl> <span data-ttu-id="87269-123"><dt>**Erreur \_ \_Mot de passe non valide**</dt> - <dt>aucune valeur donnée (0x)</dt></span><span class="sxs-lookup"><span data-stu-id="87269-123"><dt>**ERROR\_INVALID\_PASSWORD**</dt> <dt>No value given (0x)</dt></span></span> </dl>   | <span data-ttu-id="87269-124">Un ou plusieurs protecteurs de clé du type « clé externe » existent, mais le paramètre *ExternalKey* spécifié ne peut pas déverrouiller le volume.</span><span class="sxs-lookup"><span data-stu-id="87269-124">One or more key protectors of the type "External Key" exist, but the specified *ExternalKey* parameter cannot unlock the volume.</span></span><br/> |
| <dl> <span data-ttu-id="87269-125"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="87269-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="87269-126">Le paramètre *ExternalKey* n’est pas un tableau de taille 4.</span><span class="sxs-lookup"><span data-stu-id="87269-126">The *ExternalKey* parameter is not an array of size 4.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="87269-127"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="87269-127"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="87269-128">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="87269-128">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="87269-129">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="87269-129">Add a key protector to enable BitLocker.</span></span> <br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="87269-130">Notes</span><span class="sxs-lookup"><span data-stu-id="87269-130">Remarks</span></span>

<span data-ttu-id="87269-131">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="87269-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="87269-132">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="87269-132">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="87269-133">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="87269-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="87269-134">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="87269-134">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87269-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87269-135">Requirements</span></span>



| <span data-ttu-id="87269-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87269-136">Requirement</span></span> | <span data-ttu-id="87269-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="87269-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87269-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87269-138">Minimum supported client</span></span><br/> | <span data-ttu-id="87269-139">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87269-139">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="87269-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87269-140">Minimum supported server</span></span><br/> | <span data-ttu-id="87269-141">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="87269-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="87269-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="87269-142">Namespace</span></span><br/>                | <span data-ttu-id="87269-143">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="87269-143">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="87269-144">MOF</span><span class="sxs-lookup"><span data-stu-id="87269-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87269-145"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87269-145"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87269-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87269-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87269-147">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="87269-147">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
