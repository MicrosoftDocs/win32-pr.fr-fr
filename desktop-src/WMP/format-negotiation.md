---
title: Négociation de format
description: Négociation de format
ms.assetid: 7847d4e3-1250-4c35-88e1-52d61bf1553f
keywords:
- Plug-ins du lecteur Windows Media, négociation de format
- plug-ins, négociation de format
- plug-ins de traitement de signal numérique, négociation de format
- Plug-ins DSP, négociation de format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc805b18d3e2be081e4f85bcc5ed42aded06853
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512459"
---
# <a name="format-negotiation"></a><span data-ttu-id="9c724-107">Négociation de format</span><span class="sxs-lookup"><span data-stu-id="9c724-107">Format Negotiation</span></span>

<span data-ttu-id="9c724-108">Pour que le lecteur Windows Media et un plug-in DSP partagent des données, les deux programmes doivent s’accorder sur le format des données qu’ils traitent.</span><span class="sxs-lookup"><span data-stu-id="9c724-108">For Windows Media Player and a DSP plug-in to share data, both programs must agree on the format of the data they are processing.</span></span> <span data-ttu-id="9c724-109">Le plug-in DSP implémente les méthodes que le lecteur appelle pour déterminer les formats pris en charge par le plug-in.</span><span class="sxs-lookup"><span data-stu-id="9c724-109">The DSP plug-in implements methods that the Player calls to determine which formats the plug-in supports.</span></span> <span data-ttu-id="9c724-110">Le plug-in implémente également des méthodes que le lecteur appelle pour définir le format actuel.</span><span class="sxs-lookup"><span data-stu-id="9c724-110">The plug-in also implements methods that the Player calls to set the current format.</span></span>

<span data-ttu-id="9c724-111">Si le plug-in joue le rôle d’un objet multimédia DirextX (DMO), le lecteur Windows Media Découvre et définit les formats multimédias en appelant les méthodes de l’interface **IMediaObject** .</span><span class="sxs-lookup"><span data-stu-id="9c724-111">If the plug-in is acting as a DirextX Media Object (DMO), Windows Media Player discovers and sets media formats by calling methods of the **IMediaObject** interface.</span></span> <span data-ttu-id="9c724-112">Par exemple, le lecteur appelle à plusieurs reprises le plug-in **IMediaObject :: GetInputType** pour obtenir une liste de tous les formats d’entrée pris en charge par le plug-in.</span><span class="sxs-lookup"><span data-stu-id="9c724-112">For example, the Player calls the plug-in's **IMediaObject::GetInputType** repeatedly to get a list of all input formats supported by the plug-in.</span></span> <span data-ttu-id="9c724-113">Les plug-ins DMO utilisent la structure de **\_ \_ type de média DMO** pour organiser les informations qui spécifient un format de média.</span><span class="sxs-lookup"><span data-stu-id="9c724-113">DMO plug-ins use the **DMO\_MEDIA\_TYPE** structure to organize the information that specifies a media format.</span></span> <span data-ttu-id="9c724-114">Pour plus d’informations sur la façon dont les plug-ins DMO et le format Negotiate du lecteur, consultez [à propos de IMediaObject](about-imediaobject.md).</span><span class="sxs-lookup"><span data-stu-id="9c724-114">For more information about how DMO plug-ins and the Player negotiate format, see [About IMediaObject](about-imediaobject.md).</span></span>

<span data-ttu-id="9c724-115">Si le plug-in agit en tant que Media Foundation Transform (MFT), le lecteur Windows Media Découvre et définit les formats multimédias en appelant les méthodes de l’interface **IMFTransform** .</span><span class="sxs-lookup"><span data-stu-id="9c724-115">If the plug-in is acting as a Media Foundation Transform (MFT), Windows Media Player discovers and sets media formats by calling methods of the **IMFTransform** interface.</span></span> <span data-ttu-id="9c724-116">Par exemple, le lecteur appelle à plusieurs reprises le plug-in **IMFTransform :: GetInputAvailableType** pour obtenir une liste de tous les formats d’entrée pris en charge par le plug-in.</span><span class="sxs-lookup"><span data-stu-id="9c724-116">For example, the Player calls the plug-in's **IMFTransform::GetInputAvailableType** repeatedly to get a list of all input formats supported by the plug-in.</span></span> <span data-ttu-id="9c724-117">Les plug-ins MFT et le lecteur utilisent l’interface **IMFMediaType** pour organiser et échanger des informations de format.</span><span class="sxs-lookup"><span data-stu-id="9c724-117">MFT plug-ins and the Player use the **IMFMediaType** interface to organize and exchange format information.</span></span>

<span data-ttu-id="9c724-118">Le lecteur Windows Media utilise un plug-in audio DSP uniquement si le plug-in prend en charge la même profondeur de bits que le son numérique en cours de lecture.</span><span class="sxs-lookup"><span data-stu-id="9c724-118">Windows Media Player will use an audio DSP plug-in only if the plug-in supports the same bit depth as the digital audio being played.</span></span> <span data-ttu-id="9c724-119">Par exemple, si le son numérique est de 20 bits, le plug-in doit être écrit pour traiter le son 20 bits.</span><span class="sxs-lookup"><span data-stu-id="9c724-119">For instance, if the digital audio is 20-bit, the plug-in must be written to process 20-bit audio.</span></span> <span data-ttu-id="9c724-120">Pour les CD audio, les plug-ins DSP doivent prendre en charge le traitement 20 bits.</span><span class="sxs-lookup"><span data-stu-id="9c724-120">For CD audio, DSP plug-ins must support 20-bit processing.</span></span>

<span data-ttu-id="9c724-121">Lors de la négociation de format du contenu multicanal sur un ordinateur configuré pour être utilisé avec des enceintes stéréo, le lecteur Windows Media tente d’abord de se connecter à un plug-in audio DSP à l’aide du format d’entrée et de sortie existant en appelant **IMediaObject :: SetInputType** et **IMediaObject :: SetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="9c724-121">During format negotiation of multi-channel content on a computer configured for use with stereo speakers, Windows Media Player first attempts to connect to an audio DSP plug-in using the existing input and output format by calling **IMediaObject::SetInputType** and **IMediaObject::SetOutputType**.</span></span> <span data-ttu-id="9c724-122">Une fois cette négociation initiale effectuée, le lecteur énumère ensuite les formats pris en charge par le plug-in et tente de négocier la combinaison de format optimale pour le lecteur et le plug-in.</span><span class="sxs-lookup"><span data-stu-id="9c724-122">Once this initial negotiation occurs, the Player then enumerates the formats the plug-in supports and attempts to negotiate the best format combination for the Player and the plug-in.</span></span> <span data-ttu-id="9c724-123">Si le plug-in accepte l’audio stéréo (définie par une structure **WAVEFORMATEX** ) comme format d’entrée lors de la négociation initiale, puis accepte uniquement l’audio multicanaux (défini par une structure **WAVEFORMATEXTENSIBLE** ), le lecteur fournit un son de multicanaux comme format d’entrée au plug-in.</span><span class="sxs-lookup"><span data-stu-id="9c724-123">If the plug-in accepts stereo audio (defined by a **WAVEFORMATEX** structure) as the input format during the initial negotiation, and then subsequently accepts only multi-channel audio (defined by a **WAVEFORMATEXTENSIBLE** structure), the Player will provide multi-channel audio as the input format to the plug-in.</span></span> <span data-ttu-id="9c724-124">Ce comportement au cours de la négociation de format peut être utilisé dans le système d’exploitation Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9c724-124">This behavior during format negotiation is available for use in the Microsoft Windows XP operating system.</span></span> <span data-ttu-id="9c724-125">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="9c724-125">It may be altered or unavailable in subsequent versions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c724-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9c724-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c724-127">**Vue d’ensemble des développeurs de plug-ins DSP**</span><span class="sxs-lookup"><span data-stu-id="9c724-127">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




