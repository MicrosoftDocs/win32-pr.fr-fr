---
title: Génération d’une boîte de dialogue permettant de sélectionner un format d’enregistrement
description: Génération d’une boîte de dialogue permettant de sélectionner un format d’enregistrement
ms.assetid: f833b28c-13e1-497c-bfc4-2e3bc84d7fff
keywords:
- Gestionnaire de compression audio (ACM), génération de boîtes de dialogue
- ACM (gestionnaire de compression audio), génération de boîtes de dialogue
- Exemples ACM, génération de boîtes de dialogue
- génération de boîtes de dialogue
- acmFormatChoose fonction)
- Gestionnaire de compression audio (ACM), sélection du format d’enregistrement
- ACM (gestionnaire de compression audio), sélection du format d’enregistrement
- Exemples ACM, sélection du format d’enregistrement
- sélection du format d’enregistrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55df4cd89a04bf1d3dd34512c4014928b6d5d4fb
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/27/2020
ms.locfileid: "104381623"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-saving"></a><span data-ttu-id="5fca3-112">Génération d’une boîte de dialogue permettant de sélectionner un format d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="5fca3-112">Producing a Dialog Box for Selecting a Format for Saving</span></span>

<span data-ttu-id="5fca3-113">Vous pouvez souhaiter qu’une application enregistre les données Waveform-Audio existantes dans un autre format.</span><span class="sxs-lookup"><span data-stu-id="5fca3-113">You might want an application to save existing waveform-audio data in another format.</span></span> <span data-ttu-id="5fca3-114">Par exemple, un éditeur Wave audio peut enregistrer un fichier Waveform-Audio sous forme de fichier compressé.</span><span class="sxs-lookup"><span data-stu-id="5fca3-114">For example, a waveform-audio editor could save a waveform-audio file as a compressed file.</span></span> <span data-ttu-id="5fca3-115">Pour répertorier uniquement les formats de destination suggérés pour un format source spécifié dans la boîte de dialogue créée par la fonction [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) , spécifiez le format de la source dans le membre **pwfxEnum** et l' \_ \_ indicateur de suggestion FORMATENUMF de l’ACM dans le membre **fdwEnum** de la structure [**acmFormatChoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) .</span><span class="sxs-lookup"><span data-stu-id="5fca3-115">To list only the suggested destination formats for a specified source format in the dialog box created by the [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) function, specify the source format in the **pwfxEnum** member and the ACM\_FORMATENUMF\_SUGGEST flag in the **fdwEnum** member of the [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) structure.</span></span>

<span data-ttu-id="5fca3-116">De même, pour répertorier les formats de destination valides pour un format spécifié, utilisez l' \_ indicateur ACM FORMATENUMF \_ Convert au lieu de l' \_ indicateur de suggestion FORMATENUMF ACM \_ .</span><span class="sxs-lookup"><span data-stu-id="5fca3-116">Similarly, to list valid destination formats for a specified format, use the ACM\_FORMATENUMF\_CONVERT flag instead of the ACM\_FORMATENUMF\_SUGGEST flag.</span></span>

 

 




