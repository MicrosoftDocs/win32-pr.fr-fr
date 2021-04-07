---
description: Les reconnaissance de texte divisent un échantillon d’encre en segments et traduisent les segments d’encre en texte.
ms.assetid: 9fbdde0e-5312-48ec-9273-ded6703b99a9
title: Reconnaissance de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8372af61d45bb1cc8bcd8377202149073c3decc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759513"
---
# <a name="text-recognizers"></a>Reconnaissance de texte

Les reconnaissance de texte divisent un échantillon d’encre en segments et traduisent les segments d’encre en texte. Cela est utile pour la reconnaissance de l’écriture manuscrite. Elle est également utile dans les scénarios d’écriture complexes, tels que la reconnaissance de glyphes kanji individuels et l’offre aux utilisateurs la saisie semi-automatique d’un caractère pendant qu’ils l’écrivent.

Un module de reconnaissance de texte retourne une chaîne Unicode pour chaque segment de reconnaissance d’encre. L’accompagnement de la chaîne est le niveau de confiance que le module de reconnaissance affecte au résultat et un mappage du résultat à l’encre d’origine. Ce mappage montre le segment de l’encre d’origine qui correspond à la chaîne de code Unicode. La chaîne qui représente la sortie du module de reconnaissance de texte est toujours représentée dans l’ordre linéaire, plutôt que dans l’ordre spatial ou l’ordre chronologique dans lequel les segments étaient entrés.

Le tableau suivant répertorie les langues prises en charge par les reconnaissance de l’écriture manuscrite Microsoft et les versions de Windows dans lesquelles ces langues ont été introduites pour la première fois. Notez que certains identificateurs de langage peuvent ne pas être disponibles sur certaines versions de Windows et devront être téléchargés séparément. Des détecteurs tiers peuvent également être disponibles pour des langues supplémentaires, mais ils ne sont pas nécessairement recommandés par Microsoft.



| Language                                   | Windows XP Édition Tablet PC | Windows XP Édition Tablet PC 2005 | Windows Vista | Windows 7 |
|--------------------------------------------|------------------------------|-----------------------------------|---------------|-----------|
| Chinois (simplifié et traditionnel)       | X                            |                                   |               |           |
| Anglais (États-Unis, Royaume-Uni, Canada et Australie)    | X                            |                                   |               |           |
| Français                                     | X                            |                                   |               |           |
| Allemand                                     | X                            |                                   |               |           |
| Japonais                                   | X                            |                                   |               |           |
| Coréen                                     | X                            |                                   |               |           |
| Espagnol                                    | X                            |                                   |               |           |
| Italien                                    |                              | X                                 |               |           |
| Néerlandais (Pays-Bas et Belgique)            |                              |                                   | X             |           |
| Portugais (Brésil et portugais/neutre) |                              |                                   | X             |           |
| Catalan                                    |                              |                                   |               | X         |
| Croate                                   |                              |                                   |               | X         |
| Tchèque                                      |                              |                                   |               | X         |
| Danois                                     |                              |                                   |               | X         |
| Finnois                                    |                              |                                   |               | X         |
| Allemand (Suisse)                       |                              |                                   |               | X         |
| Norvégien (bokmål et nynorsk)             |                              |                                   |               | X         |
| Polonais                                     |                              |                                   |               | X         |
| Portugais (Portugal)                      |                              |                                   |               | X         |
| Roumain                                   |                              |                                   |               | X         |
| Russe                                    |                              |                                   |               | X         |
| Serbe (cyrillique et latin)               |                              |                                   |               | X         |
| Espagnol (Argentine et Mexique)             |                              |                                   |               | X         |
| Suédois                                    |                              |                                   |               | X         |



 

 

 



