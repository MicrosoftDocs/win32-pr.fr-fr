---
description: Récupère le nom complet utilisé pour identifier un protecteur de clé donné.
ms.assetid: 2f310494-7873-4d05-836e-f09e5784571b
title: Méthode GetKeyProtectorFriendlyName de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorFriendlyName
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 45da91d08aadda2d1a25254fe36d0d266b7c53d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545021"
---
# <a name="getkeyprotectorfriendlyname-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="613ad-103">Méthode GetKeyProtectorFriendlyName de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="613ad-103">GetKeyProtectorFriendlyName method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="613ad-104">La méthode **GetKeyProtectorFriendlyName** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) récupère le nom complet utilisé pour identifier un protecteur de clé donné.</span><span class="sxs-lookup"><span data-stu-id="613ad-104">The **GetKeyProtectorFriendlyName** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the display name used to identify a given key protector.</span></span>

## <a name="syntax"></a><span data-ttu-id="613ad-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="613ad-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorFriendlyName(
  [in]  string VolumeKeyProtectorID,
  [out] string FriendlyName
);
```



## <a name="parameters"></a><span data-ttu-id="613ad-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="613ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="613ad-107">*VolumeKeyProtectorID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="613ad-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="613ad-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="613ad-108">Type: **string**</span></span>

<span data-ttu-id="613ad-109">Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="613ad-109">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="613ad-110">*FriendlyName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="613ad-110">*FriendlyName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="613ad-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="613ad-111">Type: **string**</span></span>

<span data-ttu-id="613ad-112">Chaîne qui contient le nom spécifié par l’utilisateur utilisé pour identifier le protecteur de clé donné.</span><span class="sxs-lookup"><span data-stu-id="613ad-112">A string that contains the user-specified name used to identify the given key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="613ad-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="613ad-113">Return value</span></span>

<span data-ttu-id="613ad-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="613ad-114">Type: **uint32**</span></span>

<span data-ttu-id="613ad-115">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="613ad-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="613ad-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="613ad-116">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="613ad-117">Description</span><span class="sxs-lookup"><span data-stu-id="613ad-117">Description</span></span>                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="613ad-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="613ad-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="613ad-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="613ad-119">The method was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="613ad-120"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="613ad-120"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="613ad-121">Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé valide.</span><span class="sxs-lookup"><span data-stu-id="613ad-121">The *VolumeKeyProtectorID* parameter does not refer to a valid key protector.</span></span><br/>     |
| <dl> <span data-ttu-id="613ad-122"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="613ad-122"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="613ad-123">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="613ad-123">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="613ad-124">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="613ad-124">Add a key protector to enable BitLocker.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="613ad-125">Notes</span><span class="sxs-lookup"><span data-stu-id="613ad-125">Remarks</span></span>

<span data-ttu-id="613ad-126">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="613ad-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="613ad-127">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="613ad-127">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="613ad-128">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="613ad-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="613ad-129">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="613ad-129">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="613ad-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="613ad-130">Requirements</span></span>



| <span data-ttu-id="613ad-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="613ad-131">Requirement</span></span> | <span data-ttu-id="613ad-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="613ad-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="613ad-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="613ad-133">Minimum supported client</span></span><br/> | <span data-ttu-id="613ad-134">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="613ad-134">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="613ad-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="613ad-135">Minimum supported server</span></span><br/> | <span data-ttu-id="613ad-136">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="613ad-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="613ad-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="613ad-137">Namespace</span></span><br/>                | <span data-ttu-id="613ad-138">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="613ad-138">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="613ad-139">MOF</span><span class="sxs-lookup"><span data-stu-id="613ad-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="613ad-140"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="613ad-140"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="613ad-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="613ad-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="613ad-142">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="613ad-142">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
