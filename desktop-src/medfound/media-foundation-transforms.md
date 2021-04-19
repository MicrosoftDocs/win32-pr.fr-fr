---
description: Transformations de Media Foundation
ms.assetid: cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0
title: Transformations de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa0518ced06169f6d998bdad1747878d109e0676
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106522282"
---
# <a name="media-foundation-transforms"></a><span data-ttu-id="4451a-103">Transformations de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4451a-103">Media Foundation Transforms</span></span>

<span data-ttu-id="4451a-104">Les transformations de Media Foundation (MFTs) fournissent un modèle générique pour le traitement des données multimédias.</span><span class="sxs-lookup"><span data-stu-id="4451a-104">Media Foundation transforms (MFTs) provide a generic model for processing media data.</span></span> <span data-ttu-id="4451a-105">Les MFTs sont utilisés pour les décodeurs, les encodeurs et les processeurs de signal numérique (DSP).</span><span class="sxs-lookup"><span data-stu-id="4451a-105">MFTs are used for decoders, encoders, and digital signal processors (DSPs).</span></span> <span data-ttu-id="4451a-106">En bref, tout ce qui se trouve dans le pipeline de média entre la source du média et le récepteur multimédia est une table MFT.</span><span class="sxs-lookup"><span data-stu-id="4451a-106">In short, anything that sits in the media pipeline between the media source and the media sink is an MFT.</span></span>

<span data-ttu-id="4451a-107">Cette section décrit le modèle de programmation MFT et comment implémenter une table MFT, avec des recommandations pour des types spécifiques de MFTs, tels que les décodeurs.</span><span class="sxs-lookup"><span data-stu-id="4451a-107">This section describes the MFT programming model and how to implement an MFT, with recommendations for specific types of MFTs, such as decoders.</span></span>



| <span data-ttu-id="4451a-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="4451a-108">Topic</span></span>                                                                    | <span data-ttu-id="4451a-109">Description</span><span class="sxs-lookup"><span data-stu-id="4451a-109">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4451a-110">À propos de MFTs</span><span class="sxs-lookup"><span data-stu-id="4451a-110">About MFTs</span></span>](about-mfts.md)                                             | <span data-ttu-id="4451a-111">Fournit une brève vue d’ensemble de MFTs</span><span class="sxs-lookup"><span data-stu-id="4451a-111">Provides a brief overview of MFTs</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="4451a-112">Modèle de traitement MFT de base</span><span class="sxs-lookup"><span data-stu-id="4451a-112">Basic MFT Processing Model</span></span>](basic-mft-processing-model.md)             | <span data-ttu-id="4451a-113">Décrit plus en détail le modèle de base pour le traitement des données avec une table MFT.</span><span class="sxs-lookup"><span data-stu-id="4451a-113">Describes in more detail the basic model for processing data with an MFT.</span></span>                                                                                                                           |
| [<span data-ttu-id="4451a-114">MFTs asynchrone</span><span class="sxs-lookup"><span data-stu-id="4451a-114">Asynchronous MFTs</span></span>](asynchronous-mfts.md)                               | <span data-ttu-id="4451a-115">Décrit un modèle de traitement asynchrone qui est une alternative au modèle de base.</span><span class="sxs-lookup"><span data-stu-id="4451a-115">Describes an asynchronous processing model that is an alternative to the basic model.</span></span><br/> <span data-ttu-id="4451a-116">Le traitement asynchrone a été introduit dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4451a-116">Asynchronous processing was introduced in Windows 7.</span></span> <span data-ttu-id="4451a-117">Toutes les MFT ne prennent pas en charge ce modèle.</span><span class="sxs-lookup"><span data-stu-id="4451a-117">Not every MFT supports this model.</span></span><br/> |
| [<span data-ttu-id="4451a-118">Inscription et énumération de MFTs</span><span class="sxs-lookup"><span data-stu-id="4451a-118">Registering and Enumerating MFTs</span></span>](registering-and-enumerating-mfts.md) | <span data-ttu-id="4451a-119">Comment inscrire une table MFT et comment énumérer les MFTs dans le registre.</span><span class="sxs-lookup"><span data-stu-id="4451a-119">How to register an MFT and how to enumerate MFTs in the registry.</span></span>                                                                                                                                   |
| [<span data-ttu-id="4451a-120">Champ des restrictions d’utilisation</span><span class="sxs-lookup"><span data-stu-id="4451a-120">Field of Use Restrictions</span></span>](field-of-use-restrictions.md)               | <span data-ttu-id="4451a-121">Décrit le mécanisme de déverrouillage d’une table MFT qui a des restrictions de champ d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="4451a-121">Describes the mechanism for unlocking an MFT that has field-of-use restrictions.</span></span>                                                                                                                    |
| [<span data-ttu-id="4451a-122">Comparaison entre MFT et DMO</span><span class="sxs-lookup"><span data-stu-id="4451a-122">Comparison of MFTs and DMOs</span></span>](comparison-of-mfts-and-dmos.md)           | <span data-ttu-id="4451a-123">Résume les différences entre MFTs et DMOs.</span><span class="sxs-lookup"><span data-stu-id="4451a-123">Summarizes the differences between MFTs and DMOs.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="4451a-124">Écriture d’une table MFT personnalisée</span><span class="sxs-lookup"><span data-stu-id="4451a-124">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)                         | <span data-ttu-id="4451a-125">Instructions pour l’écriture d’une table MFT personnalisée.</span><span class="sxs-lookup"><span data-stu-id="4451a-125">Guidelines for writing a custom MFT.</span></span>                                                                                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="4451a-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4451a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4451a-127">Pipeline Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4451a-127">Media Foundation Pipeline</span></span>](media-foundation-pipeline.md)
</dt> <dt>

[<span data-ttu-id="4451a-128">Architecture Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4451a-128">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="4451a-129">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="4451a-129">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




