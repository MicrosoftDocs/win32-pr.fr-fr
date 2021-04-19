---
title: Réponse du lecteur aux fonctionnalités ASF
description: Réponse du lecteur aux fonctionnalités ASF
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- Windows Media Format SDK, lecteurs réponses aux fonctionnalités ASF
- ASF (Advanced Systems Format), réponses des lecteurs aux fonctionnalités
- ASF (format de systèmes avancés), réponses de lecteur aux fonctionnalités
- réponses des lecteurs aux fonctionnalités ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291752d2d011fbc8b0a3e5211c5d8926f94b1cbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511018"
---
# <a name="reader-response-to-asf-features"></a><span data-ttu-id="9bcf5-107">Réponse du lecteur aux fonctionnalités ASF</span><span class="sxs-lookup"><span data-stu-id="9bcf5-107">Reader Response to ASF Features</span></span>

<span data-ttu-id="9bcf5-108">La plupart des fonctionnalités de fichier ASF spéciales peuvent être définies dans des fichiers pour interagir avec des applications de jeu personnalisées conçues pour les gérer.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-108">Most of the special ASF file features can be set in files to interact with custom playing applications designed to handle them.</span></span> <span data-ttu-id="9bcf5-109">Toutefois, certaines fonctionnalités offrent une prise en charge intégrée dans l’objet Reader.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-109">However, some of the features have built-in support in the reader object.</span></span>

<span data-ttu-id="9bcf5-110">L’objet lecteur sélectionne automatiquement les flux à partir des jeux qui s’excluent mutuellement par vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-110">The reader object will automatically select streams from sets that are mutually exclusive by bit rate.</span></span> <span data-ttu-id="9bcf5-111">Ce cas spécial est appelé « débit binaire multiple » (MBR).</span><span class="sxs-lookup"><span data-stu-id="9bcf5-111">This special case is referred to as multiple bit rate (MBR).</span></span> <span data-ttu-id="9bcf5-112">Le flux sélectionné par le lecteur est basé sur la vitesse de transmission du flux.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-112">The stream the reader selects is based on the bit rate of the stream.</span></span> <span data-ttu-id="9bcf5-113">Le numéro du flux et l’ordre dans lequel il a été ajouté à l’objet d’exclusion mutuelle ne sont pas pertinents pour la sélection automatique.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-113">The stream number and the order in which it was added to the mutual exclusion object are irrelevant to the automatic selection.</span></span> <span data-ttu-id="9bcf5-114">Si un fichier contient plus d’un ensemble de flux mutuellement exclusifs par vitesse de transmission, le lecteur sélectionne des flux en fonction du calcul de la meilleure utilisation de la bande passante disponible.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-114">If a file includes more than one set of streams mutually exclusive by bit rate, the reader will select streams based on calculating the best use of the available bandwidth.</span></span>

<span data-ttu-id="9bcf5-115">L’exclusion mutuelle basée sur le langage est définie à l’aide d’un paramètre de sortie avant la lecture.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-115">Language-based mutual exclusion is set using an output setting, before playback.</span></span> <span data-ttu-id="9bcf5-116">Si vous combinez la langue et l’exclusion mutuelle basée sur la fréquence de bits, vous devez regrouper les flux de bits qui s’excluent mutuellement par langue, puis rendre les groupes mutuellement exclusifs par langue.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-116">If you combine both language and bit-rate-based mutual exclusion, you should group the bit-rate-based mutually exclusive streams by language and then make the groups mutually exclusive by language.</span></span> <span data-ttu-id="9bcf5-117">Le lecteur vérifiera d’abord la langue, puis déterminera la vitesse de transmission à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-117">The reader will check the language first, and then determine which bit rate to use.</span></span>

<span data-ttu-id="9bcf5-118">La hiérarchisation des flux est définie à l’aide d’un tableau d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-118">Stream prioritization is set using an array of records.</span></span> <span data-ttu-id="9bcf5-119">Les enregistrements dans le tableau sont dans l’ordre de priorité décroissant.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-119">The records in the array are in descending order of priority.</span></span> <span data-ttu-id="9bcf5-120">Le dernier flux du tableau est le premier qui sera supprimé par le lecteur.</span><span class="sxs-lookup"><span data-stu-id="9bcf5-120">The last stream in the array is the first that will be dropped by the reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bcf5-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9bcf5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bcf5-122">**Fonctionnalités des fichiers ASF**</span><span class="sxs-lookup"><span data-stu-id="9bcf5-122">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="9bcf5-123">**Exclusion mutuelle**</span><span class="sxs-lookup"><span data-stu-id="9bcf5-123">**Mutual Exclusion**</span></span>](mutual-exclusion.md)
</dt> <dt>

[<span data-ttu-id="9bcf5-124">**Hiérarchisation des flux**</span><span class="sxs-lookup"><span data-stu-id="9bcf5-124">**Stream Prioritization**</span></span>](stream-prioritization.md)
</dt> </dl>

 

 




