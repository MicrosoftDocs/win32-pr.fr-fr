---
description: Spécifie si le codec doit utiliser le filtrage médian pendant l’encodage.
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: MFPKEY_FORCEMEDIANSETTING, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38d0aa154798e2ed42a7373a6e85a4b46f8eeb7b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869554"
---
# <a name="mfpkey_forcemediansetting-property"></a><span data-ttu-id="2f905-103">MFPKEY \_ propriété FORCEMEDIANSETTING</span><span class="sxs-lookup"><span data-stu-id="2f905-103">MFPKEY\_FORCEMEDIANSETTING Property</span></span>

<span data-ttu-id="2f905-104">Spécifie si le codec doit utiliser le filtrage médian pendant l’encodage.</span><span class="sxs-lookup"><span data-stu-id="2f905-104">Specifies whether the codec should use median filtering during encoding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2f905-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2f905-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="2f905-106">\_wszWMVCForceMedianSetting g</span><span class="sxs-lookup"><span data-stu-id="2f905-106">g\_wszWMVCForceMedianSetting</span></span>

## <a name="data-type"></a><span data-ttu-id="2f905-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="2f905-107">Data Type</span></span>

<span data-ttu-id="2f905-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="2f905-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="2f905-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="2f905-109">Default Value</span></span>

<span data-ttu-id="2f905-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="2f905-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="2f905-111">Notes</span><span class="sxs-lookup"><span data-stu-id="2f905-111">Remarks</span></span>

<span data-ttu-id="2f905-112">Le filtrage médian indique au codec d’ignorer le bruit et le grain lors du calcul du mouvement entre les frames.</span><span class="sxs-lookup"><span data-stu-id="2f905-112">Median filtering tells the codec to ignore noise and grain when calculating motion between frames.</span></span> <span data-ttu-id="2f905-113">Cela peut améliorer la qualité de la vidéo très bruyante, mais peut entraîner des traces de mouvement (également appelées « artefacts de fin ») lorsqu’elle est appliquée à une vidéo source propre.</span><span class="sxs-lookup"><span data-stu-id="2f905-113">This can improve the quality of very noisy video, but can lead to motion trails (also known as trailing artifacts) when applied to clean source video.</span></span>

<span data-ttu-id="2f905-114">Par défaut, le codec utilise une logique interne pour déterminer si le filtrage médian doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="2f905-114">By default, the codec uses internal logic to determine whether median filtering should be used.</span></span> <span data-ttu-id="2f905-115">Si vous définissez cette propriété, cette logique sera remplacée.</span><span class="sxs-lookup"><span data-stu-id="2f905-115">If you set this property, that logic will be overridden.</span></span>

> [!Note]  
> <span data-ttu-id="2f905-116">Ce filtre n’est pas le même que les filtres de flou médian trouvés dans de nombreuses applications d’édition vidéo et de traitement.</span><span class="sxs-lookup"><span data-stu-id="2f905-116">This filter is not the same as median blur filters found in many video editing and post-processing applications.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2f905-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f905-117">Requirements</span></span>



| <span data-ttu-id="2f905-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f905-118">Requirement</span></span> | <span data-ttu-id="2f905-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f905-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f905-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f905-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2f905-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f905-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2f905-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f905-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2f905-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f905-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f905-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f905-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f905-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f905-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f905-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f905-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f905-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2f905-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




