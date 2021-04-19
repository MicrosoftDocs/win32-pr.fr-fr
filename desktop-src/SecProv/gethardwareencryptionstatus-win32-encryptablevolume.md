---
description: Détermine si le volume se trouve sur un lecteur qui prend en charge ou peut prendre en charge le chiffrement matériel.
ms.assetid: C6007BC4-71CD-404A-A0E9-D9662906151F
title: Méthode GetHardwareEncryptionStatus de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareEncryptionStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 2f48bb7115d19779f437a849078238cee967f2d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516633"
---
# <a name="gethardwareencryptionstatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="136ef-103">Méthode GetHardwareEncryptionStatus de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="136ef-103">GetHardwareEncryptionStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="136ef-104">La méthode **GetHardwareEncryptionStatus** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) détermine si le volume se trouve sur un lecteur qui prend en charge ou peut prendre en charge le chiffrement matériel.</span><span class="sxs-lookup"><span data-stu-id="136ef-104">The **GetHardwareEncryptionStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class determines whether the volume is located on a drive that supports or can support hardware encryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="136ef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="136ef-105">Syntax</span></span>


```mof
uint32 GetHardwareEncryptionStatus(
  [out] uint32 HardwareEncryptionStatus
);
```



## <a name="parameters"></a><span data-ttu-id="136ef-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="136ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="136ef-107">*HardwareEncryptionStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="136ef-107">*HardwareEncryptionStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="136ef-108">Spécifie si le lecteur peut prendre en charge le chiffrement matériel.</span><span class="sxs-lookup"><span data-stu-id="136ef-108">Specifies whether the drive can support hardware encryption.</span></span> <span data-ttu-id="136ef-109">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="136ef-109">This can be one of the following values.</span></span>



| <span data-ttu-id="136ef-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="136ef-110">Value</span></span>                                                                                                                                                                                                                                               | <span data-ttu-id="136ef-111">Signification</span><span class="sxs-lookup"><span data-stu-id="136ef-111">Meaning</span></span>                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="Not_supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span><dl> <span data-ttu-id="136ef-112"><dt>**Non pris en charge**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="136ef-112"><dt>**Not supported**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="136ef-113">Le chiffrement matériel n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="136ef-113">Hardware encryption is not supported.</span></span><br/>    |
| <span id="No_protection"></span><span id="no_protection"></span><span id="NO_PROTECTION"></span><dl> <span data-ttu-id="136ef-114"><dt>**Aucune protection**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="136ef-114"><dt>**No protection**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="136ef-115">Le chiffrement du lecteur n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="136ef-115">Drive encryption is not supported.</span></span><br/>       |
| <span id="Uses_software"></span><span id="uses_software"></span><span id="USES_SOFTWARE"></span><dl> <span data-ttu-id="136ef-116"><dt>**Utilise le logiciel**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="136ef-116"><dt>**Uses software**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="136ef-117">La méthode de chiffrement est basée sur logiciel.</span><span class="sxs-lookup"><span data-stu-id="136ef-117">The encryption method is software-based.</span></span><br/> |
| <span id="Uses_hardware"></span><span id="uses_hardware"></span><span id="USES_HARDWARE"></span><dl> <span data-ttu-id="136ef-118"><dt>**Utilise le matériel**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="136ef-118"><dt>**Uses hardware**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="136ef-119">Le lecteur prend en charge le chiffrement matériel.</span><span class="sxs-lookup"><span data-stu-id="136ef-119">The drive supports hardware encryption.</span></span><br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="136ef-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="136ef-120">Return value</span></span>

<span data-ttu-id="136ef-121">Cette fonction retourne la valeur zéro (0) si le volume est compatible avec le chiffrement matériel BitLocker.</span><span class="sxs-lookup"><span data-stu-id="136ef-121">This function returns zero (0) if the volume is compatible with BitLocker hardware encryption.</span></span> <span data-ttu-id="136ef-122">Dans le cas contraire, la fonction retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="136ef-122">Otherwise, the function returns an error.</span></span>



| <span data-ttu-id="136ef-123">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="136ef-123">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="136ef-124">Description</span><span class="sxs-lookup"><span data-stu-id="136ef-124">Description</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="136ef-125"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="136ef-125"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="136ef-126">Le volume est compatible avec le chiffrement matériel BitLocker.</span><span class="sxs-lookup"><span data-stu-id="136ef-126">The volume is compatible with BitLocker hardware encryption.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="136ef-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="136ef-127">Requirements</span></span>



| <span data-ttu-id="136ef-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="136ef-128">Requirement</span></span> | <span data-ttu-id="136ef-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="136ef-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="136ef-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="136ef-130">Minimum supported client</span></span><br/> | <span data-ttu-id="136ef-131">Windows 8 entreprise, applications de bureau Windows 8 professionnel \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="136ef-131">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="136ef-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="136ef-132">Minimum supported server</span></span><br/> | <span data-ttu-id="136ef-133">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="136ef-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="136ef-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="136ef-134">Namespace</span></span><br/>                | <span data-ttu-id="136ef-135">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="136ef-135">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="136ef-136">MOF</span><span class="sxs-lookup"><span data-stu-id="136ef-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="136ef-137"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="136ef-137"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="136ef-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="136ef-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="136ef-139">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="136ef-139">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




