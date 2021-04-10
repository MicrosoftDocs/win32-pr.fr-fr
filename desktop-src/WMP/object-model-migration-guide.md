---
title: Guide de migration du modèle objet
description: Guide de migration du modèle objet
ms.assetid: 2fd4f7ec-36b0-49da-9a11-546dd41c7a98
keywords:
- Lecteur Windows Media, modèle objet
- Lecteur Windows Media, Guide de migration
- Modèle d’objet du lecteur Windows Media, Guide de migration
- modèle objet, Guide de migration
- Contrôle ActiveX du lecteur Windows Media, Guide de migration
- Contrôle ActiveX, Guide de migration
- Windows Media Player Mobile contrôle ActiveX, Guide de migration
- Windows Media Player Mobile, modèle objet
- Windows Media Player Mobile, Guide de migration
- Guide de migration, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29c9be40e3cc252ed9461bcb18ea5bfed49bb58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029638"
---
# <a name="object-model-migration-guide"></a><span data-ttu-id="42044-113">Guide de migration du modèle objet</span><span class="sxs-lookup"><span data-stu-id="42044-113">Object Model Migration Guide</span></span>

<span data-ttu-id="42044-114">Le lecteur Windows Media 7 a introduit un nouveau modèle objet qui offre un nouvel ensemble riche de fonctionnalités que vous pouvez utiliser pour améliorer vos pages Web.</span><span class="sxs-lookup"><span data-stu-id="42044-114">Windows Media Player 7 introduced a new object model that offers a rich new set of functionality that you can use to enhance your webpages.</span></span> <span data-ttu-id="42044-115">Les versions suivantes ont étendu le modèle d’objet de la version 7 avec des propriétés, des méthodes et des événements supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="42044-115">Subsequent versions have extended the version 7 object model with additional properties, methods, and events.</span></span> <span data-ttu-id="42044-116">Toutefois, le nouveau modèle d’objet diffère considérablement du modèle d’objet du lecteur Windows Media 6,4. vous devez donc comprendre comment mettre à jour votre code existant si vous souhaitez prendre en charge Windows Media Player 7 et versions ultérieures dans vos projets.</span><span class="sxs-lookup"><span data-stu-id="42044-116">However, the new object model differs substantially from the Windows Media Player 6.4 object model, so you need to understand how to update your existing code if you want to support Windows Media Player 7 and later in your projects.</span></span>

<span data-ttu-id="42044-117">Pour obtenir un exemple qui montre comment détecter la version du lecteur Windows Media et le navigateur actuel de l’utilisateur, consultez l’exemple nommé « détection » installé avec ce kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="42044-117">For a sample that demonstrates how to detect the user's Windows Media Player version and current browser, see the sample named "detection" that is installed with this SDK.</span></span> <span data-ttu-id="42044-118">Pour plus d’informations sur les exemples, consultez [exemples](samples.md).</span><span class="sxs-lookup"><span data-stu-id="42044-118">For more information about samples, see [Samples](samples.md).</span></span>

<span data-ttu-id="42044-119">Ce guide fait référence au nouveau modèle d’objet en tant que modèle objet Windows Media Player 7 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="42044-119">This guide refers to the new object model as the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="42044-120">Pour plus d’informations sur les fonctionnalités disponibles dans chaque version du lecteur Windows Media, consultez [Référence du modèle objet pour les scripts](object-model-reference-for-scripting.md).</span><span class="sxs-lookup"><span data-stu-id="42044-120">For details about which functionality is available in each version of Windows Media Player, see [Object Model Reference for Scripting](object-model-reference-for-scripting.md).</span></span>

<span data-ttu-id="42044-121">Ces problèmes de modèle objet sont traités dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="42044-121">These object model issues are covered by the following topics:</span></span>

-   [<span data-ttu-id="42044-122">Différences entre les modèles objet</span><span class="sxs-lookup"><span data-stu-id="42044-122">Differences Between the Object Models</span></span>](differences-between-the-object-models.md)
-   [<span data-ttu-id="42044-123">Utilisation du modèle objet Windows Media Player 7 ou version ultérieure</span><span class="sxs-lookup"><span data-stu-id="42044-123">Using the Windows Media Player 7 or Later Object Model</span></span>](using-the-windows-media-player-7-or-later-object-model.md)
-   [<span data-ttu-id="42044-124">Gestion des erreurs</span><span class="sxs-lookup"><span data-stu-id="42044-124">Error Handling</span></span>](error-handling.md)
-   [<span data-ttu-id="42044-125">Sélections</span><span class="sxs-lookup"><span data-stu-id="42044-125">Playlists</span></span>](playlists.md)
-   [<span data-ttu-id="42044-126">Sous-titrage</span><span class="sxs-lookup"><span data-stu-id="42044-126">Closed Captioning</span></span>](closed-captioning.md)
-   [<span data-ttu-id="42044-127">DVD</span><span class="sxs-lookup"><span data-stu-id="42044-127">DVD</span></span>](dvd.md)
-   [<span data-ttu-id="42044-128">Comparaison du modèle d’objet détaillé</span><span class="sxs-lookup"><span data-stu-id="42044-128">Detailed Object Model Comparison</span></span>](detailed-object-model-comparison.md)

## <a name="related-topics"></a><span data-ttu-id="42044-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="42044-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42044-130">**Guide de contrôle du lecteur**</span><span class="sxs-lookup"><span data-stu-id="42044-130">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




