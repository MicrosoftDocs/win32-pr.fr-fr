---
description: Récupère la clé externe pour un protecteur de clé donné.
ms.assetid: d2b5e7d4-97c1-4d7f-a155-b5cdca2b552e
title: Méthode GetKeyProtectorExternalKey de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorExternalKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 7125038a9e93803f7f8773ce5da078983a5a544c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201353"
---
# <a name="getkeyprotectorexternalkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="fbff6-103">Méthode GetKeyProtectorExternalKey de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="fbff6-103">GetKeyProtectorExternalKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="fbff6-104">La méthode **GetKeyProtectorExternalKey** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) récupère la clé externe pour un protecteur de clé donné du type approprié.</span><span class="sxs-lookup"><span data-stu-id="fbff6-104">The **GetKeyProtectorExternalKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the external key for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="fbff6-105">L’identificateur de protecteur de clé doit faire référence à un protecteur de clé de type « clé externe », « TPM et clé de démarrage » ou « TPM et clé de démarrage ».</span><span class="sxs-lookup"><span data-stu-id="fbff6-105">The key protector identifier must refer to a key protector of type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="fbff6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fbff6-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorExternalKey(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="fbff6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fbff6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbff6-108">*VolumeKeyProtectorID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fbff6-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbff6-109">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="fbff6-109">Type: **string**</span></span>

<span data-ttu-id="fbff6-110">Identificateur de chaîne unique utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="fbff6-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="fbff6-111">*ExternalKey* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fbff6-111">*ExternalKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fbff6-112">Type : **UInt8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="fbff6-112">Type: **uint8\[\]**</span></span>

<span data-ttu-id="fbff6-113">Tableau d’octets qui spécifie la clé externe 256 bits qui peut être utilisée pour déverrouiller le volume correspondant.</span><span class="sxs-lookup"><span data-stu-id="fbff6-113">An array of bytes that specifies the 256-bit external key that can be used to unlock the corresponding volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbff6-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fbff6-114">Return value</span></span>

<span data-ttu-id="fbff6-115">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fbff6-115">Type: **uint32**</span></span>

<span data-ttu-id="fbff6-116">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="fbff6-116">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="fbff6-117">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="fbff6-117">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="fbff6-118">Description</span><span class="sxs-lookup"><span data-stu-id="fbff6-118">Description</span></span>                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="fbff6-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="fbff6-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="fbff6-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="fbff6-120">The method was successful.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="fbff6-121"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="fbff6-121"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="fbff6-122">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="fbff6-122">The volume is locked.</span></span><br/>                                                                                                                                       |
| <dl> <span data-ttu-id="fbff6-123"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="fbff6-123"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="fbff6-124">Le paramètre *VolumeKeyProtectorID* ne fait pas référence à un protecteur de clé du type « clé externe », « TPM et clé de démarrage », ou « TPM et clé de démarrage ».</span><span class="sxs-lookup"><span data-stu-id="fbff6-124">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "External Key", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="fbff6-125"><dt>**FVE \_ E \_ non \_ activée**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="fbff6-125"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="fbff6-126">BitLocker n’est pas activé sur le volume.</span><span class="sxs-lookup"><span data-stu-id="fbff6-126">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="fbff6-127">Ajoutez un protecteur de clé pour activer BitLocker.</span><span class="sxs-lookup"><span data-stu-id="fbff6-127">Add a key protector to enable BitLocker.</span></span> <br/>                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="fbff6-128">Notes</span><span class="sxs-lookup"><span data-stu-id="fbff6-128">Remarks</span></span>

<span data-ttu-id="fbff6-129">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="fbff6-129">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="fbff6-130">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="fbff6-130">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="fbff6-131">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="fbff6-131">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="fbff6-132">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="fbff6-132">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fbff6-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fbff6-133">Requirements</span></span>



| <span data-ttu-id="fbff6-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fbff6-134">Requirement</span></span> | <span data-ttu-id="fbff6-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="fbff6-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbff6-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbff6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fbff6-137">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbff6-137">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fbff6-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fbff6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fbff6-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fbff6-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fbff6-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="fbff6-140">Namespace</span></span><br/>                | <span data-ttu-id="fbff6-141">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="fbff6-141">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="fbff6-142">MOF</span><span class="sxs-lookup"><span data-stu-id="fbff6-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbff6-143"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbff6-143"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbff6-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fbff6-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbff6-145">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="fbff6-145">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
