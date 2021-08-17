---
description: Cette rubrique fournit des actions à effectuer pour créer du code prenant en charge plusieurs marchés. Considérez ces instructions comme un guide lors de la conception du code et comme des mesures lorsque vous évaluez les builds.
ms.assetid: cf2ac58e-7fc3-4635-8b82-586a0732b2a3
title: Liste de contrôle d’internationalisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd4650f7bd1111f35c911d6efe12bfbec4b537f2cdabdc50160965b5e602708b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147512"
---
# <a name="internationalization-checklist"></a>Liste de contrôle d’internationalisation

Cette rubrique fournit des actions à effectuer pour créer du code prenant en charge plusieurs marchés. Considérez ces instructions comme un guide lors de la conception du code et comme des mesures lorsque vous évaluez les builds.

-   Créez les spécifications du programme pour prendre en compte les considérations internationales dès le départ.
    -   Concevez les icônes et les bitmaps pour qu’elles soient significatives et non choquantes sur vos marchés cibles, et ne contiennent pas de texte.
    -   Concevoir des menus et des boîtes de dialogue pour laisser de la place pour l’expansion de texte. Par exemple, les chaînes en anglais s’étendent souvent de 40% lorsqu’elles sont traduites en allemand ou néerlandais.
    -   N’utilisez pas d’argot ou de références spécifiques à la culture dans des éléments d’interface utilisateur ou des messages.
    -   Créez des combinaisons de touches de raccourci qui sont accessibles sur les claviers internationaux. Par exemple, évitez d’utiliser des touches de caractère de ponctuation comme touches de raccourci, car elles ne se trouvent pas toujours sur les claviers internationaux ou sont facilement générées par l’utilisateur. pour obtenir des exemples de dispositions du clavier, consultez [Windows les dispositions du clavier](https://msdn.microsoft.com/goglobal/bb964651.aspx).
    -   Tenez compte des lois locales qui affectent les conceptions de fonctionnalités, telles que les exigences que les entités gouvernementales achètent des logiciels qui prennent en charge plusieurs langues officielles.
    -   Développez des contrats tiers qui prennent en charge les normes d’interface utilisateur internationales et les décisions de conception de votre organisation.
    -   Utilisez une terminologie cohérente dans les chaînes d’interface utilisateur qui doivent être traduites.

<!-- -->

-   Créez du code indépendant des paramètres régionaux.
    -   Ne concaténez pas de chaînes pour former des phrases.
    -   N’utilisez pas une variable de chaîne donnée dans plusieurs contextes, telles que la réutilisation d’un fragment de phrase dans différents messages et invites, car ces chaînes peuvent ne pas être faciles à traduire.
    -   Documentez les chaînes à l’aide de commentaires pour fournir un contexte aux traducteurs, et marquez clairement les chaînes ou les caractères qui ne doivent pas être localisés.
    -   N’utilisez pas de constantes de caractères codées en dur, de constantes numériques, de positions d’écran, de noms de fichiers ou de chemins d’accès qui présupposent une langue particulière.
    -   Augmentez la taille des mémoires tampon pour qu’elles contiennent des chaînes traduites.
    -   Autorisez l’entrée de données avec des formats qui varient selon les paramètres régionaux, tels que les dates, les heures et les devises.
    -   Utilisez le format de papier, la taille d’enveloppe et d’autres valeurs par défaut appropriées pour les paramètres régionaux donnés.
    -   Vérifiez que chaque édition de langue peut lire les documents créés par les autres éditions.
    -   Assurez la prise en charge du matériel spécifique aux paramètres régionaux, si nécessaire.
    -   Configurez les fonctionnalités qui ne s’appliquent pas aux marchés internationaux en tant qu’options d’implémentation qui peuvent être facilement désactivées.

<!-- -->

-   Créez du code qui tire parti des fonctionnalités internationales offertes par Microsoft Windows.
    -   Utilisez les informations internationales fournies par le système (prise en charge des langues nationales).
    -   Utilisez les fonctions système pour le tri, la conversion de casse et le mappage de chaînes.
    -   Utilisez des fonctions de mise en page de texte génériques.
    -   Répondez aux modifications apportées aux paramètres internationaux dans le panneau de configuration.
    -   Gérez le \_ message WM INPUTLANGCHANGEREQUEST.
    -   Prise en charge des éditeurs de méthode d’entrée, du texte vertical et des règles de saut de ligne dans les éditions East asiatique.

<!-- -->

-   Compilez toutes les éditions internationales du programme à partir d’un ensemble de fichiers sources.
    -   Réduisez ou éliminez les mécanismes qui nécessitent une recompilation du code pour différentes éditions de langue.
    -   stocker des éléments localisables, tels que des chaînes et des icônes, dans des fichiers de ressources Windows.
    -   Stockez les documents dans toutes les éditions de langue en utilisant le même format de fichier.

<!-- -->

-   Prenez en charge des jeux de caractères différents, et pas seulement la page de codes latin 1, numéro 1252.
    -   Le programme prend en charge les environnements réseau dans lesquels les ordinateurs exécutent des systèmes d’exploitation avec des pages de codes par défaut différentes.
    -   Utilisez GetCPInfoEx pour récupérer les plages de bits des pages de codes d’Extrême-Orient.
    -   Analyser les caractères codés sur deux octets dans les applications de langage extrême-orientale, sauf si le code est basé sur Unicode.
    -   Prend en charge Unicode ou la conversion entre Unicode et la page de codes locale.
    -   Ne partez pas du principe que tous les caractères sont de 8 ou 16 bits.
    -   Utilisez les types de données génériques et les prototypes de fonction génériques.
    -   Utilisez la propriété jeu de caractères de police, qui appelle EnumFontFamiliesEx et la fonction de boîte de dialogue commune ChooseFont.
    -   Affichez et imprimez du texte à l’aide des polices appropriées pour les paramètres régionaux.

<!-- -->

-   Testez les fonctionnalités internationales du programme.
    -   Le texte traduit doit respecter les normes des orateurs natifs.
    -   Les boîtes de dialogue doivent être redimensionnées correctement et le texte doit être coupé de manière appropriée, lorsque différentes langues sont affichées.
    -   Les boîtes de dialogue, les barres d’État, les barres d’outils et les menus doivent tenir sur l’écran et être lus de façon lisible lorsque l’affichage est défini selon des résolutions différentes, pour toutes les langues traduites.
    -   Les accélérateurs de boîtes de dialogue et de menus doivent être uniques.
    -   Les utilisateurs doivent être en mesure de taper des caractères à partir de scripts non européens dans des documents, des boîtes de dialogue et des noms de fichiers.
    -   Les utilisateurs doivent pouvoir couper, coller, enregistrer et imprimer correctement des caractères à partir de scripts non européens.
    -   Le tri et la conversion de casse doivent être précis pour des paramètres régionaux différents.
    -   L’application doit fonctionner correctement dans les versions localisées de Windows.

 

 



