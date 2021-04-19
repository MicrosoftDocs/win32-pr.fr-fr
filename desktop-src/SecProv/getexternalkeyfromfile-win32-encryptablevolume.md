---
description: Retourne la clé externe à partir d’un fichier.
ms.assetid: b61b71fb-af6f-4fe3-859b-a9f2f42ca6d2
title: Méthode GetExternalKeyFromFile de la classe Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetExternalKeyFromFile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: ba0c2cf4744c12143090488d730a1d49bab9b431
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534682"
---
# <a name="getexternalkeyfromfile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="464f7-103">Méthode GetExternalKeyFromFile de la \_ classe Win32 EncryptableVolume</span><span class="sxs-lookup"><span data-stu-id="464f7-103">GetExternalKeyFromFile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="464f7-104">La méthode **GetExternalKeyFromFile** de la [**classe \_ EncryptableVolume Win32**](win32-encryptablevolume.md) retourne la clé externe à partir d’un fichier créé par [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md), en fonction de l’emplacement de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="464f7-104">The **GetExternalKeyFromFile** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class returns the external key from a file created by [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md), given the location of that file.</span></span>

## <a name="syntax"></a><span data-ttu-id="464f7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="464f7-105">Syntax</span></span>


```mof
uint32 GetExternalKeyFromFile(
  [in]  string PathWithFileName,
  [out] uint8  ExternalKey[]
);
```



## <a name="parameters"></a><span data-ttu-id="464f7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="464f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="464f7-107">*PathWithFileName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="464f7-107">*PathWithFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="464f7-108">Type : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="464f7-108">Type: **string**</span></span>

<span data-ttu-id="464f7-109">Chaîne qui spécifie l’emplacement du fichier contenant une clé externe.</span><span class="sxs-lookup"><span data-stu-id="464f7-109">A string that specifies the location of the file containing an external key.</span></span>

</dd> <dt>

<span data-ttu-id="464f7-110">*ExternalKey* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="464f7-110">*ExternalKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="464f7-111">Type : **UInt8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="464f7-111">Type: **uint8\[\]**</span></span>

<span data-ttu-id="464f7-112">Tableau d’octets qui est la clé externe 256 bits contenue dans le fichier qui peut être utilisé pour déverrouiller un volume.</span><span class="sxs-lookup"><span data-stu-id="464f7-112">An array of bytes that is the 256-bit external key contained within the file that can be used to unlock a volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="464f7-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="464f7-113">Return value</span></span>

<span data-ttu-id="464f7-114">Type : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="464f7-114">Type: **uint32**</span></span>

<span data-ttu-id="464f7-115">Cette méthode retourne l’un des codes suivants, ou un autre code d’erreur en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="464f7-115">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="464f7-116">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="464f7-116">Return code/value</span></span>                                                                                                                                                                   | <span data-ttu-id="464f7-117">Description</span><span class="sxs-lookup"><span data-stu-id="464f7-117">Description</span></span>                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <span data-ttu-id="464f7-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="464f7-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                   | <span data-ttu-id="464f7-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="464f7-119">The method was successful.</span></span><br/>                  |
| <dl> <span data-ttu-id="464f7-120"><dt>**E \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="464f7-120"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>           | <span data-ttu-id="464f7-121">Le fichier ne contient pas de clé externe.</span><span class="sxs-lookup"><span data-stu-id="464f7-121">The file does not contain an external key.</span></span><br/>  |
| <dl> <span data-ttu-id="464f7-122"><dt>**Erreur \_ FICHIER \_ \_ introuvable**</dt> <dt>2147942402 (0x80070002)</dt></span><span class="sxs-lookup"><span data-stu-id="464f7-122"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt> <dt>2147942402 (0x80070002)</dt></span></span> </dl> | <span data-ttu-id="464f7-123">Impossible de trouver le fichier à l’emplacement spécifié.</span><span class="sxs-lookup"><span data-stu-id="464f7-123">Cannot find file at the location specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="464f7-124">Notes</span><span class="sxs-lookup"><span data-stu-id="464f7-124">Remarks</span></span>

<span data-ttu-id="464f7-125">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="464f7-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="464f7-126">Les fichiers MOF ne sont pas installés dans le cadre de la SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="464f7-126">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="464f7-127">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="464f7-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="464f7-128">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="464f7-128">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="464f7-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="464f7-129">Requirements</span></span>



| <span data-ttu-id="464f7-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="464f7-130">Requirement</span></span> | <span data-ttu-id="464f7-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="464f7-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="464f7-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="464f7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="464f7-133">Windows Vista entreprise, les applications de bureau Windows Vista Édition intégrale \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="464f7-133">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="464f7-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="464f7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="464f7-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="464f7-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="464f7-136">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="464f7-136">Namespace</span></span><br/>                | <span data-ttu-id="464f7-137">Racine \\ de \\ sécurité cimv2 \\ MicrosoftVolumeEncryption</span><span class="sxs-lookup"><span data-stu-id="464f7-137">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="464f7-138">MOF</span><span class="sxs-lookup"><span data-stu-id="464f7-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="464f7-139"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="464f7-139"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="464f7-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="464f7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="464f7-141">**\_EncryptableVolume Win32**</span><span class="sxs-lookup"><span data-stu-id="464f7-141">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
