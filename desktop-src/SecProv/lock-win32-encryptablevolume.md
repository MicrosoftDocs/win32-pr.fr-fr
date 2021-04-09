---
description: Démonte le volume et supprime la clé de chiffrement du volume de la mémoire système.
ms.assetid: 8d6e42a0-7b43-46d2-aa5e-941567ef2842
title: Méthode Lock de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.Lock
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 8fb6cd7b4134f4921cdaf57414843fb6522c5823
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862286"
---
# <a name="lock-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="b7dbf-103">Méthode Lock de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="b7dbf-103">Lock method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="b7dbf-104">La méthode **Lock** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) démonte le volume et supprime la clé de chiffrement du volume de la mémoire système.</span><span class="sxs-lookup"><span data-stu-id="b7dbf-104">The **Lock** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class dismounts the volume and removes the volume's encryption key from system memory.</span></span> <span data-ttu-id="b7dbf-105">Le contenu du volume reste inaccessible jusqu’à ce qu’il soit déverrouillé par la méthode [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) ou par la méthode [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="b7dbf-105">The contents of the volume remain inaccessible until it is unlocked by either the [**UnlockWithExternalKey**](unlockwithexternalkey-win32-encryptablevolume.md) method or the [**UnlockWithNumericalPassword**](unlockwithnumericalpassword-win32-encryptablevolume.md) method.</span></span> <span data-ttu-id="b7dbf-106">Cette méthode ne peut pas être exécutée correctement pour le volume du système d’exploitation en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="b7dbf-106">This method cannot be successfully run for the currently running operating system volume.</span></span>

> [!Note]  
> <span data-ttu-id="b7dbf-107">Si le disque prend en charge le chiffrement matériel, la bande est définie sur « verrouillé ».</span><span class="sxs-lookup"><span data-stu-id="b7dbf-107">If the disc supports hardware encryption, the band is set to "locked".</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b7dbf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7dbf-108">Syntax</span></span>


```mof
uint32 Lock(
  [in, optional] boolean ForceDismount
);
```



## <a name="parameters"></a><span data-ttu-id="b7dbf-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7dbf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7dbf-110">*ForceDismount* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b7dbf-110">*ForceDismount* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7dbf-111">Type : **booléen**</span><span class="sxs-lookup"><span data-stu-id="b7dbf-111">Type: **boolean**</span></span>

<span data-ttu-id="b7dbf-112">Si la **valeur est true** , le disque est démonté de force.</span><span class="sxs-lookup"><span data-stu-id="b7dbf-112">If **true** the disk is forcibly dismounted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7dbf-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7dbf-113">Return value</span></span>

<span data-ttu-id="b7dbf-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b7dbf-114">Type: **uint32**</span></span>

<span data-ttu-id="b7dbf-115">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="b7dbf-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="b7dbf-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="b7dbf-116">Return code/value</span></span>                                                                                                                                                                           | <span data-ttu-id="b7dbf-117">Description</span><span class="sxs-lookup"><span data-stu-id="b7dbf-117">Description</span></span>                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b7dbf-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="b7dbf-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                           | <span data-ttu-id="b7dbf-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="b7dbf-119">The method was successful.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="b7dbf-120"><dt>**E \_ ACCÈS \_ refusé**</dt> <dt>2147942405 (0x80070005)</dt></span><span class="sxs-lookup"><span data-stu-id="b7dbf-120"><dt>**E\_ACCESS\_DENIED**</dt> <dt>2147942405 (0x80070005)</dt></span></span> </dl>               | <span data-ttu-id="b7dbf-121">Les applications accèdent à ce volume.</span><span class="sxs-lookup"><span data-stu-id="b7dbf-121">Applications are accessing this volume.</span></span> <span data-ttu-id="b7dbf-122">Si tous les accès ne sont pas exclusifs, la spécification du paramètre *ForceDismount* sur true permet à la méthode de s’exécuter correctement.</span><span class="sxs-lookup"><span data-stu-id="b7dbf-122">If all access is nonexclusive, specifying the *ForceDismount* parameter as true allows the method to run successfully.</span></span><br/> |
| <dl> <span data-ttu-id="b7dbf-123"><dt>**FVE \_ E \_ non \_ chiffré**</dt> <dt>2150694913 (0x80310001)</dt></span><span class="sxs-lookup"><span data-stu-id="b7dbf-123"><dt>**FVE\_E\_NOT\_ENCRYPTED**</dt> <dt>2150694913 (0x80310001)</dt></span></span> </dl>          | <span data-ttu-id="b7dbf-124">Le volume est entièrement déchiffré et ne peut pas être verrouillé.</span><span class="sxs-lookup"><span data-stu-id="b7dbf-124">The volume is fully decrypted and cannot be locked.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="b7dbf-125"><dt>**FVE \_ \_Protection E \_ désactivée**</dt> <dt>2150694945 (0x80310021)</dt></span><span class="sxs-lookup"><span data-stu-id="b7dbf-125"><dt>**FVE\_E\_PROTECTION\_DISABLED**</dt> <dt>2150694945 (0x80310021)</dt></span></span> </dl>    | <span data-ttu-id="b7dbf-126">La clé de chiffrement du volume est disponible en clair sur le disque, ce qui empêche le verrouillage du volume.</span><span class="sxs-lookup"><span data-stu-id="b7dbf-126">The volume's encryption key is available in the clear on the disk, preventing the volume from being locked.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="b7dbf-127"><dt>**FVE \_ \_Clé de récupération E \_ \_ requise**</dt> <dt>2150694946 (0x80310022)</dt></span><span class="sxs-lookup"><span data-stu-id="b7dbf-127"><dt>**FVE\_E\_RECOVERY\_KEY\_REQUIRED**</dt> <dt>2150694946 (0x80310022)</dt></span></span> </dl> | <span data-ttu-id="b7dbf-128">Le volume n’a pas de protecteurs de clé du type « mot de passe numérique » ou « clé externe » nécessaires au déverrouillage du volume.</span><span class="sxs-lookup"><span data-stu-id="b7dbf-128">The volume does not have key protectors of the type "Numerical Password" or "External Key" that are necessary to unlock the volume.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="b7dbf-129">Notes</span><span class="sxs-lookup"><span data-stu-id="b7dbf-129">Remarks</span></span>

<span data-ttu-id="b7dbf-130">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="b7dbf-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b7dbf-131">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="b7dbf-131">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="b7dbf-132">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="b7dbf-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b7dbf-133">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="b7dbf-133">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7dbf-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7dbf-134">Requirements</span></span>



| <span data-ttu-id="b7dbf-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7dbf-135">Requirement</span></span> | <span data-ttu-id="b7dbf-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7dbf-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7dbf-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7dbf-137">Minimum supported client</span></span><br/> | <span data-ttu-id="b7dbf-138">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7dbf-138">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b7dbf-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7dbf-139">Minimum supported server</span></span><br/> | <span data-ttu-id="b7dbf-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7dbf-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b7dbf-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="b7dbf-141">Namespace</span></span><br/>                | <span data-ttu-id="b7dbf-142">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="b7dbf-142">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="b7dbf-143">MOF</span><span class="sxs-lookup"><span data-stu-id="b7dbf-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7dbf-144"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7dbf-144"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7dbf-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7dbf-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7dbf-146">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="b7dbf-146">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
