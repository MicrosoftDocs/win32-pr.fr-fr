---
title: Génération d’une boîte de dialogue permettant de sélectionner un format d’enregistrement
description: Génération d’une boîte de dialogue permettant de sélectionner un format d’enregistrement
ms.assetid: e94ca8da-4ee6-4362-a144-27b86f2cadac
keywords:
- Gestionnaire de compression audio (ACM), génération de boîtes de dialogue
- ACM (gestionnaire de compression audio), génération de boîtes de dialogue
- Exemples ACM, génération de boîtes de dialogue
- génération de boîtes de dialogue
- acmFormatChoose fonction)
- Audio Compression Manager (ACM), sélection du format de recodage
- ACM (gestionnaire de compression audio), sélection du format de recodage
- Exemples ACM, sélection du format de recodage
- sélection du format de recodage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7584d5f56904a6aa5241930041bf89c10373f6b1
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/27/2020
ms.locfileid: "104381622"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-recording"></a><span data-ttu-id="d6485-112">Génération d’une boîte de dialogue permettant de sélectionner un format d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="d6485-112">Producing a Dialog Box for Selecting a Format for Recording</span></span>

<span data-ttu-id="d6485-113">Une application peut permettre à l’utilisateur de sélectionner un format pour lequel un périphérique Wave-Audio installé fournit une prise en charge native.</span><span class="sxs-lookup"><span data-stu-id="d6485-113">An application can allow the user to select a format for which an installed waveform-audio device provides native support.</span></span> <span data-ttu-id="d6485-114">Par exemple, vous souhaiterez peut-être qu’un éditeur Wave Audio enregistre de nouvelles données audio Waveform sans utiliser de compresseur ou décompresseur ACM pour fournir une couche de traduction.</span><span class="sxs-lookup"><span data-stu-id="d6485-114">For example, you might want a waveform-audio editor to record new waveform-audio data without using an ACM compressor or decompressor to provide a translation layer.</span></span> <span data-ttu-id="d6485-115">Pour ce faire, utilisez la fonction [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , en spécifiant le \_ matériel ACM FORMATENUMF et les \_ \_ \_ indicateurs d’entrée ACM FORMATENUMF dans le membre **fdwEnum** de la structure [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) .</span><span class="sxs-lookup"><span data-stu-id="d6485-115">To do this, use the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, specifying the ACM\_FORMATENUMF\_HARDWARE and ACM\_FORMATENUMF\_INPUT flags in the **fdwEnum** member of the [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) structure.</span></span>

 

 




