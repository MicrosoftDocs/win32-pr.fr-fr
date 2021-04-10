---
title: AverageLevel
description: L’attribut AverageLevel contient une valeur d’amplitude de 16 bits désignant le niveau de volume moyen de contenu audio.
ms.assetid: e6270ac8-5de3-4dee-824c-ba25fdd272c8
keywords:
- Format Windows Media AverageLevel
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 632379e42fa6c64e44018173b9d40340add4ee61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104030211"
---
# <a name="averagelevel"></a><span data-ttu-id="df3fa-104">AverageLevel</span><span class="sxs-lookup"><span data-stu-id="df3fa-104">AverageLevel</span></span>

<span data-ttu-id="df3fa-105">L’attribut **AverageLevel** contient une valeur d’amplitude de 16 bits désignant le niveau de volume moyen de contenu audio.</span><span class="sxs-lookup"><span data-stu-id="df3fa-105">The **AverageLevel** attribute contains a 16-bit amplitude value designating the average volume level of audio content.</span></span> <span data-ttu-id="df3fa-106">Avec [**PeakValue**](peakvalue.md), cet attribut est utilisé pour la normalisation.</span><span class="sxs-lookup"><span data-stu-id="df3fa-106">With [**PeakValue**](peakvalue.md), this attribute is used for normalization.</span></span> <span data-ttu-id="df3fa-107">La normalisation est le processus qui consiste à ajuster le niveau de volume de lecture des fichiers audio afin que les parties les plus intenses de lecture des fichiers au même niveau et le volume moyen pour chaque volume soient identiques.</span><span class="sxs-lookup"><span data-stu-id="df3fa-107">Normalization is the process of adjusting the playback volume level of audio files so that the loudest parts of files playback at the same level and the average volume for each is the same.</span></span>

## <a name="global-constant"></a><span data-ttu-id="df3fa-108">Constante globale</span><span class="sxs-lookup"><span data-stu-id="df3fa-108">Global Constant</span></span>

<span data-ttu-id="df3fa-109">\_wszAverageLevel g</span><span class="sxs-lookup"><span data-stu-id="df3fa-109">g\_wszAverageLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="df3fa-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="df3fa-110">Data Type</span></span>

<span data-ttu-id="df3fa-111">**\_valeur DWORD de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="df3fa-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="df3fa-112">Notes</span><span class="sxs-lookup"><span data-stu-id="df3fa-112">Remarks</span></span>

<span data-ttu-id="df3fa-113">Cet attribut est défini par l’objet writer en fonction des informations du codec.</span><span class="sxs-lookup"><span data-stu-id="df3fa-113">This attribute is set by the writer object based on information from the codec.</span></span> <span data-ttu-id="df3fa-114">Seuls les flux compressés avec l’un des codecs Windows Media Audio ont une valeur définie automatiquement.</span><span class="sxs-lookup"><span data-stu-id="df3fa-114">Only streams compressed with one of the Windows Media Audio codecs have an automatically set value.</span></span>

<span data-ttu-id="df3fa-115">**AverageLevel** n’est pas en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="df3fa-115">**AverageLevel** is not read-only.</span></span> <span data-ttu-id="df3fa-116">Toutefois, si le fichier est lu par le lecteur Windows Media, vous ne devez pas modifier cette valeur.</span><span class="sxs-lookup"><span data-stu-id="df3fa-116">However, if the file will be played by the Windows Media Player, you should not alter this value.</span></span> <span data-ttu-id="df3fa-117">Le lecteur Windows Media l’utilise pour normaliser les niveaux de fichiers dans une sélection.</span><span class="sxs-lookup"><span data-stu-id="df3fa-117">The Windows Media Player uses this for normalizing the levels of files in a playlist.</span></span>

## <a name="see-also"></a><span data-ttu-id="df3fa-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df3fa-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df3fa-119">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="df3fa-119">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




