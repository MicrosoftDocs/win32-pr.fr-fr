---
description: Énumération des types audio pour des modes d’encodage spécifiques
ms.assetid: d44960eb-da5e-4379-ba9d-cb804559dc53
title: Énumération des types audio pour des modes d’encodage spécifiques (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16a8b97afdd48cb1d7828f80778aa9fcf8dc1ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393268"
---
# <a name="enumerating-audio-types-for-specific-encoding-modes-microsoft-media-foundation"></a><span data-ttu-id="3c6df-103">Énumération des types audio pour des modes d’encodage spécifiques (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="3c6df-103">Enumerating Audio Types for Specific Encoding Modes (Microsoft Media Foundation)</span></span>

<span data-ttu-id="3c6df-104">Les types de média d’entrée et de sortie acceptés par l’encodeur audio sont très structurés.</span><span class="sxs-lookup"><span data-stu-id="3c6df-104">The input and output media types accepted by the audio encoder are very structured.</span></span> <span data-ttu-id="3c6df-105">Vous devez obtenir les types de sortie pris en charge en appelant la méthode **IMediaObject :: GetOutputType** ou **IMFTransform :: GetOutputType**.</span><span class="sxs-lookup"><span data-stu-id="3c6df-105">You must obtain supported output types by calling **IMediaObject::GetOutputType** method or **IMFTransform::GetOutputType**.</span></span> <span data-ttu-id="3c6df-106">Une fois que vous avez obtenu un type de sortie, vous ne devez pas le modifier.</span><span class="sxs-lookup"><span data-stu-id="3c6df-106">After you get an output type, you must not alter it.</span></span>

<span data-ttu-id="3c6df-107">Si vous souhaitez utiliser un mode d’encodage autre qu’un passe CBR, vous devez définir le mode, puis énumérer les types de sortie pour ce mode. l’encodeur modifie les types de sortie pris en charge selon le mode défini.</span><span class="sxs-lookup"><span data-stu-id="3c6df-107">If you want to use an encoding mode other than one-pass CBR, you must set the mode and then enumerate the output types for that mode; the encoder changes the supported output types depending upon the mode set.</span></span> <span data-ttu-id="3c6df-108">Les propriétés qui contrôlent le mode d’encodage sont [**MFPKEY \_ VBRENABLED**](mfpkey-vbrenabledproperty.md) et [**MFPKEY \_ PASSESUSED**](mfpkey-passesusedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="3c6df-108">The properties that control the encoding mode are [**MFPKEY\_VBRENABLED**](mfpkey-vbrenabledproperty.md) and [**MFPKEY\_PASSESUSED**](mfpkey-passesusedproperty.md).</span></span> <span data-ttu-id="3c6df-109">Lorsque le mode est défini dans l’encodeur, vous devez énumérer et sélectionner un type de sortie, en l’utilisant sans modification, comme avec CBR.</span><span class="sxs-lookup"><span data-stu-id="3c6df-109">When the mode is set in the encoder, you must enumerate and select an output type, using it without alteration, just as with CBR.</span></span>

## <a name="identifying-quality-based-vbr-types"></a><span data-ttu-id="3c6df-110">Identification des types VBR basés sur la qualité</span><span class="sxs-lookup"><span data-stu-id="3c6df-110">Identifying Quality Based VBR Types</span></span>

<span data-ttu-id="3c6df-111">La procédure d’identification des types VBR basés sur la qualité varie selon que l’encodeur agit comme un objet de média DirectX (DMO) ou agit comme une transformation de Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="3c6df-111">The procedure for identifying quality based VBR types depends on whether the encoder is acting as a DirectX Media Object (DMO) or acting as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="3c6df-112">Pour plus d’informations sur le moment où un encodeur agit comme DMO ou MFT, consultez les pages de référence des codecs individuels sous [objets codec](codecobjects.md).</span><span class="sxs-lookup"><span data-stu-id="3c6df-112">For information on when an encoder acts as a DMO or an MFT, see the individual codec reference pages under [Codec Objects](codecobjects.md).</span></span>

<span data-ttu-id="3c6df-113">Lorsqu’un encodeur audio fait office de DMO et que vous configurez l’encodeur pour utiliser le VBR à passage unique, il énumère tous les types de sortie pris en charge.</span><span class="sxs-lookup"><span data-stu-id="3c6df-113">When an audio encoder is acting as a DMO and you configure the encoder to use one-pass VBR, it enumerates all of the supported output types.</span></span> <span data-ttu-id="3c6df-114">Toutefois, vous souhaiterez généralement sélectionner un type VBR à un passage basé sur le paramètre Quality.</span><span class="sxs-lookup"><span data-stu-id="3c6df-114">However, you will typically want to select a one-pass VBR type based on the quality parameter.</span></span> <span data-ttu-id="3c6df-115">L’encodeur place la valeur de qualité pour les types de sortie VBR à un passage dans le membre **nAvgBytesPerSec** de la structure **WAVEFORMATEX** désignée par **DMO \_ Media \_ type. pbFormat**.</span><span class="sxs-lookup"><span data-stu-id="3c6df-115">The encoder puts the quality value for one-pass VBR output types in the **nAvgBytesPerSec** member of the **WAVEFORMATEX** structure pointed to by **DMO\_MEDIA\_TYPE.pbFormat**.</span></span>

<span data-ttu-id="3c6df-116">Cette valeur est stockée au format suivant : 0x7FFFFFXX, où XX est la valeur de qualité (comprise entre 0 et 100).</span><span class="sxs-lookup"><span data-stu-id="3c6df-116">This value is stored in the following format: 0x7FFFFFXX, where XX is the quality value (from 0 to 100).</span></span> <span data-ttu-id="3c6df-117">Par exemple, la valeur **nAvgBytesPerSec** de 0x7FFFFF62 spécifie le niveau de qualité 98 (0x62 = 98).</span><span class="sxs-lookup"><span data-stu-id="3c6df-117">For example, the **nAvgBytesPerSec** value of 0x7FFFFF62 specifies quality level 98 (0x62 = 98).</span></span>

<span data-ttu-id="3c6df-118">L’exemple suivant montre comment vérifier le niveau de qualité d’un format lorsque l’encodeur agit comme DMO.</span><span class="sxs-lookup"><span data-stu-id="3c6df-118">The following example shows how to check the quality level of a format when the encoder is acting as a DMO.</span></span>


```
void ShowQuality(WAVEFORMATEX* pWave)
{
    // Store the average bytes per second in a local variable
    // with a more manageable name.
    DWORD dwBps = pWave->nAvgBytesPerSec;

    // Verify that the value is a VBR quality level by using 
    // a bitmask to check for the bit pattern 0x7FFFFFXX. 
    if(dwBps & 0x7FFFFF00 == 0x7FFFFF00)
        printf("VBR Quality: %d%%\n",(dwBps & 0x000000FF));
    else // Not a valid VBR quality value.
        printf("Not a valid one-pass VBR audio format.\n");
}
```



<span data-ttu-id="3c6df-119">Lorsque l’encodeur joue le rôle de MFT et qu’il énumère un type de sortie sur un appel à **GetAvailableOutputType**, vous pouvez interroger la table MFT pour la propriété **\_ \_ \_ \_ VBRQUALITY énumérée la plus récente MFPKEY** .</span><span class="sxs-lookup"><span data-stu-id="3c6df-119">When the encoder is acting as an MFT and it enumerates an output type on a call to **GetAvailableOutputType**, you can query the MFT for the **MFPKEY\_MOST\_RECENTLY\_ENUMERATED\_VBRQUALITY** property.</span></span> <span data-ttu-id="3c6df-120">La valeur retournée indique la qualité VBR du type de média de sortie retourné le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="3c6df-120">The value returned indicates the VBR quality of the most recently returned output media type.</span></span> <span data-ttu-id="3c6df-121">Vous pouvez ensuite utiliser cette valeur pour définir la propriété [**MFPKEY \_ souhaitée \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="3c6df-121">Then you can use that value to set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property of the encoder.</span></span>

## <a name="setting-peak-constraints"></a><span data-ttu-id="3c6df-122">Définition des contraintes de pointe</span><span class="sxs-lookup"><span data-stu-id="3c6df-122">Setting Peak Constraints</span></span>

<span data-ttu-id="3c6df-123">Pour les VBR basés sur la qualité VBR (un passage) et les deux passes sans contrainte, aucun paramètre supplémentaire n’est nécessaire après avoir récupéré le type de sortie.</span><span class="sxs-lookup"><span data-stu-id="3c6df-123">For quality based VBR (one-pass) and unconstrained two-pass VBR, no additional settings are required after retrieving the output type.</span></span> <span data-ttu-id="3c6df-124">Pour utiliser le VBR à limite maximale, récupérez un type de sortie avec VBR activé et deux passes définies.</span><span class="sxs-lookup"><span data-stu-id="3c6df-124">To use peak-constrained VBR, retrieve an output type with VBR enabled and two passes set.</span></span> <span data-ttu-id="3c6df-125">Ce type, sans modification, décrit les paramètres VBR non restreints.</span><span class="sxs-lookup"><span data-stu-id="3c6df-125">This type, without alteration, describes unconstrained VBR settings.</span></span> <span data-ttu-id="3c6df-126">Pour définir des contraintes de pointe, définissez les propriétés [MFPKEY \_ Rmax](mfpkey-rmaxproperty.md) et [MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="3c6df-126">To set peak constraints, set the [MFPKEY\_RMAX](mfpkey-rmaxproperty.md) and [MFPKEY\_BMAX](mfpkey-bmaxproperty.md) properties.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c6df-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3c6df-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c6df-128">Configuration de l’encodage audio</span><span class="sxs-lookup"><span data-stu-id="3c6df-128">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> <dt>

[<span data-ttu-id="3c6df-129">Recherche de types de sortie d’encodeur audio</span><span class="sxs-lookup"><span data-stu-id="3c6df-129">Finding Audio Encoder Output Types</span></span>](findingaudioencoderoutputtypes.md)
</dt> <dt>

[<span data-ttu-id="3c6df-130">Utilisation de l’encodage Two-Pass</span><span class="sxs-lookup"><span data-stu-id="3c6df-130">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
</dt> <dt>

[<span data-ttu-id="3c6df-131">Utilisation de l’encodage VBR</span><span class="sxs-lookup"><span data-stu-id="3c6df-131">Using VBR Encoding</span></span>](usingvbrencoding.md)
</dt> </dl>

 

 



