---
description: Pour déléguer les informations d’identification au protocole CredSSP (Credential Security Support Provider Protocol), vous devez spécifier les serveurs auxquels il est possible de déléguer.
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: Paramètres stratégie de groupe CredSSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a159b7a162df3eda692462a3d3972159e61797e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524283"
---
# <a name="credssp-group-policy-settings"></a>Paramètres stratégie de groupe CredSSP

Pour déléguer les informations d’identification au [protocole CredSSP (Credential Security Support Provider Protocol)](credential-security-support-provider.md) , vous devez spécifier les serveurs auxquels il est possible de déléguer. Pour spécifier ces serveurs, modifiez les paramètres dans le composant logiciel enfichable MMC (Microsoft Management Console) de l’éditeur de stratégie de groupe (GPE). Les paramètres GPE qui contrôlent la délégation sont sous **Configuration ordinateur \| modèles d’administration la délégation des \| \| informations d’identification système**.

> [!Caution]  
> Il ne s’agit pas d’une délégation restreinte. CredSSP transmet les informations d’identification complètes de l’utilisateur au serveur sans aucune contrainte.

 

Les paramètres de stratégie de groupe contrôlent la délégation des types d’informations d’identification suivants.



| Type d’informations d’identification                                                                                                                                 | Description                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>Informations d’identification par défaut<br/> | Informations d’identification obtenues lorsque l’utilisateur se connecte pour la première fois à Windows.<br/>                   |
| <span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>Nouvelles informations d’identification<br/>         | Informations d’identification demandées par l’utilisateur lors de l’exécution d’une application.<br/>       |
| <span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>Informations d’identification enregistrées<br/>         | Informations d’identification enregistrées à l’aide du [Gestionnaire d’informations d’identification](credential-manager.md).<br/> |



 

Pour inclure un serveur dans la catégorie associée à un paramètre de stratégie de groupe particulier, ajoutez le [*nom de principal du service*](/windows/desktop/SecGloss/s-gly) (SPN) de ce serveur à la liste des serveurs de ce paramètre de stratégie de groupe. Le nom de principal du service peut contenir un caractère générique unique.

 

