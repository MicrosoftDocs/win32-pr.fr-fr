---
description: Pour créer des modules de fusion, utilisez les instructions générales qui sont décrites dans la rubrique modules de fusion de création.
ms.assetid: 9d5e60dc-9133-4c6e-9a47-dd341f2757fa
title: Création d’un module de fusion qui peut être configuré par le End-User
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db6ff7bd85fb1b6704fc2452c488b8a3bbc06b3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091898"
---
# <a name="creating-a-merge-module-that-can-be-configured-by-the-end-user"></a>Création d’un module de fusion qui peut être configuré par le End-User

Pour créer des modules de fusion, utilisez les instructions générales qui sont décrites dans la rubrique [modules de fusion de création](authoring-merge-modules.md) . En outre, vous devez effectuer les opérations suivantes pour créer un module de fusion qui peut être configuré par l’utilisateur final du module :

-   Les utilisateurs finaux doivent disposer de la version 2,0 de Mergemod.dll pour configurer votre module. Les utilisateurs qui ont des versions antérieures de Mergemod.dll peuvent appliquer le module, mais ils obtiennent toujours les paramètres par défaut.
-   Ajoutez une [table ModuleConfiguration](moduleconfiguration-table.md) au module de fusion pour identifier les éléments qui peuvent être configurés par un utilisateur final. Ajoutez un enregistrement dans cette table pour chaque élément configurable. Ces éléments sont remplacés par les modèles qui sont spécifiés dans la [table ModuleSubstitution](modulesubstitution-table.md). Entrez un nom pour chaque élément configurable dans le champ nom. Entrez le format, le type et le contexte sémantique pour chaque élément dans les colonnes format, type et ContextData. Pour plus d’informations, consultez [types sémantiques](semantic-types.md). Entrez une valeur par défaut pour l’élément dans le champ DefaultValue en utilisant le [format spécial CMSM](cmsm-special-format.md).
-   Ajoutez une [table ModuleSubstitution](modulesubstitution-table.md) au module de fusion. Chaque enregistrement dans cette table correspond à une substitution d’un ou plusieurs éléments configurables dans un champ de la base de données du module de fusion. Entrez la table, la ligne et la colonne du champ qui reçoit la substitution. Entrez un modèle de mise en forme pour la substitution dans la colonne valeur à l’aide du [format spécial CMSM](cmsm-special-format.md).
-   Ajoutez des enregistrements à la [table de validation](-validation-table.md) pour les tables ModuleSubstitution et ModuleConfiguration.
-   Ajoutez des enregistrements à la [table ModuleIgnoreTable](moduleignoretable-table.md) pour la table [ModuleSubstitution](modulesubstitution-table.md) et la [table ModuleConfiguration](moduleconfiguration-table.md). Cela permet de s’assurer que le module est compatible pour les utilisateurs qui ont des versions de Mergemod.dll antérieures à la version 2,0.

 

 



