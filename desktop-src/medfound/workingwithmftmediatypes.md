---
description: Utilisation des types de médias MFT
ms.assetid: 16c270ee-f246-4222-97e9-d8d0fe009155
title: Utilisation des types de médias MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98bfc996704f6069ca1d16570b33f456ea1cc115
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104211226"
---
# <a name="working-with-mft-media-types"></a><span data-ttu-id="b2c38-103">Utilisation des types de médias MFT</span><span class="sxs-lookup"><span data-stu-id="b2c38-103">Working with MFT Media Types</span></span>

<span data-ttu-id="b2c38-104">Un type de média est un moyen de décrire le format d’un flux multimédia.</span><span class="sxs-lookup"><span data-stu-id="b2c38-104">A media type is a way to describe the format of a media stream.</span></span> <span data-ttu-id="b2c38-105">Dans Media Foundation, les types de média sont représentés par l’interface **IMFMediaType** .</span><span class="sxs-lookup"><span data-stu-id="b2c38-105">In Media Foundation, media types are represented by the **IMFMediaType** interface.</span></span> <span data-ttu-id="b2c38-106">Cette interface hérite de l’interface **IMFAttributes** .</span><span class="sxs-lookup"><span data-stu-id="b2c38-106">This interface inherits the **IMFAttributes** interface.</span></span> <span data-ttu-id="b2c38-107">Les détails d’un type de média sont spécifiés en tant qu’attributs.</span><span class="sxs-lookup"><span data-stu-id="b2c38-107">The details of a media type are specified as attributes.</span></span>

<span data-ttu-id="b2c38-108">Pour créer un type de média, appelez la fonction **MFCreateMediaType** .</span><span class="sxs-lookup"><span data-stu-id="b2c38-108">To create a new media type, call the **MFCreateMediaType** function.</span></span> <span data-ttu-id="b2c38-109">Cette fonction retourne un pointeur vers l’interface **IMFMediaType** .</span><span class="sxs-lookup"><span data-stu-id="b2c38-109">This function returns a pointer to the **IMFMediaType** interface.</span></span> <span data-ttu-id="b2c38-110">Initialement, le type de média n’a pas d’attribut.</span><span class="sxs-lookup"><span data-stu-id="b2c38-110">The media type initially has no attributes.</span></span>

<span data-ttu-id="b2c38-111">Le kit de développement logiciel (SDK) Media Foundation fournit plusieurs fonctions d’assistance pour l’initialisation des types de média à partir de structures de format.</span><span class="sxs-lookup"><span data-stu-id="b2c38-111">The Media Foundation SDK provides several helper functions for initializing Media Types from format structures.</span></span> <span data-ttu-id="b2c38-112">Par exemple, la fonction **MFInitMediaTypeFromVideoInfoHeader** Initialise un type de vidéo à partir d’une structure **VIDEOINFOHEADER** , et la fonction **MFInitMediaTypeFromWaveFormatEx** Initialise un type de vidéo à partir d’une structure **WAVEFORMATEX** ou **WAVEFORMATEXTENSIBLE** .</span><span class="sxs-lookup"><span data-stu-id="b2c38-112">For example the function **MFInitMediaTypeFromVideoInfoHeader** initializes a video type from a **VIDEOINFOHEADER** structure, and the function **MFInitMediaTypeFromWaveFormatEx** initializes a video type from a **WAVEFORMATEX** or **WAVEFORMATEXTENSIBLE** structure.</span></span>

<span data-ttu-id="b2c38-113">Les types de format utilisés par les codecs sont généralement limités à ceux décrits par les structures **VIDEOINFOHEADER** et **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="b2c38-113">The format types that are used by the codecs are generally limited to those described by the **VIDEOINFOHEADER** and **WAVEFORMATEX** structures.</span></span>

<span data-ttu-id="b2c38-114">Vous trouverez plus d’informations sur la création et l’accès aux Media Foundation types de média dans la documentation du kit de développement logiciel (SDK) Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="b2c38-114">More information on creating and accessing Media Foundation media types is available in the Media Foundation SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2c38-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2c38-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2c38-116">Utilisation du codec MFTs</span><span class="sxs-lookup"><span data-stu-id="b2c38-116">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



