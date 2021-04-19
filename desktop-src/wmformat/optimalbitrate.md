---
title: OptimalBitrate
description: L’attribut OptimalBitrate contient la vitesse de transmission de la meilleure lecture du fichier.
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- Format Windows Media OptimalBitrate
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff71c6b64cbc4bf4ccc4f346e62a5eae066e78ce
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "106510242"
---
# <a name="optimalbitrate"></a><span data-ttu-id="0a064-104">OptimalBitrate</span><span class="sxs-lookup"><span data-stu-id="0a064-104">OptimalBitrate</span></span>

<span data-ttu-id="0a064-105">L’attribut **OptimalBitrate** contient la vitesse de transmission de la meilleure lecture du fichier.</span><span class="sxs-lookup"><span data-stu-id="0a064-105">The **OptimalBitrate** attribute contains the bit rate at which the file is best played.</span></span>

## <a name="global-constant"></a><span data-ttu-id="0a064-106">Constante globale</span><span class="sxs-lookup"><span data-stu-id="0a064-106">Global Constant</span></span>

<span data-ttu-id="0a064-107">\_wszWMOptimalBitrate g</span><span class="sxs-lookup"><span data-stu-id="0a064-107">g\_wszWMOptimalBitrate</span></span>

## <a name="data-type"></a><span data-ttu-id="0a064-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="0a064-108">Data Type</span></span>

<span data-ttu-id="0a064-109">**\_valeur DWORD de type WMT \_**</span><span class="sxs-lookup"><span data-stu-id="0a064-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="0a064-110">Notes</span><span class="sxs-lookup"><span data-stu-id="0a064-110">Remarks</span></span>

<span data-ttu-id="0a064-111">Il s’agit d’un attribut codé.</span><span class="sxs-lookup"><span data-stu-id="0a064-111">This is a coded attribute.</span></span>

<span data-ttu-id="0a064-112">Pour les fichiers qui contiennent des flux à débit binaire variable (VBR), cette valeur est le taux binaire de pointe pour les flux dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="0a064-112">For files that contain variable bit rate (VBR) streams, this value is the peak bit rate for the streams in the file.</span></span> <span data-ttu-id="0a064-113">Pour les fichiers sans VBR, cette valeur est identique à la [**vitesse de transmission**](bit-rate.md).</span><span class="sxs-lookup"><span data-stu-id="0a064-113">For files without VBR, this value is the same as [**Bitrate**](bit-rate.md).</span></span>

<span data-ttu-id="0a064-114">Cet attribut ne peut pas être dupliqué au niveau du fichier.</span><span class="sxs-lookup"><span data-stu-id="0a064-114">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="0a064-115">Si cet attribut est utilisé pour un flux individuel, il sera traité en tant que métadonnées personnalisées et ne transmettra pas sa signification normale aux objets du kit de développement logiciel (SDK) du format Windows Media.</span><span class="sxs-lookup"><span data-stu-id="0a064-115">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a064-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a064-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a064-117">**Liste d’attributs**</span><span class="sxs-lookup"><span data-stu-id="0a064-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




