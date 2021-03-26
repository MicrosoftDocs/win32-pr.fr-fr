---
description: Le tableau suivant spécifie les métriques de police les plus importantes pour les applications qui nécessitent des documents portables et les fonctions qui permettent à une application de les récupérer.
ms.assetid: 61f6d244-7397-42af-af58-0ab9d07bf19e
title: Mesures pour les documents portables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c840b1b8e8014086b97098a44890f170a6bd11d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972650"
---
# <a name="metrics-for-portable-documents"></a>Mesures pour les documents portables

Le tableau suivant spécifie les métriques de police les plus importantes pour les applications qui nécessitent des documents portables et les fonctions qui permettent à une application de les récupérer.



| Fonction                                               | Métrique                | Utilisation                                                                                                          |
|--------------------------------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)           | **ntmSizeEM**         | Récupération des métriques de conception ; conversion en métriques de l’appareil.                                                   |
| [**GetCharABCWidths**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)           | **ABCWidths**         | Positionnement précis des caractères au début et à la fin des marges, des limites de l’image et d’autres sauts de texte. |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)               | **AdvanceWidths**     | Positionnement des caractères sur une ligne.                                                                           |
| [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) | **otmfsType**         | Bits d’incorporation de police.                                                                                         |
|                                                        | **otmsCharSlopeRise** | Composant Y pour la pente du curseur pour les polices italiques.                                                            |
|                                                        | **otmsCharSlopeRun**  | Composant X pour la pente du curseur pour les polices en italique.                                                            |
|                                                        | **otmAscent**         | Interligne.                                                                                                |
|                                                        | **otmDescent**        | Interligne.                                                                                                |
|                                                        | **otmLineGap**        | Interligne.                                                                                                |
|                                                        | **otmpFamilyName**    | Identification de la police.                                                                                         |
|                                                        | **otmpStyleName**     | Identification de la police.                                                                                         |
|                                                        | **otmpFullName**      | Identification des polices (généralement, nom de famille et de style).                                                      |



 

Les membres **otmsCharSlopeRise**, **otmsCharSlopeRun**, **otmAscent**, **otmDescent** et **otmLineGap** de la structure [OUTLINETEXTMETRIC](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) sont mis à l’échelle ou transformés pour correspondre au mode d’appareil actuel et à la hauteur physique (comme spécifié dans le membre **tmHeight** de la structure [NEWTEXTMETRIC](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) ).

L’identification des polices est importante dans les cas où une application doit sélectionner la même police, par exemple lorsqu’un document est rouvert ou déplacé vers un autre système d’exploitation. Le mappeur de polices sélectionne toujours la police correcte lorsqu’une application demande une police par son nom complet. Les noms de famille et de style fournissent une entrée à la boîte de dialogue police standard, qui garantit que les barres de sélection sont placées correctement.

Les valeurs **otmsCharSlopeRise** et **otmsCharSlopeRun** sont utilisées pour produire une approximation proche de l’angle d’italique principal de la police. Pour les polices romanes standard, **otmsCharSlopeRise** est 1 et **otmsCharSlopeRun** est égal à 0. Pour les polices en italique, les valeurs tentent de rapprocher le sinus et le cosinus de l’angle d’italique principal de la police (dans les degrés gauches après la barre verticale); Notez que l’angle italique pour les polices verticales est 0. Comme ces valeurs ne sont pas exprimées en unités de conception, elles ne doivent pas être converties en unités de périphérique.

Les métriques d’emplacement des caractères et d’interligne permettent à une application de calculer des sauts de ligne indépendants du périphérique, portables sur des écrans, des imprimantes, des typesetters et même des plates-formes.

**Pour effectuer une mise en page indépendante du périphérique**

1.  Normaliser toutes les mesures de conception sur une valeur de haute résolution UHR (par exemple, 65 536 PPP); Cela empêche les erreurs d’arrondi.
2.  Sauts de ligne de calcul en fonction des métriques UHR et de la largeur de page physique ; Cela donne un point de départ et un point de fin d’une ligne dans le flux de texte.
3.  Calculez la largeur de page de l’appareil en unités d’appareil (par exemple, pixels).
4.  Ajuster chaque ligne de texte à la largeur de la page de l’appareil à l’aide des sauts de ligne calculés à l’étape 2.
5.  Calculez les sauts de page à l’aide des métriques UHR et de la longueur de page physique ; le nombre de lignes par page est ainsi généré.
6.  Calculez les hauteurs de ligne en unités de périphérique.
7.  Ajustez les lignes de texte sur la page, en utilisant les lignes par page de l’étape 5 et les hauteurs de ligne de l’étape 6.

Si toutes les applications adoptent ces techniques, les développeurs peuvent quasiment garantir que les documents déplacés d’une application à l’autre conserveront leur apparence et leur format d’origine.

 

 



