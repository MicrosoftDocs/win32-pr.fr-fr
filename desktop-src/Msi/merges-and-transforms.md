---
description: le Windows Installer conserve toutes les informations relatives à l’installation dans une base de données relationnelle. Vous pouvez modifier cette base de données et, par conséquent, l’installation, à l’aide de transformations et de fusions.
ms.assetid: 32163e06-d03d-4b65-b744-62f306f2100d
title: Fusions et transformations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec6314e81afb5afa9d74346b64fe3129ba5ed30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230297"
---
# <a name="merges-and-transforms"></a>Fusions et transformations

le Windows Installer conserve toutes les informations relatives à l’installation dans une base de données relationnelle. Vous pouvez modifier cette base de données et, par conséquent, l’installation, à l’aide de transformations et de fusions.

## <a name="transforms"></a>Transformations

Une [transformation de base de données](database-transforms.md) ajoute ou remplace des éléments dans la base de données d’origine. Par exemple, une transformation peut modifier l’ensemble du texte de l’interface utilisateur de l’application, du français au français.

Les utilisations principales des transformations sont les suivantes :

-   Personnalisation des packages d’installation de base pour des groupes d’utilisateurs particuliers.

    Les transformations peuvent être utilisées pour encapsuler les différentes personnalisations d’un package de base qui sont requises par différents groupes d’utilisateurs. Par exemple, cela s’avère utile dans les organisations où les services de support technique et de personnel ont besoin de différentes installations d’un produit particulier. Le package de base d’un produit peut être mis à la disposition de tous les utilisateurs d’un point d’installation administratif avec des personnalisations appropriées distribuées à chaque groupe d’utilisateurs séparément.

-   Synchronisation des applications dans plusieurs langues.

    Les transformations sont utiles pour la conservation des packages créés à des emplacements largement séparés synchronisés au cours de la création. Par exemple, si une mise à niveau est d’abord développée pour une version anglaise d’une application qui existe en anglais et en français, une transformation peut être appliquée à la version anglaise mise à niveau qui la convertit en version française mise à niveau.

    Plusieurs transformations peuvent être appliquées à un package de base, puis appliquées à la volée pendant l’installation. Cela étend les fonctionnalités du programme d’installation pour créer des packages personnalisés et fournit un mécanisme permettant d’attribuer efficacement les installations les plus appropriées à différents groupes d’utilisateurs.

-   Application de correctifs aux applications.

    Les transformations peuvent être utilisées pour appliquer un correctif mineur à une application qui ne garantit pas une mise à niveau majeure. Pour plus d’informations sur les correctifs, consultez [packages de correctifs](patch-packages.md).

## <a name="merges"></a>Fusions

Une fusion combine deux bases de données dans une base de données et ajoute des informations au lieu de les remplacer. Si les deux bases de données comportent des informations identiques, un conflit de fusion se produit. Les fusions sont utiles pour les équipes de développement, car elles permettent de diviser une application volumineuse en parties pouvant être recombinées ultérieurement. Par exemple, les éléments de base de données pour l’installation d’un nouveau composant peuvent être développés séparément et par la suite fusionnés dans la base de données d’installation principale. Pour plus d’informations, consultez [fusionner des modules](merge-modules.md).

Une équipe de développement peut appliquer une opération de fusion de la façon suivante :

1.  Séparer en groupes et travailler simultanément sur différents composants d’une grande application.
2.  Chaque groupe de développement remplit ensuite une base de données avec les informations d’installation de son propre composant, sans se préoccuper des autres composants de l’application.
3.  Une fois le développement d’un composant terminé, la base de données de ce composant peut être fusionnée dans la base de données d’installation principale pour l’application entière.

 

 



