---
description: La base de données d’un module de fusion contient toutes les propriétés d’installation et la logique de configuration pour le module.
ms.assetid: 72e42392-54e6-4be8-9a43-04158552be3d
title: Base de données de module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb75614218e7464879f62ea1527245e36d65d1dc14f19a9b82a13a893997f1c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804601"
---
# <a name="merge-module-database"></a>Base de données de module de fusion

La base de données d’un module de fusion contient toutes les propriétés d’installation et la logique de configuration pour le module. Il s’agit essentiellement d’une [base de données de programme d’installation](installer-database.md) simplifiée ou d’un fichier .msi. Les fichiers de base de données de module de fusion standard sont indiqués par une extension. msm. Pour obtenir la liste de toutes les tables de base de données qui peuvent exister dans les modules de fusion, consultez [tables de base de données de module de fusion](merge-module-database-tables.md). Les tables suivantes sont requises dans la base de données de chaque fichier. msm :

[Composant](component-table.md)

[Directory](directory-table.md)

[FeatureComponents](featurecomponents-table.md)

[File](file-table.md)

[ModuleSignature](modulesignature-table.md)

[ModuleComponents](modulecomponents-table.md)

Notez que le composant, le répertoire, FeatureComponents et les tables de fichiers sont également présents dans tous les fichiers .msi. Une base de données de module de fusion ne contient pas de [table de fonctionnalités](feature-table.md) et le fichier. msm ne peut donc pas être installé seul. Pour installer un module de fusion, il doit d’abord être fusionné à l’aide d’un outil de fusion dans un fichier de .msi.

La [table ModuleSignature](modulesignature-table.md) est uniquement présente dans .msi fichiers qui ont été fusionnés avec au moins un fichier. msm. Si cette table est présente dans un fichier .msi, elle contient un enregistrement pour chaque module de fusion précédemment fusionné dans la base de données d’installation.

Les modules de fusion peuvent contenir des tables de séquences MergeModule facultatives. Ces tables se produisent uniquement dans les fichiers. msm. Lorsque les fichiers. msm sont fusionnés dans un fichier .msi, ces tables modifient les [*tables de séquences*](s-gly.md) d’action du fichier .msi.

Les modules de fusion peuvent contenir des tables personnalisées. Ces tables sont utilisées par les [actions personnalisées](custom-actions.md) définies dans le module de fusion.

Les modules de fusion requièrent rarement des tables d’interface utilisateur. Ces tables doivent être présentes uniquement dans de rares cas où le module de fusion requiert une entrée de l’utilisateur pendant l’installation. Pour plus d’informations, consultez [création d’interfaces utilisateur dans les modules de fusion](authoring-user-interfaces-in-merge-modules.md).

 

 



