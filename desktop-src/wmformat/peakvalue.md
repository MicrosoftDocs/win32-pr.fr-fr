---
title: PeakValue
description: L’attribut PeakValue contient une valeur d’amplitude de 16 bits désignant le niveau de volume maximal de contenu audio.
ms.assetid: 885f6d4c-661a-4681-96b6-c1a282c8bf18
keywords:
- Format Windows Media PeakValue
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef933ec1b10555aa4c88a24261313abb261163
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106510235"
---
# <a name="peakvalue"></a><span data-ttu-id="b19d4-104">PeakValue</span><span class="sxs-lookup"><span data-stu-id="b19d4-104">PeakValue</span></span>

<span data-ttu-id="b19d4-105">L’attribut **PeakValue** contient une valeur d’amplitude de 16 bits désignant le niveau de volume maximal de contenu audio.</span><span class="sxs-lookup"><span data-stu-id="b19d4-105">The **PeakValue** attribute contains contains a 16-bit amplitude value designating the peak volume level of audio content.</span></span> <span data-ttu-id="b19d4-106">Avec [**AverageLevel**](averagelevel.md), cet attribut est utilisé pour la normalisation.</span><span class="sxs-lookup"><span data-stu-id="b19d4-106">With [**AverageLevel**](averagelevel.md), this attribute is used for normalization.</span></span> <span data-ttu-id="b19d4-107">La normalisation est le processus qui consiste à ajuster le niveau de volume de lecture des fichiers audio afin que les parties les plus intenses de lecture des fichiers au même niveau et le volume moyen pour chacun d’eux soient identiques.</span><span class="sxs-lookup"><span data-stu-id="b19d4-107">Normalization is the process of adjusting the playback volume level of audio files so that the loudest parts of files playback at the same level and the average volume for each is the same..</span></span>

## <a name="global-constant"></a><span data-ttu-id="b19d4-108">Constante globale</span><span class="sxs-lookup"><span data-stu-id="b19d4-108">Global Constant</span></span>

<span data-ttu-id="b19d4-109">\_wszPeakValue g</span><span class="sxs-lookup"><span data-stu-id="b19d4-109">g\_wszPeakValue</span></span>

## <a name="data-type"></a><span data-ttu-id="b19d4-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="b19d4-110">Data Type</span></span>

<span data-ttu-id="b19d4-111">**\_valeur DWORD de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="b19d4-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="b19d4-112">Notes</span><span class="sxs-lookup"><span data-stu-id="b19d4-112">Remarks</span></span>

<span data-ttu-id="b19d4-113">Cet attribut est défini par l’objet writer en fonction des informations du codec.</span><span class="sxs-lookup"><span data-stu-id="b19d4-113">This attribute is set by the writer object based on information from the codec.</span></span> <span data-ttu-id="b19d4-114">Seuls les flux compressés avec l’un des codecs Windows Media Audio ont une valeur définie automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b19d4-114">Only streams compressed with one of the Windows Media Audio codecs have an automatically set value.</span></span>

<span data-ttu-id="b19d4-115">**PeakValue** n’est pas en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b19d4-115">**PeakValue** is not read-only.</span></span> <span data-ttu-id="b19d4-116">Toutefois, si le fichier est lu par le lecteur Windows Media, vous ne devez pas modifier cette valeur.</span><span class="sxs-lookup"><span data-stu-id="b19d4-116">However, if the file will be played by the Windows Media Player, you should not alter this value.</span></span> <span data-ttu-id="b19d4-117">Le lecteur Windows Media l’utilise pour normaliser les niveaux de fichiers dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="b19d4-117">The Windows Media Player uses this for normalizing the levels of files in a playlist.</span></span>

## <a name="see-also"></a><span data-ttu-id="b19d4-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b19d4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b19d4-119">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="b19d4-119">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




