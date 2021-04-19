---
description: Utilisation des objets codec et DSP
ms.assetid: ec571d31-6542-421a-8027-d4c61ce00035
title: Utilisation des objets codec et DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a88670298bfc16ca1dc5053cabeb4f4e631c5c47
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106535743"
---
# <a name="using-the-codec-and-dsp-objects"></a><span data-ttu-id="569f0-103">Utilisation des objets codec et DSP</span><span class="sxs-lookup"><span data-stu-id="569f0-103">Using the Codec and DSP Objects</span></span>

<span data-ttu-id="569f0-104">Il existe plusieurs façons d’utiliser la Windows Media Audio et les codecs vidéo et DSP pour encoder, décoder ou transformer votre contenu multimédia numérique.</span><span class="sxs-lookup"><span data-stu-id="569f0-104">There are several ways to use the Windows Media Audio and Video codecs and DSPs to encode, decode, or transform your digital media content.</span></span> <span data-ttu-id="569f0-105">Le codec Windows Media Audio et vidéo et l’API DSP sont destinés aux utilisateurs qui doivent configurer les objets codec et DSP manuellement ou les utiliser en dehors du contexte de l’un des kits de développement logiciel (SDK) Windows Media, tels que le kit de développement logiciel (SDK) Windows Media format ou le kit de développement logiciel (SDK) Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="569f0-105">The Windows Media Audio and Video Codec and DSP API is intended for those users who need to configure codec and DSP objects manually or use them outside of the context one of the Windows Media SDKs, such as the Windows Media Format SDK or Media Foundation SDK.</span></span>

<span data-ttu-id="569f0-106">Les créateurs de contenu et les utilisateurs finaux peuvent utiliser un large éventail d’outils et d’applications pour encoder du contenu dans des flux de Windows Media Audio ou Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="569f0-106">Content creators and end users can use a variety of tools and applications to encode content in Windows Media Audio or Windows Media Video streams.</span></span> <span data-ttu-id="569f0-107">Windows Media Encoder, par exemple, est spécifiquement conçu pour faciliter le processus d’encodage.</span><span class="sxs-lookup"><span data-stu-id="569f0-107">Windows Media Encoder, for example, is specifically designed to make the encoding process easy.</span></span> <span data-ttu-id="569f0-108">De même, le lecteur Windows Media est spécialement conçu pour fonctionner correctement avec les données multimédias numériques qui sont codées dans les formats Windows Media.</span><span class="sxs-lookup"><span data-stu-id="569f0-108">Likewise, Windows Media Player is specially designed to work well with digital media data that is encoded in Windows Media formats.</span></span> <span data-ttu-id="569f0-109">Pour de nombreuses applications, l’utilisation du kit de développement logiciel (SDK) Windows Media Encoder ou du kit SDK Windows Media Player est tout ce qui est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="569f0-109">For many applications, using the Windows Media Encoder SDK or the Windows Media Player SDK is all that is needed.</span></span> <span data-ttu-id="569f0-110">En particulier, ces deux technologies conviennent parfaitement aux scénarios qui ressemblent à la fonctionnalité des outils qu’elles automatisent.</span><span class="sxs-lookup"><span data-stu-id="569f0-110">In particular, these two technologies are good for scenarios that resemble the functionality of the tools they automate.</span></span>

<span data-ttu-id="569f0-111">Si vous avez besoin d’un meilleur contrôle sur le processus d’encodage ou de décodage, mais que vous envisagez d’utiliser le format ASF (Advanced Systems Format) comme conteneur pour vos données multimédias, le kit de développement logiciel (SDK) du format Windows Media peut être un bon choix.</span><span class="sxs-lookup"><span data-stu-id="569f0-111">If you need greater control over the encoding or decoding process, but you still intend to use the Advanced Systems Format (ASF) as a container for your media data, the Windows Media Format SDK might be a good choice.</span></span> <span data-ttu-id="569f0-112">Les objets du kit de développement logiciel (SDK) du format Windows Media offrent une infrastructure flexible pour la création de fichiers ASF et offrent une prise en charge intégrée des codecs vidéo et Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="569f0-112">The objects of the Windows Media Format SDK provide a flexible framework for creating ASF files, and provide built-in support for the Windows Media Audio and Video codecs.</span></span>

<span data-ttu-id="569f0-113">Le kit de développement logiciel (SDK) Media Foundation, qui est nouveau pour Windows Vista, simplifie grandement l’encodage et le décodage en fournissant un pipeline de média personnalisable.</span><span class="sxs-lookup"><span data-stu-id="569f0-113">The Media Foundation SDK, which is new for Windows Vista, greatly simplifies encoding and decoding by providing a customizable media pipeline.</span></span> <span data-ttu-id="569f0-114">Vous pouvez définir les propriétés du média d’entrée et de sortie et le chargeur de topologie Media Foundation configurera les codecs et les DSP nécessaires pour vous.</span><span class="sxs-lookup"><span data-stu-id="569f0-114">You can set input and output media properties and the Media Foundation topology loader will configure the necessary codecs and DSPs for you.</span></span>

<span data-ttu-id="569f0-115">La raison principale de l’utilisation directe des objets codec est l’utilisation des codecs Windows Media Audio et vidéo en dehors du conteneur ASF.</span><span class="sxs-lookup"><span data-stu-id="569f0-115">The primary reason for using the codec objects directly is to use the Windows Media Audio and Video codecs outside of the ASF container.</span></span> <span data-ttu-id="569f0-116">L’utilisation des objets codec et DSP fournit également un niveau de contrôle qui n’est pas disponible à l’aide des technologies les plus abstraites.</span><span class="sxs-lookup"><span data-stu-id="569f0-116">Using the codec and DSP objects also provides a level of control that is unavailable using any of the more abstracted technologies.</span></span>

## <a name="related-topics"></a><span data-ttu-id="569f0-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="569f0-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="569f0-118">Codecs Windows Media</span><span class="sxs-lookup"><span data-stu-id="569f0-118">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



