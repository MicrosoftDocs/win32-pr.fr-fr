---
description: cette section décrit les technologies de Windows qui vous permettent de prendre en charge les nombreuses cultures et les langues écrites de la place de marché internationale dans votre application Microsoft Win32 basée sur C ou C++.
ms.assetid: 90dbbd70-3609-4c12-bdc1-7fa222c96f67
title: Internationalisation pour les applications Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78f4831390ffc31a5f3290f0784d32c3aa1044863c708e6e0329225519c2cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147542"
---
# <a name="internationalization-for-windows-applications"></a>Internationalisation pour les applications Windows

(Anciennement intitulé « support international »)

cette section décrit les technologies de Windows qui vous permettent de prendre en charge les nombreuses cultures et les langues écrites de la place de marché internationale dans votre application Microsoft Win32 basée sur C ou C++.

Windows est devenu une plateforme essentielle pour les clients du monde entier. Les utilisateurs internationaux attendent des solutions adaptées à leurs langues et régions dans le monde entier. Dans cette section, vous trouverez les informations dont vous avez besoin pour développer des solutions multilingues, multiculturelles et multisites. la prise en charge internationale intégrée à Windows vous permet d’implémenter de nombreux scénarios avec une surcharge d’ingénierie moins importante que jamais.

Le développement d’applications mondialisables requiert l’utilisation de nombreux services et outils. Windows contient des fonctionnalités qui vous permettent de développer des solutions qui :

- Prenez en charge les différents besoins spécifiques des langues et propres aux paramètres régionaux des utilisateurs dans le monde entier (y compris la prise en charge de texte spécialisée, le comportement de tri, la mise en forme de la date et de l’heure et les dispositions du clavier). (Pour plus d’informations, consultez le [Centre de connaissances du support linguistique national](./national-language-support-reference.md).)
- Sont globalisés (peuvent être déployés dans le monde entier à partir d’une seule image binaire) et peuvent être localisés (adaptés à des marchés locaux spécifiques). (pour plus d’informations, consultez [interface utilisateur multilingue](./multilingual-user-interface.md).)
- Affichez les polices et le texte internationaux, et autorisez les utilisateurs à spécifier la police de leur choix. (Pour plus d’informations, consultez [prise en charge des scripts et des polices dans Windows](/globalization/input/font-support).)
- Autorisez l’utilisateur à entrer des caractères et des symboles complexes à l’aide d’un clavier standard.
- Assurez la prise en charge de nombreux langages écrits différents par le biais de jeux de caractères Unicode et traditionnels.
- Découvrez l’entrée de langue d’un utilisateur et personnalisez l’expérience utilisateur fournie par votre application. (pour plus d’informations, consultez [écriture d’Applications mondialisables dans Windows : Services linguistiques étendus dans Windows](./using-extended-linguistic-services.md).)

## <a name="in-this-section"></a>Dans cette section

Les technologies de support internationales suivantes sont documentées dans cette section. Ils sont répertoriés dans certains scénarios clés pour lesquels ils peuvent être utilisés.

- [Prise en main avec le développement International Windows](getting-started-with-international-development.md)

    Décrit comment prendre en main la création d’applications mondialisables et fournit un didacticiel illustrant une tâche courante dans l’écriture de logiciels globaux.

    Scénarios courants :

    - Déterminez le chemin à suivre pour apprendre à développer des logiciels internationaux.
    - découvrez les technologies d’internationalisation disponibles dans le kit de développement logiciel (SDK) de Microsoft Windows.
    - Suivez un didacticiel qui prend une application monolingue existante et ajoute la prise en charge de langues supplémentaires.

- [Services de globalisation](globalization-services.md)

    Décrit les [services linguistiques étendus](extended-linguistic-services.md), qui vous permettent de découvrir le langage dans lequel les entrées de texte et utilisateur sont écrites, ainsi que la [prise en charge linguistique nationale (nls)](national-language-support.md), qui permet à une application d’utiliser les informations de paramètres régionaux pour afficher des informations dépendantes de la culture (telles que l’heure, les dates et la monnaie) et trier correctement les chaînes.

    Scénarios courants :

    - Découvrez la langue de l’entrée de l’utilisateur, afin que le contenu de l’aide puisse être affiché dans un langage compréhensible.
    - Détecte le script utilisé dans le texte à afficher. S’il s’agit d’un chinois simplifié ou traditionnel, offrez à l’utilisateur la possibilité de faire la transcription du texte de l’un à l’autre.
    - Permet à l’utilisateur de sélectionner des paramètres régionaux (une collection d’informations sur les préférences de l’utilisateur relatives à la langue).
    - Affichez des heures, des dates, des informations de calendrier, des devises et de nombreux autres objets dépendants de la culture dans les langages et formats appropriés.
    - Triez les chaînes dans l’ordre attendu par l’utilisateur des paramètres régionaux donnés.

- [Gestionnaire de méthode d’entrée](input-method-manager.md)

    Décrit la technologie utilisée par une application pour communiquer avec un éditeur de méthode d’entrée (IME). L’IME permet aux utilisateurs de l’ordinateur d’entrer des caractères et des symboles complexes à l’aide d’un clavier standard.

    Scénario courant :

    - Autorisez l’utilisateur à utiliser un clavier standard pour entrer des caractères Kanji japonais.

- [Polices internationales et affichage du texte](international-fonts-and-text-display.md)

    décrit la prise en charge fournie par la plateforme Windows pour les polices internationales, le texte international et la typographie fine.

    Scénarios courants :

    - Permet à l’utilisateur de sélectionner des polices internationales basées sur le jeu de caractères.
    - Affichez le texte international.
    - Traiter des scripts complexes, notamment le rendu bidirectionnel, la mise en forme contextuelle et les ligatures (Uniscribe).
    - Autorisez un degré élevé de contrôle pour la typographie fine (Uniscribe).

- [Interface utilisateur multilingue](multilingual-user-interface.md)

    Décrit comment les applications peuvent séparer les ressources dépendantes du langage du code indépendant du langage pour les langues d’interface utilisateur prises en charge.

    Scénarios courants :

    - Créer des images de déploiement unique régionales ou mondiales d’une application.
    - Localiser une solution en mettant à jour les ressources d’application sans modifier le code source de l’application.
    - Autorisez les utilisateurs à basculer d’une langue d’interface utilisateur à une autre au moment de l’exécution.

- [Unicode et jeux de caractères](unicode-and-character-sets.md)

    Décrit comment les applications peuvent tirer parti d’Unicode, la norme de codage de caractères mondiale qui utilise des valeurs de code de 16 bits pour représenter tous les caractères utilisés dans l’informatique moderne, y compris les symboles techniques et les caractères spéciaux utilisés dans la publication.

    Scénarios courants :

    - Prendre en charge les différentes langues de la place de marché internationale par le biais d’Unicode.
    - Convertit les caractères Unicode vers et à partir d’autres jeux de caractères, si nécessaire.

- [Considérations relatives à la sécurité : fonctionnalités internationales](security-considerations--international-features.md)

    Fournit des informations sur les considérations de sécurité liées aux fonctionnalités de prise en charge du développement international.

    Les informations de sécurité se rapportent à tous les scénarios.

## <a name="related-international-technologies"></a>Technologies internationales associées

La prise en charge du développement international est également disponible pour les applications écrites en code managé. si vous développez pour le .NET Framework, vous aurez besoin d’une partie ou de la totalité des éléments suivants :

- L' [espace de noms System. Globalization](/dotnet/api/system.globalization) contient des classes qui définissent des informations liées à la culture et fournissent des fonctions de globalisation avancées.
- L' [espace de noms System. Text](/dotnet/api/system.text) contient des classes qui représentent des encodages de caractères, des blocs de caractères et des objets de chaîne de manipulation et de mise en forme.
