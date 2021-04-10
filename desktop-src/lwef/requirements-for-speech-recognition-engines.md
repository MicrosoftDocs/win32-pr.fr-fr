---
title: Configuration requise pour les moteurs de reconnaissance vocale
description: Configuration requise pour les moteurs de reconnaissance vocale
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9214f13b11a071ec8d8599f0b6dd542884ae05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940215"
---
# <a name="requirements-for-speech-recognition-engines"></a><span data-ttu-id="720ee-103">Configuration requise pour les moteurs de reconnaissance vocale</span><span class="sxs-lookup"><span data-stu-id="720ee-103">Requirements for Speech Recognition Engines</span></span>

<span data-ttu-id="720ee-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="720ee-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="720ee-105">Un moteur de reconnaissance vocale doit également être un moteur de commande et de contrôle (C&C) entièrement conforme en fonction de SAPI 4,0.</span><span class="sxs-lookup"><span data-stu-id="720ee-105">A speech recognition engine must also be a fully compliant Command and Control (C&C) engine according to SAPI 4.0.</span></span> <span data-ttu-id="720ee-106">Il doit prendre en charge plusieurs grammaires au format binaire décrit dans la spécification et autoriser l’activation ou la désactivation de ces grammaires en temps réel.</span><span class="sxs-lookup"><span data-stu-id="720ee-106">It must support multiple grammars in the binary format described in the specification and allow those grammars to be activated or deactivated in real time.</span></span>

<span data-ttu-id="720ee-107">Notez que SAPI 4,0 requiert que les moteurs de reconnaissance vocale prennent en charge les caractères larges, les interfaces Unicode.</span><span class="sxs-lookup"><span data-stu-id="720ee-107">Note that SAPI 4.0 requires that speech recognition engines support the wide character, Unicode interfaces.</span></span> <span data-ttu-id="720ee-108">Toutefois, dans la prise en charge de ces interfaces, le moteur ne doit pas dépendre de la conversion des données Unicode en ANSI, car le moteur peut ne pas fonctionner correctement sur certains systèmes.</span><span class="sxs-lookup"><span data-stu-id="720ee-108">However, in supporting these interfaces, the engine should not depend on converting Unicode data to ANSI, as the engine may not function correctly on some systems.</span></span> <span data-ttu-id="720ee-109">Par exemple, un moteur japonais qui convertit Unicode en ANSI peut ne pas fonctionner sur un système Microsoft Windows 95 de langue anglaise.</span><span class="sxs-lookup"><span data-stu-id="720ee-109">For example, a Japanese engine that converts Unicode to ANSI may not work on an English-language Microsoft Windows 95 system.</span></span>

<span data-ttu-id="720ee-110">En outre, pour être considéré comme conforme à Microsoft Agent, le moteur doit retourner des objets de résultats lors de la reconnaissance réussie d’une expression (par le biais de ISRGramNotifySinkW ::P hraseFinish).</span><span class="sxs-lookup"><span data-stu-id="720ee-110">In addition, to be considered Microsoft Agent-compliant, the engine must return results objects upon the successful recognition of a phrase (through ISRGramNotifySinkW::PhraseFinish).</span></span> <span data-ttu-id="720ee-111">Ces objets de résultats doivent prendre en charge ISRResBasic, comme la spécification le requiert.</span><span class="sxs-lookup"><span data-stu-id="720ee-111">These results objects must support ISRResBasic, as the specification requires.</span></span> <span data-ttu-id="720ee-112">En outre, ils doivent prendre en charge ISRResScore.</span><span class="sxs-lookup"><span data-stu-id="720ee-112">In addition, they should support ISRResScore.</span></span> <span data-ttu-id="720ee-113">Bien que Microsoft Agent s’exécute avec un moteur qui prend uniquement en charge ISRResBasic, ou même avec un moteur qui ne retourne aucun objet de résultats, les performances sont généralement beaucoup plus faibles avec ces moteurs.</span><span class="sxs-lookup"><span data-stu-id="720ee-113">Although Microsoft Agent will run with an engine that supports only ISRResBasic, or even with an engine that returns no results objects whatsoever, performance will usually be significantly poorer with such engines.</span></span> <span data-ttu-id="720ee-114">De nombreuses applications utilisent les valeurs de confiance fournies par le moteur pour contrôler la façon dont elles répondent à diverses commandes.</span><span class="sxs-lookup"><span data-stu-id="720ee-114">Many applications use the confidence values provided by the engine to control how they respond to various commands.</span></span>

 

 




