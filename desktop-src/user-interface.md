---
description: Cette section fournit des conseils pour l’intégration et l’extension des fonctionnalités d’accès utilisateur de Windows.
ms.assetid: 1ffeeb4f-b337-45b9-885f-307b81670557
title: Environnement de bureau
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb60457f700489ca4e9e7368425df380f8d10d64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515641"
---
# <a name="desktop-environment"></a>Environnement de bureau

Cette section fournit des conseils pour l’intégration et l’extension des fonctionnalités d’accès utilisateur de Windows. Vous pouvez apprendre à vous assurer que vos applications et formats de fichiers s’affichent et se comportent correctement dans Démarrer, dans la barre des tâches, sur le bureau et dans l’Explorateur de fichiers. Vous pouvez également vous assurer que vos formats de fichiers et vos magasins de données sont indexables et pouvant faire l’objet de recherches.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Shell Windows](./shell/shell-entry.md)<br/>                                      | L’interface utilisateur du bureau Windows permet aux utilisateurs d’accéder à un large éventail d’objets nécessaires pour exécuter des applications et gérer le système d’exploitation. Les plus nombreux et les plus familiers de ces objets sont les dossiers et les fichiers qui résident sur les lecteurs de disque de l’ordinateur. Il existe également un certain nombre d’objets virtuels qui permettent à l’utilisateur d’effectuer des tâches telles que l’envoi de fichiers à des imprimantes distantes ou l’accès à la corbeille. L’interpréteur de commandes organise ces objets dans un espace de noms hiérarchique et fournit aux utilisateurs et aux applications un moyen cohérent et efficace d’accéder aux objets et de les gérer.<br/> |
| [Système de propriétés Windows](./properties/windows-properties-system.md)<br/>         | Le système de propriétés Windows est un système extensible en lecture/écriture de définitions de données qui offre un moyen uniforme d’exprimer des métadonnées sur les éléments de l’interpréteur de commandes. Le système de propriétés Windows vous permet de stocker et de récupérer des métadonnées pour les éléments de Shell. Un élément de Shell est un élément de contenu unique, tel qu’un fichier, un dossier, un message électronique ou un contact. Une propriété est un élément de métadonnées individuel associé à un élément de Shell.<br/>                                                                                                                                                                             |
| [Recherche Windows](./search/windows-search.md)<br/>                                 | Windows Search est une plateforme de recherche de bureau qui possède des fonctionnalités de recherche instantanée pour la plupart des types de données et de fichiers courants, tels que les courriers électroniques, les contacts, les rendez-vous, les documents, les photos, les éléments multimédias et d’autres formats pouvant être étendus par des développeurs tiers. Ces fonctionnalités permettent aux utilisateurs de rechercher, de gérer et d’organiser la quantité grandissante de données communes dans les environnements de bureau et d’entreprise.<br/>                                                                                                                                                                                    |
| [Stations et postes de travail Windows](./winstation/window-stations-and-desktops.md)<br/> | Windows fournit trois catégories d’objets principales : l’interface utilisateur, l’interface GDI (Graphics Device Interface) et le noyau. Les objets noyau sont sécurisables, contrairement aux objets utilisateur et aux objets GDI. Par conséquent, pour fournir une sécurité supplémentaire, les objets d’interface utilisateur sont gérés à l’aide de stations de travail et de postes de travail, qui sont eux-mêmes des objets sécurisables.<br/>                                                                                                                                                                                                                                              |
| [Aide de Windows](/windows/win32/api/winuser/nf-winuser-winhelpa)<br/>                                        | Décrit les technologies d’aide disponibles dans Windows.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [Consoles](/windows/console/character-mode-applications)<br/>                        | Les consoles gèrent les entrées et sorties (e/s) des applications en mode caractère (les applications qui ne fournissent pas leur propre interface utilisateur graphique).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement de l’interface utilisateur des applications Windows](./windows-application-ui-development.md)
</dt> </dl>

 

 
