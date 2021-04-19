---
description: Spécifie le nombre de frames prédictifs bidirectionnels (frames B).
ms.assetid: 8bd95baa-c130-4616-8ab7-7d902162e4ed
title: MFPKEY_NUMBFRAMES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc3b0655a4a5e24b92f9699b198f10232de8edf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527418"
---
# <a name="mfpkey_numbframes-property"></a><span data-ttu-id="e6081-103">MFPKEY \_ propriété NUMBFRAMES</span><span class="sxs-lookup"><span data-stu-id="e6081-103">MFPKEY\_NUMBFRAMES Property</span></span>

<span data-ttu-id="e6081-104">Spécifie le nombre de frames prédictifs bidirectionnels (frames B).</span><span class="sxs-lookup"><span data-stu-id="e6081-104">Specifies the number of bidirectional predictive frames (B-frames).</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="e6081-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="e6081-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="e6081-106">\_wszWMVCNumBFrames g</span><span class="sxs-lookup"><span data-stu-id="e6081-106">g\_wszWMVCNumBFrames</span></span>

## <a name="data-type"></a><span data-ttu-id="e6081-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="e6081-107">Data Type</span></span>

<span data-ttu-id="e6081-108">VT-I4</span><span class="sxs-lookup"><span data-stu-id="e6081-108">VT-I4</span></span>

## <a name="default-value"></a><span data-ttu-id="e6081-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="e6081-109">Default Value</span></span>

<span data-ttu-id="e6081-110">0</span><span class="sxs-lookup"><span data-stu-id="e6081-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="e6081-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e6081-111">Remarks</span></span>

<span data-ttu-id="e6081-112">Par défaut, Windows Media Video 9 utilise uniquement les intraframes (I-frames), également appelés images clés ou frames d’ancrage, qui sont des frames entièrement encodés, et des images prédictives (images P), qui sont encodées comme une différence par rapport au frame I précédent.</span><span class="sxs-lookup"><span data-stu-id="e6081-112">By default, Windows Media Video 9 uses only intraframes (I-frames), also known as key frames or anchor frames, which are fully encoded frames, and predictive frames (P-frames), which are encoded as a difference from the previous I-frame.</span></span> <span data-ttu-id="e6081-113">Les frames B sont différents des frames P, car ils stockent à la fois les différences par rapport à l’image précédente et les différences par rapport au frame suivant.</span><span class="sxs-lookup"><span data-stu-id="e6081-113">B-frames are different from P-frames because they store both the differences from the previous frame and the differences from the following frame.</span></span>

<span data-ttu-id="e6081-114">Quand vous configurez le codec pour utiliser des frames B, il utilise le nombre spécifié d’images B entre chaque paire de frames de type I ou P.</span><span class="sxs-lookup"><span data-stu-id="e6081-114">When you configure the codec to uses B-frames, it will use the specified number of B-frames between each pair of frames of either I or P type.</span></span>

<span data-ttu-id="e6081-115">Par exemple, si une séquence de frames sans B-frames est « IPPPPPPPPI », le même encodage de séquence avec deux frames B serait « IBBPBBPBBI ».</span><span class="sxs-lookup"><span data-stu-id="e6081-115">For example, if a sequence of frames without B-frames is "IPPPPPPPPI" then the same sequence encoding with two B-frames would be "IBBPBBPBBI".</span></span>

<span data-ttu-id="e6081-116">Pour la plupart des contenus, un ou deux frames B sont appropriés.</span><span class="sxs-lookup"><span data-stu-id="e6081-116">For most content either one or two B-frames are appropriate.</span></span> <span data-ttu-id="e6081-117">À des débits de données supérieurs, une image B est normalement le choix optimal.</span><span class="sxs-lookup"><span data-stu-id="e6081-117">At higher data rates, one B-frame is normally the optimal choice.</span></span> <span data-ttu-id="e6081-118">Trois ou plus sont rarement utiles.</span><span class="sxs-lookup"><span data-stu-id="e6081-118">Three or more are rarely useful.</span></span>

<span data-ttu-id="e6081-119">La plage de valeurs valide pour cette propriété est comprise entre 0 et 7.</span><span class="sxs-lookup"><span data-stu-id="e6081-119">The valid range of values for this property is 0 to 7.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6081-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6081-120">Requirements</span></span>



| <span data-ttu-id="e6081-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6081-121">Requirement</span></span> | <span data-ttu-id="e6081-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6081-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6081-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6081-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e6081-124">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6081-124">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e6081-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6081-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e6081-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6081-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e6081-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6081-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6081-128"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6081-128"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6081-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6081-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6081-130">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e6081-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




