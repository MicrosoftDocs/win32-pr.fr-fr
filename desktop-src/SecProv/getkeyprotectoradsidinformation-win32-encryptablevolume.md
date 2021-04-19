---
description: Récupère l’identificateur de sécurité et les indicateurs utilisés pour protéger une clé.
ms.assetid: 5EF97F44-78FF-4FBF-9142-F2DD0A849057
title: Méthode GetKeyProtectorAdSidInformation de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 57e72488a9e53f49383d179b0bcb1a8b9ff1f706
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "106542812"
---
# <a name="getkeyprotectoradsidinformation-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="ed857-103">Méthode GetKeyProtectorAdSidInformation de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="ed857-103">GetKeyProtectorAdSidInformation method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="ed857-104">La méthode **GetKeyProtectorAdSidInformation** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) récupère l’identificateur de sécurité et les indicateurs utilisés pour protéger une clé.</span><span class="sxs-lookup"><span data-stu-id="ed857-104">The **GetKeyProtectorAdSidInformation** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the security identifier and flags used to protect a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed857-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed857-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] string SidString,
  [out] uint32 Flags
);
```



## <a name="parameters"></a><span data-ttu-id="ed857-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed857-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed857-107">*VolumeKeyProtectorID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ed857-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed857-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ed857-108">Type: **string**</span></span>

<span data-ttu-id="ed857-109">Identificateur de chaîne qui peut être utilisé pour gérer un protecteur de clé de volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="ed857-109">A string identifier that can be used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="ed857-110">*SidString* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ed857-110">*SidString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed857-111">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ed857-111">Type: **string**</span></span>

<span data-ttu-id="ed857-112">Chaîne qui contient l’identificateur de sécurité (SID).</span><span class="sxs-lookup"><span data-stu-id="ed857-112">A string that contains the security identifier (SID).</span></span>

</dd> <dt>

<span data-ttu-id="ed857-113">*Indicateurs* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ed857-113">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed857-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed857-114">Type: **uint32**</span></span>

<span data-ttu-id="ed857-115">Indicateurs qui modifient le comportement de la fonction.</span><span class="sxs-lookup"><span data-stu-id="ed857-115">Flags that change the function behavior.</span></span> <span data-ttu-id="ed857-116">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ed857-116">This can be one of the following values.</span></span>



| <span data-ttu-id="ed857-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed857-117">Value</span></span>                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="ed857-118">Signification</span><span class="sxs-lookup"><span data-stu-id="ed857-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <span data-ttu-id="ed857-119"><dt>**FVE \_ \_Indicateur DPAPI \_ ng \_ aucun**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="ed857-119"><dt>**FVE\_DPAPI\_NG\_FLAG\_NONE**</dt> <dt>0x0000</dt></span></span> </dl>                                                                   | <span data-ttu-id="ed857-120">Aucun effet.</span><span class="sxs-lookup"><span data-stu-id="ed857-120">No effect.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <span data-ttu-id="ed857-121"><dt>**FVE \_ \_ \_ Indicateur \_ de déverrouillage de l’indicateur GN GN \_ en tant que \_ \_ compte de service**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="ed857-121"><dt>**FVE\_DPAPI\_NG\_FLAG\_UNLOCK\_AS\_SERVICE\_ACCOUNT**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="ed857-122">Spécifie que le protecteur basé sur SID a été protégé sur un compte de service.</span><span class="sxs-lookup"><span data-stu-id="ed857-122">Specifies that the SID-based protector was protected to a service account.</span></span> <span data-ttu-id="ed857-123">Si cet indicateur est spécifié, l’appelant doit s’assurer qu’il s’exécute en tant que compte de service approprié avant d’appeler [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (en supprimant temporairement l’emprunt d’identité, par exemple).</span><span class="sxs-lookup"><span data-stu-id="ed857-123">If this flag is specified, the caller should ensure that it is running as the appropriate service account before calling [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (by temporarily dropping impersonation, for example).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed857-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ed857-124">Return value</span></span>

<span data-ttu-id="ed857-125">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed857-125">Type: **uint32**</span></span>

<span data-ttu-id="ed857-126">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="ed857-126">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="ed857-127">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ed857-127">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="ed857-128">Description</span><span class="sxs-lookup"><span data-stu-id="ed857-128">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ed857-129"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ed857-129"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="ed857-130">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="ed857-130">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ed857-131">Notes</span><span class="sxs-lookup"><span data-stu-id="ed857-131">Remarks</span></span>

<span data-ttu-id="ed857-132">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="ed857-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ed857-133">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="ed857-133">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ed857-134">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="ed857-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ed857-135">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ed857-135">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed857-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed857-136">Requirements</span></span>



| <span data-ttu-id="ed857-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed857-137">Requirement</span></span> | <span data-ttu-id="ed857-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed857-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed857-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed857-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ed857-140">Windows 8 entreprise, applications de bureau Windows 8 professionnel \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed857-140">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ed857-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed857-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ed857-142">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ed857-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ed857-143">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ed857-143">Namespace</span></span><br/>                | <span data-ttu-id="ed857-144">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="ed857-144">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="ed857-145">MOF</span><span class="sxs-lookup"><span data-stu-id="ed857-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed857-146"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed857-146"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed857-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed857-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed857-148">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="ed857-148">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
