---
description: Suspend le chiffrement ou le déchiffrement d’un volume.
ms.assetid: 3c365299-f0e1-480e-ad96-c91bb4108bb2
title: Méthode PauseConversion de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.PauseConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 1c9756da2339a6a3d8e87466651f61c8ff3f83a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530886"
---
# <a name="pauseconversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="d3b18-103">Méthode PauseConversion de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="d3b18-103">PauseConversion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="d3b18-104">La méthode **PauseConversion** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) interrompt le chiffrement ou le déchiffrement d’un volume.</span><span class="sxs-lookup"><span data-stu-id="d3b18-104">The **PauseConversion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class pauses the encryption or decryption of a volume.</span></span>

> [!Note]  
> <span data-ttu-id="d3b18-105">Si le disque prend en charge le chiffrement matériel, cette fonction peut suspendre une opération de nettoyage, mais ne peut pas suspendre le chiffrement basé sur le matériel.</span><span class="sxs-lookup"><span data-stu-id="d3b18-105">If the disc supports hardware encryption, this function can pause a wiping operation but cannot pause hardware-based encryption.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d3b18-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d3b18-106">Syntax</span></span>


```mof
uint32 PauseConversion();
```



## <a name="parameters"></a><span data-ttu-id="d3b18-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d3b18-107">Parameters</span></span>

<span data-ttu-id="d3b18-108">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="d3b18-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3b18-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d3b18-109">Return value</span></span>

<span data-ttu-id="d3b18-110">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d3b18-110">Type: **uint32**</span></span>

<span data-ttu-id="d3b18-111">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="d3b18-111">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="d3b18-112">Si cette méthode est utilisée sur un volume entièrement chiffré ou entièrement déchiffré, ou si le chiffrement/déchiffrement est déjà suspendu sur le volume, la valeur 0 est retournée en supposant qu’aucune autre erreur ne se produise.</span><span class="sxs-lookup"><span data-stu-id="d3b18-112">If this method is used on a fully encrypted or fully decrypted volume, or if encryption/decryption is already paused on the volume, 0 is returned assuming no other errors occur.</span></span>



| <span data-ttu-id="d3b18-113">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d3b18-113">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="d3b18-114">Description</span><span class="sxs-lookup"><span data-stu-id="d3b18-114">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="d3b18-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="d3b18-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="d3b18-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="d3b18-116">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="d3b18-117"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="d3b18-117"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="d3b18-118">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="d3b18-118">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="d3b18-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d3b18-119">Remarks</span></span>

<span data-ttu-id="d3b18-120">Si cette méthode est utilisée sur un volume avec chiffrement/déchiffrement en cours, l’exécution correcte de cette méthode amène [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) à indiquer que le chiffrement ou le déchiffrement est suspendu.</span><span class="sxs-lookup"><span data-stu-id="d3b18-120">If this method is used on a volume with encryption/decryption in progress, successfully running this method causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that encryption or decryption is paused.</span></span>

<span data-ttu-id="d3b18-121">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="d3b18-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d3b18-122">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="d3b18-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="d3b18-123">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="d3b18-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d3b18-124">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="d3b18-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d3b18-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d3b18-125">Requirements</span></span>



| <span data-ttu-id="d3b18-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d3b18-126">Requirement</span></span> | <span data-ttu-id="d3b18-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="d3b18-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3b18-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3b18-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d3b18-129">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3b18-129">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d3b18-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d3b18-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d3b18-131">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d3b18-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3b18-132">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="d3b18-132">Namespace</span></span><br/>                | <span data-ttu-id="d3b18-133">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="d3b18-133">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="d3b18-134">MOF</span><span class="sxs-lookup"><span data-stu-id="d3b18-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d3b18-135"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d3b18-135"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3b18-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d3b18-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3b18-137">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="d3b18-137">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
