---
description: Retourne la chaîne d’identificateur disponible dans les métadonnées du volume.
ms.assetid: 0573cbcd-6fb1-4648-bb06-4433796f6bb5
title: Méthode GetIdentificationField de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: bb70f76d9556df5bed70639471eb7a0f3afaaecc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112638"
---
# <a name="getidentificationfield-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="86ab3-103">Méthode GetIdentificationField de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="86ab3-103">GetIdentificationField method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="86ab3-104">La méthode **GetIdentificationField** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) retourne la chaîne d’identificateur disponible dans les métadonnées du volume.</span><span class="sxs-lookup"><span data-stu-id="86ab3-104">The **GetIdentificationField** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the identifier string available in the volume's metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="86ab3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="86ab3-105">Syntax</span></span>


```mof
uint32 GetIdentificationField(
  [out] string IdentificationField
);
```



## <a name="parameters"></a><span data-ttu-id="86ab3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="86ab3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86ab3-107">*IdentificationField* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="86ab3-107">*IdentificationField* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86ab3-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="86ab3-108">Type: **string**</span></span>

<span data-ttu-id="86ab3-109">Chaîne qui spécifie le champ d’identification affecté au volume.</span><span class="sxs-lookup"><span data-stu-id="86ab3-109">A string that specifies the identification field that is assigned to the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86ab3-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="86ab3-110">Return value</span></span>

<span data-ttu-id="86ab3-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="86ab3-111">Type: **uint32**</span></span>

<span data-ttu-id="86ab3-112">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="86ab3-112">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="86ab3-113">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="86ab3-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="86ab3-114">Description</span><span class="sxs-lookup"><span data-stu-id="86ab3-114">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="86ab3-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="86ab3-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="86ab3-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="86ab3-116">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="86ab3-117"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="86ab3-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="86ab3-118">Ce lecteur est verrouillé par Chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="86ab3-118">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="86ab3-119">Vous devez déverrouiller ce volume à partir du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="86ab3-119">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="86ab3-120"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="86ab3-120"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="86ab3-121">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="86ab3-121">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="86ab3-122">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="86ab3-122">Add a key protector to enable BitLocker.</span></span> <br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="86ab3-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="86ab3-123">Requirements</span></span>



| <span data-ttu-id="86ab3-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="86ab3-124">Requirement</span></span> | <span data-ttu-id="86ab3-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="86ab3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86ab3-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86ab3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="86ab3-127">Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86ab3-127">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="86ab3-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="86ab3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="86ab3-129">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="86ab3-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="86ab3-130">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="86ab3-130">Namespace</span></span><br/>                | <span data-ttu-id="86ab3-131">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="86ab3-131">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="86ab3-132">MOF</span><span class="sxs-lookup"><span data-stu-id="86ab3-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="86ab3-133"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="86ab3-133"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86ab3-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="86ab3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86ab3-135">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="86ab3-135">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




