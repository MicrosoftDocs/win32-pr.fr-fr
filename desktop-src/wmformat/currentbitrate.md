---
title: CurrentBitrate
description: L’attribut CurrentBitrate contient la vitesse de transmission totale actuelle des flux actifs dans le fichier.
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- Format Windows Media CurrentBitrate
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdcd8db7d60c65bcb7ceedcac4498ac650f90d9a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106543042"
---
# <a name="currentbitrate"></a><span data-ttu-id="eadf7-104">CurrentBitrate</span><span class="sxs-lookup"><span data-stu-id="eadf7-104">CurrentBitrate</span></span>

<span data-ttu-id="eadf7-105">L’attribut CurrentBitrate contient la vitesse de transmission totale actuelle des flux actifs dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="eadf7-105">The CurrentBitrate attribute contains the current total bit rate of the active streams in the file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="eadf7-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="eadf7-106">Global Constant</span></span>

<span data-ttu-id="eadf7-107">\_wszWMCurrentBitrate g</span><span class="sxs-lookup"><span data-stu-id="eadf7-107">g\_wszWMCurrentBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="eadf7-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="eadf7-108">Data Type</span></span>

<span data-ttu-id="eadf7-109">**\_valeur DWORD de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="eadf7-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="eadf7-110">Notes</span><span class="sxs-lookup"><span data-stu-id="eadf7-110">Remarks</span></span>

<span data-ttu-id="eadf7-111">Il s’agit d’un attribut codé.</span><span class="sxs-lookup"><span data-stu-id="eadf7-111">This is a coded attribute.</span></span>

<span data-ttu-id="eadf7-112">La valeur récupérée pour **CurrentBitrate** est différente selon l’objet utilisé.</span><span class="sxs-lookup"><span data-stu-id="eadf7-112">The value retrieved for **CurrentBitrate** is different depending upon the object used.</span></span> <span data-ttu-id="eadf7-113">Dans le lecteur ou l’objet lecteur synchrone, la valeur est la vitesse de transmission réelle au moment de l’appel.</span><span class="sxs-lookup"><span data-stu-id="eadf7-113">In the reader or synchronous reader object, the value is the actual bit rate at the time of the call.</span></span> <span data-ttu-id="eadf7-114">Dans l’objet de l’éditeur de métadonnées, la valeur correspond à la vitesse de transmission moyenne du fichier.</span><span class="sxs-lookup"><span data-stu-id="eadf7-114">In the metadata editor object, the value is the average bit rate of the file.</span></span>

<span data-ttu-id="eadf7-115">La vitesse de transmission réelle d’un fichier est égale à la vitesse de transmission de tous les flux actifs, plus une surcharge.</span><span class="sxs-lookup"><span data-stu-id="eadf7-115">The actual bit rate of a file is equal to the bit rates of all active streams plus some overhead.</span></span> <span data-ttu-id="eadf7-116">Il s’agit de la valeur qui, par exemple, est affichée lors de la lecture d’un fichier avec le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="eadf7-116">This is the value that is, for example, displayed when playing a file with the Windows Media Player.</span></span>

<span data-ttu-id="eadf7-117">Cet attribut ne peut pas être dupliqué au niveau du fichier.</span><span class="sxs-lookup"><span data-stu-id="eadf7-117">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="eadf7-118">Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="eadf7-118">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="eadf7-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eadf7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eadf7-120">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="eadf7-120">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




