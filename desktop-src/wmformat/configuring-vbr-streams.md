---
title: Configuration de flux VBR
description: Configuration de flux VBR
ms.assetid: 83caabb7-b7fa-4b0a-a608-d5a86e4101b8
keywords:
- flux, configuration des flux VBR
- flux, débit binaire variable (VBR)
- Vitesse de transmission variable (VBR), flux
- VBR (vitesse de transmission variable), flux
- flux, interface IWMPropertyVault
- IWMPropertyVault
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6667dc9cf66932cf8af90da0b0e59ad27860ab3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103940676"
---
# <a name="configuring-vbr-streams"></a><span data-ttu-id="63708-109">Configuration de flux VBR</span><span class="sxs-lookup"><span data-stu-id="63708-109">Configuring VBR Streams</span></span>

<span data-ttu-id="63708-110">Vous pouvez utiliser l’encodage VBR (variable binaire rate) pour produire des flux de haute qualité pour les fichiers locaux ou pour le téléchargement et la diffusion.</span><span class="sxs-lookup"><span data-stu-id="63708-110">You can use variable bit rate (VBR) encoding to produce high quality streams for local files or for downloading and playing.</span></span> <span data-ttu-id="63708-111">Il existe trois options pour VBR : basée sur la qualité (une passe), sans contrainte (deux passes) et contraint (deux passes).</span><span class="sxs-lookup"><span data-stu-id="63708-111">There are three options for VBR: quality-based (one-pass), unconstrained (two-pass), and constrained (two-pass).</span></span> <span data-ttu-id="63708-112">Pour plus d’informations sur les types d’encodage VBR, consultez l' [encodage VBR (variable bit rate)](variable-bit-rate--vbr--encoding.md).</span><span class="sxs-lookup"><span data-stu-id="63708-112">For more information about the types of VBR encoding, see [Variable Bit Rate (VBR) Encoding](variable-bit-rate--vbr--encoding.md).</span></span>

<span data-ttu-id="63708-113">Vous pouvez configurer l’encodage VBR dans un profil en définissant les propriétés avec l’interface [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) .</span><span class="sxs-lookup"><span data-stu-id="63708-113">You can configure VBR encoding in a profile by setting properties with the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface.</span></span> <span data-ttu-id="63708-114">Le tableau suivant décrit les propriétés utilisées pour configurer l’encodage VBR.</span><span class="sxs-lookup"><span data-stu-id="63708-114">The following table describes the properties used to configure VBR encoding.</span></span>



| <span data-ttu-id="63708-115">Propriété</span><span class="sxs-lookup"><span data-stu-id="63708-115">Property</span></span>                     | <span data-ttu-id="63708-116">Description</span><span class="sxs-lookup"><span data-stu-id="63708-116">Description</span></span>                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63708-117">**\_wszVBREnabled g**</span><span class="sxs-lookup"><span data-stu-id="63708-117">**g\_wszVBREnabled**</span></span>         | <span data-ttu-id="63708-118">Valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="63708-118">Boolean value.</span></span> <span data-ttu-id="63708-119">Affectez la valeur true pour utiliser l’encodage VBR.</span><span class="sxs-lookup"><span data-stu-id="63708-119">Set to True to use VBR encoding.</span></span>                                                   |
| <span data-ttu-id="63708-120">**\_wszVBRQuality g**</span><span class="sxs-lookup"><span data-stu-id="63708-120">**g\_wszVBRQuality**</span></span>         | <span data-ttu-id="63708-121">Valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="63708-121">**DWORD** value.</span></span> <span data-ttu-id="63708-122">Définissez le niveau de qualité souhaité (de 1 à 100) pour l’encodage VBR basé sur la qualité.</span><span class="sxs-lookup"><span data-stu-id="63708-122">Set to the desired quality level (1 to 100) for quality-based VBR encoding.</span></span>      |
| <span data-ttu-id="63708-123">**\_wszVBRBitrateMax g**</span><span class="sxs-lookup"><span data-stu-id="63708-123">**g\_wszVBRBitrateMax**</span></span>      | <span data-ttu-id="63708-124">Valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="63708-124">**DWORD** value.</span></span> <span data-ttu-id="63708-125">Définissez sur la vitesse de transmission maximale, en bits par seconde, pour l’encodage VBR limité.</span><span class="sxs-lookup"><span data-stu-id="63708-125">Set to the maximum bit rate, in bits per second, for constrained VBR encoding.</span></span>   |
| <span data-ttu-id="63708-126">**\_wszVBRBufferWindowMax g**</span><span class="sxs-lookup"><span data-stu-id="63708-126">**g\_wszVBRBufferWindowMax**</span></span> | <span data-ttu-id="63708-127">Valeur **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="63708-127">**DWORD** value.</span></span> <span data-ttu-id="63708-128">Défini sur la fenêtre de mémoire tampon maximale, en millisecondes, pour l’encodage VBR limité.</span><span class="sxs-lookup"><span data-stu-id="63708-128">Set to the maximum buffer window, in milliseconds, for constrained VBR encoding.</span></span> |



 

<span data-ttu-id="63708-129">Les sections suivantes décrivent comment utiliser les différents types de codage à vitesse de transmission variable.</span><span class="sxs-lookup"><span data-stu-id="63708-129">The following sections describe how to use the different types of variable bit rate encoding.</span></span>



| <span data-ttu-id="63708-130">Section</span><span class="sxs-lookup"><span data-stu-id="63708-130">Section</span></span>                                                              | <span data-ttu-id="63708-131">Description</span><span class="sxs-lookup"><span data-stu-id="63708-131">Description</span></span>                                                                                                        |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="63708-132">Pour configurer Quality-Based VBR</span><span class="sxs-lookup"><span data-stu-id="63708-132">To Configure Quality-Based VBR</span></span>](to-configure-quality-based-vbr.md) | <span data-ttu-id="63708-133">Décrit comment utiliser un encodage à débit binaire variable basé sur un niveau de qualité statique.</span><span class="sxs-lookup"><span data-stu-id="63708-133">Describes how to use variable bit rate encoding based on a static quality level.</span></span>                                   |
| [<span data-ttu-id="63708-134">Pour configurer le VBR sans contrainte</span><span class="sxs-lookup"><span data-stu-id="63708-134">To Configure Unconstrained VBR</span></span>](to-configure-unconstrained-vbr.md) | <span data-ttu-id="63708-135">Décrit comment utiliser un encodage à débit binaire variable basé sur un taux de bits moyen cible sans valeur de pic explicite.</span><span class="sxs-lookup"><span data-stu-id="63708-135">Describes how to use variable bit rate encoding based on a target average bit rate without an explicit peak value.</span></span> |
| [<span data-ttu-id="63708-136">Pour configurer le VBR restreint</span><span class="sxs-lookup"><span data-stu-id="63708-136">To Configure Constrained VBR</span></span>](to-configure-constrained-vbr.md)     | <span data-ttu-id="63708-137">Décrit comment utiliser un encodage à débit binaire variable basé sur une vitesse de transmission moyenne cible et une valeur de pic explicite.</span><span class="sxs-lookup"><span data-stu-id="63708-137">Describes how to use variable bit rate encoding based on a target average bit rate and an explicit peak value.</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="63708-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="63708-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63708-139">**Configuration de flux**</span><span class="sxs-lookup"><span data-stu-id="63708-139">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




