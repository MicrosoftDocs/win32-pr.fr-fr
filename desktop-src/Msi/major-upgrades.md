---
description: Une mise à niveau majeure est une mise à jour complète d’un produit qui nécessite une modification de la propriété ProductCode.
ms.assetid: 0c8f2aad-b301-4404-9051-694d97db1a8d
title: Mises à niveau majeures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7795695072f6c153373db914781ac4b919cd2572
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021363"
---
# <a name="major-upgrades"></a>Mises à niveau majeures

Une mise à niveau majeure est une mise à jour complète d’un produit qui nécessite une modification de la propriété [**ProductCode**](productcode.md) .

Une mise à niveau majeure classique supprime une version précédente d’une application et installe une nouvelle version. Une mise à niveau majeure peut réorganiser l’arborescence des composants de la fonctionnalité. Pour plus d’informations, consultez [**ProductCode**](productcode.md) et [modification du code du produit](changing-the-product-code.md).

au cours d’une mise à niveau majeure à l’aide de Windows Installer, le programme d’installation recherche les applications associées à la mise à niveau en attente sur l’ordinateur de l’utilisateur et, lorsqu’il en détecte un, il récupère la version de l’application installée à partir du registre système. Le programme d’installation utilise ensuite les informations de la base de données de mise à niveau pour déterminer s’il faut mettre à niveau l’application installée.

Pour activer les fonctionnalités de mise à niveau du programme d’installation, chaque package doit avoir une propriété [**UpgradeCode**](upgradecode.md) et une [table de mise à niveau](upgrade-table.md). Chaque produit autonome ou suite de produits doit avoir sa propre **UpgradeCode**. Pour plus d’informations sur l’utilisation de **UpgradeCode** , consultez la section [utilisation de UpgradeCode](using-an-upgradecode.md). Chaque enregistrement de la table de mise à niveau fournit une combinaison du code de mise à niveau, de la version du produit et des informations de langue utilisées pour identifier un ensemble de produits affectés par la mise à niveau. Lorsque l' [action FindRelatedProducts](findrelatedproducts-action.md) détecte qu’un produit affecté est installé sur le système, il ajoute le code de produit à une propriété de la colonne ActionProperty de la table de mise à niveau. L' [action RemoveExistingProducts](removeexistingproducts-action.md) et l' [action MigrateFeatureStates](migratefeaturestates-action.md) suppriment ou migrent les produits répertoriés dans la liste ActionProperty. Les auteurs de package peuvent également suivre la procédure décrite dans la rubrique : [préparation d’une application pour les futures mises à niveau majeures](preparing-an-application-for-future-major-upgrades.md).

Windows Les packages de mise à niveau du programme d’installation peuvent être créés de telle sorte que les mises à niveau majeures ne s’installeront pas si l’utilisateur a déjà une version plus récente de l’application installée. Pour plus d’informations sur la création d’un package qui n’est pas installé sur une version plus récente, consultez la page [empêcher l’installation d’un ancien package sur une version plus récente](preventing-an-old-package-from-installing-over-a-newer-version.md)

> [!Note]  
> Windows Le programme d’installation utilise uniquement les trois premiers champs de la version du produit. Consultez propriété [**ProductVersion**](productversion.md) pour obtenir une description de ces champs. Si vous incluez un quatrième champ dans la version de votre produit, le programme d’installation ignore le quatrième champ.

 

La méthode recommandée pour appliquer une mise à niveau majeure consiste à installer le package complet pour le produit mis à jour. Pour plus d’informations sur l’application d’une mise à niveau majeure en installant le produit, consultez [application des mises à niveau majeures en installant le produit](applying-major-upgrades-by-installing-the-product.md).

Une mise à niveau majeure appliquée en tant que [package de correctif](patch-packages.md) pour le produit ne peut pas être séquencée avec d’autres mises à jour et n’est pas un correctif impossible à [installer](uninstallable-patches.md). pour plus d’informations sur la façon d’appliquer un package correctif de mise à niveau majeur à un package Windows Installer consultez [application de mises à niveau majeures en appliquant des correctifs à l’Installation locale du produit](applying-major-upgrades-by-patching-the-local-installation-of-the-product.md). L’application d’une mise à niveau majeure à l’aide d’un package de correctifs n’est pas recommandée. Appliquez plutôt des mises à niveau majeures en installant le produit complet.

> [!Note]  
> Si une application est installée dans le [contexte d’installation](installation-context.md)par utilisateur, toute mise à niveau majeure de l’application doit également être effectuée à l’aide du contexte par utilisateur. Si une application est installée dans le contexte d’installation par ordinateur, toute mise à niveau majeure de l’application doit également être effectuée à l’aide du contexte par ordinateur. le Windows Installer n’installe pas les mises à niveau majeures dans le contexte d’installation.

 

Vous pouvez conditionner des actions personnalisées qui sont séquencées après [InstallValidate](installvalidate-action.md) pour gérer les principales mises à niveau à l’aide de la propriété [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) :

-   Si vous souhaitez qu’une action personnalisée s’exécute pendant la désinstallation du produit, mais pas pendant la suppression du produit par une mise à niveau majeure, utilisez cette condition.

    REMOVE = "ALL" et non pas [ **UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

-   Si vous souhaitez qu’une action personnalisée s’exécute uniquement pendant une mise à niveau majeure, utilisez cette condition.

    [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md)

 

 



