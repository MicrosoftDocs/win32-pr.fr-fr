---
description: Vous pouvez utiliser le programme d’installation pour ajouter les informations d’une base de données dans une autre base de données en effectuant une fusion.
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: Fusion de bases de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212355f37a12aa3b92bc10e6e3e41abdcf361dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127230291"
---
# <a name="merging-databases"></a>Fusion de bases de données

Vous pouvez utiliser le programme d’installation pour ajouter les informations d’une base de données dans une autre base de données en effectuant une fusion. Les [fusions et les transformations](merges-and-transforms.md) opèrent sur une base de données entière, et une fusion combine deux bases de données en une seule. Les fusions sont utiles pour les équipes de développement, car elles permettent de diviser la base de données d’installation d’une application de grande taille en plus petites parties, puis de les recombiner ultérieurement dans la base de données d’installation complète.

**Pour fusionner plusieurs bases de données de composants dans une seule base de données complète**

1.  Développez les bases de données de composants partielles séparément.
2.  Fusionnez chaque base de données de composant dans la base de données principale du produit en appelant la fonction [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) .

 

 



