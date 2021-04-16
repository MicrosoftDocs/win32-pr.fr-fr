---
description: Il existe deux façons de créer la base de données d’installation Windows Installer afin qu’une action soit appelée uniquement lorsque le package est désinstallé.
ms.assetid: 67b205bb-11d8-454f-b5d5-93330219f6cc
title: Mesures de conditionnement à exécuter pendant la suppression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0e84f21b42f569744af9b8a7a46bb1e3df7a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528647"
---
# <a name="conditioning-actions-to-run-during-removal"></a>Mesures de conditionnement à exécuter pendant la suppression

Il existe deux façons de créer la base de données d’installation afin qu’une action soit appelée uniquement lors de la désinstallation du package :

-   Si l’action est séquencée après l' [action InstallValidate](installvalidate-action.md) dans la [table InstallExecuteSequence](installexecutesequence-table.md), l’auteur du package peut spécifier une condition Remove = "All" pour l’action dans la colonne condition. Notez qu’il n’est pas garanti que la propriété [**Remove**](remove.md) soit définie sur All pendant une désinstallation avant que le programme d’installation exécute l’action InstallValidate. Notez que les guillemets entourant la valeur sont tous obligatoires dans ce cas.
-   Si l’action est séquencée après l' [action CostFinalize](costfinalize-action.md) et toutes les actions susceptibles de changer l’état de la fonctionnalité, par exemple l' [action MigrateFeatureStates](migratefeaturestates-action.md), l’action peut être conditionnée sur l’état d’une fonctionnalité ou d’un composant particulier. Consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md). Utilisez cette option pour appeler une action pendant la suppression d’une fonctionnalité ou d’un composant particulier, ce qui peut se produire en dehors de la suppression complète de l’application.

Notez que la propriété [**installed**](installed.md) peut être utilisée dans les expressions conditionnelles pour déterminer si un produit est installé par ordinateur ou pour l’utilisateur actuel. Pour déterminer si le produit est installé pour un autre utilisateur, vérifiez la propriété [**ProductState**](productstate.md) .

Notez que les versions antérieures d’un produit peuvent être supprimées pendant une mise à niveau par l' [action RemoveExistingProducts](removeexistingproducts-action.md). La [table de mise à niveau](upgrade-table.md) peut également définir la propriété [**Remove**](remove.md) sur All dans ce cas. Pour déterminer si un produit est supprimé par une mise à niveau, vérifiez la propriété [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) . Le programme d’installation ne définit cette propriété que lorsque RemoveExistingProducts supprime le produit. Le programme d’installation ne définit pas la propriété pendant une désinstallation normale, telle que la suppression avec ajout/suppression de programmes.

 

 



