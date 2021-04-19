---
description: Sécurise la clé de chiffrement du volume à l’aide d’un identificateur de sécurité (SID) Active Directory.
ms.assetid: 881EEAF2-49C5-4BBD-B2AA-5E30B61E7D3A
title: Méthode ProtectKeyWithAdSid de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0279a6edc8aaa275fdf75a855452d987de802d86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521076"
---
# <a name="protectkeywithadsid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="c8379-103">Méthode ProtectKeyWithAdSid de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="c8379-103">ProtectKeyWithAdSid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="c8379-104">La méthode **ProtectKeyWithAdSid** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) sécurise la clé de chiffrement du volume à l’aide d’un identificateur de sécurité (SID) Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c8379-104">The **ProtectKeyWithAdSid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using a Active Directory security identifier (SID).</span></span>

## <a name="syntax"></a><span data-ttu-id="c8379-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8379-105">Syntax</span></span>


```mof
uint32 ProtectKeyWithAdSid(
  [in, optional] string FriendlyName,
  [in]           string SidString,
  [in]           uint32 Flags,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="c8379-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8379-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8379-107">*FriendlyName* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="c8379-107">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c8379-108">Chaîne qui spécifie un identificateur affecté à l’utilisateur pour ce protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="c8379-108">A string that specifies a user-assigned identifier for this key protector.</span></span> <span data-ttu-id="c8379-109">Si ce paramètre n’est pas spécifié, une valeur vide est utilisée.</span><span class="sxs-lookup"><span data-stu-id="c8379-109">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="c8379-110">*SidString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c8379-110">*SidString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8379-111">Chaîne qui contient le SID Active Directory utilisé pour protéger la clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="c8379-111">String that contains the Active Directory SID used to protect the encryption key.</span></span>

</dd> <dt>

<span data-ttu-id="c8379-112">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="c8379-112">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c8379-113">Indicateurs qui modifient le comportement de la fonction.</span><span class="sxs-lookup"><span data-stu-id="c8379-113">Flags that change the function behavior.</span></span> <span data-ttu-id="c8379-114">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="c8379-114">This can be one of the following values.</span></span>



| <span data-ttu-id="c8379-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8379-115">Value</span></span>                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="c8379-116">Signification</span><span class="sxs-lookup"><span data-stu-id="c8379-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <span data-ttu-id="c8379-117"><dt>**FVE \_ \_Indicateur DPAPI \_ ng \_ aucun**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="c8379-117"><dt>**FVE\_DPAPI\_NG\_FLAG\_NONE**</dt> <dt>0x0000</dt></span></span> </dl>                                                                   | <span data-ttu-id="c8379-118">Aucun effet.</span><span class="sxs-lookup"><span data-stu-id="c8379-118">No effect.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <span data-ttu-id="c8379-119"><dt>**FVE \_ \_ \_ Indicateur \_ de déverrouillage de l’indicateur GN GN \_ en tant que \_ \_ compte de service**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="c8379-119"><dt>**FVE\_DPAPI\_NG\_FLAG\_UNLOCK\_AS\_SERVICE\_ACCOUNT**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="c8379-120">Spécifie que le protecteur basé sur SID a été protégé sur un compte de service.</span><span class="sxs-lookup"><span data-stu-id="c8379-120">Specifies that the SID-based protector was protected to a service account.</span></span> <span data-ttu-id="c8379-121">Si cet indicateur est spécifié, l’appelant doit s’assurer qu’il s’exécute en tant que compte de service approprié avant d’appeler [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (en supprimant temporairement l’emprunt d’identité, par exemple).</span><span class="sxs-lookup"><span data-stu-id="c8379-121">If this flag is specified, the caller should ensure that it is running as the appropriate service account before calling [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (by temporarily dropping impersonation, for example).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c8379-122">*VolumeKeyProtectorID* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c8379-122">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8379-123">Identificateur unique associé au protecteur créé.</span><span class="sxs-lookup"><span data-stu-id="c8379-123">A unique identifier associated with the created protector.</span></span> <span data-ttu-id="c8379-124">Vous pouvez utiliser cette chaîne pour gérer le protecteur de clé.</span><span class="sxs-lookup"><span data-stu-id="c8379-124">You can use this string to manage the key protector.</span></span>

<span data-ttu-id="c8379-125">Si le lecteur prend en charge le chiffrement matériel et que BitLocker n’a pas pris possession de la bande, la chaîne d’ID est définie sur « BitLocker » et le protecteur de clé est écrit dans les métadonnées par bande.</span><span class="sxs-lookup"><span data-stu-id="c8379-125">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8379-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c8379-126">Return value</span></span>

<span data-ttu-id="c8379-127">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="c8379-127">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="c8379-128">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c8379-128">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="c8379-129">Description</span><span class="sxs-lookup"><span data-stu-id="c8379-129">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="c8379-130"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c8379-130"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="c8379-131">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="c8379-131">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c8379-132">Notes</span><span class="sxs-lookup"><span data-stu-id="c8379-132">Remarks</span></span>

<span data-ttu-id="c8379-133">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="c8379-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c8379-134">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="c8379-134">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c8379-135">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="c8379-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c8379-136">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md) .</span><span class="sxs-lookup"><span data-stu-id="c8379-136">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md)</span></span>

<span data-ttu-id="c8379-137">Par défaut, vous ne pouvez pas ajouter à distance un compte Active Directory ou un protecteur de groupe.</span><span class="sxs-lookup"><span data-stu-id="c8379-137">By default, you cannot add an Active Directory account or group protector remotely.</span></span> <span data-ttu-id="c8379-138">Vous devez activer la délégation avec restriction sur le contrôleur de domaine et l’ordinateur source.</span><span class="sxs-lookup"><span data-stu-id="c8379-138">You must enable constrained delegation on the domain controller and source computer.</span></span> <span data-ttu-id="c8379-139">Sur le contrôleur de domaine, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="c8379-139">On the domain controller, perform the following steps:</span></span>

1.  <span data-ttu-id="c8379-140">Ouvrir le gestionnaire de serveur</span><span class="sxs-lookup"><span data-stu-id="c8379-140">Open Server Manager</span></span>
2.  <span data-ttu-id="c8379-141">Sélectionner les ordinateurs dans Active Directory rôles</span><span class="sxs-lookup"><span data-stu-id="c8379-141">Select Computers in Active Directory roles</span></span>
3.  <span data-ttu-id="c8379-142">Sélectionnez l’ordinateur client cible et cliquez avec le bouton droit</span><span class="sxs-lookup"><span data-stu-id="c8379-142">Select the target client computer and right click</span></span>
4.  <span data-ttu-id="c8379-143">Sélectionner l’onglet délégation</span><span class="sxs-lookup"><span data-stu-id="c8379-143">Select the Delegation tab</span></span>
5.  <span data-ttu-id="c8379-144">Cochez la case « n’approuver cet ordinateur que pour la délégation aux services spécifiés »</span><span class="sxs-lookup"><span data-stu-id="c8379-144">Select the "Trust this computer for delegation to specified services only" radio button</span></span>
6.  <span data-ttu-id="c8379-145">Sélectionnez la case d’option « utiliser Kerberos uniquement »</span><span class="sxs-lookup"><span data-stu-id="c8379-145">Select the "Use Kerberos only" radio button</span></span>
7.  <span data-ttu-id="c8379-146">Cliquez sur Ajouter.</span><span class="sxs-lookup"><span data-stu-id="c8379-146">Click Add</span></span>
8.  <span data-ttu-id="c8379-147">Sélectionnez « utilisateurs ou ordinateurs »</span><span class="sxs-lookup"><span data-stu-id="c8379-147">Select "Users or Computers"</span></span>
9.  <span data-ttu-id="c8379-148">Sélectionner l’hôte/comme nom de principal du service</span><span class="sxs-lookup"><span data-stu-id="c8379-148">Select host/ as the Service Principal Name</span></span>

<span data-ttu-id="c8379-149">Effectuez les étapes 3 à 9 sur l’ordinateur source.</span><span class="sxs-lookup"><span data-stu-id="c8379-149">Perform steps 3 through 9 on the source computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8379-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8379-150">Requirements</span></span>



| <span data-ttu-id="c8379-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8379-151">Requirement</span></span> | <span data-ttu-id="c8379-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8379-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8379-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8379-153">Minimum supported client</span></span><br/> | <span data-ttu-id="c8379-154">Windows 8 entreprise, applications de bureau Windows 8 professionnel \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8379-154">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c8379-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c8379-155">Minimum supported server</span></span><br/> | <span data-ttu-id="c8379-156">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c8379-156">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8379-157">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c8379-157">Namespace</span></span><br/>                | <span data-ttu-id="c8379-158">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="c8379-158">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="c8379-159">MOF</span><span class="sxs-lookup"><span data-stu-id="c8379-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8379-160"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8379-160"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8379-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8379-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8379-162">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="c8379-162">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
