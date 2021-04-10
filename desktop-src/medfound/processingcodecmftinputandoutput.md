---
description: Traitement de l’entrée et de la sortie MFT du codec
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: Traitement de l’entrée et de la sortie MFT du codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af3a16fa1855574f1b7618bc0d41bf85c15412f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201855"
---
# <a name="processing-codec-mft-input-and-output"></a><span data-ttu-id="93f6f-103">Traitement de l’entrée et de la sortie MFT du codec</span><span class="sxs-lookup"><span data-stu-id="93f6f-103">Processing Codec MFT Input and Output</span></span>

<span data-ttu-id="93f6f-104">Lorsque vous avez configuré le type d’entrée et le type de sortie pour une table MFT, vous pouvez commencer à traiter les exemples de données.</span><span class="sxs-lookup"><span data-stu-id="93f6f-104">When you have configured the input type and output type for an MFT, you can begin processing data samples.</span></span> <span data-ttu-id="93f6f-105">Vous transmettez des exemples à la MFT en vue de leur traitement à l’aide de la méthode [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) , puis vous récupérez l’exemple traité en appelant [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span><span class="sxs-lookup"><span data-stu-id="93f6f-105">You pass samples to the MFT for processing by using the [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method, and then retrieve the processed sample by calling [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="93f6f-106">Vous devez définir des horodatages précis et des durées pour tous les exemples d’entrée passés.</span><span class="sxs-lookup"><span data-stu-id="93f6f-106">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="93f6f-107">Les horodatages ne sont pas strictement obligatoires, mais ils permettent de maintenir la synchronisation audio/vidéo.</span><span class="sxs-lookup"><span data-stu-id="93f6f-107">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="93f6f-108">Si vous n’avez pas les horodatages de vos échantillons, il est préférable de les exclure de l’utilisation de valeurs incertaines.</span><span class="sxs-lookup"><span data-stu-id="93f6f-108">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93f6f-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="93f6f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93f6f-110">Utilisation du codec MFTs</span><span class="sxs-lookup"><span data-stu-id="93f6f-110">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



