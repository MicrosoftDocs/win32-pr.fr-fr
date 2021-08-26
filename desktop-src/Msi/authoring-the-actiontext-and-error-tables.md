---
description: Les exemples de spécifications incluent l’envoi de messages ActionData lorsqu’une action personnalisée crée ou supprime un compte d’utilisateur, et signale une erreur si un compte ne peut pas être créé.
ms.assetid: ee90fe3d-51f4-433b-a5ce-950a03e1d8fb
title: Création des tables ActionText et Error
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a7b89c8150e3767841fe914cf55fc7be8c92e8cecf8f54f8486993d955349be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045399"
---
# <a name="authoring-the-actiontext-and-error-tables"></a>Création des tables ActionText et Error

Les exemples de spécifications incluent l’envoi de messages ActionData lorsqu’une action personnalisée crée ou supprime un compte d’utilisateur, et signale une erreur si un compte ne peut pas être créé.

Entrez les entrées suivantes dans la table ActionText pour fournir les informations utilisées par les messages ActionText.

[Table ActionText](actiontext-table.md)



| Action            | Description                                                       | Modèle                          |
|-------------------|-------------------------------------------------------------------|-----------------------------------|
| ProcessAccounts   | Génération d’actions pour créer des comptes d’utilisateur sur l’ordinateur local. | Compte : \[ 1 \] , attributs : \[ 2\] |
| CreateAccount     | Création d’un compte d’utilisateur sur l’ordinateur local.                      | Compte : \[ 1\]                    |
| RemoveAccount     | Suppression du compte d’utilisateur de l’ordinateur local.                    | Compte : \[ 1\]                    |
| RollbackAccount   | Restauration de la création de comptes d’utilisateur sur l’ordinateur local. | Compte : \[ 1\]                    |
| UninstallAccounts | Génération d’actions pour supprimer des comptes d’utilisateur sur l’ordinateur local. | Compte : \[ 1\]                    |



 

Entrez les entrées suivantes dans la table d’erreurs pour fournir les informations utilisées par le rapport d’erreurs.

[Table des erreurs](error-table.md)



| Error | Message                                                                        |
|-------|--------------------------------------------------------------------------------|
| 25001 | Impossible de créer le compte d’utilisateur « \[ 2 \] » sur l’ordinateur local. Code d’erreur : \[ 3 \] . |
| 25002 | Le compte d’utilisateur « \[ 2 \] » existe déjà sur l’ordinateur local.                      |
| 25003 | Impossible de supprimer le compte d’utilisateur' \[ 2 \] 'sur l’ordinateur local. Code d’erreur : \[ 3 \] . |
| 25004 | Le compte d’utilisateur « \[ 2 \] » n’existe pas sur l’ordinateur local.                      |



 

Passez à [la création de la table InstallExecuteSequence](authoring-the-installexecutesequence-table.md).

 

 



