---
description: Les noms des clés primaires une base de données de module de fusion doivent adhérer à une convention d’affectation de noms standard.
ms.assetid: 72822c25-cd21-454b-ab49-846474b55ef1
title: Attribution d’un nom aux clés primaires dans les bases de données de module de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e5481e7fd29c4d3750e8fac01b6ca4bd6593af3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230123"
---
# <a name="naming-primary-keys-in-merge-module-databases"></a>Attribution d’un nom aux clés primaires dans les bases de données de module de fusion

Les noms des clés primaires une base de données de module de fusion doivent adhérer à une convention d’affectation de noms standard. L’objectif de cette Convention d’affectation de noms est de réduire la possibilité de créer un conflit de noms entre les colonnes de table dans le module de fusion et le package d’installation cible. La Convention d’affectation de noms ne peut pas être appliquée à des tables dans lesquelles la clé primaire est des données installables. N’appliquez pas la Convention d’affectation de noms aux tables suivantes :

-   [Table MIME](mime-table.md)
-   [Table d’extension](extension-table.md)
-   [Table d’icônes](icon-table.md)
-   [Table de verbes](verb-table.md)
-   [Table ProgId](progid-table.md)

Par exemple, n’utilisez pas pour la clé primaire de la table MIME, car il s’agit du type MIME et l’application de la procédure d’affectation de noms modifierait sa signification. Dans ces cas, les conflits de noms dépendent de la signification des données qui sont uniques dans les modules.

Le nom d’une clé primaire dans un module de fusion doit être un nom lisible ajouté à une chaîne créée à partir du GUID du module de fusion. Chaque module de fusion doit avoir son propre [*GUID*](g-gly.md). Le GUID du module de fusion doit également être créé dans la propriété [**Résumé du numéro de révision**](revision-number-summary.md) du module de fusion. Les développeurs peuvent créer des GUID à l’aide d’un utilitaire tel que GUIDGEN.

La procédure suivante décrit comment générer une clé de base de données primaire conforme à la Convention d’affectation de noms standard. Appliquez la procédure suivante uniquement aux tables où la clé primaire n’est pas une donnée en cours d’installation.

**Pour nommer une clé primaire d’un enregistrement de table dans un module de fusion**

1.  Créez la partie lisible du nom pour la clé primaire. Choisissez un nom lisible qui identifie cet enregistrement, par exemple MyRowEntry.
2.  Générez ou obtenez le GUID du module de fusion. Notez que tous les GUID doivent être créés en majuscules. Pour plus d’informations sur les GUID, consultez [GUID](guid.md). Voici un exemple de GUID : {880DE2F0-CDD8-11D1-A849-006097ABDE17}. Dans les étapes suivantes, vous allez modifier cela en une chaîne de caractères qui doit être ajoutée à chaque nom de clé primaire dans le module de fusion.
3.  Supprimez les accolades à partir du début et de la fin du GUID.
4.  Remplacez tous les tirets par des traits de soulignement.
5.  Ajoutez le résultat à la fin de la partie lisible du nom de la clé primaire. Séparez le nom lisible du GUID modifié par un point. Le nom de la clé primaire de l’exemple de GUID indiqué ci-dessus devient MyRowEntry. 880DE2F0 \_ CDD8 \_ 11D1 \_ A849 \_ 006097ABDE17.
6.  Répétez cette opération pour nommer toutes les clés primaires de toutes les tables dans le module de fusion.

 

 



