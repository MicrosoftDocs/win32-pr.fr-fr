---
description: Traitement de l’entrée et de la sortie du codec DMO
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: Traitement de l’entrée et de la sortie du codec DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c6781d877f4c863161537fcc5b6a746691cfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318741"
---
# <a name="processing-codec-dmo-input-and-output"></a><span data-ttu-id="ffc40-103">Traitement de l’entrée et de la sortie du codec DMO</span><span class="sxs-lookup"><span data-stu-id="ffc40-103">Processing Codec DMO Input and Output</span></span>

<span data-ttu-id="ffc40-104">Lorsque vous avez configuré le type d’entrée et le type de sortie pour un DMO, vous pouvez commencer à traiter les exemples de données.</span><span class="sxs-lookup"><span data-stu-id="ffc40-104">When you have configured the input type and output type for a DMO, you can begin processing data samples.</span></span> <span data-ttu-id="ffc40-105">Vous transmettez des exemples à DMO pour traitement à l’aide de la méthode **IMediaObject ::P rocessinput** , puis vous récupérez l’exemple traité en appelant **IMediaObject ::P rocessoutput**.</span><span class="sxs-lookup"><span data-stu-id="ffc40-105">You pass samples to the DMO for processing using the **IMediaObject::ProcessInput** method, and then retrieve the processed sample by calling **IMediaObject::ProcessOutput**.</span></span> <span data-ttu-id="ffc40-106">Vous devez définir des horodatages précis et des durées pour tous les exemples d’entrée passés.</span><span class="sxs-lookup"><span data-stu-id="ffc40-106">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="ffc40-107">Les horodatages ne sont pas strictement obligatoires, mais ils permettent de maintenir la synchronisation audio/vidéo.</span><span class="sxs-lookup"><span data-stu-id="ffc40-107">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="ffc40-108">Si vous n’avez pas les horodatages de vos échantillons, il est préférable de les exclure de l’utilisation de valeurs incertaines.</span><span class="sxs-lookup"><span data-stu-id="ffc40-108">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffc40-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ffc40-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffc40-110">Utilisation du codec DMOs</span><span class="sxs-lookup"><span data-stu-id="ffc40-110">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 



