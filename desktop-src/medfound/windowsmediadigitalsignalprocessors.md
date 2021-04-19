---
description: Processeurs de signaux numériques
ms.assetid: cd3952ca-3958-4944-8fde-f0163a47bff9
title: Processeurs de signaux numériques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0961554d9c9902e68f74c6b2b57662b23846614f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106531450"
---
# <a name="digital-signal-processors"></a><span data-ttu-id="580fe-103">Processeurs de signaux numériques</span><span class="sxs-lookup"><span data-stu-id="580fe-103">Digital Signal Processors</span></span>

<span data-ttu-id="580fe-104">Cette section décrit les objets DSP (digital signal Processor) fournis par Windows.</span><span class="sxs-lookup"><span data-stu-id="580fe-104">This section describes the digital signal processor (DSP) objects provided by Windows.</span></span>

<span data-ttu-id="580fe-105">Microsoft utilise le terme « *processeur de signal numérique* » pour désigner un ensemble d’objets COM qui effectuent des transformations sur des données audio et vidéo non compressées.</span><span class="sxs-lookup"><span data-stu-id="580fe-105">Microsoft uses the term *digital signal processor* to designate a set of COM objects that perform transformations on uncompressed audio and video data.</span></span> <span data-ttu-id="580fe-106">Les DSP décrits dans ce kit de développement logiciel (SDK) transforment l’audio et la vidéo dans différents formats non compressés.</span><span class="sxs-lookup"><span data-stu-id="580fe-106">The DSPs described in this SDK transform audio and video in a variety of uncompressed formats.</span></span>

<span data-ttu-id="580fe-107">Les DSP peuvent être utilisés par eux-mêmes, ou en combinaison avec des codecs audio et vidéo.</span><span class="sxs-lookup"><span data-stu-id="580fe-107">The DSPs can be used by themselves, or in combination with audio and video codecs.</span></span> <span data-ttu-id="580fe-108">À l’exception du DSP de capture vocale, chaque DSP répertorié ici implémente deux interfaces distinctes mais similaires.</span><span class="sxs-lookup"><span data-stu-id="580fe-108">With the exception of the Voice Capture DSP, each DSP listed here implements two separate but similar interfaces.</span></span>



| <span data-ttu-id="580fe-109">Interface</span><span class="sxs-lookup"><span data-stu-id="580fe-109">Interface</span></span>                              | <span data-ttu-id="580fe-110">Description</span><span class="sxs-lookup"><span data-stu-id="580fe-110">Description</span></span>                                 |
|----------------------------------------|---------------------------------------------|
| [<span data-ttu-id="580fe-111">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="580fe-111">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | <span data-ttu-id="580fe-112">Compatible avec Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="580fe-112">Compatible with Microsoft Media Foundation.</span></span> |
| [<span data-ttu-id="580fe-113">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="580fe-113">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | <span data-ttu-id="580fe-114">Compatible avec DirectShow.</span><span class="sxs-lookup"><span data-stu-id="580fe-114">Compatible with DirectShow.</span></span>                 |



 

<span data-ttu-id="580fe-115">Vous pouvez configurer le DSP à l’aide de l’interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pour définir les propriétés.</span><span class="sxs-lookup"><span data-stu-id="580fe-115">You can configure the DSPs by using the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface to set properties.</span></span> <span data-ttu-id="580fe-116">Certains DSP ont des interfaces supplémentaires qui définissent des propriétés.</span><span class="sxs-lookup"><span data-stu-id="580fe-116">Some of the DSPs have additional interfaces that set properties.</span></span> <span data-ttu-id="580fe-117">Pour utiliser ces interfaces, appelez la méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de toute autre interface du DSP.</span><span class="sxs-lookup"><span data-stu-id="580fe-117">To use these interfaces, call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of any other interface of the DSP.</span></span> <span data-ttu-id="580fe-118">La rubrique de référence pour chaque DSP répertorie les propriétés, interfaces et autres fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="580fe-118">The reference topic for each DSP lists the supported properties, interfaces, and other features.</span></span>

<span data-ttu-id="580fe-119">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="580fe-119">This section contains the following topics.</span></span>



| <span data-ttu-id="580fe-120">DSP</span><span class="sxs-lookup"><span data-stu-id="580fe-120">DSP</span></span>                                                      | <span data-ttu-id="580fe-121">Description</span><span class="sxs-lookup"><span data-stu-id="580fe-121">Description</span></span>                                          |
|----------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="580fe-122">Modèle de rééchantillonnage audio DSP</span><span class="sxs-lookup"><span data-stu-id="580fe-122">Audio Resampler DSP</span></span>](audioresampler.md)                | <span data-ttu-id="580fe-123">Convertit le taux d’échantillonnage d’un flux audio.</span><span class="sxs-lookup"><span data-stu-id="580fe-123">Converts the sampling rate of an audio stream.</span></span>       |
| [<span data-ttu-id="580fe-124">Transformation de contrôle de couleur DSP</span><span class="sxs-lookup"><span data-stu-id="580fe-124">Color Control Transform DSP</span></span>](colorcontroltransform.md) | <span data-ttu-id="580fe-125">Ajuste les caractéristiques de couleur d’un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="580fe-125">Adjusts the color characteristics of a video stream.</span></span> |
| [<span data-ttu-id="580fe-126">Convertisseur de couleurs DSP</span><span class="sxs-lookup"><span data-stu-id="580fe-126">Color Converter DSP</span></span>](colorconverter.md)                | <span data-ttu-id="580fe-127">Convertit un flux vidéo entre des formats de couleur.</span><span class="sxs-lookup"><span data-stu-id="580fe-127">Converts a video stream between color formats.</span></span>       |
| [<span data-ttu-id="580fe-128">Convertisseur de fréquence d’images DSP</span><span class="sxs-lookup"><span data-stu-id="580fe-128">Frame Rate Converter DSP</span></span>](framerateconverter.md)       | <span data-ttu-id="580fe-129">Modifie la fréquence d’images d’un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="580fe-129">Changes the frame rate of a video stream.</span></span>            |
| [<span data-ttu-id="580fe-130">Dimensionnement vidéo DSP</span><span class="sxs-lookup"><span data-stu-id="580fe-130">Video Resizer DSP</span></span>](videoresizer.md)                    | <span data-ttu-id="580fe-131">Redimensionne un flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="580fe-131">Resizes a video stream.</span></span>                              |
| [<span data-ttu-id="580fe-132">DSP de capture vocale</span><span class="sxs-lookup"><span data-stu-id="580fe-132">Voice Capture DSP</span></span>](voicecapturedmo.md)                 | <span data-ttu-id="580fe-133">Encapsule plusieurs DSP associés à la capture vocale.</span><span class="sxs-lookup"><span data-stu-id="580fe-133">Encapsulates several DSPs related to voice capture.</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="580fe-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="580fe-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="580fe-135">Référence de programmation Media Foundation</span><span class="sxs-lookup"><span data-stu-id="580fe-135">Media Foundation Programming Reference</span></span>](media-foundation-programming-reference.md)
</dt> </dl>

 

 
