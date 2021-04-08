---
description: Filtre de décodeur CC
ms.assetid: 57ef75f6-411c-4b1f-b0dc-ac293ebc0b9c
title: Filtre de décodeur CC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93995207e4f1a397db28f743d1f972b871b0553
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950036"
---
# <a name="cc-decoder-filter"></a><span data-ttu-id="5406a-103">Filtre de décodeur CC</span><span class="sxs-lookup"><span data-stu-id="5406a-103">CC Decoder Filter</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5406a-104">Ce composant a été supprimé de Windows Vista et des systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="5406a-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="5406a-105">Il peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="5406a-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="5406a-106">Le décodeur CC VBI est un filtre de classe de flux en mode noyau.</span><span class="sxs-lookup"><span data-stu-id="5406a-106">The CC VBI Decoder is a kernel-mode stream class filter.</span></span> <span data-ttu-id="5406a-107">Il apparaît dans GraphEdit sous la catégorie « codecs VBI de streaming WDM ».</span><span class="sxs-lookup"><span data-stu-id="5406a-107">It appears in GraphEdit under the "WDM Streaming VBI Codecs" category.</span></span> <span data-ttu-id="5406a-108">Il accepte les exemples d’onde fournis par un filtre de capture et fournit des données décodées de sous-titrage au [décodeur de ligne 21](line-21-decoder-filter.md) et/ou aux applications intéressées.</span><span class="sxs-lookup"><span data-stu-id="5406a-108">It accepts sample waveforms delivered by a capture filter and delivers decoded closed-captioning data to the [Line 21 Decoder](line-21-decoder-filter.md) and/or to interested applications.</span></span>

<span data-ttu-id="5406a-109">Ce filtre a deux broches d’entrée, VBI et HWCC.</span><span class="sxs-lookup"><span data-stu-id="5406a-109">This filter has two input pins, VBI and HWCC.</span></span> <span data-ttu-id="5406a-110">Le code confidentiel VBI est utilisé pour les données de VBI brutes, et le code PIN HWCC est utilisé lorsque le décodage VBI est effectué dans le matériel par le filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="5406a-110">The VBI pin is used for raw VBI data, and the HWCC pin is used when the VBI decoding is performed in hardware by the capture filter.</span></span> <span data-ttu-id="5406a-111">Lorsque les données sont reçues sur le code confidentiel HWCC, le décodeur CC fonctionne en mode « pass-through » et envoie les données directement au décodeur de ligne 21 sans le traiter de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="5406a-111">When the data is received on the HWCC pin, the CC Decoder operates in "pass-through" mode, and sends the data directly to the Line 21 Decoder without processing it in any way.</span></span> <span data-ttu-id="5406a-112">Si le filtre de capture expose un code confidentiel HWCC, il doit être connecté directement au code PIN correspondant sur le décodeur CC.</span><span class="sxs-lookup"><span data-stu-id="5406a-112">If the capture filter exposes an HWCC pin, it must be connected directly to the corresponding pin on the CC Decoder.</span></span> <span data-ttu-id="5406a-113">La catégorie pin est **PINNAME \_ vidéo \_ cc \_ capture**.</span><span class="sxs-lookup"><span data-stu-id="5406a-113">The pin category is **PINNAME\_VIDEO\_CC\_CAPTURE**.</span></span>

<span data-ttu-id="5406a-114">Le décodeur CC contient jusqu’à huit broches de sortie, chacune pouvant sélectionner ses propres lignes et sous-flux.</span><span class="sxs-lookup"><span data-stu-id="5406a-114">The CC Decoder has up to eight output pins, each of which can select their own lines and substreams.</span></span> <span data-ttu-id="5406a-115">La première broche de sortie est connectée au décodeur Line-21.</span><span class="sxs-lookup"><span data-stu-id="5406a-115">The first output pin is connected to the Line-21 Decoder.</span></span>

<span data-ttu-id="5406a-116">Le filtre de décodeur CC apparaît dans la catégorie de filtre « codecs VBI de flux WDM » (**am \_ KSCATEGORY \_ VBICODEC**).</span><span class="sxs-lookup"><span data-stu-id="5406a-116">The CC Decoder filter appears in the "WDM Streaming VBI Codecs" filter category (**AM\_KSCATEGORY\_VBICODEC**).</span></span>

<span data-ttu-id="5406a-117">Étant donné qu’il s’agit d’un filtre en mode noyau, les applications ne peuvent pas la créer directement à l’aide de **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="5406a-117">Because this is a kernel-mode filter, applications cannot create it directly using **CoCreateInstance**.</span></span> <span data-ttu-id="5406a-118">Utilisez plutôt l' [énumérateur du périphérique système](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="5406a-118">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="5406a-119">Pour plus d’informations, consultez [création de filtres de Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="5406a-119">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5406a-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5406a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5406a-121">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="5406a-121">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="5406a-122">Affichage des sous-titres</span><span class="sxs-lookup"><span data-stu-id="5406a-122">Viewing Closed Captions</span></span>](viewing-closed-captions.md)
</dt> </dl>

 

 



