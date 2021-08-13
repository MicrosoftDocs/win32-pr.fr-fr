---
description: Vous pouvez utiliser le programme d’installation pour ajouter les informations d’une base de données dans une autre base de données en effectuant une fusion.
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: Fusion de bases de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2931bb624037f2f909b99cfeb19a64fcb4abef689fe988a308d35766f50b1dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628705"
---
# <a name="merging-databases"></a>Fusion de bases de données

Vous pouvez utiliser le programme d’installation pour ajouter les informations d’une base de données dans une autre base de données en effectuant une fusion. Les [fusions et les transformations](merges-and-transforms.md) opèrent sur une base de données entière, et une fusion combine deux bases de données en une seule. Les fusions sont utiles pour les équipes de développement, car elles permettent de diviser la base de données d’installation d’une application de grande taille en plus petites parties, puis de les recombiner ultérieurement dans la base de données d’installation complète.

**Pour fusionner plusieurs bases de données de composants dans une seule base de données complète**

1.  Développez les bases de données de composants partielles séparément.
2.  Fusionnez chaque base de données de composant dans la base de données principale du produit en appelant la fonction [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) .

 

 



