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
# <a name="text-to-speech-engines-text-normalization"></a>Normalisation du texte des moteurs de synthèse vocale

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

La normalisation est le processus qui consiste à identifier les nombres, les abréviations, les acronymes et les idiomatics et à les transformer en texte intégral en fonction des besoins, généralement en fonction du contexte de la phrase.

Par exemple, à l’aide du moteur de synthèse vocale de L&H TruVoice pour l’anglais américain, la phrase suivante :

King George VI of England est décédé le 6 février 1952.

sera lu dans un **contexte normal** comme suit :

   King George V I of England, mort le 6 février 19 52.

Mais sous le **contexte du courrier électronique**, il est lu comme suit :

   King George The sixième of England, mort le sixième février 19 52.

Vous trouverez des informations **sur l’utilisation** de la balise de synthèse vocale dans la documentation de programmation de l’agent [balises de sortie vocale Microsoft Agent](microsoft-agent-speech-output-tags.md).

 

 




