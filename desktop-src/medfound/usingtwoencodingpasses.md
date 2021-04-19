---
description: L’encodage en deux passes peut être utilisé pour le débit binaire constant (CBR) et pour l’encodage VBR (variable bit rate) avec certains codecs Windows Media.
ms.assetid: eec5085c-9441-496a-8127-cf5d2686d917
title: Utilisation de l’encodage Two-Pass (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993af0015452db410b5a9f2c13233566fc17a3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534184"
---
# <a name="using-two-pass-encoding-microsoft-media-foundation"></a><span data-ttu-id="dc0db-103">Utilisation de l’encodage Two-Pass (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="dc0db-103">Using Two-Pass Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="dc0db-104">L’encodage en deux passes peut être utilisé pour le débit binaire constant (CBR) et pour l’encodage VBR (variable bit rate) avec certains codecs Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dc0db-104">Two-pass encoding can be used for constant bit rate (CBR) and for variable bit rate (VBR) encoding with some of the Windows Media codecs.</span></span> <span data-ttu-id="dc0db-105">Vous pouvez trouver le nombre maximal de passes d’encodage pris en charge par un codec en extrayant la propriété [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="dc0db-105">You can find the maximum number of encoding passes supported by a codec by retrieving the [MFPKEY\_PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md) property.</span></span> <span data-ttu-id="dc0db-106">Aucun des codecs ne prend en charge plus de deux passes.</span><span class="sxs-lookup"><span data-stu-id="dc0db-106">None of the codecs supports more than two passes.</span></span> <span data-ttu-id="dc0db-107">Configurez DMO pour qu’il utilise deux passages en affectant à la propriété [ \_ PASSESUSED MFPKEY](mfpkey-passesusedproperty.md) la valeur 2.</span><span class="sxs-lookup"><span data-stu-id="dc0db-107">Configure the DMO to use two passes by setting the [MFPKEY\_PASSESUSED](mfpkey-passesusedproperty.md) property to 2.</span></span>

<span data-ttu-id="dc0db-108">Fournissez les exemples à l’encodeur DMO un à la fois, comme vous le feriez dans un mode à passage unique.</span><span class="sxs-lookup"><span data-stu-id="dc0db-108">Deliver the samples to the encoder DMO one at a time, as you would in a one-pass mode.</span></span> <span data-ttu-id="dc0db-109">Lorsque vous traitez les exemples d’entrée pour votre passe de prétraitement, les appels à [**IMediaObject ::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) ou [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) renverront la **\_ valeur S false** pour indiquer qu’aucune sortie n’est produite.</span><span class="sxs-lookup"><span data-stu-id="dc0db-109">When you process the input samples for your preprocessing pass, the calls to [**IMediaObject::ProcessInput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput) or [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) will return **S\_FALSE**, to indicate that no output is produced.</span></span>

<span data-ttu-id="dc0db-110">À la fin de la première passe (après le premier traitement de la dernière entrée), vous devez définir la propriété [MFPKEY \_ ENDOFPASS](mfpkey-endofpassproperty.md) pour informer le codec que l’entrée suivante traitée est la première entrée de la deuxième passe.</span><span class="sxs-lookup"><span data-stu-id="dc0db-110">At the end of the first pass (after the last input is processed for the first time), you then must set the [MFPKEY\_ENDOFPASS](mfpkey-endofpassproperty.md) property to notify the codec that the next input processed is the first input of the second pass.</span></span> <span data-ttu-id="dc0db-111">Aucune valeur n’est requise pour cette propriété. vous devez donc utiliser une structure **Variant** vide.</span><span class="sxs-lookup"><span data-stu-id="dc0db-111">No value is required for this property, so you should use an empty **VARIANT** structure.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc0db-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dc0db-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc0db-113">Codecs Windows Media</span><span class="sxs-lookup"><span data-stu-id="dc0db-113">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 
