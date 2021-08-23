---
description: Si vous ne parvenez pas à trouver les évaluateurs de cohérence internes dont vous avez besoin parmi les actions personnalisées ICE existantes répertoriées dans la référence ICE, vous devrez préparer votre propre glace pour valider votre package.
ms.assetid: d9ff43ee-8e7a-4132-ac2f-232dc24606d8
title: Génération d’une glace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b4b79ab8e17d53ccfb60484c0d307f668c44a7a0e530cf776b10e73a697541c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500762"
---
# <a name="building-an-ice"></a>Génération d’une glace

Si vous ne parvenez pas à trouver les [évaluateurs de cohérence internes](internal-consistency-evaluators-ices.md) dont vous avez besoin parmi les actions personnalisées Ice existantes répertoriées dans la [référence Ice](ice-reference.md), vous devrez préparer votre propre glace pour valider votre package.

Lorsque vous créez des actions personnalisées ICE, vous devez effectuer les opérations suivantes :

-   Basez le CIEM uniquement sur les actions personnalisées des types répertoriés dans le tableau indiqué.
-   Appelez [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) et publiez un \_ message de type utilisateur INSTALLMESSAGE. Lorsque vous créez vos messages ICE, suivez le format du message dans les [instructions relatives aux messages Ice](ice-message-guidelines.md).
-   Écrivez votre glace de sorte qu’elle capture toutes les erreurs d’API et retourne toujours l’erreur de \_ réussite. Cela est nécessaire pour permettre aux actions personnalisées suivantes de s’exécuter après l’échec d’une glace.

Les actions personnalisées ICE sont limitées aux types d’actions personnalisées suivants.



| Type d’action personnalisé                                 | Description               |
|----------------------------------------------------|---------------------------|
| [Type d’action personnalisé 1](custom-action-type-1.md)   | DLL dans un flux binaire      |
| [Type d’action personnalisé 2](custom-action-type-2.md)   | EXE dans un flux binaire      |
| [Type d’action personnalisé 5](custom-action-type-5.md)   | JScript dans un flux binaire  |
| [Type d’action personnalisé 6](custom-action-type-6.md)   | VBScript dans un flux binaire |
| [Type d’action personnalisé 37](custom-action-type-37.md) | JScript le code en tant que chaîne    |
| [Type d’action personnalisé 38](custom-action-type-38.md) | Code VBScript sous forme de chaîne   |



 

Lors de la création d’une action personnalisée ICE, n’effectuez pas les opérations suivantes :

-   Ne supposez pas que le descripteur du moteur que la glace reçoit est une instance d’installation de la base de données du programme d’installation. S’il ne s’agit pas d’une instance d’installation, certaines propriétés ne sont pas définies, les répertoires source et cible ne sont pas résolus et les États des fonctionnalités actuelles ne sont pas définis.
-   Ne vous fiez pas à l’exécution antérieure, ou non, d’une action du programme d’installation, d’une action personnalisée ou d’une autre glace. Comme une ICE précédente peut avoir créé des colonnes temporaires dans une table, les auteurs doivent référencer les colonnes par nom chaque fois que cela est possible. Le CIEM doit nettoyer les tables ou colonnes temporaires avant de quitter.
-   Ne partez pas du principe que les auteurs ont accès à une image du répertoire source de la base de données.
-   Ne partez pas du principe que les modifications apportées à la base de données ne sont pas conservées.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de code ICE en C++](sample-ice-in-c-.md)
</dt> <dt>

[Exemple de code ICE dans VBScript](sample-ice-in-vbscript.md)
</dt> </dl>

 

 



