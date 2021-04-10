---
description: Définit la chaîne d’identificateur spécifiée dans les métadonnées du volume.
ms.assetid: 21355669-2052-4e7a-9c9d-aaa67533dd5e
title: Méthode SetIdentificationField de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.SetIdentificationField
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e8405be7aef91571bd3bd5d7dcb97214dcdfdb4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868190"
---
# <a name="setidentificationfield-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="36f0b-103">Méthode SetIdentificationField de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="36f0b-103">SetIdentificationField method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="36f0b-104">La méthode **SetIdentificationField** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) définit la chaîne d’identificateur spécifiée dans les métadonnées du volume.</span><span class="sxs-lookup"><span data-stu-id="36f0b-104">The **SetIdentificationField** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class sets the specified identifier string in the volume's metadata.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f0b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36f0b-105">Syntax</span></span>


```mof
uint32 SetIdentificationField(
  [in, optional] string IdentificationField
);
```



## <a name="parameters"></a><span data-ttu-id="36f0b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36f0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36f0b-107">*IdentificationField* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="36f0b-107">*IdentificationField* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="36f0b-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="36f0b-108">Type: **string**</span></span>

<span data-ttu-id="36f0b-109">Chaîne qui spécifie le champ d’identification affecté au volume.</span><span class="sxs-lookup"><span data-stu-id="36f0b-109">A string that specifies the identification field that is assigned to the volume.</span></span> <span data-ttu-id="36f0b-110">Si la chaîne facultative est absente, les valeurs du jeu de Registre sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="36f0b-110">If the optional string is not present, the registry set values are used.</span></span> <span data-ttu-id="36f0b-111">Si la chaîne est présente et n’est pas vide, la valeur spécifiée est utilisée.</span><span class="sxs-lookup"><span data-stu-id="36f0b-111">If the string is present and not empty, the specified value is used.</span></span> <span data-ttu-id="36f0b-112">Le paramètre *IdentificationField* n’est pas sensible à la casse.</span><span class="sxs-lookup"><span data-stu-id="36f0b-112">The *IdentificationField* parameter is not case-sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36f0b-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36f0b-113">Return value</span></span>

<span data-ttu-id="36f0b-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="36f0b-114">Type: **uint32**</span></span>

<span data-ttu-id="36f0b-115">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="36f0b-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="36f0b-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="36f0b-116">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="36f0b-117">Description</span><span class="sxs-lookup"><span data-stu-id="36f0b-117">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="36f0b-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="36f0b-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="36f0b-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="36f0b-119">The method was successful.</span></span><br/>                                                                           |
| <dl> <span data-ttu-id="36f0b-120"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="36f0b-120"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="36f0b-121">Ce lecteur est verrouillé par Chiffrement de lecteur BitLocker.</span><span class="sxs-lookup"><span data-stu-id="36f0b-121">This drive is locked by BitLocker Drive Encryption.</span></span> <span data-ttu-id="36f0b-122">Vous devez déverrouiller ce volume à partir du panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="36f0b-122">You must unlock this volume from Control Panel.</span></span> <br/> |
| <dl> <span data-ttu-id="36f0b-123"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="36f0b-123"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="36f0b-124">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="36f0b-124">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="36f0b-125">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="36f0b-125">Add a key protector to enable BitLocker.</span></span> <br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="36f0b-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36f0b-126">Requirements</span></span>



| <span data-ttu-id="36f0b-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36f0b-127">Requirement</span></span> | <span data-ttu-id="36f0b-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="36f0b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36f0b-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36f0b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="36f0b-130">Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36f0b-130">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="36f0b-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36f0b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="36f0b-132">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="36f0b-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="36f0b-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="36f0b-133">Namespace</span></span><br/>                | <span data-ttu-id="36f0b-134">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="36f0b-134">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="36f0b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="36f0b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="36f0b-136"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="36f0b-136"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36f0b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36f0b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f0b-138">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="36f0b-138">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




