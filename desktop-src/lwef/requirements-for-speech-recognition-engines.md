---
title: Configuration requise pour les moteurs de reconnaissance vocale
description: Configuration requise pour les moteurs de reconnaissance vocale
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1315d395e3053d5f6f71fd7f8ff17cb815bea26fc4875878da74dd77113d5e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975749"
---
# <a name="requirements-for-speech-recognition-engines"></a>Configuration requise pour les moteurs de reconnaissance vocale

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

Un moteur de reconnaissance vocale doit également être un moteur de commande et de contrôle (C&C) entièrement conforme en fonction de SAPI 4,0. Il doit prendre en charge plusieurs grammaires au format binaire décrit dans la spécification et autoriser l’activation ou la désactivation de ces grammaires en temps réel.

Notez que SAPI 4,0 requiert que les moteurs de reconnaissance vocale prennent en charge les caractères larges, les interfaces Unicode. Toutefois, dans la prise en charge de ces interfaces, le moteur ne doit pas dépendre de la conversion des données Unicode en ANSI, car le moteur peut ne pas fonctionner correctement sur certains systèmes. par exemple, un moteur japonais qui convertit Unicode en ANSI peut ne pas fonctionner sur un système Microsoft Windows 95 de langue anglaise.

En outre, pour être considéré comme conforme à Microsoft Agent, le moteur doit retourner des objets de résultats lors de la reconnaissance réussie d’une expression (par le biais de ISRGramNotifySinkW ::P hraseFinish). Ces objets de résultats doivent prendre en charge ISRResBasic, comme la spécification le requiert. En outre, ils doivent prendre en charge ISRResScore. Bien que Microsoft Agent s’exécute avec un moteur qui prend uniquement en charge ISRResBasic, ou même avec un moteur qui ne retourne aucun objet de résultats, les performances sont généralement beaucoup plus faibles avec ces moteurs. De nombreuses applications utilisent les valeurs de confiance fournies par le moteur pour contrôler la façon dont elles répondent à diverses commandes.

 

 




