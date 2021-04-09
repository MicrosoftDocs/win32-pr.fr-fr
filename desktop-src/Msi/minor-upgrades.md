---
description: Une mise à niveau mineure est une mise à jour qui apporte des modifications à de nombreuses ressources.
ms.assetid: 74c962f9-93cd-40ed-a8fe-141ccac79d79
title: Mises à niveau mineures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833bb46e2cafe0545f83c0ed0f8ff8aba00f0695
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867286"
---
# <a name="minor-upgrades"></a>Mises à niveau mineures

Une mise à niveau mineure est une mise à jour qui apporte des modifications à de nombreuses ressources. Aucune des modifications ne peut nécessiter de modifier la valeur [**ProductCode**](productcode.md). Une mise à jour requiert une [mise à niveau majeure](major-upgrades.md) pour modifier la valeur **ProductCode**. Une mise à niveau mineure peut être utilisée pour ajouter de nouveaux composants et fonctionnalités, mais ne peut pas réorganiser l’arborescence des composants de fonctionnalité. Les mises à niveau mineures fournissent une différenciation des produits sans définir réellement un produit différent. Une mise à niveau mineure classique comprend tous les correctifs des petites mises à jour précédentes, combinés dans un correctif. Une mise à niveau mineure est également communément appelée mise à jour de Service Pack (SP). Pour plus d’informations sur les mises à jour qui ne nécessitent pas de modification de la **ProductCode** , consultez [modification du code du produit](changing-the-product-code.md).

Une mise à niveau mineure modifie la propriété [**ProductVersion**](productversion.md) . La modification de la version du produit de l’application signifie que les différentes mises à jour ont une commande. Par exemple, si un correctif a existé pour mettre à jour la version v 9,0 à la version 9,1, et qu’un autre correctif existait pour le correctif v 9,1 à v 9,2, le programme d’installation peut appliquer l’ordre correct en vérifiant la version du produit avant d’appliquer le correctif. Cela empêche également l’application du correctif v 9,1 à v 9,2 à v 9,0. Pour les correctifs, ce classement est appliqué par le biais des bits de validation de version de produit définis dans les transformations incluses dans le [package de correctifs](patch-packages.md).

Une mise à niveau mineure et une petite mise à jour diffèrent dans le fait qu’une mise à niveau mineure modifie le code du package et la version du produit. Pour obtenir des instructions sur les types de mises à jour pouvant être gérées par une petite mise à jour ou une mise à niveau mineure, consultez [petites mises](small-updates.md) à jour. Les mises à niveau mineures sont fournies en tant que package d’installation complète du produit ou en tant que [package correctif](patch-packages.md). Toutefois, une mise à niveau mineure ne peut pas utiliser un autre nom de volume pour la nouvelle version.

Pour plus d’informations sur l’application d’une mise à niveau mineure, consultez les rubriques suivantes :

-   [Application de petites mises à jour en appliquant des correctifs à l’installation locale du produit](applying-small-updates-by-patching-the-local-installation-of-the-product.md)
-   [Application de petites mises à jour en réinstallant le produit](applying-small-updates-by-reinstalling-the-product.md)
-   [Application de petites mises à jour en corrigeant une image administrative](applying-small-updates-by-patching-an-administrative-image.md)

 

 



