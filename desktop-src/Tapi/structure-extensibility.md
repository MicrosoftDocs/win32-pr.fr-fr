---
description: En savoir plus sur l’extensibilité de la structure. Des dispositions sont prises pour étendre les constantes et les structures de manière indépendante du périphérique et de manière spécifique à l’appareil.
ms.assetid: d30f80c3-3535-4d78-b0a1-c9a7389f8fd4
title: Extensibilité de la structure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378defd35304f6745d42723a44e21c0aa56a34e1f6c40c2f96d5f6743d61b805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991719"
---
# <a name="structure-extensibility"></a>Extensibilité de la structure

Des dispositions sont prises pour étendre les constantes et les structures de manière indépendante du périphérique et dans un mode spécifique au périphérique (spécifique au fournisseur).

Dans les constantes qui sont des énumérations scalaires, une plage de valeurs est réservée aux futures extensions communes. Le reste des valeurs est identifié comme étant spécifique à l’appareil. Un fournisseur peut définir des significations pour ces valeurs de quelque manière que ce soit. L’interprétation de ces valeurs est indexée dans l' *identificateur d’extension* fourni via la structure de données [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) . Pour les constantes définies en tant qu’indicateurs binaires, une plage de bits de poids faible est réservée, où les bits de poids fort peuvent être spécifiques à l’extension. Il est recommandé que les valeurs étendues et les tableaux de bits utilisent des bits de la valeur la plus élevée ou du bit de poids fort. Cela laisse la possibilité de déplacer la bordure entre la partie commune et la portion d’extension si vous devez le faire à l’avenir. Les extensions des structures de données sont affectées à un champ de taille variable de taille/décalage faisant partie de la partie fixe. TSPI décrit pour chaque structure de données les extensions spécifiques aux appareils qui sont autorisées.

En plus de reconnaître un identificateur d’extension spécifique, TAPI (opérant pour le compte d’une application) doit négocier le numéro de version de l’extension sous lequel l’application et le fournisseur de services s’exécutent. Pour ce faire, utilisez les fonctions [**TSPI \_ LineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) et [**TSPI \_ phoneNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion) .

Un identificateur d’extension est un identificateur global unique. Il n’existe pas de registre central pour les identificateurs d’extension. Au lieu de cela, ils sont générés localement par le fabricant par un utilitaire disponible avec la boîte à outils. Le nombre est constitué de parties telles qu’une adresse LAN (unique), une heure de la journée et un nombre aléatoire, afin de garantir l’unicité globale. Les identificateurs globaux uniques sont conçus pour être distingués des identificateurs universels uniques HP/DEC et sont donc entièrement compatibles avec eux.

 

 
