---
description: Crée un volume BitLocker avec le type de système de fichiers spécifié du volume de détection.
ms.assetid: 088e7224-a336-4742-a12f-86755defe16c
title: Méthode PrepareVolume de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PrepareVolume
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 918e4289f8f2c38af2a4a51bfe92f82a74b30b22
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112634"
---
# <a name="preparevolume-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="1c0d4-103">Méthode PrepareVolume de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="1c0d4-103">PrepareVolume method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="1c0d4-104">La méthode **PrepareVolume** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) crée un volume BitLocker avec le type de système de fichiers spécifié du volume de détection.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-104">The **PrepareVolume** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class creates a BitLocker volume with the specified file system type of the discovery volume.</span></span> <span data-ttu-id="1c0d4-105">Cette méthode doit être appelée pour que le volume puisse être protégé avec l’une des méthodes \**ProtectKeyWith \** _.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-105">This method must be called before the volume can be protected with any of the \**ProtectKeyWith\** _ methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c0d4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1c0d4-106">Syntax</span></span>

```mof
uint32 PrepareVolume(
  [in] string DiscoveryVolumeType,
  [in] uint32 ForceEncryptionType
);
```

## <a name="parameters"></a><span data-ttu-id="1c0d4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1c0d4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c0d4-108">_DiscoveryVolumeType \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c0d4-108">_DiscoveryVolumeType\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c0d4-109">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1c0d4-109">Type: **string**</span></span>

<span data-ttu-id="1c0d4-110">Chaîne qui spécifie le type de volume de détection.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-110">A string that specifies the type of discovery volume.</span></span>

| <span data-ttu-id="1c0d4-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c0d4-111">Value</span></span>               | <span data-ttu-id="1c0d4-112">Signification</span><span class="sxs-lookup"><span data-stu-id="1c0d4-112">Meaning</span></span>                                                            |
|---------------------|--------------------------------------------------------------------|
| <span data-ttu-id="1c0d4-113">**&lt;None&gt;**</span><span class="sxs-lookup"><span data-stu-id="1c0d4-113">**&lt;none&gt;**</span></span>    | <span data-ttu-id="1c0d4-114">Aucun volume de détection.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-114">No discovery volume.</span></span> <span data-ttu-id="1c0d4-115">Cette valeur crée un volume BitLocker natif.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-115">This value creates a native BitLocker volume.</span></span> |
| <span data-ttu-id="1c0d4-116">**&lt;default&gt;**</span><span class="sxs-lookup"><span data-stu-id="1c0d4-116">**&lt;default&gt;**</span></span> | <span data-ttu-id="1c0d4-117">Cette valeur est le comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-117">This value is the default behavior.</span></span>                                |
| <span data-ttu-id="1c0d4-118">**FAT32**</span><span class="sxs-lookup"><span data-stu-id="1c0d4-118">**FAT32**</span></span>           | <span data-ttu-id="1c0d4-119">Cette valeur crée un volume de détection FAT32.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-119">This value creates a FAT32 discovery volume.</span></span>                       |

</dd> <dt>

<span data-ttu-id="1c0d4-120">*ForceEncryptionType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1c0d4-120">*ForceEncryptionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c0d4-121">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c0d4-121">Type: **uint32**</span></span>

<span data-ttu-id="1c0d4-122">Entier qui spécifie le type de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-122">Integer that specifies the encryption type.</span></span> <span data-ttu-id="1c0d4-123">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-123">This can be one of the following values.</span></span>

| <span data-ttu-id="1c0d4-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c0d4-124">Value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="1c0d4-125">Signification</span><span class="sxs-lookup"><span data-stu-id="1c0d4-125">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span><dl> <span data-ttu-id="1c0d4-126"><dt>0</dt> <dt>**non spécifié**</dt></span><span class="sxs-lookup"><span data-stu-id="1c0d4-126"><dt>**Unspecified**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="1c0d4-127">Le type de chiffrement n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-127">The encryption type is not specified.</span></span><br/> |
| <span id="Software"></span><span id="software"></span><span id="SOFTWARE"></span><dl> <span data-ttu-id="1c0d4-128"><dt>**Logiciel**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1c0d4-128"><dt>**Software**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="1c0d4-129">Chiffrement logiciel.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-129">Software encryption.</span></span><br/>                  |
| <span id="Hardware"></span><span id="hardware"></span><span id="HARDWARE"></span><dl> <span data-ttu-id="1c0d4-130"><dt>**Matériel**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1c0d4-130"><dt>**Hardware**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="1c0d4-131">Chiffrement matériel.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-131">Hardware encryption.</span></span><br/>                  |

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c0d4-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1c0d4-132">Return value</span></span>

<span data-ttu-id="1c0d4-133">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c0d4-133">Type: **uint32**</span></span>

<span data-ttu-id="1c0d4-134">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-134">This method returns one of the following codes or another error code if it fails.</span></span>

| <span data-ttu-id="1c0d4-135">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="1c0d4-135">Return code/value</span></span>      | <span data-ttu-id="1c0d4-136">Description</span><span class="sxs-lookup"><span data-stu-id="1c0d4-136">Description</span></span>                     |
|------------------------|---------------------------------|
| <span data-ttu-id="1c0d4-137">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="1c0d4-137">**S_OK**</span></span> <br/> <span data-ttu-id="1c0d4-138">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="1c0d4-138">0 (0x0)</span></span> | <span data-ttu-id="1c0d4-139">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="1c0d4-139">The method was successful.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="1c0d4-140">Notes</span><span class="sxs-lookup"><span data-stu-id="1c0d4-140">Remarks</span></span>

<span data-ttu-id="1c0d4-141">Si vous n’appelez pas cette méthode lors de l’activation d’un volume BitLocker, elle revient à appeler cette méthode avec la valeur par défaut dans le paramètre *DiscoveryVolumeType* .</span><span class="sxs-lookup"><span data-stu-id="1c0d4-141">If you do not call this method when enabling a BitLocker volume, it is the same as calling this method with the default value in the *DiscoveryVolumeType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c0d4-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1c0d4-142">Requirements</span></span>

| <span data-ttu-id="1c0d4-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1c0d4-143">Requirement</span></span> | <span data-ttu-id="1c0d4-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="1c0d4-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c0d4-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c0d4-145">Minimum supported client</span></span><br/> | <span data-ttu-id="1c0d4-146">Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c0d4-146">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1c0d4-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1c0d4-147">Minimum supported server</span></span><br/> | <span data-ttu-id="1c0d4-148">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1c0d4-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="1c0d4-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="1c0d4-149">Namespace</span></span><br/>                | <span data-ttu-id="1c0d4-150">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="1c0d4-150">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="1c0d4-151">MOF</span><span class="sxs-lookup"><span data-stu-id="1c0d4-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c0d4-152"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c0d4-152"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="1c0d4-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c0d4-153">See also</span></span>

[<span data-ttu-id="1c0d4-154">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="1c0d4-154">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
