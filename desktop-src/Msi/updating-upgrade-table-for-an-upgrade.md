---
description: pour appliquer une mise à niveau majeure à l’aide de Windows Installer, le package d’installation du produit d’origine doit spécifier une propriété UpgradeCode, décrite dans préparation d’une Application pour les futures mises à niveau majeures, et le package de mise à niveau doit avoir une table de mise à niveau.
ms.assetid: 041f5bab-cb13-4e17-8465-484bcd3c6957
title: Mise à jour de la table de mise à niveau pour une mise à niveau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba65db43019c09e27824c54265244c65b900e4f3c94dacd24405e7fac2e0272a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809749"
---
# <a name="updating-upgrade-table-for-an-upgrade"></a>Mise à jour de la table de mise à niveau pour une mise à niveau

pour appliquer une mise à niveau majeure à l’aide de Windows Installer, le package d’installation du produit d’origine doit spécifier une propriété [**UpgradeCode**](upgradecode.md) , décrite dans [préparation d’une Application pour les futures mises à niveau majeures](preparing-an-application-for-future-major-upgrades.md), et le package de mise à niveau doit avoir une [table de mise](upgrade-table.md)à niveau.

Pour plus d’informations sur les mises à niveau majeures, consultez [mises à niveau majeures](major-upgrades.md) dans [correctifs et mises à niveau](patching-and-upgrades.md).

La propriété [**UpgradeCode**](upgradecode.md) du package d’installation de MNP2000.msi a été affectée, comme décrit dans la section [spécification des propriétés](specifying-properties.md).

Windows Le programme d’installation applique la mise à niveau si l’utilisateur a déjà installé les versions 1,0 à 1,4 (inclusives) de la langue anglaise MNP2000. Windows Le programme d’installation migre tous les paramètres des fonctionnalités du produit d’origine vers le produit mis à niveau. Le programme d’installation supprime les fichiers appartenant aux produits originaux qui ne sont pas utilisés par la mise à niveau du produit.

Si votre copie de MNP2001.msi n’inclut pas de [table de mise à niveau](upgrade-table.md), utilisez Orca ou un autre éditeur de table pour importer une table de mise à niveau vide dans la base de données à partir de Schema.msi. Le kit de développement logiciel (SDK) fournit une copie de Schema.msi. Utilisez votre éditeur de base de données pour ouvrir MNP2001.msi et entrez les données suivantes dans la table de mise à niveau vide.



| UpgradeCode                            | VersionMin | VersionMax | Langage | Attributs | Supprimer | ActionProperty |
|----------------------------------------|------------|------------|----------|------------|--------|----------------|
| {908E378A-9551-4772-BF1D-5CFAF6FD9CB4} | 01.00.0000 | 01.40.0000 | 1033     | 769        |        | OLDAPPFOUND    |



 

[Continuer](updating-properties-for-an-upgrade.md)

 

 



