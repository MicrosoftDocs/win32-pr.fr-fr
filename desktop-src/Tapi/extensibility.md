---
description: En savoir plus sur l’extensibilité. Des dispositions sont prises pour étendre les constantes et les structures de manière indépendante du périphérique et de manière spécifique à l’appareil.
ms.assetid: bc0a18f3-1f58-4a24-8afb-c31f3b561375
title: Extensibilité (API de téléphonie)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f29ad34b5156bdd652ab6b6f8901be7a2341bdc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406562"
---
# <a name="extensibility"></a>Extensibilité

Des dispositions sont prises pour étendre les constantes et les structures de manière indépendante du périphérique et dans un mode spécifique au périphérique (spécifique au fournisseur). Dans les constantes qui sont des énumérations scalaires, une plage de valeurs est réservée aux futures extensions communes. Le reste des valeurs est identifié comme étant spécifique à l’appareil. Un fournisseur peut définir des significations pour ces valeurs de la manière souhaitée. Leur interprétation est indexée dans l' *identificateur d’extension* fourni dans la structure de données [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) . Pour les constantes définies en tant qu’indicateurs binaires, une plage de bits de poids faible est réservée, où les bits de poids fort peuvent être spécifiques à l’extension. Il est recommandé que les valeurs étendues et les tableaux de bits utilisent des bits de la valeur la plus élevée ou du bit de poids fort. Cela laisse la possibilité de déplacer la bordure entre la partie commune et la portion d’extension si vous devez le faire à l’avenir. Les extensions des structures de données sont affectées à un champ de taille variable de taille/décalage faisant partie de la partie fixe. L’interface TAPI décrit pour chaque structure de données les extensions spécifiques à l’appareil qui sont autorisées.

En plus de reconnaître un identificateur d’extension spécifique, l’application doit négocier le numéro de version de l’extension que l’application et le fournisseur de services utilisent. Cette opération s’effectue dans la phase de négociation de la deuxième version de la fonction [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) .

Un identificateur d’extension est un identificateur global unique. Il n’existe pas de registre central pour les identificateurs d’extension. Au lieu de cela, ils sont générés localement par le fabricant par un utilitaire disponible avec la boîte à outils. Le nombre est constitué de parties telles qu’une adresse LAN unique, une heure de la journée et un nombre aléatoire, afin de garantir l’unicité globale. Les identificateurs globaux uniques sont conçus pour être distingués des identificateurs universels uniques HP/DEC et sont donc entièrement compatibles avec eux.

 

 
