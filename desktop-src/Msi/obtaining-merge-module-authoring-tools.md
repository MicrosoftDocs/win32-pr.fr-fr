---
description: Pour générer un module de fusion, vous devez obtenir un outil logiciel permettant de modifier un fichier. msm.
ms.assetid: bc14d36a-b299-4c61-ade2-43fad142d21d
title: Obtention d’outils de création de module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a85fb75c0317a6737393e67f12a7a03cd8b76c68a8261c9d26d10d06cbe484c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327879"
---
# <a name="obtaining-merge-module-authoring-tools"></a>Obtention d’outils de création de module de fusion

Pour générer un module de fusion, vous devez obtenir un outil logiciel permettant de modifier un fichier. msm. Étant donné qu’un fichier. msm est fondamentalement un fichier .msi simplifié, vous pourrez peut-être utiliser les mêmes outils que ceux utilisés pour créer une base de données d’installation. par exemple, l’application Orca.exe fournie avec le kit de développement logiciel (SDK) Windows Installer.

Une alternative consiste à acheter l’un des outils d’empaquetage du programme d’installation à la disposition des éditeurs de logiciels indépendants. Plusieurs outils tiers en cours de développement peuvent être utilisés pour produire des modules de fusion. Si vous choisissez d’utiliser un outil tiers, vous devez vérifier qu’il génère des modules de fusion qui sont cohérents avec la norme décrite dans ce document. En particulier, vous devez déterminer que les outils d’édition n’ont pas effectué les opérations suivantes dans le module de fusion.

-   Ajout de tables superflues au module de fusion qui ne sont pas référencées dans la [table ModuleIgnoreTable](moduleignoretable-table.md).

    Supprimez ces tables ou ajoutez-les à la table ModuleIgnoreTable.

-   Ajout d’une [table](textstyle-table.md) de style TextStyle inutile au module de fusion.

    Si votre module de fusion n’a pas d’interface utilisateur (et cela ne doit généralement pas), vous pouvez supprimer cette table en toute sécurité.

-   Ajout d’entrées inutiles à la [table de répertoires](directory-table.md).

    Supprimez les entrées inutiles de la table de répertoires.

-   Informations de gauche dans le tableau de validation du module de fusion \_ .

    Cela empêche la validation du module de fusion. Ajoutez une \_ table de validation complète.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’interfaces utilisateur dans les modules de fusion](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[Création de tables de répertoires de module de fusion](authoring-merge-module-directory-tables.md)
</dt> <dt>

[Validation des modules de fusion](validating-merge-modules.md)
</dt> </dl>

 

 



