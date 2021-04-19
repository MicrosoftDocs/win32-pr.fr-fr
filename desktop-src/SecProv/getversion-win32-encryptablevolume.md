---
description: Retourne la version des métadonnées FVE du volume.
ms.assetid: 21d5bf6d-c613-4200-b35c-1bad1ee72ec7
title: Méthode GetVersion de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetVersion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 25952c29b6db6db045fe839951d76994cc907b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544640"
---
# <a name="getversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c851b-103">Méthode GetVersion de la \_ classe EncryptableVolume Win32</span><span class="sxs-lookup"><span data-stu-id="c851b-103">GetVersion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c851b-104">La méthode **GetVersion** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) retourne la version de métadonnées FVE du volume.</span><span class="sxs-lookup"><span data-stu-id="c851b-104">The **GetVersion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the FVE metadata version of the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="c851b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c851b-105">Syntax</span></span>


```mof
uint32 GetVersion(
  [out] uint32 Version
);
```



## <a name="parameters"></a><span data-ttu-id="c851b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c851b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c851b-107">*Version* \[ de à\]</span><span class="sxs-lookup"><span data-stu-id="c851b-107">*Version* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c851b-108">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c851b-108">Type: **uint32**</span></span>

<span data-ttu-id="c851b-109">Entier non signé qui indique la version des métadonnées du volume.</span><span class="sxs-lookup"><span data-stu-id="c851b-109">An unsigned integer that indicates the metadata version of the volume.</span></span>



| <span data-ttu-id="c851b-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="c851b-110">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="c851b-111">Signification</span><span class="sxs-lookup"><span data-stu-id="c851b-111">Meaning</span></span>                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="c851b-112"><dt>**Inconnu**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c851b-112"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="c851b-113">Le système d’exploitation est inconnu.</span><span class="sxs-lookup"><span data-stu-id="c851b-113">The operating system is unknown.</span></span><br/>                                                                                                                                                                                               |
| <span id="Vista"></span><span id="vista"></span><span id="VISTA"></span><dl> <span data-ttu-id="c851b-114"><dt>**Vista**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c851b-114"><dt>**Vista**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="c851b-115">Format Windows Vista, ce qui signifie que le volume a été protégé avec BitLocker sur un ordinateur exécutant Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c851b-115">Windows Vista format, meaning that the volume was protected with BitLocker on a computer running Windows Vista.</span></span><br/>                                                                                                                |
| <span id="Win7"></span><span id="win7"></span><span id="WIN7"></span><dl> <span data-ttu-id="c851b-116"><dt>**Win7**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c851b-116"><dt>**Win7**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="c851b-117">Format Windows 7, ce qui signifie que le volume a été protégé avec BitLocker sur un ordinateur exécutant Windows 7 ou que le format des métadonnées a été mis à niveau à l’aide de la méthode [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="c851b-117">Windows 7 format, meaning that the volume was protected with BitLocker on a computer running Windows 7 or the metadata format was upgraded by using the [**UpgradeVolume**](upgradevolume-win32-encryptablevolume.md) method.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c851b-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c851b-118">Return value</span></span>

<span data-ttu-id="c851b-119">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c851b-119">Type: **uint32**</span></span>

<span data-ttu-id="c851b-120">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="c851b-120">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="c851b-121">Si le volume est déjà déverrouillé et qu’aucune autre erreur ne se produit, cette méthode retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="c851b-121">If the volume is already unlocked and no other errors occur, this method returns zero.</span></span>



| <span data-ttu-id="c851b-122">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c851b-122">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="c851b-123">Description</span><span class="sxs-lookup"><span data-stu-id="c851b-123">Description</span></span>                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="c851b-124"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c851b-124"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                       | <span data-ttu-id="c851b-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="c851b-125">The method succeeded.</span></span><br/>                               |
| <dl> <span data-ttu-id="c851b-126"><dt>**E \_ INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span><span class="sxs-lookup"><span data-stu-id="c851b-126"><dt>**E\_INVALIDARG**</dt> <dt>214794287 (0xCCD802F)</dt></span></span> </dl> | <span data-ttu-id="c851b-127">La valeur du paramètre de *version* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c851b-127">The value for the *Version* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="c851b-128"><dt>**Erreur \_ \_Données non valides**</dt> <dt>13 (0xD)</dt></span><span class="sxs-lookup"><span data-stu-id="c851b-128"><dt>**ERROR\_INVALID\_DATA**</dt> <dt>13 (0xD)</dt></span></span> </dl>       | <span data-ttu-id="c851b-129">Le pilote a renvoyé un format de données non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="c851b-129">The driver returned an unsupported data format.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="c851b-130">Notes</span><span class="sxs-lookup"><span data-stu-id="c851b-130">Remarks</span></span>

<span data-ttu-id="c851b-131">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c851b-131">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c851b-132">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="c851b-132">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c851b-133">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c851b-133">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c851b-134">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c851b-134">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c851b-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c851b-135">Requirements</span></span>



| <span data-ttu-id="c851b-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c851b-136">Requirement</span></span> | <span data-ttu-id="c851b-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="c851b-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c851b-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c851b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c851b-139">Windows 7 entreprise, les applications de bureau Windows 7 édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c851b-139">Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c851b-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c851b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c851b-141">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c851b-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c851b-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c851b-142">Namespace</span></span><br/>                | <span data-ttu-id="c851b-143">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="c851b-143">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c851b-144">MOF</span><span class="sxs-lookup"><span data-stu-id="c851b-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c851b-145"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c851b-145"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c851b-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c851b-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c851b-147">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="c851b-147">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
