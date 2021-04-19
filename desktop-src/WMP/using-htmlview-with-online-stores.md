---
title: Utilisation de HTMLView avec des magasins en ligne
description: Utilisation de HTMLView avec des magasins en ligne
ms.assetid: 78de7ef3-400c-4411-8ade-35c421805df8
keywords:
- Windows Media Player Online stores, HTMLView
- magasins en ligne, HTMLView
- tapez 1 magasins en ligne, HTMLView
- tapez 2 magasins en ligne, HTMLView
- HTMLView, magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d136be4f7866b6911b8b007de7e784d6133c217
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510441"
---
# <a name="using-htmlview-with-online-stores"></a><span data-ttu-id="f1421-108">Utilisation de HTMLView avec des magasins en ligne</span><span class="sxs-lookup"><span data-stu-id="f1421-108">Using HTMLView with Online Stores</span></span>

<span data-ttu-id="f1421-109">Le lecteur Windows Media demande à l’utilisateur l’autorisation d’afficher le contenu HTMLView en **cours de lecture**.</span><span class="sxs-lookup"><span data-stu-id="f1421-109">Windows Media Player prompts users for permission to display HTMLView content in **Now Playing**.</span></span> <span data-ttu-id="f1421-110">Les magasins en ligne peuvent désactiver cette invite en spécifiant une valeur d’URL de base dans l’élément **HTMLView** du document serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="f1421-110">Online stores can disable this prompt by specifying a base URL value in the **HTMLView** element of the ServiceInfo document.</span></span> <span data-ttu-id="f1421-111">Lorsque le lecteur Windows Media ouvre une sélection qui spécifie le contenu de HTMLView à afficher, le lecteur compare l’URL de base du document ServiceInfo du magasin en ligne actif à l’URL de base du contenu HTMLView.</span><span class="sxs-lookup"><span data-stu-id="f1421-111">When Windows Media Player opens a playlist that specifies HTMLView content to display, the Player compares the base URL from the ServiceInfo document of the current active online store to the base URL of the HTMLView content.</span></span> <span data-ttu-id="f1421-112">S’ils correspondent, le lecteur Windows Media affiche le contenu HTMLView sans inviter l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f1421-112">If they match, Windows Media Player displays the HTMLView content without prompting the user.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1421-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f1421-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1421-114">**Affichage des pages Web dans le lecteur Windows Media**</span><span class="sxs-lookup"><span data-stu-id="f1421-114">**Displaying Web Pages in Windows Media Player**</span></span>](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[<span data-ttu-id="f1421-115">**Élément HTMLView**</span><span class="sxs-lookup"><span data-stu-id="f1421-115">**HTMLView Element**</span></span>](htmlview-element.md)
</dt> <dt>

[<span data-ttu-id="f1421-116">**Informations communes aux magasins en ligne de type 1 et de type 2**</span><span class="sxs-lookup"><span data-stu-id="f1421-116">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




