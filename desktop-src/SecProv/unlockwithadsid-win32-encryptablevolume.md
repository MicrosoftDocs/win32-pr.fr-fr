---
description: Utilise le fourni Active Directory chaîne d’identificateur de sécurité (SID) pour obtenir la clé dérivée et déverrouiller le volume chiffré.
ms.assetid: 89FBC815-859D-415A-8F26-170FB2DB7387
title: Méthode UnlockWithAdSid de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.UnlockWithAdSid
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: cbd2a327a2ede322c01009fe32aa0492a7e65610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518896"
---
# <a name="unlockwithadsid-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="747f7-103">Méthode UnlockWithAdSid de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="747f7-103">UnlockWithAdSid method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="747f7-104">La méthode **UnlockWithAdSid** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) utilise le fourni Active Directory chaîne d’identificateur de sécurité (SID) pour obtenir la clé dérivée et déverrouiller le volume chiffré.</span><span class="sxs-lookup"><span data-stu-id="747f7-104">The **UnlockWithAdSid** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class uses the provided Active Directory security identifier (SID) string to obtain the derived key and unlock the encrypted volume.</span></span>

> [!Note]  
> <span data-ttu-id="747f7-105">Si le disque prend en charge le chiffrement matériel, cette fonction définit l’état de la bande sur « déverrouillé ».</span><span class="sxs-lookup"><span data-stu-id="747f7-105">If the disc supports hardware encryption this function sets the band status to "unlocked""</span></span>

 

## <a name="syntax"></a><span data-ttu-id="747f7-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="747f7-106">Syntax</span></span>


```mof
uint32 UnlockWithAdSid(
  [in]  string SidString
);
```



## <a name="parameters"></a><span data-ttu-id="747f7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="747f7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="747f7-108">*SidString* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="747f7-108">*SidString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="747f7-109">Chaîne qui contient le SID Active Directory.</span><span class="sxs-lookup"><span data-stu-id="747f7-109">String that contains the Active Directory SID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="747f7-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="747f7-110">Return value</span></span>

<span data-ttu-id="747f7-111">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="747f7-111">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="747f7-112">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="747f7-112">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="747f7-113">Description</span><span class="sxs-lookup"><span data-stu-id="747f7-113">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="747f7-114"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="747f7-114"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="747f7-115">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="747f7-115">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="747f7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="747f7-116">Remarks</span></span>

<span data-ttu-id="747f7-117">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="747f7-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="747f7-118">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="747f7-118">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="747f7-119">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="747f7-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="747f7-120">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="747f7-120">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="747f7-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="747f7-121">Requirements</span></span>



| <span data-ttu-id="747f7-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="747f7-122">Requirement</span></span> | <span data-ttu-id="747f7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="747f7-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="747f7-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="747f7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="747f7-125">Windows 8 entreprise, applications de bureau Windows 8 professionnel \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="747f7-125">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="747f7-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="747f7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="747f7-127">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="747f7-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="747f7-128">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="747f7-128">Namespace</span></span><br/>                | <span data-ttu-id="747f7-129">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="747f7-129">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="747f7-130">MOF</span><span class="sxs-lookup"><span data-stu-id="747f7-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="747f7-131"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="747f7-131"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="747f7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="747f7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="747f7-133">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="747f7-133">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
