---
description: Contrôle de la fréquence
ms.assetid: 6529859f-cfb6-4983-a489-bcc2f04e721f
title: Contrôle de la fréquence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f484a0469d96578ca1bb7e1d661d7e2319bd8bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524527"
---
# <a name="rate-control"></a><span data-ttu-id="44f69-103">Contrôle de la fréquence</span><span class="sxs-lookup"><span data-stu-id="44f69-103">Rate Control</span></span>

<span data-ttu-id="44f69-104">La [session multimédia](media-session.md) prend en charge la modification de la vitesse de lecture, qu’une application peut utiliser pour implémenter des fonctionnalités de lecture telles que l’avance rapide et le rembobinage.</span><span class="sxs-lookup"><span data-stu-id="44f69-104">The [Media Session](media-session.md) supports changing the playback rate, which an application can use to implement playback features such as fast-forward and rewind.</span></span> <span data-ttu-id="44f69-105">Cette section décrit comment les applications peuvent modifier la vitesse de lecture lors de l’utilisation de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="44f69-105">This section describes how applications can change the playback rate while using the Media Session.</span></span>

<span data-ttu-id="44f69-106">Pour plus d’informations sur la prise en charge du contrôle des taux dans vos propres composants de pipeline, consultez [Implementing Rate Control](implementing-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="44f69-106">For information about supporting rate control in your own pipeline components, see [Implementing Rate Control](implementing-rate-control.md).</span></span>

<span data-ttu-id="44f69-107">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="44f69-107">This section contains the following topics.</span></span>



| <span data-ttu-id="44f69-108">Rubrique</span><span class="sxs-lookup"><span data-stu-id="44f69-108">Topic</span></span>                                                                                                      | <span data-ttu-id="44f69-109">Description</span><span class="sxs-lookup"><span data-stu-id="44f69-109">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="44f69-110">À propos du contrôle du taux</span><span class="sxs-lookup"><span data-stu-id="44f69-110">About Rate Control</span></span>](about-rate-control.md)                                                               | <span data-ttu-id="44f69-111">Donne une vue d’ensemble générale du contrôle de la fréquence.</span><span class="sxs-lookup"><span data-stu-id="44f69-111">Gives a general overview of rate control.</span></span>                              |
| [<span data-ttu-id="44f69-112">Comment déterminer les tarifs pris en charge</span><span class="sxs-lookup"><span data-stu-id="44f69-112">How to Determine Supported Rates</span></span>](how-to-determine-supported-rates.md)                                   | <span data-ttu-id="44f69-113">Comment trouver les vitesses de lecture les plus rapides et les plus lentes prises en charge.</span><span class="sxs-lookup"><span data-stu-id="44f69-113">How to find the fastest and slowest supported playback rates.</span></span>          |
| [<span data-ttu-id="44f69-114">Comment définir la vitesse de lecture sur la session multimédia</span><span class="sxs-lookup"><span data-stu-id="44f69-114">How to Set the Playback Rate on the Media Session</span></span>](how-to-set-the-playback-rate-on-the-media-session.md) | <span data-ttu-id="44f69-115">Comment modifier la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="44f69-115">How to change the playback rate.</span></span>                                       |
| [<span data-ttu-id="44f69-116">Comment effectuer un nettoyage</span><span class="sxs-lookup"><span data-stu-id="44f69-116">How to Perform Scrubbing</span></span>](how-to-perform-scrubbing.md)                                                   | <span data-ttu-id="44f69-117">Comment effectuer un pas à pas détaillé d’une image vidéo à la fois.</span><span class="sxs-lookup"><span data-stu-id="44f69-117">How to step one video frame at a time.</span></span>                                 |
| [<span data-ttu-id="44f69-118">Mise en œuvre du contrôle de taux</span><span class="sxs-lookup"><span data-stu-id="44f69-118">Implementing Rate Control</span></span>](implementing-rate-control.md)                                                 | <span data-ttu-id="44f69-119">Comment prendre en charge des taux de lecture variables dans un composant de pipeline personnalisé.</span><span class="sxs-lookup"><span data-stu-id="44f69-119">How to support variable playback rates in a custom pipeline component.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="44f69-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="44f69-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44f69-121">Session multimédia</span><span class="sxs-lookup"><span data-stu-id="44f69-121">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="44f69-122">Recherche, avance rapide et lecture inversée</span><span class="sxs-lookup"><span data-stu-id="44f69-122">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



