---
title: ASFLeakyBucketPairs
description: L’attribut ASFLeakyBucketPairs est un attribut facultatif qui décrit les exigences de mise en mémoire tampon pour un fichier de vitesse de transmission variable.
ms.assetid: d1b3e8cc-c082-4283-88bc-172f58adf2d9
keywords:
- Format Windows Media ASFLeakyBucketPairs
topic_type:
- apiref
api_name:
- ASFLeakyBucketPairs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e94bfa6084c67428fb89e57b9152283cc3d4a3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106530787"
---
# <a name="asfleakybucketpairs"></a><span data-ttu-id="74ae3-104">ASFLeakyBucketPairs</span><span class="sxs-lookup"><span data-stu-id="74ae3-104">ASFLeakyBucketPairs</span></span>

<span data-ttu-id="74ae3-105">L’attribut **ASFLeakyBucketPairs** est un attribut facultatif qui décrit les exigences de mise en mémoire tampon pour un fichier de vitesse de transmission variable.</span><span class="sxs-lookup"><span data-stu-id="74ae3-105">The **ASFLeakyBucketPairs** attribute is an optional attribute that describes the buffering requirements for a variable bit rate file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="74ae3-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="74ae3-106">Global Constant</span></span>

<span data-ttu-id="74ae3-107">\_wszASFLeakyBucketPairs g</span><span class="sxs-lookup"><span data-stu-id="74ae3-107">g\_wszASFLeakyBucketPairs</span></span>

## <a name="data-type"></a><span data-ttu-id="74ae3-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="74ae3-108">Data Type</span></span>

<span data-ttu-id="74ae3-109">**\_binaire de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="74ae3-109">**WMT\_TYPE\_BINARY**</span></span>

## <a name="remarks"></a><span data-ttu-id="74ae3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="74ae3-110">Remarks</span></span>

<span data-ttu-id="74ae3-111">Cet attribut a le format suivant :</span><span class="sxs-lookup"><span data-stu-id="74ae3-111">This attribute has the following format:</span></span>

``` syntax
struct
{
    WORD wReserved;
    WM_LEAKY_BUCKET_PAIR bucket[2];
};
```

<span data-ttu-id="74ae3-112">Où *wReserved* doit être égal à zéro et *compartiment* est un tableau de structures de [**\_ \_ \_ paires de compartiments WM Leaky**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) .</span><span class="sxs-lookup"><span data-stu-id="74ae3-112">Where *wReserved* must equal zero, and *bucket* is an array of [**WM\_LEAKY\_BUCKET\_PAIR**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_leaky_bucket_pair) structures.</span></span> <span data-ttu-id="74ae3-113">Le tableau doit contenir au moins deux entrées, mais peut être plus grande.</span><span class="sxs-lookup"><span data-stu-id="74ae3-113">The array must contain at least two entries, but can be larger.</span></span> <span data-ttu-id="74ae3-114">L’objet lecteur utilise cet attribut pour déterminer la quantité de contenu à mettre en mémoire tampon avant la lecture.</span><span class="sxs-lookup"><span data-stu-id="74ae3-114">The reader object uses this attribute to determine the amount of content to buffer before playback.</span></span>

## <a name="see-also"></a><span data-ttu-id="74ae3-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74ae3-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74ae3-116">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="74ae3-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




