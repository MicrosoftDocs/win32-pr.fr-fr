---
description: Les actions personnalisées ProcessAccounts et UninstallAccounts génèrent les actions personnalisées différées qui créent, suppriment ou restaurent des comptes d’utilisateur.
ms.assetid: 245b576b-96cc-4eab-8848-5ff78ba32873
title: Création de la table InstallExecuteSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aa09895d5e5d2543b5594f4795734d26163a4f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092446"
---
# <a name="authoring-the-installexecutesequence-table"></a>Création de la table InstallExecuteSequence

Les actions personnalisées ProcessAccounts et UninstallAccounts génèrent les actions personnalisées différées qui créent, suppriment ou restaurent des comptes d’utilisateur. Les actions personnalisées ProcessAccounts et UninstallAccounts doivent être entrées dans la [table InstallExecuteSequence](installexecutesequence-table.md) à exécuter. Ajoutez les entrées suivantes à la [table InstallExecuteSequence](installexecutesequence-table.md). Étant donné que ces actions personnalisées doivent faire partie de la génération de script, les deux actions personnalisées doivent être séquencées après l' [action InstallInitialize](installinitialize-action.md).

La condition sur ProcessAccounts garantit ce qui suit. Consultez [syntaxe d’instruction conditionnelle](conditional-statement-syntax.md).

-   ProcessAccounts s’exécute uniquement si le composant TestAccount est installé localement sur l’ordinateur.
-   Le compte de test de composant n’est actuellement pas installé ou est installé pour s’exécuter à partir de la source.

La condition sur UninstallAccount garantit les éléments suivants :

-   UninstallAccounts s’exécute uniquement si le composant TestAccount est installé localement sur l’ordinateur.
-   Le compte de test de composant est en cours de suppression ou d’installation pour être exécuté à partir de la source.

[Table InstallExecuteSequence](installexecutesequence-table.md)



| Action            | Condition                                                           | Séquence |
|-------------------|---------------------------------------------------------------------|----------|
| ProcessAccounts   | VersionNT et ( ? TestAccount = 2 ou ? TestAccount = 4) et $TestAccount = 3 | 1550     |
| UninstallAccounts | VersionNT et ? TestAccount = 3 et ($TestAccount = 4 ou $TestAccount = 2) | 1560     |



 

Continuez à [créer l’interface utilisateur pour l’entrée de mot de passe](authoring-the-user-interface-for-password-input.md).

 

 



