---
description: Spécifie si le codec doit tenter de détecter les bords bruyants du cadre et les supprimer.
ms.assetid: fdb4f3a8-1447-4e1e-a208-0f9b717f7626
title: MFPKEY_NOISEEDGEREMOVAL, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30acd92bae7693d0714e42d6b4f832a521557bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202346"
---
# <a name="mfpkey_noiseedgeremoval-property"></a><span data-ttu-id="9673b-103">MFPKEY \_ propriété NOISEEDGEREMOVAL</span><span class="sxs-lookup"><span data-stu-id="9673b-103">MFPKEY\_NOISEEDGEREMOVAL Property</span></span>

<span data-ttu-id="9673b-104">Spécifie si le codec doit tenter de détecter les bords bruyants du cadre et les supprimer.</span><span class="sxs-lookup"><span data-stu-id="9673b-104">Specifies whether the codec should attempt to detect noisy frame edges and remove them.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="9673b-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="9673b-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="9673b-106">\_wszWMVCNoiseEdgeRemoval g</span><span class="sxs-lookup"><span data-stu-id="9673b-106">g\_wszWMVCNoiseEdgeRemoval</span></span>

## <a name="data-type"></a><span data-ttu-id="9673b-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="9673b-107">Data Type</span></span>

<span data-ttu-id="9673b-108">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="9673b-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="9673b-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="9673b-109">Default Value</span></span>

<span data-ttu-id="9673b-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="9673b-110">FALSE</span></span>

## <a name="remarks"></a><span data-ttu-id="9673b-111">Notes</span><span class="sxs-lookup"><span data-stu-id="9673b-111">Remarks</span></span>

<span data-ttu-id="9673b-112">En règle générale, un bord de cadre bruyant est le nombre de données de l’intervalle de occultation verticale (VBI) d’une image de télévision.</span><span class="sxs-lookup"><span data-stu-id="9673b-112">A noisy frame edge is usually the vertical blanking interval (VBI) data from a frame of broadcast television.</span></span> <span data-ttu-id="9673b-113">Le VBI correspond aux 21 premières lignes de balayage du cadre de télévision.</span><span class="sxs-lookup"><span data-stu-id="9673b-113">The VBI is the first 21 scan lines of the television frame.</span></span> <span data-ttu-id="9673b-114">Ces lignes de numérisation ne contiennent pas de données vidéo, elles contiennent des données sur la diffusion.</span><span class="sxs-lookup"><span data-stu-id="9673b-114">These scan lines do not contain video data—they contain data about the broadcast.</span></span> <span data-ttu-id="9673b-115">Lorsqu’un signal de télévision est enregistré par une carte de capture, le VBI est généralement supprimé du cadre.</span><span class="sxs-lookup"><span data-stu-id="9673b-115">When a television signal is recorded by a capture card, the VBI is usually removed from the frame.</span></span> <span data-ttu-id="9673b-116">La détection et la correction des bords bruyants effectuées par le codec peuvent uniquement corriger une arête qui a au moins trois lignes de bruit.</span><span class="sxs-lookup"><span data-stu-id="9673b-116">The noisy edge detection and correction performed by the codec can only correct an edge that has three or fewer lines of noise.</span></span> <span data-ttu-id="9673b-117">Si la vidéo capturée contient plus de trois lignes bruyantes, il y a un problème avec le matériel utilisé pour capturer la vidéo.</span><span class="sxs-lookup"><span data-stu-id="9673b-117">If captured video contains more than three noisy lines, there is a problem with the hardware used to capture the video.</span></span>

<span data-ttu-id="9673b-118">Si le codec est défini pour supprimer les bords bruyants, il duplique les lignes adjacentes à la périphérie bruyante pour remplir le cadre.</span><span class="sxs-lookup"><span data-stu-id="9673b-118">If the codec is set to remove noisy edges, it duplicates lines adjacent to the noisy edge to fill in the frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="9673b-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9673b-119">Requirements</span></span>



| <span data-ttu-id="9673b-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9673b-120">Requirement</span></span> | <span data-ttu-id="9673b-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9673b-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9673b-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9673b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9673b-123">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9673b-123">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9673b-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9673b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9673b-125">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9673b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9673b-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9673b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9673b-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9673b-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9673b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9673b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9673b-129">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9673b-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




