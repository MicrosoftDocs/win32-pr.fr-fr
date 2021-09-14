---
description: En savoir plus sur l’extensibilité constante. Des dispositions sont prises pour étendre les constantes et les structures de manière indépendante du périphérique et de manière spécifique à l’appareil.
ms.assetid: 78430503-3e1f-49ab-be9c-d48bd21a840e
title: Extensibilité constante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975d2901dcc3f7e574ffdacdabbcf457821ef932
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013509"
---
# <a name="constant-extensibility"></a>Extensibilité constante

Des dispositions sont prises pour étendre les constantes et les structures de manière indépendante du périphérique et dans un mode spécifique au périphérique (spécifique au fournisseur).

Dans les constantes qui sont des énumérations scalaires, une plage de valeurs est réservée aux futures extensions communes. Le reste des valeurs est identifié comme étant spécifique à l’appareil. Un fournisseur peut définir des significations pour ces valeurs de la manière souhaitée. L’interprétation de ces valeurs est indexée dans l’ID d’extension fourni via la structure de données [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) . Pour les constantes définies en tant qu’indicateurs binaires, une plage de bits de poids faible est réservée, où les bits de poids fort peuvent être spécifiques à l’extension. Il est recommandé que les valeurs étendues et les tableaux de bits utilisent des bits de la valeur la plus élevée ou du bit de poids fort. Cela laisse la possibilité de déplacer la bordure entre la partie commune et la portion d’extension si nécessaire pour le faire à l’avenir. Les extensions des structures de données sont affectées à un champ de taille variable de taille/décalage faisant partie de la partie fixe. TSPI décrit les extensions spécifiques au périphérique qui sont autorisées pour chaque structure de données. Pour plus d’informations, consultez la rubrique [allocation de mémoire](./memory-allocation.md) .

En plus de reconnaître un identificateur d’extension spécifique, TAPI (opérant pour le compte d’une application) doit négocier le numéro de version de l’extension sous lequel l’application et le fournisseur de services s’exécutent. Pour ce faire, utilisez les fonctions [**TSPI \_ LineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) et [**TSPI \_ phoneNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion) .

Un identificateur d’extension est un identificateur global unique. Il n’existe pas de registre central pour les identificateurs d’extension. Au lieu de cela, ils sont générés localement par le fabricant par un utilitaire disponible avec la boîte à outils. Pour garantir l’unicité globale, le nombre est composé de parties telles qu’une adresse LAN (unique), une heure de la journée et un nombre aléatoire. Les identificateurs globaux uniques sont conçus pour être distingués des identificateurs universels uniques HP/DEC et sont donc entièrement compatibles avec eux.

 

 
