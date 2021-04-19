---
description: Utilise la phrase secrète pour obtenir la clé dérivée.
ms.assetid: 09b4ae7f-7084-42bd-8bbe-da686d6280e9
title: Méthode UnlockWithPassphrase de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithPassphrase
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 75c5522a0781b1cd229bf97d2549433a426fbfc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521376"
---
# <a name="unlockwithpassphrase-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="8ead6-103">Méthode UnlockWithPassphrase de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="8ead6-103">UnlockWithPassphrase method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="8ead6-104">La méthode **UnlockWithPassphrase** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) utilise la phrase secrète pour obtenir la clé dérivée.</span><span class="sxs-lookup"><span data-stu-id="8ead6-104">The **UnlockWithPassphrase** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the passphrase to obtain the derived key.</span></span> <span data-ttu-id="8ead6-105">Une fois la clé dérivée calculée, la clé dérivée est utilisée pour déverrouiller la clé principale du volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="8ead6-105">After the derived key is calculated, the derived key is used to unlock the encrypted volume's master key.</span></span>

> [!Note]  
> <span data-ttu-id="8ead6-106">Si le disque prend en charge le chiffrement matériel, cette fonction définit l’état de la bande sur « déverrouillé ».</span><span class="sxs-lookup"><span data-stu-id="8ead6-106">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8ead6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8ead6-107">Syntax</span></span>


```mof
uint32 UnlockWithPassphrase(
  [in] string Passphrase
);
```



## <a name="parameters"></a><span data-ttu-id="8ead6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8ead6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ead6-109">*Phrase secrète* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8ead6-109">*Passphrase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ead6-110">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="8ead6-110">Type: **string**</span></span>

<span data-ttu-id="8ead6-111">Chaîne qui spécifie la phrase secrète.</span><span class="sxs-lookup"><span data-stu-id="8ead6-111">A string that specifies the passphrase.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ead6-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8ead6-112">Return value</span></span>

<span data-ttu-id="8ead6-113">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ead6-113">Type: **uint32**</span></span>

<span data-ttu-id="8ead6-114">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="8ead6-114">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="8ead6-115">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8ead6-115">Return code/value</span></span>                                                                                                                                                                                       | <span data-ttu-id="8ead6-116">Description</span><span class="sxs-lookup"><span data-stu-id="8ead6-116">Description</span></span>                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ead6-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8ead6-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                       | <span data-ttu-id="8ead6-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="8ead6-118">The method was successful.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="8ead6-119"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="8ead6-119"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>                      | <span data-ttu-id="8ead6-120">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="8ead6-120">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="8ead6-121">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="8ead6-121">Add a key protector to enable BitLocker.</span></span> <br/>                              |
| <dl> <span data-ttu-id="8ead6-122"><dt>**FVE \_ E \_ FIPS \_ empêche la \_ phrase secrète**</dt> <dt>2150695020 (0x8031006C)</dt></span><span class="sxs-lookup"><span data-stu-id="8ead6-122"><dt>**FVE\_E\_FIPS\_PREVENTS\_PASSPHRASE**</dt> <dt>2150695020 (0x8031006C)</dt></span></span> </dl>          | <span data-ttu-id="8ead6-123">Le paramètre de stratégie de groupe qui requiert la conformité FIPS a empêché la création ou l’utilisation de la phrase secrète.</span><span class="sxs-lookup"><span data-stu-id="8ead6-123">The group policy setting that requires FIPS compliance prevented the passphrase from being generated or used.</span></span> <br/> |
| <dl> <span data-ttu-id="8ead6-124"><dt>**FVE \_ \_Longueur de \_ la \_ phrase \_ secrète non valide de la stratégie E**</dt> <dt>2150695040 (0x80310080)</dt></span><span class="sxs-lookup"><span data-stu-id="8ead6-124"><dt>**FVE\_E\_POLICY\_INVALID\_PASSPHRASE\_LENGTH**</dt> <dt>2150695040 (0x80310080)</dt></span></span> </dl> | <span data-ttu-id="8ead6-125">La phrase secrète fournie ne répond pas aux exigences de longueur minimale ou maximale.</span><span class="sxs-lookup"><span data-stu-id="8ead6-125">The passphrase provided does not meet the minimum or maximum length requirements.</span></span><br/>                              |
| <dl> <span data-ttu-id="8ead6-126"><dt>**FVE \_ \_Phrase secrète de la stratégie E \_ \_ trop \_ simple**</dt> <dt>2150695041 (0x80310081)</dt></span><span class="sxs-lookup"><span data-stu-id="8ead6-126"><dt>**FVE\_E\_POLICY\_PASSPHRASE\_TOO\_SIMPLE**</dt> <dt>2150695041 (0x80310081)</dt></span></span> </dl>     | <span data-ttu-id="8ead6-127">La phrase secrète ne respecte pas les exigences de complexité définies par l’administrateur dans la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="8ead6-127">The passphrase does not meet the complexity requirements set by the administrator in group policy.</span></span><br/>             |
| <dl> <span data-ttu-id="8ead6-128"><dt>**FVE \_ E \_ échec de \_ l’authentification**</dt> <dt>2150694951 (0x80310027)</dt></span><span class="sxs-lookup"><span data-stu-id="8ead6-128"><dt>**FVE\_E\_FAILED\_AUTHENTICATION**</dt> <dt>2150694951 (0x80310027)</dt></span></span> </dl>              | <span data-ttu-id="8ead6-129">Le volume ne peut pas être déverrouillé avec les informations fournies.</span><span class="sxs-lookup"><span data-stu-id="8ead6-129">The volume cannot be unlocked with the provided information.</span></span> <br/>                                                  |
| <dl> <span data-ttu-id="8ead6-130"><dt>**FVE \_ \_Protecteur E \_ \_ introuvable**</dt> <dt>2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="8ead6-130"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>               | <span data-ttu-id="8ead6-131">Le protecteur de clé fourni n’existe pas sur le volume.</span><span class="sxs-lookup"><span data-stu-id="8ead6-131">The provided key protector does not exist on the volume.</span></span> <span data-ttu-id="8ead6-132">Vous devez entrer un autre protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="8ead6-132">You must enter another key protector.</span></span><br/>                 |



 

## <a name="requirements"></a><span data-ttu-id="8ead6-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ead6-133">Requirements</span></span>



| <span data-ttu-id="8ead6-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ead6-134">Requirement</span></span> | <span data-ttu-id="8ead6-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ead6-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ead6-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ead6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="8ead6-137">Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ead6-137">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8ead6-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ead6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="8ead6-139">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ead6-139">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="8ead6-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="8ead6-140">Namespace</span></span><br/>                | <span data-ttu-id="8ead6-141">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="8ead6-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="8ead6-142">MOF</span><span class="sxs-lookup"><span data-stu-id="8ead6-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ead6-143"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ead6-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ead6-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ead6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ead6-145">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="8ead6-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




