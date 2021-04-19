---
title: Normalisation du texte des moteurs de synthèse vocale
description: Normalisation du texte des moteurs de synthèse vocale
ms.assetid: 1974d47b-4877-47e3-89d8-fd70967e7605
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb7bda7cb8041e31ef8e741df4d3f5d807610f1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511017"
---
# <a name="text-to-speech-engines-text-normalization"></a><span data-ttu-id="e4a16-103">Normalisation du texte des moteurs de synthèse vocale</span><span class="sxs-lookup"><span data-stu-id="e4a16-103">Text-to-Speech Engines Text Normalization</span></span>

<span data-ttu-id="e4a16-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e4a16-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="e4a16-105">La normalisation est le processus qui consiste à identifier les nombres, les abréviations, les acronymes et les idiomatics et à les transformer en texte intégral en fonction des besoins, généralement en fonction du contexte de la phrase.</span><span class="sxs-lookup"><span data-stu-id="e4a16-105">Normalization is the process of identifying numbers, abbreviations, acronyms and idiomatics and transforming them into full text as needed, usually based on the context of the sentence.</span></span>

<span data-ttu-id="e4a16-106">Par exemple, à l’aide du moteur de synthèse vocale de L&H TruVoice pour l’anglais américain, la phrase suivante :</span><span class="sxs-lookup"><span data-stu-id="e4a16-106">For example, using the L&H TruVoice American English TTS Engine, the sentence:</span></span>

<span data-ttu-id="e4a16-107">King George VI of England est décédé le 6 février 1952.</span><span class="sxs-lookup"><span data-stu-id="e4a16-107">King George VI of England died on Feb 6, 1952.</span></span>

<span data-ttu-id="e4a16-108">sera lu dans un **contexte normal** comme suit :</span><span class="sxs-lookup"><span data-stu-id="e4a16-108">will be read under **normal context** as:</span></span>

   <span data-ttu-id="e4a16-109">King George V I of England, mort le 6 février 19 52.</span><span class="sxs-lookup"><span data-stu-id="e4a16-109">King George V I of England, died on February six, nineteen fifty-two.</span></span>

<span data-ttu-id="e4a16-110">Mais sous le **contexte du courrier électronique**, il est lu comme suit :</span><span class="sxs-lookup"><span data-stu-id="e4a16-110">But under **E-mail context**, it will be read as:</span></span>

   <span data-ttu-id="e4a16-111">King George The sixième of England, mort le sixième février 19 52.</span><span class="sxs-lookup"><span data-stu-id="e4a16-111">King George the sixth of England, died on February sixth, nineteen fifty-two.</span></span>

<span data-ttu-id="e4a16-112">Vous trouverez des informations **sur l’utilisation** de la balise de synthèse vocale dans la documentation de programmation de l’agent [balises de sortie vocale Microsoft Agent](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="e4a16-112">Information about using the **Context** speech tag can be found in the Agent programming documentation [Microsoft Agent Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

 

 




