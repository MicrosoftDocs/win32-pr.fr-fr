---
description: L’action FindRelatedProducts s’exécute dans l’ordre de chaque enregistrement de la table de mise à niveau et compare le code de mise à niveau, la version du produit et la langue de chaque ligne aux produits installés sur le système.
ms.assetid: 7efcb767-9bdf-43a4-83b8-61b6fc84adf6
title: Action FindRelatedProducts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87973631e51315df17a156bc8c57aa9facd84f3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021726"
---
# <a name="findrelatedproducts-action"></a>Action FindRelatedProducts

L’action FindRelatedProducts s’exécute dans l’ordre de chaque enregistrement de la [table de mise à niveau](upgrade-table.md) et compare le code de mise à niveau, la version du produit et la langue de chaque ligne aux produits installés sur le système. Quand FindRelatedProducts détecte une correspondance entre les informations de mise à niveau et un produit installé, il ajoute le code de produit à la propriété spécifiée dans la colonne ActionProperty de UpgradeTable.

L’action FindRelatedProducts s’exécute uniquement lors de la première installation du produit. L’action FindRelatedProducts ne s’exécute pas en mode maintenance ni en cours de désinstallation.

## <a name="database-tables-queried"></a>Tables de base de données interrogées

Cette action interroge le tableau suivant :

[Mettre à niveau la table](upgrade-table.md)

## <a name="properties-used"></a>Propriétés utilisées

L’action FindRelatedProducts utilise la propriété [**UpgradeCode**](upgradecode.md) et les informations sur la version et la langue que vous avez créées dans la table de mise à niveau pour détecter les produits installés affectés par la mise à niveau en attente. Il ajoute le code de produit des produits détectés à la propriété dans la colonne ActionProperty de UpgradeTable.

FindRelatedProducts reconnaît uniquement les produits existants qui ont été installés à l’aide de l’Windows Installer avec un .msi qui définit une propriété [**UpgradeCode**](upgradecode.md) , une propriété [**ProductVersion**](productversion.md) et une valeur pour la propriété [**ProductLanguage**](productlanguage.md) qui est l’une des langues listées dans la propriété [**résumé du modèle**](template-summary.md) .

Notez que FindRelatedProducts utilise la langue retournée par [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa). Pour que FindRelatedProducts fonctionne correctement, l’auteur du package doit être certain que la propriété [**ProductLanguage**](productlanguage.md) de la [table de propriétés](property-table.md) est définie sur une langue qui est également indiquée dans la propriété Résumé du [**modèle**](template-summary.md) . Consultez [préparation d’une application pour les futures mises à niveau majeures](preparing-an-application-for-future-major-upgrades.md).

## <a name="sequence-restrictions"></a>Restrictions de séquence

FindRelatedProducts doit être créé dans la [table InstallUISequence](installuisequence-table.md) et les tables [InstallExecuteSequence](installexecutesequence-table.md) . Le programme d’installation empêche les produits FindRelated de s’exécuter dans InstallExecuteSequence si l’action a déjà été exécutée dans InstallUISequence. L’action FindRelatedProducts doit précéder l’action [MigrateFeatureStates](migratefeaturestates-action.md) et l’action [RemoveExistingProducts](removeexistingproducts-action.md).

## <a name="actiondata-messages"></a>Messages ActionData

FindRelatedProducts envoie un message de données d’action pour chaque produit associé détecté sur le système.

 

 



