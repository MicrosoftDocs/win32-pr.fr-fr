---
description: 'Le tableau ci-dessous répertorie les cinq actions personnalisées utilisées pour satisfaire les exemples de spécifications : ProcessAccounts, UninstallAccounts, CreateAccounts, RemoveAccounts et RollbackAccounts.'
ms.assetid: 389ec652-243e-4392-aec9-3a7eb90e6c68
title: Création des actions personnalisées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e09525490304762b98635bcbbe6c238ce3fe413f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127092450"
---
# <a name="authoring-the-custom-actions"></a>Création des actions personnalisées

Le tableau ci-dessous répertorie les cinq actions personnalisées utilisées pour satisfaire les exemples de spécifications : ProcessAccounts, UninstallAccounts, CreateAccounts, RemoveAccounts et RollbackAccounts. Toutes ces actions personnalisées se trouvent dans les [bibliothèques de liens dynamiques](dynamic-link-libraries.md) stockées dans la [table binaire](binary-table.md). le code source C++ pour les bibliothèques de liens dynamiques contenant les exemples d’actions personnalisées est fourni dans le kit de développement logiciel (SDK) Windows Installer. ProcessAccounts et UninstallAccounts se trouvent dans le fichier process. cpp. CreateAccount se trouve dans le fichier Create. cpp. RemoveAccount et RollbackAccount se trouvent dans le fichier Remove. cpp. Ces fichiers sources peuvent être utilisés pour créer les fichiers Process.dll, Create.dll et Remove.dll.

Étant donné que la création ou la suppression d’un compte d’utilisateur nécessite des privilèges élevés, les [actions personnalisées d’exécution différée](deferred-execution-custom-actions.md) qui s’exécutent dans le contexte du système doivent être utilisées pour créer, supprimer ou restaurer des comptes d’utilisateur. Les actions personnalisées d’exécution immédiate, ProcessAccounts et UninstallAccounts, génèrent les actions personnalisées différées qui créent, suppriment ou restaurent les comptes d’utilisateur : CreateAccount, RemoveAccount et RollbackAccount.

Étant donné que les actions personnalisées différées ne peuvent pas lire les informations dans les tables de base de données, ProcessAccounts et UninstallUserAccouts doivent définir une propriété CustomActionData pour transmettre les informations de la table UserAccounts aux actions personnalisées différées, comme décrit dans [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md). Quand le programme d’installation exécute le script d’exécution, les actions personnalisées différées gèrent les comptes d’utilisateur en fonction des informations contenues dans la propriété CustomActionData.

Étant donné que toutes les actions personnalisées se trouvent dans les bibliothèques de liens dynamiques stockées dans la table binaire, elles incluent toutes les constantes msidbCustomActionTypeDll et msidbCustomActionTypeBinaryData dans leur type numérique de base. ProcessAccounts et UninstallAccounts sont des exemples de [type d’action personnalisée pur 1](custom-action-type-1.md). Pour plus d’informations sur les autres types d’actions personnalisées, consultez la [liste récapitulative de tous les types d’actions personnalisées](summary-list-of-all-custom-action-types.md).

CreateAccount et RemoveAccount sont des [actions personnalisées d’exécution différée](deferred-execution-custom-actions.md) qui n’autorisent pas les services à emprunter l’identité d’utilisateurs particuliers. Ces actions personnalisées incluent les constantes msidbCustomActionTypeInScript et msidbCustomActionTypeNoImpersonate pour spécifier ces actions [personnalisées dans les options d’exécution de script](custom-action-in-script-execution-options.md).

RollbackAccount est une [action personnalisée de restauration](rollback-custom-actions.md) qui supprime uniquement les comptes d’utilisateur lors d’une [installation de restauration](rollback-installation.md). RollbackAccount comprend les constantes msidbCustomActionTypeInScript et msidbCustomActionTypeRollback pour spécifier ces [actions personnalisées dans les options d’exécution de script](custom-action-in-script-execution-options.md).

Ces actions personnalisées peuvent gérer des données sensibles telles que des mots de passe utilisateur, qui ne doivent pas être écrits dans le fichier journal. Les actions personnalisées différées doivent donc inclure msidbCustomActionTypeHideTarget dans le type d’action personnalisé. Les noms des actions personnalisées différées doivent également être ajoutés à la liste de propriétés [**MsiHiddenProperties**](msihiddenproperties.md) dans la [table des propriétés](property-table.md) en raison de la façon dont les actions personnalisées immédiates transmettent les données aux actions personnalisées différées à l’aide de la propriété CustomActionData.



| Action personnalisée     | Point d’entrée de DLL                       | Type d’action personnalisé                                                                                                                                                         |
|-------------------|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ProcessAccounts   | ProcessUserAccounts dans Process.dll.   | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData = 1                                                                                                             |
| UninstallAccounts | UninstallUserAccounts dans Process.dll. | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData = 1                                                                                                             |
| CreateAccount     | CreateUserAccount dans Create.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate + msidbCustomActionTypeHideTarget = 11265. |
| RemoveAccount     | RemoveUserAccount dans Remove.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate + msidbCustomActionTypeHideTarget = 11265. |
| RollbackAccount   | RemoveUserAccount dans Remove.dll.      | msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeInScript + msidbCustomActionTypeRollback + msidbCustomActionTypeHideTarget = 9473.       |



 

Passez à [la création de la table CustomAction](authoring-the-customaction-table.md).

 

 



