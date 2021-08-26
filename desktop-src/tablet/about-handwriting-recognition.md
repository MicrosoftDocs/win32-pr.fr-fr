---
description: Tablet PC comprend une technologie permettant de reconnaître l’entrée manuscrite qui est le plus souvent sous la forme d’une écriture manuscrite.
ms.assetid: 614971a8-2b56-40d4-abb6-aba5ded01883
title: À propos de la reconnaissance de l’écriture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e4106d887eaa5bae2a162ab3c08a42c0d3b425b05a09b50bfcde626c05707f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119884049"
---
# <a name="about-handwriting-recognition"></a>À propos de la reconnaissance de l’écriture

Tablet PC comprend une technologie permettant de reconnaître l’entrée manuscrite qui est le plus souvent sous la forme d’une écriture manuscrite. Le module logiciel qui fournit la reconnaissance porte le nom de module de reconnaissance. Un module de reconnaissance reconnaît une langue, un groupe de langues associées ou une classe d’objets connexes tels que des notes musicales, des gestes système ou des formes géométriques. Vous pouvez ajouter dynamiquement des modules de reconnaissance au système des services d’encre.

## <a name="recognition-steps"></a>Étapes de reconnaissance

La reconnaissance est gérée à l’aide d’un contexte de module de reconnaissance. La reconnaissance se compose de quatre étapes de base :

1.  Configuration des contraintes de reconnaissance en :
    -   Sélection du module de reconnaissance et du mode de saisie (contraintes géométriques).
    -   Définition des contraintes de langue. Par exemple, vous pouvez limiter l’entrée à des caractères alphanumériques ou vous pouvez passer des schémas pour aider le module de reconnaissance.
2.  Envoi d’une entrée manuscrite au module de reconnaissance.
3.  Traitement de l’entrée (reconnaissance).
4.  Retour des résultats de la reconnaissance.

Les étapes 2 et 3 peuvent être répétées dans une boucle, ou tous les traits d’encre peuvent être ajoutés à l’encre avant une tentative de reconnaissance.

## <a name="samples-and-related-topics"></a>Exemples et Rubriques connexes

L' [exemple de reconnaissance avancée](advanced-recognition-sample.md) montre comment utiliser des détecteurs avec des objets [**Ink**](inkdisp-class.md) pour effectuer la reconnaissance de l’encre.

L' [exemple de modèle de dll de reconnaissance](recognizer-dll-sample-template.md) contient un modèle pour la création d’une dll de module de reconnaissance. Le modèle contient des fonctions pour l’inscription et l’annulation de l’inscription du serveur, ainsi que des squelettes pour les fonctions de reconnaissance principales.

Les sections suivantes décrivent les concepts de base qui sous-tendent la technologie de reconnaissance de Tablet PC. Pour plus d’informations sur la création de détecteurs personnalisés, consultez [création d’un module de reconnaissance](creating-a-recognizer.md).

-   [Reconnaissance de texte](text-recognizers.md)
-   [Identificateurs d’objets](object-recognizers.md)
-   [Utilisation de la collection Recognizers](using-the-recognizers-collection.md)
-   [Contexte du module de reconnaissance](recognizer-context.md)
-   [Segments de reconnaissance](recognition-segments.md)
-   [Reconnaissance du texte en angle](recognition-of-angled-text.md)
-   [Prise en charge de la réorganisation de la séquence de reconnaissance](recognizer-stroke-reordering-support.md)
-   [Dictionnaires et Factoids](dictionaries-and-factoids.md)
-   [Propriété \[ de confiance sur la reconnaissance\]](confidence-property--about-recognition.md)
-   [Alternatives](alternates.md)
-   [Segments d’encre et alternatives](ink-segments-and-alternates.md)

 

 



