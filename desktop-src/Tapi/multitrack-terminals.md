---
description: TAPI 3,1 introduit la notion de terminal multipiste, un terminal qui, par essence, est une collection de &\# 0034 ; track&\# 0034 ; terminaux.
ms.assetid: 8dd6f792-a29e-40fd-9f5b-ee5525028c2e
title: Terminaux multipiste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb795169f5e7cbd669e0bceb1d635e33c912c50a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516050"
---
# <a name="multitrack-terminals"></a><span data-ttu-id="fb6d6-103">Terminaux multipiste</span><span class="sxs-lookup"><span data-stu-id="fb6d6-103">Multitrack Terminals</span></span>

<span data-ttu-id="fb6d6-104">TAPI 3,1 introduit la notion de terminal multipiste, un terminal qui, par essence, est un ensemble de terminaux de « suivi ».</span><span class="sxs-lookup"><span data-stu-id="fb6d6-104">TAPI 3.1 introduces the notion of a multitrack terminal, a terminal that, in essence, is a collection of "track" terminals.</span></span> <span data-ttu-id="fb6d6-105">Les terminaux multipiste facilitent la charge du programmeur dans les situations où plusieurs flux multimédias sont impliqués dans une session de communication.</span><span class="sxs-lookup"><span data-stu-id="fb6d6-105">Multitrack terminals ease the programmer's load in situations where multiple media streams are involved in a communications session.</span></span>

<span data-ttu-id="fb6d6-106">Le [terminal d’enregistrement de fichier](file-playback-terminal-and-file-recording-terminal.md) est un exemple de terminal multipiste.</span><span class="sxs-lookup"><span data-stu-id="fb6d6-106">The [File Recording Terminal](file-playback-terminal-and-file-recording-terminal.md) is an example of a multitrack terminal.</span></span> <span data-ttu-id="fb6d6-107">Il se compose de « pistes », où chaque « piste » est un terminal correspondant à un flux dans le fichier enregistré.</span><span class="sxs-lookup"><span data-stu-id="fb6d6-107">It consists of "tracks," where each "track" is a terminal corresponding to a stream in the recorded file.</span></span>

<span data-ttu-id="fb6d6-108">Un [terminal de suivi](track-terminals.md) peut être un autre terminal multipiste ou un seul terminal.</span><span class="sxs-lookup"><span data-stu-id="fb6d6-108">A [track terminal](track-terminals.md) can be another multitrack terminal or a single-track terminal.</span></span> <span data-ttu-id="fb6d6-109">Un terminal à un seul rail est un terminal qui n’a pas de terminaux de suivi.</span><span class="sxs-lookup"><span data-stu-id="fb6d6-109">A single-track terminal is a terminal that does not have any track terminals.</span></span> <span data-ttu-id="fb6d6-110">Un terminal simple-Track est un terminal dans le sens TAPI 3 du mot.</span><span class="sxs-lookup"><span data-stu-id="fb6d6-110">A single-track terminal is a terminal in the TAPI 3 sense of the word.</span></span>

<span data-ttu-id="fb6d6-111">Pour plus d’informations sur les terminaux multipiste, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb6d6-111">For more information about multitrack terminals, see the following topics:</span></span>

-   [<span data-ttu-id="fb6d6-112">À propos des terminaux multipiste</span><span class="sxs-lookup"><span data-stu-id="fb6d6-112">About Multitrack Terminals</span></span>](about-multitrack-terminals.md)
-   [<span data-ttu-id="fb6d6-113">Mécanisme de sélection par défaut des terminaux</span><span class="sxs-lookup"><span data-stu-id="fb6d6-113">Default Terminal Selection Mechanism</span></span>](default-terminal-selection-mechanism.md)
-   [<span data-ttu-id="fb6d6-114">Sélection manuelle des terminaux</span><span class="sxs-lookup"><span data-stu-id="fb6d6-114">Manual Terminal Selection</span></span>](manual-terminal-selection.md)
-   [<span data-ttu-id="fb6d6-115">Utilisation des terminaux multipiste et du mécanisme de sélection par défaut</span><span class="sxs-lookup"><span data-stu-id="fb6d6-115">Using Multitrack Terminals and the Default Selection Mechanism</span></span>](using-multitrack-terminals-and-the-default-selection-mechanism.md)

 

 



