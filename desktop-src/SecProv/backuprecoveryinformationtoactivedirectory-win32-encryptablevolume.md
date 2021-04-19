---
description: Sauvegarde les données de récupération dans Active Directory.
ms.assetid: 664562b3-5679-4185-8bbc-5d5350494707
title: Méthode BackupRecoveryInformationToActiveDirectory de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.BackupRecoveryInformationToActiveDirectory
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a04901139aa46f42e06eaea1c91af0e3bac202e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545152"
---
# <a name="backuprecoveryinformationtoactivedirectory-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="0d78e-103">Méthode BackupRecoveryInformationToActiveDirectory de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="0d78e-103">BackupRecoveryInformationToActiveDirectory method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="0d78e-104">La méthode **BackupRecoveryInformationToActiveDirectory** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) sauvegarde les données de récupération dans Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0d78e-104">The **BackupRecoveryInformationToActiveDirectory** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class backs up recovery data to Active Directory.</span></span> <span data-ttu-id="0d78e-105">Cette méthode nécessite la présence d’un protecteur de mot de passe numérique sur le volume.</span><span class="sxs-lookup"><span data-stu-id="0d78e-105">This method requires a numerical password protector to be present on the volume.</span></span> <span data-ttu-id="0d78e-106">Stratégie de groupe doit également être configuré pour permettre la sauvegarde des informations de récupération sur Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0d78e-106">Group Policy must also be configured to enable backup of recovery information to Active Directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d78e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d78e-107">Syntax</span></span>


```mof
uint32 BackupRecoveryInformationToActiveDirectory(
  [in] string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="0d78e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d78e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d78e-109">*VolumeKeyProtectorID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0d78e-109">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d78e-110">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="0d78e-110">Type: **string**</span></span>

<span data-ttu-id="0d78e-111">Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="0d78e-111">A unique string identifier used to manage an encrypted volume key protector.</span></span> <span data-ttu-id="0d78e-112">Ce protecteur de clé doit être un protecteur de mot de passe numérique.</span><span class="sxs-lookup"><span data-stu-id="0d78e-112">This key protector must be a numerical password protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d78e-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0d78e-113">Return value</span></span>

<span data-ttu-id="0d78e-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d78e-114">Type: **uint32**</span></span>

<span data-ttu-id="0d78e-115">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="0d78e-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="0d78e-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="0d78e-116">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="0d78e-117">Description</span><span class="sxs-lookup"><span data-stu-id="0d78e-117">Description</span></span>                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0d78e-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0d78e-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="0d78e-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="0d78e-119">The method was successful.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="0d78e-120"><dt>**S \_ FALSe**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0d78e-120"><dt>**S\_FALSE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                                         | <span data-ttu-id="0d78e-121">Stratégie de groupe n’autorise pas le stockage des informations de récupération à Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0d78e-121">Group Policy does not permit the storage of recovery information to Active Directory.</span></span><br/>                         |
| <dl> <span data-ttu-id="0d78e-122"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="0d78e-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="0d78e-123">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="0d78e-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="0d78e-124">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="0d78e-124">Add a key protector to enable BitLocker.</span></span> <br/>                             |
| <dl> <span data-ttu-id="0d78e-125"><dt>**FVE \_ E \_ \_ \_ type de protecteur non valide**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="0d78e-125"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="0d78e-126">Le protecteur de clé spécifié n’est pas un protecteur de clé numérique.</span><span class="sxs-lookup"><span data-stu-id="0d78e-126">The specified key protector is not a numerical key protector.</span></span> <span data-ttu-id="0d78e-127">Vous devez entrer un protecteur de mot de passe numérique.</span><span class="sxs-lookup"><span data-stu-id="0d78e-127">You must enter a numerical password protector.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="0d78e-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d78e-128">Requirements</span></span>



| <span data-ttu-id="0d78e-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d78e-129">Requirement</span></span> | <span data-ttu-id="0d78e-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d78e-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d78e-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d78e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0d78e-132">Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d78e-132">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0d78e-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d78e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0d78e-134">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0d78e-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="0d78e-135">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="0d78e-135">Namespace</span></span><br/>                | <span data-ttu-id="0d78e-136">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="0d78e-136">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="0d78e-137">MOF</span><span class="sxs-lookup"><span data-stu-id="0d78e-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d78e-138"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d78e-138"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d78e-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d78e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d78e-140">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="0d78e-140">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




