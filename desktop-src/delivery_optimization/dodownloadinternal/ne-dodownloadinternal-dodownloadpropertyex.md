---
title: Énumération DODownloadPropertyEx
description: Spécifie l’ID des propriétés étendues pour l’opération de téléchargement.
keywords:
- Énumération DODownloadPropertyEx, DODownloadPropertyEx
topic_type:
- apiref
api_name:
- DODownloadPropertyEx
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 5df0f53778d9059ef8767f5b8052940847e36c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843717"
---
# <a name="dodownloadpropertyex-enumeration"></a><span data-ttu-id="d818e-104">Énumération DODownloadPropertyEx</span><span class="sxs-lookup"><span data-stu-id="d818e-104">DODownloadPropertyEx enumeration</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d818e-105">L’énumération **DODownloadPropertyEx** est déconseillée.</span><span class="sxs-lookup"><span data-stu-id="d818e-105">The **DODownloadPropertyEx** enumeration is deprecated.</span></span> <span data-ttu-id="d818e-106">Utilisez plutôt l’énumération [DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) avec [IDODownload :: GetProperty](../do/nf-do-idodownload-getproperty.md) et [IDODownload :: SetProperty](../do/nf-do-idodownload-setproperty.md).</span><span class="sxs-lookup"><span data-stu-id="d818e-106">Instead, use the [DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) enumeration with [IDODownload::GetProperty](../do/nf-do-idodownload-getproperty.md) and [IDODownload::SetProperty](../do/nf-do-idodownload-setproperty.md).</span></span>

<span data-ttu-id="d818e-107">L’énumération **DODownloadPropertyEx** spécifie l’ID des propriétés étendues pour l’opération de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="d818e-107">The **DODownloadPropertyEx** enumeration specifies the ID of extended properties for the DO download operation.</span></span> <span data-ttu-id="d818e-108">Cette énumération est utilisée par l’interface **IDODownloadInternal** et une valeur de **type Variant** est utilisée pour obtenir et définir la valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="d818e-108">This enumeration is used by the **IDODownloadInternal** interface, and a **VARIANT** value is used to get and set the property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="d818e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d818e-109">Syntax</span></span>

```cpp
typedef enum _DODownloadPropertyEx
{
  DODownloadPropertyEx_UpdateId = 0,
  DODownloadPropertyEx_CorrelationVector,
  DODownloadPropertyEx_DecryptionInfo,    
  DODownloadPropertyEx_IntegrityCheckInfo,   
  DODownloadPropertyEx_IntegrityCheckMandatory, 
  DODownloadPropertyEx_TotalSizeBytes, 
  DODownloadPropertyEx_TempLocalFileUsage 
} DODownloadPropertyEx;
```
## <a name="constants"></a><span data-ttu-id="d818e-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="d818e-110">Constants</span></span>

| <span data-ttu-id="d818e-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d818e-111">Requirement</span></span> | <span data-ttu-id="d818e-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d818e-112">Value</span></span> |
|-|-|
| <span data-ttu-id="d818e-113">DODownloadPropertyEx_UpdateId</span><span class="sxs-lookup"><span data-stu-id="d818e-113">DODownloadPropertyEx_UpdateId</span></span> | <span data-ttu-id="d818e-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="d818e-114">Reserved.</span></span> <span data-ttu-id="d818e-115">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="d818e-115">Do not use.</span></span> |
| <span data-ttu-id="d818e-116">DODownloadPropertyEx_CorrelationVector</span><span class="sxs-lookup"><span data-stu-id="d818e-116">DODownloadPropertyEx_CorrelationVector</span></span> | <span data-ttu-id="d818e-117">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d818e-117">Optional.</span></span> <span data-ttu-id="d818e-118">Définit un vecteur de corrélation spécifique à des fins de télémétrie.</span><span class="sxs-lookup"><span data-stu-id="d818e-118">Sets a specific correlation vector for telemetry purposes.</span></span> <span data-ttu-id="d818e-119">Le type VARIANT est VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="d818e-119">VARIANT type is VT_BSTR.</span></span> |
| <span data-ttu-id="d818e-120">DODownloadPropertyEx_DecryptionInfo</span><span class="sxs-lookup"><span data-stu-id="d818e-120">DODownloadPropertyEx_DecryptionInfo</span></span> | <span data-ttu-id="d818e-121">Réservé.</span><span class="sxs-lookup"><span data-stu-id="d818e-121">Reserved.</span></span> <span data-ttu-id="d818e-122">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="d818e-122">Do not use.</span></span> |
| <span data-ttu-id="d818e-123">DODownloadPropertyEx_IntegrityCheckInfo</span><span class="sxs-lookup"><span data-stu-id="d818e-123">DODownloadPropertyEx_IntegrityCheckInfo</span></span> | <span data-ttu-id="d818e-124">Facultatif en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="d818e-124">Optional write-only.</span></span> <span data-ttu-id="d818e-125">Définit l’emplacement du fichier de hachage de l’élément (PHF), utilisé par pour effectuer des vérifications de l’intégrité du Runtime sur le contenu téléchargé.</span><span class="sxs-lookup"><span data-stu-id="d818e-125">Sets the piece hash file (PHF) location, which is used by DO to perform runtime integrity checks on the downloaded content.</span></span> <span data-ttu-id="d818e-126">Le type VARIANT est VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="d818e-126">VARIANT type is VT_BSTR.</span></span> |
| <span data-ttu-id="d818e-127">DODownloadPropertyEx_IntegrityCheckMandatory</span><span class="sxs-lookup"><span data-stu-id="d818e-127">DODownloadPropertyEx_IntegrityCheckMandatory</span></span> | <span data-ttu-id="d818e-128">Optionnel.</span><span class="sxs-lookup"><span data-stu-id="d818e-128">Optional.</span></span> <span data-ttu-id="d818e-129">Définit un indicateur booléen indiquant si l’utilisation du fichier de hachage de la pièce (PHF) est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d818e-129">Sets a boolean flag indicating whether usage of the piece hash file (PHF) is mandatory.</span></span> <span data-ttu-id="d818e-130">Si VARIANT_TRUE, le téléchargement est abandonné une fois la vérification d’intégrité en échec.</span><span class="sxs-lookup"><span data-stu-id="d818e-130">If VARIANT_TRUE, the download will be aborted once the integrity check is failed.</span></span> <span data-ttu-id="d818e-131">Le type VARIANT est VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="d818e-131">VARIANT type is VT_BOOL.</span></span> |
| <span data-ttu-id="d818e-132">DODownloadPropertyEx_TotalSizeBytes</span><span class="sxs-lookup"><span data-stu-id="d818e-132">DODownloadPropertyEx_TotalSizeBytes</span></span> | <span data-ttu-id="d818e-133">Réservé.</span><span class="sxs-lookup"><span data-stu-id="d818e-133">Reserved.</span></span> <span data-ttu-id="d818e-134">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="d818e-134">Do not use.</span></span> |
| <span data-ttu-id="d818e-135">DODownloadPropertyEx_TempLocalFileUsage</span><span class="sxs-lookup"><span data-stu-id="d818e-135">DODownloadPropertyEx_TempLocalFileUsage</span></span> | <span data-ttu-id="d818e-136">Réservé.</span><span class="sxs-lookup"><span data-stu-id="d818e-136">Reserved.</span></span> <span data-ttu-id="d818e-137">Ne pas utiliser.</span><span class="sxs-lookup"><span data-stu-id="d818e-137">Do not use.</span></span> |

## <a name="requirements"></a><span data-ttu-id="d818e-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d818e-138">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d818e-139">**Client minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="d818e-139">**Minimum supported client**</span></span> | <span data-ttu-id="d818e-140">Windows 10, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d818e-140">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="d818e-141">**Serveur minimal pris en charge**</span><span class="sxs-lookup"><span data-stu-id="d818e-141">**Minimum supported server**</span></span> | <span data-ttu-id="d818e-142">Windows Server, version 1809 \[ applications Win32 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d818e-142">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="d818e-143">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="d818e-143">**Header**</span></span> | <span data-ttu-id="d818e-144">DODownloadInternal. h</span><span class="sxs-lookup"><span data-stu-id="d818e-144">DODownloadInternal.h</span></span> |
