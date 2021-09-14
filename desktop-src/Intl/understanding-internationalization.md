---
description: Compréhension de l’internationalisation
ms.assetid: 9147cd20-eeae-4ad4-8d51-ac1d68a4b2c5
title: Compréhension de l’internationalisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df3fc38ab844ec991c0e87f286ffb48c3d48ec7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224260"
---
# <a name="understanding-internationalization"></a>Compréhension de l’internationalisation

Le développement de produits logiciels internationaux requiert non seulement la production de code correct, mais également une conception permettant au produit de prendre en charge de nombreux paramètres régionaux. Les développeurs et leurs responsables doivent connaître le niveau d’effort et l’attention aux détails nécessaires à la création d’applications mondialisables, qu’elles les diffusent en tant que fichiers binaires uniques prêts à l’emploi sur de nombreux marchés différents ou en tant que fichiers binaires multiples spécifiques à un paramètre régional. En tant que développeur, assurez-vous que votre gestion comprend que l’internationalisation implique plus que le simple développement de code. La conception de l’internationalisation au début de votre cycle de produit vous fait gagner du temps, de l’argent et des efforts.

L' **internationalisation** est la création de logiciels qui s’adaptent aux paramètres régionaux dans le monde entier. Les **paramètres régionaux** sont un ensemble de préférences utilisateur liées à la langue. Les paramètres régionaux sont spécifiés par le jumelage d’une langue et d’une région géographique. Par exemple, l’anglais (États-Unis) et l’anglais (Royaume-Uni) sont deux paramètres régionaux différents, tels que l’anglais (Canada) et le français (Canada).

Les logiciels internationaux possèdent les attributs suivants :

-   **Le monde** de la préparation couvre la conception et l’implémentation qui séparent le code indépendant des paramètres régionaux des ressources dépendantes des paramètres régionaux et comprend deux domaines majeurs :
    -   La **globalisation** est le processus de développement d’un noyau de programme avec des fonctionnalités et une conception de code indépendantes de la langue ou des paramètres régionaux. Au lieu de cela, la conception prend en charge l’entrée, l’affichage et la sortie des scripts de langage pris en charge par Unicode, ainsi que les données relatives à des paramètres régionaux spécifiques.
    -   L' **adaptabilité** est la conception de la base de code et des ressources logicielles, de telle sorte qu’un programme peut être localisé, comme indiqué ci-dessous, dans différentes éditions de langue sans aucune modification du code source. Par exemple, les mémoires tampons de chaîne dans le code et les zones de texte de l’interface utilisateur doivent être suffisamment grandes pour prendre en charge des chaînes de texte plus longues dans des langues telles que l’allemand ou le néerlandais.
-   **Localisation** Cela implique la traduction et la personnalisation d’un produit pour un marché spécifique, et il s’agit essentiellement de créer des fichiers de ressources plutôt que d’écrire du code source.

Par exemple, l’utilisation du service NLS (National Language Support) fourni par l’API Microsoft Win32 est un processus de développement de logiciels qui prend en charge le monde, tandis que la modification des éléments de l’interface utilisateur, la traduction de texte et la terminologie de normalisation sont des étapes de localisation généralement effectuées par une personne qui est un spécialiste linguistique, tel qu’un traducteur. Même lorsque le développement de votre code met l’accent sur le monde, vous devez comprendre la localisation, car vos décisions de conception affectent le travail du traducteur.

 

 



