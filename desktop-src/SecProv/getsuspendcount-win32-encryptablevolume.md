---
description: Récupère le nombre de fois que BitLocker a été interrompu.
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: Méthode GetSuspendCount de la classe Win32_EncryptableVolume (Activdbg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetSuspendCount
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eb28f019674f39946674399f8931fb63421ef982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545020"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="59b0e-103">Méthode GetSuspendCount de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="59b0e-103">GetSuspendCount method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="59b0e-104">La méthode **GetSuspendCount** de la classe [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) récupère le nombre de redémarrages avant que la protection ne soit reprise automatiquement.</span><span class="sxs-lookup"><span data-stu-id="59b0e-104">The **GetSuspendCount** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the number of reboots before protection will automatically be resumed.</span></span>

## <a name="syntax"></a><span data-ttu-id="59b0e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59b0e-105">Syntax</span></span>


```mof
uint32 GetSuspendCount(
   uint32 SuspendCount
);
```



## <a name="parameters"></a><span data-ttu-id="59b0e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59b0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59b0e-107">*SuspendCount*</span><span class="sxs-lookup"><span data-stu-id="59b0e-107">*SuspendCount*</span></span> 
</dt> <dd>

<span data-ttu-id="59b0e-108">Valeur entière comprise entre 0 et 15.</span><span class="sxs-lookup"><span data-stu-id="59b0e-108">An integer value from 0 to 15.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59b0e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59b0e-109">Return value</span></span>

<span data-ttu-id="59b0e-110">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="59b0e-110">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="59b0e-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="59b0e-111">Return code</span></span>                                                                                          | <span data-ttu-id="59b0e-112">Description</span><span class="sxs-lookup"><span data-stu-id="59b0e-112">Description</span></span>                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="59b0e-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0e-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="59b0e-114">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="59b0e-114">The method was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="59b0e-115"><dt>**ERREUR \_ non \_ prise en charge**</dt></span><span class="sxs-lookup"><span data-stu-id="59b0e-115"><dt>**ERROR\_NOT\_SUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="59b0e-116">Retourné si le volume n’est pas suspendu ou s’il ne s’agit pas d’un volume de système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="59b0e-116">Returned if the volume is not suspended or is not an OS volume.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="59b0e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="59b0e-117">Remarks</span></span>

<span data-ttu-id="59b0e-118">Cette méthode s’applique uniquement au volume du système d’exploitation, et uniquement si elle est effectivement suspendue à ce moment-là.</span><span class="sxs-lookup"><span data-stu-id="59b0e-118">This method only applies to the OS volume, and only if it is actually suspended at the time.</span></span> <span data-ttu-id="59b0e-119">Si le volume n’est pas suspendu ou n’est pas un volume du système d’exploitation, l' **erreur \_ non \_ prise en charge** est retournée.</span><span class="sxs-lookup"><span data-stu-id="59b0e-119">If the volume is not suspended or is not an OS volume, **ERROR\_NOT\_SUPPORTED** will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="59b0e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59b0e-120">Requirements</span></span>



| <span data-ttu-id="59b0e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59b0e-121">Requirement</span></span> | <span data-ttu-id="59b0e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="59b0e-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59b0e-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59b0e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="59b0e-124">Windows 8 entreprise, applications de bureau Windows 8 professionnel \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59b0e-124">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="59b0e-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59b0e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="59b0e-126">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59b0e-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="59b0e-127">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="59b0e-127">Namespace</span></span><br/>                | <span data-ttu-id="59b0e-128">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="59b0e-128">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="59b0e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="59b0e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="59b0e-130"><dt>Activdbg. h</dt></span><span class="sxs-lookup"><span data-stu-id="59b0e-130"><dt>Activdbg.h</dt></span></span> </dl>                   |
| <span data-ttu-id="59b0e-131">MOF</span><span class="sxs-lookup"><span data-stu-id="59b0e-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="59b0e-132"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="59b0e-132"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59b0e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59b0e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59b0e-134">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="59b0e-134">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




