---
description: Une fois qu’un appel est à l’état connecté, les informations peuvent être transmises sur celui-ci.
ms.assetid: a2afa7e9-c625-48ec-920b-0ae8c3e1b395
title: Génération de chiffres et de tonalités inbande
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f144d4bc6b6273f71da37f6b9864146465c5ca29b91018a2e2ff097f6f19b44f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424879"
---
# <a name="generating-inband-digits-and-tones"></a>Génération de chiffres et de tonalités inbande

Une fois qu’un appel est à l’état *connecté* , les informations peuvent être transmises sur celui-ci. Deux fonctions sont fournies pour permettre la signalisation inbande de bout en bout entre l’application et l’équipement de station à distance, comme un ordinateur de réponse. Une fonction est [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits), qui génère des chiffres inbandes sur un appel, en les signalant sur le canal vocal. Les chiffres peuvent être signalés sous la forme de séquences de type rotation/impulsion ou de tonalités DTMF. L’autre fonction est [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone), ce qui permet à l’application de générer une série de tonalités multifréquences (sur le flux multimédia). Cela génère des tonalités téléphoniques, telles que le rappel, le signal sonore et le temps d’activité, ainsi que des tonalités multifréquences arbitraires.

Une seule génération de chiffres ou de tonalités peut être en cours sur un appel à un moment donné. Lorsque la génération d’un chiffre ou d’un ton est terminée, un message de génération de [**ligne \_**](line-generate.md) est envoyé à l’application qui a demandé la génération. Dans le cas où plusieurs chiffres sont générés, un seul message est renvoyé après la génération de tous les chiffres. L’appel de [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) ou [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) lorsque la génération de chiffres ou de tonalités est en cours, annule la génération en cours et envoie le message de génération de la ligne \_ à l’application dont la génération a été abandonnée avec une indication d’annulation.

 

 



