---
description: Cette rubrique vous aide à créer des applications mondialisables, en spécifiant des conditions préalables, en résumant les technologies et en introduisant un didacticiel de prise en main.
ms.assetid: 80c10bc2-b7e3-4f24-8bac-826149a376c7
title: Prise en main avec le développement International Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c346f03717b5f50c27911891daaea8aa4ed55ce199e7ca807690d2f3185d8114
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949428"
---
# <a name="getting-started-with-international-windows-development"></a>Prise en main avec le développement International Windows

Cette rubrique vous aide à créer des applications mondialisables, en spécifiant des conditions préalables, en résumant les technologies et en introduisant un didacticiel de prise en main.

## <a name="getting-started"></a>Mise en route

Si vous écrivez des applications pour les utilisateurs dans un seul paramètre régional, ces applications peuvent réussir même si vous les concevez avec des hypothèses spécifiques aux paramètres régionaux, telles que la présentation de dates dans un format particulier ou le tri de chaînes dans une séquence particulière. Mais maintenant, vous devez vous assurer que vos applications peuvent être utilisées dans plusieurs pays, par des utilisateurs qui ont des langues et des cultures différentes. Pour que la tentative aboutisse à plusieurs paramètres régionaux, les applications doivent s’adapter aux paramètres régionaux dans lesquels elles s’exécutent. Cette flexibilité est importante, que vous l’ajoutiez à une application existante ou que vous la conceviez dans une nouvelle application.

Cette section vous aide à prendre en main le développement international. Il présente des liens vers des rubriques qui fournissent des présentations préalables de l’internationalisation. Il résume les technologies que le kit de développement logiciel (SDK) propose pour la prise en charge des clients dans le monde entier. Enfin, cette section fournit un exemple d’application qui résout un problème que vous rencontrez souvent lors de l’écriture de logiciels globaux.

## <a name="prerequisites"></a>Prérequis

Vous devez vous familiariser avec les problèmes qui surviennent lors du développement de logiciels internationaux pour Windows. Commencez avec ces vues d’ensemble.

-   La compréhension de l' [internationalisation](understanding-internationalization.md) explique la difficulté supplémentaire du développement d’applications mondialisables et définit des termes clés.
-   La rubrique [obtenir un monde](https://msdn.microsoft.com/goglobal/bb895995.aspx) public vous amène à des instructions et des méthodes recommandées que vous pouvez parcourir ou explorer en fonction des besoins.
-   La [liste de contrôle d’internationalisation](internationalization-checklist.md) récapitule les mesures à prendre pour créer une application mondialisable.
-   La sécurité est toujours un problème dans le développement de logiciels, mais vous devez prendre en compte d’autres problèmes lors du développement de logiciels internationaux. Examinez les [considérations relatives à la sécurité : fonctionnalités internationales](security-considerations--international-features.md).

Tenez également compte des articles les plus complets qui se trouvent dans le [Centre de développement Go Global](https://msdn.microsoft.com/globalization/mt613165) dans la section [étape par étape de la globalisation](https://msdn.microsoft.com/globalization/mt642951) . Au fur et à mesure que vous développez des logiciels internationaux, vous souhaiterez consulter les vues d’ensemble et les Articles détaillés supplémentaires qui se trouvent ici.

## <a name="learning-paths"></a>Parcours d’apprentissage

Le chemin d’accès que vous suivez ensuite pour créer des logiciels internationaux dépend des scénarios que vous rencontrez. les scénarios suivants sont basés sur ceux introduits dans la rubrique principale section, [internationalisation pour les Applications Windows](international-support.md).

-   **Créer des applications qui peuvent être déployées dans plusieurs régions dans plusieurs langues.**

    Le défi consiste à développer une application qui n’a pas besoin d’être réécrite pour chaque langue ou culture.

    -   lisez l’article [understanding interface utilisateur multilingue (MUI)](./about-multilingual-user-interface.md).
    -   explorez la documentation de [interface utilisateur multilingue](multilingual-user-interface.md).
    -   Prise en main de l’application [Hello MUI](#the-hello-mui-application) .

-   **Prend en charge l’entrée et l’affichage de différentes langues, jeux de caractères et polices.**

    Votre application peut avoir besoin de prendre en charge plusieurs jeux de caractères, de prendre en charge des scripts complexes (tels que ceux utilisés pour représenter les langues hébreu, arabe, thaï et Indo-aryen), d’autoriser l’utilisateur à sélectionner des polices internationales ou d’autoriser l’utilisateur à entrer des caractères et des symboles, tels que le japonais kanji, pour d’autres langues à l’aide d’un clavier

    -   Lisez les articles :

        -   [Prise en charge des scripts et des polices dans Windows](https://msdn.microsoft.com/globalization/mt791278)
        -   [Langue d’entrée : claviers et IME](https://msdn.microsoft.com/globalization/mt662332)

    -   Explorez la documentation de :

        -   [Unicode et jeux de caractères](unicode-and-character-sets.md)
        -   [Polices internationales et affichage du texte](international-fonts-and-text-display.md)
        -   [Gestionnaire de méthode d’entrée](input-method-manager.md)

-   **Affichez les objets dépendants de la culture dans les formats appropriés.**

    Les applications internationales doivent utiliser des paramètres régionaux pour trier correctement les chaînes et afficher des informations dépendantes de la culture, telles que l’heure, les dates et les devises.

    -   Explorez le [Centre de connaissances en matière de prise en charge linguistique nationale](./national-language-support-reference.md).
    -   Consultez la documentation relative au [service NLS (National Language Support)](national-language-support.md).

-   **Découvrez la langue ou le script utilisé par l’utilisateur et appliquez-le aux autres services de l’application.**

    Si votre application peut déterminer la langue dans laquelle le texte et l’entrée utilisateur sont écrits, elle peut afficher du contenu tel que des invites ou de l’aide dans un langage compréhensible.

    -   lisez l’article [sur l’écriture d’Applications mondialisables dans Windows : Services linguistiques étendus dans Windows](./using-extended-linguistic-services.md).
    -   Explorez la documentation des [services linguistiques étendus (ELS)](extended-linguistic-services.md).

## <a name="internationalization-technologies-in-the-sdk"></a>Technologies d’internationalisation dans le kit de développement logiciel (SDK)

La section prise en charge du développement international du kit de développement logiciel (SDK) fournit des technologies qui permettent à l’application d’énumérer les langues, les paramètres régionaux et les formats propres aux paramètres régionaux. Vous pouvez les utiliser dans les applications Microsoft Win32 que vous écrivez en C ou C++.

Les [services linguistiques étendus](extended-linguistic-services.md) offrent une technologie brevetée par Microsoft pour l’identification des langues et des scripts dans du texte. Votre application peut déterminer les services disponibles en fonction de la catégorie, ainsi que de la langue d’entrée et de sortie, du script et du type de contenu.

les [polices et l’affichage de texte internationaux](international-fonts-and-text-display.md) fournissent des informations sur les polices internationales, les scripts complexes et les glyphes, ainsi que le rendu parfait de la typographie sur la plateforme Windows.

Le [Gestionnaire de méthode d’entrée](input-method-manager.md) est une technologie qui permet à l’application de recevoir l’entrée d’un logiciel de l’éditeur de méthode d’entrée (IME), qui à son tour autorise l’entrée de caractères et de symboles, tels que le japonais kanji, pour d’autres langues à l’aide d’un clavier standard.

## <a name="the-hello-mui-application"></a>L’application Hello MUI

Une tâche courante dans le développement international commence par une application monolingue que vous devez rendre universelle. Vous devez ajouter la prise en charge de langues supplémentaires, mais d’une manière qui ne nécessite pas de réécrire le code pour chaque nouvelle langue ou culture.

cette tâche offre la possibilité de présenter un didacticiel qui vous guide tout au long de la création d’une application Hello mui, en utilisant le modèle de ressource de l' [interface utilisateur multilingue (mui)](multilingual-user-interface.md) et la prise en charge associée fournie dans Windows.

Ce didacticiel adopte le concept de l’application Hello World familière, en expliquant l’utilisation de l’interface MUI pour créer une application multilingue de base.

vous pouvez commencer le didacticiel sur l’interface MUI Hello [pour ajouter interface utilisateur multilingue Support à une Application](creating-a-multilingual-user-interface-application.md).

 

 
