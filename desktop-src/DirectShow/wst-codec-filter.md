---
description: Filtre de codec WST
ms.assetid: 0a06acbf-b842-4ab6-bcf9-d2d006301d83
title: Filtre de codec WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338db987986a5f4706c144907d122eec3a0615a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320894"
---
# <a name="wst-codec-filter"></a><span data-ttu-id="8bc68-103">Filtre de codec WST</span><span class="sxs-lookup"><span data-stu-id="8bc68-103">WST Codec Filter</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8bc68-104">Ce composant a été supprimé de Windows Vista et des systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="8bc68-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="8bc68-105">Il peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8bc68-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="8bc68-106">À compter de Windows Vista, ce filtre est remplacé par le filtre VBICodec, qui est documenté dans la documentation Microsoft TV technologies.</span><span class="sxs-lookup"><span data-stu-id="8bc68-106">Starting in Windows Vista, this filter is replaced by the VBICodec filter, which is documented in the Microsoft TV Technologies documentation.</span></span>

<span data-ttu-id="8bc68-107">WST (World standard Teletext) est la norme européenne pour la transmission de données à l’aide de VBI sur des signaux de télévision analogiques PAL.</span><span class="sxs-lookup"><span data-stu-id="8bc68-107">World Standard Teletext (WST) is the European standard for data transmission using VBI on PAL analog television signals.</span></span> <span data-ttu-id="8bc68-108">Les services de sous-titrage et de données sont fournis à l’aide de cette norme.</span><span class="sxs-lookup"><span data-stu-id="8bc68-108">Both captioning and data services are provided using this standard.</span></span> <span data-ttu-id="8bc68-109">Le codec WST est un filtre en mode noyau qui reçoit des exemples bruts VBI et, éventuellement, des exemples de télétexte décodé à partir du filtre de capture via le filtre de [convertisseur tee/Sink-to-Sink](tee-sink-to-sink-converter.md) .</span><span class="sxs-lookup"><span data-stu-id="8bc68-109">The WST Codec is a kernel-mode filter that receives raw VBI samples and, optionally, decoded Teletext samples from the Capture Filter via the [Tee/Sink-to-Sink Converter](tee-sink-to-sink-converter.md) filter.</span></span> <span data-ttu-id="8bc68-110">Ce codec décode et/ou duplique les données de télétexte décodées et corrigées par erreur pour le filtre de [décodeur WST](wst-decoder-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="8bc68-110">This codec decodes and/or duplicates the decoded and forward-error-corrected Teletext data for the [WST Decoder](wst-decoder-filter.md) filter.</span></span> <span data-ttu-id="8bc68-111">Le codec WST correspond au filtre de décodeur CC pour les transmissions NTSC.</span><span class="sxs-lookup"><span data-stu-id="8bc68-111">The WST Codec corresponds to the CC Decoder filter for NTSC transmissions.</span></span> <span data-ttu-id="8bc68-112">Le décodeur WST correspond au [décodeur de ligne 21](line-21-decoder-filter.md) pour NTSC ; ces filtres créent les bitmaps qui sont envoyés au mélangeur de superposition ou au convertisseur de mixage vidéo.</span><span class="sxs-lookup"><span data-stu-id="8bc68-112">The WST Decoder corresponds to the [Line 21 Decoder](line-21-decoder-filter.md) for NTSC; these filters create the bitmaps that are sent to the Overlay Mixer or the Video Mixing Renderer.</span></span>

<span data-ttu-id="8bc68-113">Ce filtre a deux broches d’entrée, VBI et HWCC.</span><span class="sxs-lookup"><span data-stu-id="8bc68-113">This filter has two input pins, VBI and HWCC.</span></span> <span data-ttu-id="8bc68-114">Le code confidentiel VBI est utilisé pour les données de VBI brutes, et le code PIN HWCC est utilisé lorsque le décodage VBI est effectué dans le matériel par le filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="8bc68-114">The VBI pin is used for raw VBI data, and the HWCC pin is used when the VBI decoding is performed in hardware by the capture filter.</span></span> <span data-ttu-id="8bc68-115">Lorsque les données sont reçues sur le code PIN HWCC, le codec WST fonctionne en mode « pass-through » et envoie les données directement au décodeur WST sans le traiter de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="8bc68-115">When the data is received on the HWCC pin, the WST Codec operates in "pass-through" mode, and sends the data directly to the WST Decoder without processing it in any way.</span></span> <span data-ttu-id="8bc68-116">Si le filtre de capture expose un code confidentiel HWCC, il doit être connecté directement au code PIN correspondant sur le codec WST.</span><span class="sxs-lookup"><span data-stu-id="8bc68-116">If the capture filter exposes an HWCC pin, it must be connected directly to the corresponding pin on the WST Codec.</span></span>

<span data-ttu-id="8bc68-117">Le filtre de codec WST s’affiche dans la catégorie de filtre « codecs VBI de flux WDM » (**am \_ KSCATEGORY \_ VBICODEC**).</span><span class="sxs-lookup"><span data-stu-id="8bc68-117">The WST Codec filter appears in the "WDM Streaming VBI Codecs" filter category (**AM\_KSCATEGORY\_VBICODEC**).</span></span>

<span data-ttu-id="8bc68-118">Étant donné qu’il s’agit d’un filtre en mode noyau, les applications ne peuvent pas la créer directement à l’aide de **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="8bc68-118">Because this is a kernel-mode filter, applications cannot create it directly using **CoCreateInstance**.</span></span> <span data-ttu-id="8bc68-119">Utilisez plutôt l' [énumérateur du périphérique système](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="8bc68-119">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="8bc68-120">Pour plus d’informations, consultez [création de filtres de Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="8bc68-120">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8bc68-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8bc68-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bc68-122">Filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="8bc68-122">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="8bc68-123">Affichage du télétexte standard du monde</span><span class="sxs-lookup"><span data-stu-id="8bc68-123">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



