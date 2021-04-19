---
description: Écrit la clé externe associée au protecteur de clé de volume spécifié dans un fichier système, masqué et en lecture seule dans le dossier spécifié.
ms.assetid: 8d928f85-b392-4119-aebb-f16021eb5c6a
title: Méthode SaveExternalKeyToFile de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SaveExternalKeyToFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 879536940ff36a005e1936dffcd7821fff585a65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529306"
---
# <a name="saveexternalkeytofile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="856c6-103">Méthode SaveExternalKeyToFile de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="856c6-103">SaveExternalKeyToFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="856c6-104">La méthode **SaveExternalKeyToFile** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) écrit la clé externe associée au protecteur de clé de volume spécifié dans un fichier système, masqué et en lecture seule dans le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="856c6-104">The **SaveExternalKeyToFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class writes the external key associated with the specified volume key protector to a system, hidden, read-only file in the specified folder.</span></span>

<span data-ttu-id="856c6-105">Cette méthode s’applique uniquement aux protecteurs de clés du type « clé externe » ou « TPM et clé de démarrage ».</span><span class="sxs-lookup"><span data-stu-id="856c6-105">This method is only applicable for key protectors of the type "External Key" or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="856c6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="856c6-106">Syntax</span></span>


```mof
uint32 SaveExternalKeyToFile(
  [in] string VolumeKeyProtectorID,
  [in] string Path
);
```



## <a name="parameters"></a><span data-ttu-id="856c6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="856c6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="856c6-108">*VolumeKeyProtectorID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="856c6-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="856c6-109">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="856c6-109">Type: **string**</span></span>

<span data-ttu-id="856c6-110">Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="856c6-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="856c6-111">*Chemin d’accès* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="856c6-111">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="856c6-112">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="856c6-112">Type: **string**</span></span>

<span data-ttu-id="856c6-113">Chaîne qui contient l’emplacement du volume ou du dossier où la clé externe associée au protecteur de clé spécifié doit être enregistrée.</span><span class="sxs-lookup"><span data-stu-id="856c6-113">A string that contains the volume or folder location where the external key associated with the specified key protector is to be saved.</span></span> <span data-ttu-id="856c6-114">Ce chemin d’accès n’inclut pas le nom du fichier, qui est interne et peut changer d’une version à l’autres.</span><span class="sxs-lookup"><span data-stu-id="856c6-114">This path does not include the name of the file, which is internal and may change from version to version.</span></span> <span data-ttu-id="856c6-115">Utilisez **GetExternalKeyFileName** pour récupérer le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="856c6-115">Use **GetExternalKeyFileName** to get the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="856c6-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="856c6-116">Return value</span></span>

<span data-ttu-id="856c6-117">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="856c6-117">Type: **uint32**</span></span>

<span data-ttu-id="856c6-118">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="856c6-118">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="856c6-119">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="856c6-119">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="856c6-120">Description</span><span class="sxs-lookup"><span data-stu-id="856c6-120">Description</span></span>                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="856c6-121"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="856c6-121"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="856c6-122">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="856c6-122">The method was successful.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="856c6-123"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="856c6-123"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>  | <span data-ttu-id="856c6-124">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="856c6-124">The volume is locked.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="856c6-125"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="856c6-125"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>           | <span data-ttu-id="856c6-126">Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé du type « clé externe » ou « TPM et clé de démarrage ».</span><span class="sxs-lookup"><span data-stu-id="856c6-126">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key" or "TPM And Startup Key".</span></span><br/>            |
| <dl> <span data-ttu-id="856c6-127"><dt>**Erreur \_ Chemin d’accès \_ \_ introuvable**</dt> <dt>2147942403 (0x80070003)</dt></span><span class="sxs-lookup"><span data-stu-id="856c6-127"><dt>**ERROR\_PATH\_NOT\_FOUND**</dt> <dt>2147942403 (0x80070003)</dt></span></span> </dl> | <span data-ttu-id="856c6-128">Le paramètre *path* ne fait pas référence à un emplacement valide.</span><span class="sxs-lookup"><span data-stu-id="856c6-128">The *Path* parameter does not refer to a valid location.</span></span><br/> <span data-ttu-id="856c6-129">Assurez-vous que le nom de fichier n’est pas inclus dans le paramètre *path* .</span><span class="sxs-lookup"><span data-stu-id="856c6-129">Ensure that the file name is not included in the *Path* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="856c6-130"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="856c6-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>  | <span data-ttu-id="856c6-131">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="856c6-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="856c6-132">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="856c6-132">Add a key protector to enable BitLocker.</span></span> <br/>                                                      |



 

## <a name="remarks"></a><span data-ttu-id="856c6-133">Notes</span><span class="sxs-lookup"><span data-stu-id="856c6-133">Remarks</span></span>

<span data-ttu-id="856c6-134">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="856c6-134">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="856c6-135">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="856c6-135">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="856c6-136">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="856c6-136">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="856c6-137">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="856c6-137">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="856c6-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="856c6-138">Requirements</span></span>



| <span data-ttu-id="856c6-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="856c6-139">Requirement</span></span> | <span data-ttu-id="856c6-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="856c6-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="856c6-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="856c6-141">Minimum supported client</span></span><br/> | <span data-ttu-id="856c6-142">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="856c6-142">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="856c6-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="856c6-143">Minimum supported server</span></span><br/> | <span data-ttu-id="856c6-144">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="856c6-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="856c6-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="856c6-145">Namespace</span></span><br/>                | <span data-ttu-id="856c6-146">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="856c6-146">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="856c6-147">MOF</span><span class="sxs-lookup"><span data-stu-id="856c6-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="856c6-148"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="856c6-148"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="856c6-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="856c6-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="856c6-150">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="856c6-150">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
