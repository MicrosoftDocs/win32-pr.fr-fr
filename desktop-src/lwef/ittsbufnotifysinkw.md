---
title: ITTSBufNotifySinkW
description: ITTSBufNotifySinkW
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a1ce3013ba1d8acf01f79b4f71d2d5088f4d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940266"
---
# <a name="ittsbufnotifysinkw"></a><span data-ttu-id="df7ca-103">ITTSBufNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="df7ca-103">ITTSBufNotifySinkW</span></span>

<span data-ttu-id="df7ca-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="df7ca-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="df7ca-105">Le moteur doit appeler par **signet**.</span><span class="sxs-lookup"><span data-stu-id="df7ca-105">The engine must call out through **BookMark**.</span></span> <span data-ttu-id="df7ca-106">Lors du prétraitement de la sortie vocale, le code Microsoft Agent insère les signets entre les « mots » et utilise l’arrivée de ces signets pour piloter le texte dans la bulle.</span><span class="sxs-lookup"><span data-stu-id="df7ca-106">During preprocessing of speech output, Microsoft Agent code inserts bookmarks between "words" and uses the arrival of those bookmarks to drive the pacing of text in the word balloon.</span></span> <span data-ttu-id="df7ca-107">Alors que SAPI ne nécessite rien de plus que l’arrivée de ces signets à un moment donné avant la fin de l’énoncé, les signets doivent être retournés de façon relativement opportune pour prendre en charge Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="df7ca-107">While SAPI does not require anything more than the arrival of those bookmarks at some time before the end of the utterance, the bookmarks must be returned in a relatively timely fashion to support Microsoft Agent.</span></span>

<span data-ttu-id="df7ca-108">Notez qu’il n’existe pas de concept strict de « Word » dans certains langages, tels que le japonais.</span><span class="sxs-lookup"><span data-stu-id="df7ca-108">Note that there is no strict concept of "word" in some languages, such as Japanese.</span></span> <span data-ttu-id="df7ca-109">La méthode [**Speak**](speak-method.md) de Microsoft Agent définit un « mot » comme une chaîne connectée de symboles qui a une signification et une prononciation en isolation.</span><span class="sxs-lookup"><span data-stu-id="df7ca-109">Microsoft Agent's [**Speak**](speak-method.md) method defines a "word" as a connected string of symbols that has a meaning and pronunciation in isolation.</span></span> <span data-ttu-id="df7ca-110">Microsoft Agent utilise un code d’analyse relativement simple pour déterminer ce qu’est un « mot » : il recherche les symboles séparés par un espace blanc.</span><span class="sxs-lookup"><span data-stu-id="df7ca-110">Microsoft Agent uses fairly simple parsing code to determine what a "word" is: it looks for symbols separated by white space.</span></span> <span data-ttu-id="df7ca-111">Par conséquent, il y a trois « mots » dans la chaîne anglaise « the 101 Dalmatians » : « The », « 101 » et « Dalmatians ».</span><span class="sxs-lookup"><span data-stu-id="df7ca-111">Thus, there are three "words" in the English string "The 101 Dalmatians": "the", "one hundred and one", and "Dalmatians".</span></span> <span data-ttu-id="df7ca-112">Le texte inclus dans la balise de la carte de l’agent Microsoft est traité comme un « mot » unique à des fins d’affichage.</span><span class="sxs-lookup"><span data-stu-id="df7ca-112">Text included in the Microsoft Agent Map tag is treated as a single "word" for display purposes.</span></span>

 

 




