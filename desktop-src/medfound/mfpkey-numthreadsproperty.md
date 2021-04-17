---
description: Spécifie le nombre de threads qui seront utilisés par l’encodeur.
ms.assetid: 2f463cba-2512-455d-9ce1-8797682d4d67
title: MFPKEY_NUMTHREADS, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93f6d38e3bb79bbb692f9bec1b1dc0edb232d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528665"
---
# <a name="mfpkey_numthreads-property"></a><span data-ttu-id="2e2ff-103">MFPKEY \_ propriété NUMTHREADS</span><span class="sxs-lookup"><span data-stu-id="2e2ff-103">MFPKEY\_NUMTHREADS Property</span></span>

<span data-ttu-id="2e2ff-104">Spécifie le nombre de threads qui seront utilisés par l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="2e2ff-104">Specifies the number of threads that the encoder will use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2e2ff-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2e2ff-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2e2ff-106">\_wszWMVCNumThreads g</span><span class="sxs-lookup"><span data-stu-id="2e2ff-106">g\_wszWMVCNumThreads</span></span>

## <a name="data-type"></a><span data-ttu-id="2e2ff-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="2e2ff-107">Data Type</span></span>

<span data-ttu-id="2e2ff-108">VT \_</span><span class="sxs-lookup"><span data-stu-id="2e2ff-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="2e2ff-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="2e2ff-109">Default Value</span></span>

<span data-ttu-id="2e2ff-110">1</span><span class="sxs-lookup"><span data-stu-id="2e2ff-110">1</span></span>

## <a name="remarks"></a><span data-ttu-id="2e2ff-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2e2ff-111">Remarks</span></span>

<span data-ttu-id="2e2ff-112">Cette valeur est destinée à diviser l’encodage en plusieurs threads pour tirer parti des ordinateurs avec plusieurs processeurs.</span><span class="sxs-lookup"><span data-stu-id="2e2ff-112">This value is intended to divide encoding into multiple threads to take advantage of computers with multiple processors.</span></span> <span data-ttu-id="2e2ff-113">Le fractionnement des tâches d’encodage en plusieurs threads peut entraîner une légère diminution de la qualité par rapport à un seul thread.</span><span class="sxs-lookup"><span data-stu-id="2e2ff-113">Splitting encoding tasks into multiple threads can cause a slight decrease in quality as compared to a single thread.</span></span>

<span data-ttu-id="2e2ff-114">Pour l’encodeur vidéo (wmvencod.dll) fourni avec Windows XP et Windows Vista, cette propriété doit avoir la valeur 1, 2 ou 4.</span><span class="sxs-lookup"><span data-stu-id="2e2ff-114">For the video encoder (wmvencod.dll) released with Windows XP and Windows Vista, this property should be set to 1, 2, or 4.</span></span> <span data-ttu-id="2e2ff-115">Les autres valeurs sont arrondies à la valeur inférieure.</span><span class="sxs-lookup"><span data-stu-id="2e2ff-115">Other values will be rounded down.</span></span>

<span data-ttu-id="2e2ff-116">Pour l’encodeur vidéo (wmvencod.dll) fourni avec Windows 7, cette propriété doit avoir la valeur 1, 2, 4 ou 8.</span><span class="sxs-lookup"><span data-stu-id="2e2ff-116">For the video encoder (wmvencod.dll) released with Windows 7, this property should be set to 1, 2, 4, or 8.</span></span> <span data-ttu-id="2e2ff-117">Les autres valeurs sont arrondies à la valeur inférieure.</span><span class="sxs-lookup"><span data-stu-id="2e2ff-117">Other values will be rounded down.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e2ff-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e2ff-118">Requirements</span></span>



| <span data-ttu-id="2e2ff-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e2ff-119">Requirement</span></span> | <span data-ttu-id="2e2ff-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e2ff-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e2ff-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e2ff-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2e2ff-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e2ff-122">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2e2ff-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e2ff-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2e2ff-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e2ff-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2e2ff-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e2ff-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e2ff-126"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e2ff-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e2ff-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e2ff-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e2ff-128">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2e2ff-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




