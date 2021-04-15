---
title: Utilisation des entrées
description: Utilisation des entrées
ms.assetid: 72daa7ca-4264-46bf-91ac-8b95fdbfd41c
keywords:
- Windows Media Format SDK, utilisation des entrées
- ASF (Advanced Systems Format), utilisation des entrées
- ASF (format de systèmes avancés), utilisation des entrées
- profils, utilisation des entrées
- flux, utilisation des entrées
- codecs, utilisation des entrées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e7016b5304b0d77e130b68d9a9feef15ffe54d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462143"
---
# <a name="working-with-inputs"></a><span data-ttu-id="bd5b9-109">Utilisation des entrées</span><span class="sxs-lookup"><span data-stu-id="bd5b9-109">Working with Inputs</span></span>

<span data-ttu-id="bd5b9-110">Tout comme la configuration de flux appropriée dans le profil est requise pour obtenir le codec pour compresser un flux, vous devez également vous assurer que le type de support non compressé que vous transmettez à l’enregistreur est décrit avec précision.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-110">Just as the proper stream configuration in the profile is required to get the codec to compress a stream, you must also ensure that the type of uncompressed media you pass to the writer is accurately described.</span></span> <span data-ttu-id="bd5b9-111">Chaque codec Windows Media est associé à un type d’entrée par défaut, mais plusieurs types d’entrée sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-111">Every Windows Media codec has an associated default input type, but several input types are supported.</span></span> <span data-ttu-id="bd5b9-112">Vous pouvez examiner les entrées prises en charge et sélectionner celle qui correspond à vos données.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-112">You can examine the supported inputs and select the one that matches your data.</span></span> <span data-ttu-id="bd5b9-113">Le processus d’utilisation des entrées est résumé dans les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="bd5b9-113">The process of working with inputs is summarized in the following steps:</span></span>

1.  <span data-ttu-id="bd5b9-114">Lorsque vous chargez un profil à utiliser par le writer, l’objet Writer affecte un numéro d’entrée pour chaque connexion dans le profil.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-114">When you load a profile for the writer to use, the writer object assigns an input number for each connection in the profile.</span></span> <span data-ttu-id="bd5b9-115">Pour plus d’informations sur le chargement des profils pour le writer, consultez [pour utiliser des profils avec le writer](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="bd5b9-115">For more information about loading profiles for the writer, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span> <span data-ttu-id="bd5b9-116">À moins que vous n’utilisiez l’exclusion mutuelle par vitesse de transmission, il existe une connexion pour chaque flux.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-116">Unless you are using mutual exclusion by bit rate, there is one connection for each stream.</span></span> <span data-ttu-id="bd5b9-117">Les flux qui sont mutuellement exclusifs par la vitesse de transmission partagent une seule connexion.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-117">Streams that are mutually exclusive by bit rate share a single connection.</span></span>
2.  <span data-ttu-id="bd5b9-118">Votre application doit identifier les numéros d’entrée du fichier.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-118">Your application should identify the input numbers for the file.</span></span> <span data-ttu-id="bd5b9-119">Pour plus d’informations sur l’identification des numéros d’entrée, consultez [pour identifier les entrées par numéro](to-identify-inputs-by-number.md).</span><span class="sxs-lookup"><span data-stu-id="bd5b9-119">For more information about identifying input numbers, see [To Identify Inputs By Number](to-identify-inputs-by-number.md).</span></span>
3.  <span data-ttu-id="bd5b9-120">Pour chaque entrée, vous devez vous assurer que le format d’entrée correspond à vos données.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-120">For each input, you should ensure that the input format matches your data.</span></span> <span data-ttu-id="bd5b9-121">Vous pouvez énumérer les formats d’entrée pris en charge par le kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="bd5b9-121">You can enumerate the input formats supported by the SDK.</span></span> <span data-ttu-id="bd5b9-122">Pour plus d’informations, consultez [pour énumérer les formats d’entrée](to-enumerate-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="bd5b9-122">For more information, see [To Enumerate Input Formats](to-enumerate-input-formats.md).</span></span> <span data-ttu-id="bd5b9-123">Vous ne pouvez pas énumérer les formats d’entrée de flux arbitraires ou de flux déjà compressés.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-123">You cannot enumerate the input formats of arbitrary streams or streams that are already compressed.</span></span> <span data-ttu-id="bd5b9-124">Pour plus d’informations sur ces cas spéciaux, consultez [entrées de flux arbitraires et précompressés](arbitrary-and-precompressed-stream-inputs.md).</span><span class="sxs-lookup"><span data-stu-id="bd5b9-124">For more information about these special cases, see [Arbitrary and Precompressed Stream Inputs](arbitrary-and-precompressed-stream-inputs.md).</span></span>
4.  <span data-ttu-id="bd5b9-125">Attribuez le format d’entrée correct pour chaque connexion.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-125">Assign the correct input format for each connection.</span></span> <span data-ttu-id="bd5b9-126">Pour plus d’informations, consultez [attribution de formats d’entrée](assigning-input-formats.md).</span><span class="sxs-lookup"><span data-stu-id="bd5b9-126">For more information, see [Assigning Input Formats](assigning-input-formats.md).</span></span>
5.  <span data-ttu-id="bd5b9-127">Certaines fonctionnalités du codec et de l’enregistreur sont configurées au moment de l’encodage plutôt que dans le profil.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-127">Some codec and writer features are configured at encoding time instead of in the profile.</span></span> <span data-ttu-id="bd5b9-128">Pour configurer ces fonctionnalités, vous devez utiliser des paramètres d’entrée.</span><span class="sxs-lookup"><span data-stu-id="bd5b9-128">To configure these features, you must use input settings.</span></span> <span data-ttu-id="bd5b9-129">Pour plus d’informations, consultez [pour définir les paramètres d’entrée](to-set-input-settings.md).</span><span class="sxs-lookup"><span data-stu-id="bd5b9-129">For more information, see [To Set Input Settings](to-set-input-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd5b9-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bd5b9-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd5b9-131">**Écriture de fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="bd5b9-131">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




