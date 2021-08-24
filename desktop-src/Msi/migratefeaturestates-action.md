---
description: L’action MigrateFeatureStates est utilisée lors de la mise à niveau et lors de l’installation d’une nouvelle application sur une application associée.
ms.assetid: 3f53c555-02a9-4249-9f1a-98cd655fc79f
title: Action MigrateFeatureStates
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbac96a3b2babf5f92ae8078ecc703875c09a0e2f61155fd565985919b5a6393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745169"
---
# <a name="migratefeaturestates-action"></a>Action MigrateFeatureStates

L’action MigrateFeatureStates est utilisée lors de la mise à niveau et lors de l’installation d’une nouvelle application sur une application associée. MigrateFeatureStates lit les États des fonctionnalités dans l’application existante, puis définit ces États de fonctionnalités dans l’installation en attente. La méthode est utile uniquement lorsque la nouvelle arborescence de fonctionnalités n’a pas beaucoup changé par rapport à l’original.

L’action MigrateFeatureStates s’exécute uniquement lors de la première installation du produit. L’action MigrateFeatureStates ne s’exécute pas en mode maintenance ni en cours de désinstallation.

L’action MigrateFeatureStates s’exécute dans l’ordre de chaque enregistrement de la [table de mise à niveau](upgrade-table.md) et compare le code de mise à niveau, la version du produit et la langue de chaque ligne à tous les produits installés sur le système. Si l’action MigrateFeatureStates détecte une correspondance, et si l’indicateur de bits msidbUpgradeAttributesMigrateFeatures est défini dans la colonne attributs de la table de mise à niveau, le programme d’installation interroge les États de fonctionnalités existants pour le produit et définit ces États pour les mêmes fonctionnalités dans la nouvelle application. L’action migre uniquement les États de fonctionnalité si la propriété [**présélectionnée**](preselected.md) n’est pas définie.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action MigrateFeatureStates doit se trouver immédiatement après l' [action CostFinalize](costfinalize-action.md). MigrateFeatureStates doit être séquencé à la fois dans la [table InstallUISequence](installuisequence-table.md) et dans la [table InstallExecuteSequence](installexecutesequence-table.md). Le programme d’installation empêche MigrateFeatureStates de s’exécuter dans InstallExecuteSequence si l’action a déjà été exécutée dans InstallUISequence.

## <a name="actiondata-messages"></a>Messages ActionData

MigrateFeatureSettings envoie un message de données d’action pour chaque produit.

## <a name="remarks"></a>Remarques

Si plusieurs produits installés partagent une fonctionnalité, l’état d’installation de cette fonctionnalité peut varier d’un produit à l’autre. L’action MigrateFeatureState utilise l’ordre de priorité suivant lors de la migration des États d’installation des fonctionnalités : exécution locale, exécution à partir de la source, publiée et désinstallée. Par exemple, le produit installé A peut avoir la fonctionnalité Y en tant que INSTALLSTATE \_ local et le produit B installé peut avoir la fonctionnalité y en tant que InstallState \_ absente. Si une mise à niveau installe le produit C et migre l’état d’installation de la fonctionnalité Y, MigrateFeatureState définit l’état d’installation de la fonctionnalité Y du produit C sur INSTALLSTATE \_ local.

Pour plus d’informations sur l’utilisation de l’action MigrateFeatureStates pour les mises à niveau de produit, consultez [préparation d’une application pour les futures mises à niveau majeures](preparing-an-application-for-future-major-upgrades.md).

 

 



