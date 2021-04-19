---
title: EQUALIZERSETTINGS. normalisation
description: L’attribut de normalisation spécifie ou récupère une valeur indiquant si la normalisation est activée.
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- EQUALIZERSETTINGS. normalisation du lecteur Windows Media
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9714359e5d5e2af0c82a0d687555f7cfcbf1cf70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528677"
---
# <a name="equalizersettingsnormalization"></a><span data-ttu-id="57f55-104">EQUALIZERSETTINGS. normalisation</span><span class="sxs-lookup"><span data-stu-id="57f55-104">EQUALIZERSETTINGS.normalization</span></span>

<span data-ttu-id="57f55-105">L’attribut de **normalisation** spécifie ou récupère une valeur indiquant si la normalisation est activée.</span><span class="sxs-lookup"><span data-stu-id="57f55-105">The **normalization** attribute specifies or retrieves a value indicating whether normalization is enabled.</span></span>

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a><span data-ttu-id="57f55-106">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="57f55-106">Possible Values</span></span>

<span data-ttu-id="57f55-107">Cet attribut est une **valeur booléenne** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="57f55-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="57f55-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="57f55-108">Value</span></span> | <span data-ttu-id="57f55-109">Description</span><span class="sxs-lookup"><span data-stu-id="57f55-109">Description</span></span>                         |
|-------|-------------------------------------|
| <span data-ttu-id="57f55-110">true</span><span class="sxs-lookup"><span data-stu-id="57f55-110">true</span></span>  | <span data-ttu-id="57f55-111">La normalisation est activée.</span><span class="sxs-lookup"><span data-stu-id="57f55-111">Normalization is enabled.</span></span>           |
| <span data-ttu-id="57f55-112">false</span><span class="sxs-lookup"><span data-stu-id="57f55-112">false</span></span> | <span data-ttu-id="57f55-113">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="57f55-113">Default.</span></span> <span data-ttu-id="57f55-114">La normalisation est désactivée.</span><span class="sxs-lookup"><span data-stu-id="57f55-114">Normalization is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="57f55-115">Notes</span><span class="sxs-lookup"><span data-stu-id="57f55-115">Remarks</span></span>

<span data-ttu-id="57f55-116">Lorsque la normalisation est activée, le signal audio d’un fichier multimédia numérique entier est mis à l’échelle jusqu’à la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="57f55-116">When normalization is enabled, the audio signal for an entire digital media file is scaled up to the maximum value.</span></span> <span data-ttu-id="57f55-117">Cela permet à plusieurs fichiers d’être lus à peu près du même volume sans nécessiter de réglages de volume.</span><span class="sxs-lookup"><span data-stu-id="57f55-117">This allows multiple files to be played at approximately the same volume without requiring volume adjustments.</span></span>

## <a name="requirements"></a><span data-ttu-id="57f55-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57f55-118">Requirements</span></span>



| <span data-ttu-id="57f55-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57f55-119">Requirement</span></span> | <span data-ttu-id="57f55-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="57f55-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="57f55-121">Version</span><span class="sxs-lookup"><span data-stu-id="57f55-121">Version</span></span><br/> | <span data-ttu-id="57f55-122">Lecteur Windows Media série 9 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="57f55-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="57f55-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57f55-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57f55-124">**Élément EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="57f55-124">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="57f55-125">**EQUALIZERSETTINGS.normalizationAverage**</span><span class="sxs-lookup"><span data-stu-id="57f55-125">**EQUALIZERSETTINGS.normalizationAverage**</span></span>](equalizersettings-normalizationaverage.md)
</dt> <dt>

[<span data-ttu-id="57f55-126">**EQUALIZERSETTINGS.normalizationPeak**</span><span class="sxs-lookup"><span data-stu-id="57f55-126">**EQUALIZERSETTINGS.normalizationPeak**</span></span>](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 





