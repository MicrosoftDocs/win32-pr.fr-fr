---
title: Énumération DeliveryOptimizationFileProperty (Deliveryoptimization. h)
description: L’énumération DeliveryOptimizationFileProperty spécifie l’ID d’une propriété facultative pour le fichier DO.
keywords:
- Énumération DeliveryOptimizationFileProperty
topic_type:
- apiref
api_name:
- DeliveryOptimizationFileProperty
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 238ad815149f7d40dd1902b991608e0a3005eb35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543624"
---
# <a name="deliveryoptimizationfileproperty-enumeration"></a><span data-ttu-id="5ea93-104">Énumération DeliveryOptimizationFileProperty</span><span class="sxs-lookup"><span data-stu-id="5ea93-104">DeliveryOptimizationFileProperty enumeration</span></span>

<span data-ttu-id="5ea93-105">L’énumération DeliveryOptimizationFileProperty spécifie l’ID d’une propriété facultative pour le fichier DO.</span><span class="sxs-lookup"><span data-stu-id="5ea93-105">The DeliveryOptimizationFileProperty enumeration specifies the ID of an optional property for the DO file.</span></span> <span data-ttu-id="5ea93-106">Cette énumération est utilisée dans l’interface IDeliveryOptimizationFile2 où la valeur de propriété de type VARIANT est passée</span><span class="sxs-lookup"><span data-stu-id="5ea93-106">This enumeration is used in the IDeliveryOptimizationFile2 interface where the property value of type VARIANT is passed</span></span>

## <a name="syntax"></a><span data-ttu-id="5ea93-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ea93-107">Syntax</span></span>

```C++
typedef enum _DeliveryOptimizationFileProperty {  
  DOFilePropertyId_DecryptionInfo,
  DOFilePropertyId_IntegrityCheckInfo,
  DOFilePropertyId_IntegrityCheckMandatory,
  DOFilePropertyId_DownloadSinkInterface,
  DOFilePropertyId_DownloadSinkFilePath,
  DOFilePropertyId_DownloadSinkMemoryStream,
  DOFilePropertyId_TotalSizeBytes
} DOFilePropertyId;
```

## <a name="constants"></a><span data-ttu-id="5ea93-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="5ea93-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5ea93-109">DOFilePropertyId_DecryptionInfo</span><span class="sxs-lookup"><span data-stu-id="5ea93-109">DOFilePropertyId_DecryptionInfo</span></span>
</dt> <dd>

<span data-ttu-id="5ea93-110">L’ID de propriété DOFilePropertyId_DecryptionInfo définit les informations de déchiffrement sous la forme d’une chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="5ea93-110">The DOFilePropertyId_DecryptionInfo property ID sets decryption information in the form of a JSON string.</span></span> <span data-ttu-id="5ea93-111">DOFilePropertyId_DecryptionInfo est une propriété en écriture seule de type VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="5ea93-111">DOFilePropertyId_DecryptionInfo is a Write only property of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="5ea93-112">DOFilePropertyId_IntegrityCheckInfo</span><span class="sxs-lookup"><span data-stu-id="5ea93-112">DOFilePropertyId_IntegrityCheckInfo</span></span>
</dt> <dd>

<span data-ttu-id="5ea93-113">L’ID de propriété DOFilePropertyId_IntegrityCheckInfo définit l’emplacement du fichier de hachage de la pièce (PHF), qui est utilisé par pour effectuer des vérifications de l’intégrité du Runtime sur le contenu téléchargé.</span><span class="sxs-lookup"><span data-stu-id="5ea93-113">The DOFilePropertyId_IntegrityCheckInfo property ID sets the piece hash file (PHF) location, which is used by DO to perform runtime integrity checks on the downloaded content.</span></span> <span data-ttu-id="5ea93-114">DOFilePropertyId_IntegrityCheckInfo est une propriété en écriture seule de type VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="5ea93-114">DOFilePropertyId_IntegrityCheckInfo is a Write only property of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="5ea93-115">DOFilePropertyId_IntegrityCheckMandatory</span><span class="sxs-lookup"><span data-stu-id="5ea93-115">DOFilePropertyId_IntegrityCheckMandatory</span></span>
</dt> <dd>

<span data-ttu-id="5ea93-116">L’ID de propriété DOFilePropertyId_IntegrityCheckMandatory définit un indicateur booléen indiquant si l’utilisation du PHF est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="5ea93-116">The DOFilePropertyId_IntegrityCheckMandatory property ID sets a boolean flag indicating whether usage of the PHF is mandatory.</span></span> <span data-ttu-id="5ea93-117">Si la valeur est TRUE, le téléchargement est abandonné après l’échec de la vérification de l’intégrité.</span><span class="sxs-lookup"><span data-stu-id="5ea93-117">If TRUE, the download will be aborted once the integrity check is failed.</span></span> <span data-ttu-id="5ea93-118">DOFilePropertyId_IntegrityCheckMandatory est une propriété en lecture/écriture de type VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="5ea93-118">DOFilePropertyId_IntegrityCheckMandatory is a Read/Write property of type VT_BOOL.</span></span>

</dd> <dt>

<span data-ttu-id="5ea93-119">DOFilePropertyId_DownloadSinkFilePath</span><span class="sxs-lookup"><span data-stu-id="5ea93-119">DOFilePropertyId_DownloadSinkFilePath</span></span>
</dt> <dd>

<span data-ttu-id="5ea93-120">L’ID de propriété DOFilePropertyId_DownloadSinkFilePath définit un emplacement de système de fichiers complet où doit stocker les éléments téléchargés.</span><span class="sxs-lookup"><span data-stu-id="5ea93-120">The DOFilePropertyId_DownloadSinkFilePath property ID sets a fully qualified file system location where DO should store the downloaded pieces.</span></span> <span data-ttu-id="5ea93-121">DOFilePropertyId_DownloadSinkFilePath est de type VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="5ea93-121">DOFilePropertyId_DownloadSinkFilePath is of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="5ea93-122">DOFilePropertyId_DownloadSinkMemoryStream</span><span class="sxs-lookup"><span data-stu-id="5ea93-122">DOFilePropertyId_DownloadSinkMemoryStream</span></span>
</dt> <dd>

<span data-ttu-id="5ea93-123">L’ID de propriété DOFilePropertyId_DownloadSinkMemoryStream est déconseillé.</span><span class="sxs-lookup"><span data-stu-id="5ea93-123">The DOFilePropertyId_DownloadSinkMemoryStream property ID is deprecated.</span></span> <span data-ttu-id="5ea93-124">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="5ea93-124">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="5ea93-125">DOFilePropertyId_TotalSizeBytes</span><span class="sxs-lookup"><span data-stu-id="5ea93-125">DOFilePropertyId_TotalSizeBytes</span></span>
</dt> <dd>

<span data-ttu-id="5ea93-126">L’ID de propriété DOFilePropertyId_TotalSizeBytes spécifie la taille totale du téléchargement.</span><span class="sxs-lookup"><span data-stu-id="5ea93-126">The DOFilePropertyId_TotalSizeBytes property ID specifies the total download size.</span></span> <span data-ttu-id="5ea93-127">DOFilePropertyId_TotalSizeBytes est de type VT_UI8.</span><span class="sxs-lookup"><span data-stu-id="5ea93-127">DOFilePropertyId_TotalSizeBytes is of type VT_UI8.</span></span>
</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5ea93-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ea93-128">Requirements</span></span>

| <span data-ttu-id="5ea93-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ea93-129">Requirement</span></span> | <span data-ttu-id="5ea93-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ea93-130">Value</span></span> |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="5ea93-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ea93-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5ea93-132">Applications de bureau Windows 10, version 1803 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ea93-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="5ea93-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ea93-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5ea93-134">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5ea93-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>  |
| <span data-ttu-id="5ea93-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ea93-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ea93-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ea93-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>               |
