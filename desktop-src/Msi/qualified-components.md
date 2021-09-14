---
description: Un composant qualifié est une méthode d’indirection à un seul niveau, similaire à un pointeur.
ms.assetid: b483fa7d-d31d-4855-89e5-f733541cd92d
title: Composants qualifiés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2197aade7f3efd5d73e666c190c4447cac9fe1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127233927"
---
# <a name="qualified-components"></a>Composants qualifiés

Un composant qualifié est une méthode d’indirection à un seul niveau, similaire à un pointeur. Les composants qualifiés sont principalement utilisés pour regrouper des composants avec des fonctionnalités parallèles dans des catégories. par exemple, si vous avez 30 composants répertoriés dans la [table des composants](component-table.md) qui sont identiques Microsoft Word modèle de télécopie localisé dans 30 langues, vous pouvez les regrouper dans une catégorie de composants qualifiés à l’aide de la [table PublishComponent](publishcomponent-table.md).

Les composants qualifiés sont entrés dans la table des composants de la même façon que les composants ordinaires. Chaque composant doit avoir un GUID d’ID de composant unique et un identificateur de composant spécifié dans la table des composants. En outre, les composants qualifiés sont associés à un GUID de catégorie et à un qualificateur de chaîne de texte dans la table PublishComponent. Les composants qualifiés sont référencés par le GUID de catégorie et le qualificateur, qui pointe juste vers le composant ordinaire dans la table des composants.

Par exemple, un GUID d’ID de composant qualifié peut pointer vers différentes versions de langage d’une DLL de ressource. Dans ce cas, le groupe de dll de ressources localisées comprend la catégorie et les chaînes d’identificateurs de paramètres régionaux (LCID) numériques sont couramment utilisées comme qualificateurs. Un développeur peut créer un package d’installation qui utilise ces composants qualifiés pour effectuer les opérations suivantes :

-   Recherchez le chemin d’accès à une version de langue particulière de la DLL de ressource à l’aide de [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) ou [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) et installez la ressource.
-   Déterminez toutes les versions linguistiques de la DLL de ressource qui sont présentes en appelant [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).
-   Préparer l’application pour prendre en charge des langues supplémentaires. Un module linguistique ultérieur pour l’application peut utiliser le composant qualifié pour ajouter d’autres versions linguistiques de la DLL de ressource.

Pour plus d’informations, consultez [utilisation de composants qualifiés](using-qualified-components.md).

 

 



