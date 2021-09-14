---
description: Pour valider une base de données, utilisez un outil de validation spécial pour fusionner un fichier. CUB contenant les évaluateurs de cohérence internes (ICEs) dans votre base de données, exécutez le CIEM et signalez les résultats.
ms.assetid: bdf38673-ee3d-47d8-ad6e-562cd5626918
title: Utilisation des évaluateurs de cohérence internes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423e6dab453ae495dc6029b54eb039c8acc60f33
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222940"
---
# <a name="using-internal-consistency-evaluators"></a>Utilisation des évaluateurs de cohérence internes

Pour valider une base de données, utilisez un outil de validation spécial pour fusionner un fichier. CUB contenant les [évaluateurs de cohérence internes](internal-consistency-evaluators-ices.md) (ICES) dans votre base de données, exécutez le CIEM et signalez les résultats. plusieurs de ces outils sont fournis dans le kit de développement logiciel (SDK) de Microsoft Windows. Les environnements de création de fournisseurs tiers peuvent également intégrer le système de validation de glace dans leur environnement de création. Il est également possible d’écrire votre propre outil pour effectuer la validation de la glace. La plupart des outils de validation ICE fusionnent le fichier. CUB et votre base de données dans une troisième base de données temporaire. Windows Le programme d’installation affiche les avertissements, les erreurs, les informations de débogage et les erreurs d’API au fur et à mesure qu’il exécute chaque ICE dans le fichier. CUB. Quand le programme d’installation a terminé l’exécution du fichier ICEs, il ferme le fichier .msi, le fichier. CUB et la base de données temporaire sans enregistrer les modifications. Le fichier .msi et le fichier. CUB restent inchangés par le test de validation.

Les actions personnalisées ICE communiquent à l’utilisateur en appelant [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) et en publiant un \_ message utilisateur INSTALLMESSAGE. Un message ICE retourne généralement des informations telles que les suivantes :

-   Nom de la glace ayant détecté une erreur
-   Date de création de la glace
-   Auteur de la glace
-   Date de la dernière modification de la glace.
-   Description de l’erreur d’API provoquant l’échec de la glace
-   Description de l’erreur
-   Un avertissement à l’utilisateur
-   Nom de la table de base de données contenant l’erreur ou l’avertissement
-   Nom de la colonne de table contenant l’erreur ou l’avertissement
-   Clés primaires de la table contenant l’erreur ou l’avertissement
-   URL vers un fichier HTML donnant des suggestions de débogage
-   Chaîne qui peut contenir d’autres informations

Les auteurs des packages d’installation peuvent écrire des actions personnalisées ICE ou utiliser l’ensemble standard de ICEs inclus dans les fichiers. CUB fournis avec le kit de développement logiciel (SDK). Pour plus d’informations sur la façon d’écrire une glace, consultez [génération d’une glace](building-an-ice.md).

Après avoir écrit le CIEM approprié pour la validation, un développeur doit rassembler les actions personnalisées dans une base de données .msi, appelée fichier. CUB, qui contient uniquement le CIEM et les tables requises. Un fichier. CUB ne peut pas être installé et est utilisé uniquement pour stocker et fournir l’accès aux actions personnalisées ICE. Pour plus d’informations sur la création de fichiers. CUB, consultez [génération d’une base de données de glace](building-an-ice-database.md). Les développeurs peuvent également valider leur package d’installation à l’aide du CIEM existant décrit dans [référence Ice](ice-reference.md). Ces CIEM peuvent être obtenues à partir de fichiers. CUB standard fournis avec le kit de développement logiciel (SDK).

L’installation de l’éditeur de table de base de données Orca ou de l’outil de validation MSIVal2 fournit les fichiers logo. CUB, Darice. CUB et Mergemod. CUB. Le jeu de fichiers CIEM dans le fichier logo. CUB est un sous-ensemble de ceux du fichier Darice. CUB. Si votre package est validé à l’aide de darice. CUB, il passe avec logo. CUB. Mergemod. CUB contient un ensemble de ICEs utilisé pour valider les modules de fusion. Pour plus d’informations, consultez Référence de la [glace du module de fusion](merge-module-ice-reference.md).

**Pour valider un package d’installation**

1.  Obtenir ou créer les actions personnalisées ICE appropriées. Vous pourrez peut-être utiliser un ou plusieurs des CIEM existants décrits dans la [référence Ice](ice-reference.md). Si votre validation requiert une ICE qui ne se trouve pas encore dans cette liste, vous pouvez créer une nouvelle ICE comme décrit dans [génération d’une glace](building-an-ice.md).
2.  Préparez une base de données ICE contenant toutes les actions personnalisées ICE. Consultez la section [création d’une base de données Ice](building-an-ice-database.md) pour plus d’informations sur la préparation d’un fichier. CUB.
3.  Fournissez le fichier. CUB et le fichier .msi à un outil de validation de package comme [Orca.exe](orca-exe.md) ou [Msival2.exe](msival2-exe.md).

Notez que les modules de fusion doivent être validés comme décrit dans [validation des modules de fusion](validating-merge-modules.md).

 

 



