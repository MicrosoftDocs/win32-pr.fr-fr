---
title: À propos des interfaces utilisateur de Active Directory Domain Services
description: Les administrateurs et les utilisateurs doivent être en mesure d’afficher et de modifier les objets de service d’annuaire dans Microsoft Active Directory Domain Services à partir d’une interface utilisateur.
ms.assetid: b6eec599-ebb3-40af-a4a2-059755285854
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b22c97cd84fd51cc19a621ae948fceda28f87fda6077a0fcb50eb10b5618ea5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118025749"
---
# <a name="about-the-user-interfaces-of-active-directory-domain-services"></a>À propos des interfaces utilisateur de Active Directory Domain Services

Les administrateurs et les utilisateurs doivent être en mesure d’afficher et de modifier les objets de service d’annuaire dans Microsoft Active Directory Domain Services à partir d’une interface utilisateur. Les administrateurs gèrent le serveur Active Directory à l’aide de différents composants logiciels enfichables MMC (Microsoft Management Console), en particulier les Active Directory Domain Services utilisateurs et ordinateurs, Active Directory Domain Services sites et services, Active Directory Domain Services domaines et approbations et Active Directory Domain Services composants logiciels enfichables du gestionnaire de schémas. L’utilisateur final, s’il dispose des autorisations appropriées, peut également utiliser les composants logiciels enfichables MMC Active Directory pour afficher les objets d’annuaire. le shell Windows peut également être utilisé pour afficher des objets d’annuaire. le shell Windows permet aux utilisateurs de parcourir les objets stockés dans l’annuaire à partir de l’élément d’annuaire dans les favoris réseau sur le bureau ou via les boîtes de dialogue de recherche disponibles dans le menu Démarrer.

Active Directory Domain Services prendre en charge une interface utilisateur qui s’adapte aux besoins des administrateurs et des utilisateurs finaux. Active Directory Domain Services vous permettent d’étendre l’interface utilisateur qui représente des classes d’objets existantes, ainsi que de nouvelles classes ajoutées au schéma. Les éléments suivants peuvent être utilisés pour contrôler ou étendre l’interface utilisateur pour chaque classe définie dans le schéma :

-   [Pages de propriétés à utiliser avec les spécificateurs d’affichage](property-pages-for-use-with-display-specifiers.md)
-   [Menus contextuels à utiliser avec les spécificateurs d’affichage](context-menus-for-use-with-display-specifiers.md)
-   [Noms complets des classes et des attributs](class-and-attribute-display-names.md)
-   [Assistants de création d’objets](object-creation-wizards.md)
-   [Icônes de classe](class-icons.md)
-   [Affichage des conteneurs en tant que nœuds terminaux](viewing-containers-as-leaf-nodes.md)

à partir de Windows 2000, le système fournit des objets COM qui implémentent des boîtes de dialogue courantes pour travailler avec des objets d’annuaire. Ces boîtes de dialogue fournissent une interface utilisateur commune sans avoir à réimplémenter ces boîtes de dialogue.

-   [Sélecteur d’objets d’annuaire](directory-object-picker.md)
-   [Explorateur de domaines](domain-browser.md)
-   [Navigateur de conteneurs](container-browser.md)

Active Directory les composants logiciels enfichables d’administration, les menus contextuels et les pages de propriétés peuvent être étendus à l’aide des composants logiciels enfichables d’extension MMC. D’autres extensions MMC, telles que des listes de tâches, des éléments d’espace de noms, des barres de contrôles et des barres d’outils, peuvent également être implémentées. Pour plus d’informations, consultez [extension des composants logiciels enfichables d’administration de Active Directory](/previous-versions/windows/desktop/mmc/extending-the-active-directory-administrative-snap-ins).

 

 