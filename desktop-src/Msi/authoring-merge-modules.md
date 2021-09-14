---
description: La procédure suivante décrit les étapes générales pour créer des modules de fusion.
ms.assetid: 4b3871c0-f452-4935-9ee3-78b0ac847e67
title: Création de modules de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ece67151872a8d065d321c6adaae660be643ad8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092482"
---
# <a name="authoring-merge-modules"></a>Création de modules de fusion

La procédure suivante décrit les étapes générales pour créer des modules de fusion.

**Pour créer un module de fusion**

1.  Procurez-vous un outil logiciel que vous pouvez utiliser pour modifier la base de données des modules de fusion.
2.  Obtenez une base de données de module de fusion vide.
3.  Générez un [GUID](guid.md) pour le module de fusion. Vous devez utiliser ce GUID lors de la création des clés primaires des tables de base de données dans le module de fusion.
4.  Ajoutez un enregistrement à la [table des composants](component-table.md) pour chaque composant remis par la fusion. Une table de composants est requise dans chaque module de fusion. Notez que les modules de fusion fonctionnent avec les composants et non avec les fonctionnalités. Dans certains cas, toutefois, une entrée de table de base de données peut être amenée à référencer une fonctionnalité. Pour plus d’informations, consultez [référencement des fonctionnalités dans les modules de fusion](referencing-features-in-merge-modules.md).
5.  Ajoutez une [table de répertoires](directory-table.md) au module de fusion qui spécifie la disposition des répertoires que le module de fusion ajoute à la base de données cible. Une table de répertoire est requise dans chaque module de fusion.
6.  Importez une [table FeatureComponents](featurecomponents-table.md) vide dans la base de données des modules de fusion. Cette table vide fournit une indication pour l’outil de fusion dans les cas où le fichier .msi ne contient pas sa propre table FeatureComponents.
7.  Collectez tous les fichiers remis par ce module de fusion et créez le fichier CAB [MergeModule. cab](mergemodule-cabinet.md) . Ajoutez le fichier CAB au module de fusion sous la forme d’un flux à l’intérieur du fichier. msm.
8.  Ajoutez un enregistrement à la table de fichiers pour chaque fichier stocké dans MergeModule. cab.
9.  Ajoutez les informations nécessaires pour identifier le module de fusion dans la [table ModuleSignature](modulesignature-table.md). Chaque module de fusion requiert une table ModuleSignature.
10. Répertoriez les composants du module de fusion dans la [table ModuleComponents](modulecomponents-table.md). Chaque module de fusion requiert une table ModuleComponents.
11. Ajoutez des tables de séquence de module de fusion au fichier. msm uniquement si le module de fusion doit modifier les [*tables de séquence*](s-gly.md) de la base de données d’installation cible.
12. Ajoutez une \_ table de validation au module de fusion. Un module de fusion requiert une \_ table de validation pour réussir la validation.
13. Les modules de fusion ne requièrent qu’une interface utilisateur dans de rares cas. L’inclusion d’une interface utilisateur avec un module de fusion n’est pas recommandée. Dans les cas où une interface utilisateur est requise, les tables de l’interface utilisateur peuvent être fusionnées dans le fichier .msi de la même façon que les autres tables.
14. Ajoutez des informations de Registre aux tables de Registre appropriées dans la base de données des modules de fusion. Ajoutez des informations de Registre pour les bibliothèques de types, les classes, les extensions et les verbes dans les tables [TypeLib](typelib-table.md), [Class](class-table.md), [AppID](appid-table.md), [ProgID](progid-table.md), [extension](extension-table.md), [verb](verb-table.md)ou [MIME](mime-table.md) . Toutes les autres informations de Registre peuvent être placées dans la [table du Registre](registry-table.md). L’utilisation de la table SelfReg n’est pas recommandée.
15. Ajoutez les informations de résumé au [flux de données Résumé du module de fusion](merge-module-summary-information-stream-reference.md).
16. Exécutez la validation sur tous les modules de fusion avant d’effectuer l’installation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Obtention de bases de données de module de fusion vides](obtaining-blank-merge-module-databases.md)
</dt> <dt>

[Obtention d’outils de création de module de fusion](obtaining-merge-module-authoring-tools.md)
</dt> <dt>

[Attribution d’un nom aux clés primaires dans les bases de données de module de fusion](naming-primary-keys-in-merge-module-databases.md)
</dt> <dt>

[Création de tables de composants de module de fusion](authoring-merge-module-component-tables.md)
</dt> <dt>

[Création de tables de répertoires de module de fusion](authoring-merge-module-directory-tables.md)
</dt> <dt>

[Création de tables FeatureComponents du module de fusion](authoring-merge-module-featurecomponents-tables.md)
</dt> <dt>

[Génération de fichiers CAB MergeModule. cab](generating-mergemodule-cabinet-cabinet-files.md)
</dt> <dt>

[Création de tables de fichier de module de fusion](authoring-merge-module-file-tables.md)
</dt> <dt>

[Création de tables ModuleSignature](authoring-modulesignature-tables.md)
</dt> <dt>

[Création de tables ModuleComponents](authoring-modulecomponents-tables.md)
</dt> <dt>

[Création de tables de séquence de module de fusion](authoring-merge-module-sequence-tables.md)
</dt> <dt>

[Validation des modules de fusion](validating-merge-modules.md)
</dt> <dt>

[Création d’interfaces utilisateur dans les modules de fusion](authoring-user-interfaces-in-merge-modules.md)
</dt> <dt>

[Création de tables de registre de module de fusion](authoring-merge-module-registry-tables.md)
</dt> <dt>

[Création des informations de synthèse du module de fusion Flux](authoring-merge-module-summary-information-streams.md)
</dt> <dt>

[Référence du flux de données de résumé du module de fusion](merge-module-summary-information-stream-reference.md)
</dt> <dt>

Validation des modules de fusion
</dt> <dt>

[Utilisation des modules de fusion 64 bits](using-64-bit-merge-modules.md)
</dt> </dl>

 

 



