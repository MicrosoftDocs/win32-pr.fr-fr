---
description: Reprend le chiffrement ou le déchiffrement d’un volume.
ms.assetid: e37f3e32-5510-431e-9782-11908e65300d
title: Méthode ResumeConversion de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ResumeConversion
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eafa700f86e51310096835e2f24b53a28e66f800
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750836"
---
# <a name="resumeconversion-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="2709b-103">Méthode ResumeConversion de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="2709b-103">ResumeConversion method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="2709b-104">La méthode **ResumeConversion** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) reprend le chiffrement ou le déchiffrement d’un volume.</span><span class="sxs-lookup"><span data-stu-id="2709b-104">The **ResumeConversion** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class resumes the encryption or decryption of a volume.</span></span>

> [!Note]  
> <span data-ttu-id="2709b-105">Si le disque prend en charge le chiffrement matériel, cette fonction peut reprendre une opération de nettoyage uniquement.</span><span class="sxs-lookup"><span data-stu-id="2709b-105">If the disc supports hardware encryption, this function can resume a wiping operation only.</span></span> <span data-ttu-id="2709b-106">Pour plus d’informations, consultez [**PauseConversion**](pauseconversion-win32-encryptablevolume.md).</span><span class="sxs-lookup"><span data-stu-id="2709b-106">For more information, see [**PauseConversion**](pauseconversion-win32-encryptablevolume.md).</span></span>

 

## <a name="syntax"></a><span data-ttu-id="2709b-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2709b-107">Syntax</span></span>


```mof
uint32 ResumeConversion();
```



## <a name="parameters"></a><span data-ttu-id="2709b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2709b-108">Parameters</span></span>

<span data-ttu-id="2709b-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="2709b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2709b-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2709b-110">Return value</span></span>

<span data-ttu-id="2709b-111">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2709b-111">Type: **uint32**</span></span>

<span data-ttu-id="2709b-112">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="2709b-112">This method returns one of the following codes or another error code if it fails.</span></span>

<span data-ttu-id="2709b-113">Si cette méthode est utilisée sur un volume entièrement chiffré ou entièrement déchiffré, ou si le chiffrement/déchiffrement est déjà en cours sur le volume, la valeur 0 est retournée en supposant qu’aucune autre erreur ne se produise.</span><span class="sxs-lookup"><span data-stu-id="2709b-113">If this method is used on a fully encrypted or fully decrypted volume, or if encryption/decryption is already in progress on the volume, 0 is returned assuming no other errors occur.</span></span>



| <span data-ttu-id="2709b-114">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="2709b-114">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="2709b-115">Description</span><span class="sxs-lookup"><span data-stu-id="2709b-115">Description</span></span>                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="2709b-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="2709b-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="2709b-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="2709b-117">The method was successful.</span></span><br/> |
| <dl> <span data-ttu-id="2709b-118"><dt>**FVE \_ E \_ Locked \_ volume**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="2709b-118"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="2709b-119">Le volume est verrouillé.</span><span class="sxs-lookup"><span data-stu-id="2709b-119">The volume is locked.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="2709b-120">Notes</span><span class="sxs-lookup"><span data-stu-id="2709b-120">Remarks</span></span>

<span data-ttu-id="2709b-121">Si cette méthode est utilisée sur un volume avec chiffrement/déchiffrement suspendu, l’exécution correcte de cette méthode amène [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) à indiquer que le chiffrement ou le déchiffrement est en cours.</span><span class="sxs-lookup"><span data-stu-id="2709b-121">If this method is used on a volume with paused encryption/decryption, successfully running this method causes [**GetConversionStatus**](getconversionstatus-win32-encryptablevolume.md) to indicate that encryption or decryption is in progress.</span></span>

<span data-ttu-id="2709b-122">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="2709b-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="2709b-123">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="2709b-123">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="2709b-124">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="2709b-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="2709b-125">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="2709b-125">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2709b-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2709b-126">Requirements</span></span>



| <span data-ttu-id="2709b-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2709b-127">Requirement</span></span> | <span data-ttu-id="2709b-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="2709b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2709b-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2709b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2709b-130">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2709b-130">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2709b-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2709b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2709b-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2709b-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2709b-133">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2709b-133">Namespace</span></span><br/>                | <span data-ttu-id="2709b-134">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="2709b-134">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="2709b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="2709b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2709b-136"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2709b-136"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2709b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2709b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2709b-138">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="2709b-138">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
